# 예제 1-4
#### INCAR 파일에서 해당 옵션으로 수정 후 저장. 원본은 INCAR.ori 로 백업
- ISIF=3
- ISPIN=1
- LCHARG=False
- EDIFF=1E-05
- PREC=Normal
#### 조건    
- INCAR 옵션 전체를 dictionary 타입으로 저장 (ex. <code>{"NWRITE": 2, "ISTART": 0, "LWAVE": ".FALSE."  ... }</code>

# 예상결과물
파이썬 dictionary 로 만든 INCAR 옵션
<pre>
print(incar_dict)
>>>
{"NWRITE": 2, "ISTART": 0, "LWAVE": ".FALSE."  ... }
</pre>
수정된 INCAR
<pre>
SYSTEM           = Li6PS5Cl                      

#1 Startparameter for this Run
NWRITE           = 2                             ! LPETIM-F    write-flag & timer
ISTART           = 0                             ! job   : 0-new  1-contEcut  2-sameBS
INIWAV           = 1                             ! 0-jellium  1-random
IWAVPR           = 1                             ! prediction:  0-non 1-charg 2-wave 3-comb
ICHARG           = 2                             ! 0-from WF  1-from CHGCAR  2-from atom  11-12-fixed
LWAVE            = .FALSE.                       ! determines whether the wavefunctions are written to the WAVECAR file
LCHARG           = False                         !

#2 Electronic Relaxation 1
NELM             = 100                           ! number of iterations
EDIFF            = 1E-05                         ! stopping-criterion for ELM
BMIX             = 3.00                          ! sets the cutoff wave vector for Kerker mixing for the magnetization density
ENCUT            = 500                           ! Cut-Off Energy

#3 Electronic Relaxation 1
# IALGO          = 48                            ! algorithm for the e-relax
LDIAG            = T                             ! sub-space diagonalisation
LREAL            = auto                          ! real-space projection
PREC             = Normal                        ! accuracy
# NBANDS         = 30                            ! number of bands for diagonalization

#4 Ionic Relaxation
NSW              = 200                           ! number of steps for IOM
NBLOCK           = 1                             ! inner block
KBLOCK           = 10                            ! outer block
IBRION           = 2                             ! ionic relax: 0-MD 1-quasi-New 2-CG
ISIF             = 3                             ! ion&cell relax: 0-MD 2-ion&stress 3-ion&cell&stress
ISYM             = 2                             ! switch symmetry stuff ON (1 or 2) or OFF (0)
# SYMPREC        =  1e-6                         !
LCORR            = T                             ! Harris-correction to forces
EDIFFG           = -0.04                         ! Criterion for geom opt (eV/Ang)
POTIM            = 0.50                          ! time-step for ionic motion (fs)
SMASS            = 3.00                          ! Nose mass-parameter (am)

#5 DOS related values
ISMEAR           = 0                             ! Broadening methode -5-tet -1-fermi 0-gaus 1-mp 2-mp2
SIGMA            = 0.05                          ! Broadening in eV
LORBIT           = 11                            ! l-decomposed DOS
# RWIGS          = 1.63  1.00                    ! Wigner-Zeits radius
# EMIN           =                               ! Minimum energy for DOS
# EMAX           =                               ! Maximum energy for DOS
# NEDOS          = 1001                          ! Number of DOS points
# NELECT         = 100                           ! Total number of electrons
# NUPDOWN        = 2                             ! Difference between UP&DOWN electrons

#6 Parallelizationoption
LPLANE           = T                             ! Parallelization for PWs
NCORE            = 4                             !
LSCALU           = F                             !
NSIM             = 4                             !
ISPIN            = 1                             ! spin polarized-2, non spin polarized-1
# MAGMOM         = 24*0.0 4*0.6 20*0.6 4*0.6     !

#7 optB86b-vdW functional requires vdw_kernel.bindat
# GGA            = MK                            !
# PARAM1         = 0.1234                        !
# PARAM2         = 1.0000                        !
# LUSE_VDW       = .TRUE.                        !
# AGGAC          = 0.0000                        !

#8 TS calculation         ! default:Nudged Elestic Band method
# ICHAIN         = 0                             ! Method (0-NEB, 1-Dynamical matrix, 2-Dimer, 3-Lanczos)
# SPRING         = -5                            ! in eV/Ang*2 (sping constant)
# IMAGES         = 3                             ! Number of images btw Reactant & Product
# LCLIMB         = .true.                        ! cNEB: driven up to the saddle point
# LTANGENTOLD    = .true.                        ! Old central difference tangent
# LDNEB          = .true.                        ! Modified doubble nudging
# NEBCELL        = .true.                        ! NEB for variable cell (w/ ISIF-3)

#9 Dipole Correctionoption
# IDIPOL         = 3                             !
# LDIPOL         =                               !

#10 lda+uparameters
# LMAXMIX        = 4                             !
# LDAU           = .TRUE.                        ! or .FALSE.
# LDAUTYPE       = 2                             ! or 1
# LDAUL          = 2 2 2 2                       !
# LDAUU          = 0 0 0 0                       !
# LDAUJ          = 0 0 0 0                       !

#11 vdWcorrections
# IVDW           = 12                            !

</pre>
