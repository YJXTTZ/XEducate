# PID
## PID公式
本节主要介绍PID控制原理,其计算公式如下图所示，通过控制比例项、积分项、微分项的比例系数达到接近期望值的目的。
![https://raw.githubusercontent.com/YJXTTZ/XEducate/main/PIDPrinciple/Images/Formula.png](images/Formula.png)
## PID公式中各项的作用
**比例项的作用**
如下图所示，假设无人机受到的升力F=e/P，受到的重力为G，其中e=X-Y，假设只有比例项作用，随着无人机的位置不断上升，当无人机飞到一定位置时F=G，此时无人机始终与目标点具有一定的距离。
![https://raw.githubusercontent.com/YJXTTZ/XEducate/main/PIDPrinciple/Images/ProportionalTerm.png](images/ProportionalTerm.png)
**积分项的作用**
如上图只有比例项作用时，无人机始终与目标点存在一定距离，故此时在比例项的基础上加入积分项，随着e在时间上的积分，积分值越来越大，最终F在比例项与积分项的作用下无人机的位置可能超出目标点的位置，此时e为负值，在比例项的作用下，F可能小于G导致无人机下降，故无人机位置在目标点位置震荡。
![https://raw.githubusercontent.com/YJXTTZ/XEducate/main/PIDPrinciple/Images/IntegralTerm.png](images/IntegralTerm.png)
**微分项的作用**
为了让无人机快速收敛到目标点位置，加入微分项，微分项描述的是e的变化趋势，通过减 小e的变化趋势，进而减小震荡幅度，达到快速收敛的目的。
![https://raw.githubusercontent.com/YJXTTZ/XEducate/main/PIDPrinciple/Images/DifferentialTerm.png](images/DifferentialTerm.png)