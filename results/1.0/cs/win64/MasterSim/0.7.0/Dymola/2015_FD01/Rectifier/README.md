# Validation of 'Rectifier'

## Variables
Weighted-root-mean-square norm with RelTol = 1e-3 and AbsTol = 1e-3, where
AbsTol is based on max. magnitude of reference values.

```
WRMS(uDC) = 1.8448068418100292
WRMS(iAC[1]) = 38.99031088966157
WRMS(iAC[2]) = 50.57312657597094
WRMS(iAC[3]) = 76.37978023408682
WRMS(uAC[1]) = 47.20349328669486
WRMS(uAC[2]) = 64.70441416712231
WRMS(uAC[3]) = 46.84884827797074
WRMS(Losses) = 35.12500642343665
```

## MasterSim project file

Below is the project file that was used to successfully simulation the test case.
Mind: project file is copied from working directory, hence relative path to fmu file.

```

tStart               0.000000e+00 s
tEnd                 1.000000e-01 s
hMax                 30 min
hMin                 1e-6 s
hFallBackLimit       0.001 s
hStart               0.000000e+00 s
hOutputMin           1.000000e-03 s
adjustStepSize       no
absTol               1e-06
relTol               1.000000e-04
MasterMode           GAUSS_JACOBI
ErrorControlMode     NONE
maxIterations        1

simulator 0 0 slave1 #ffff8c00 "..\..\fmi-cross-check\fmus\1.0\cs\win64\Dymola\2015_FD01\Rectifier\Rectifier.fmu"


```

