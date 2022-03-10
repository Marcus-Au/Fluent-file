# Fluent-file
链接：https://pan.baidu.com/s/1Gh-DynSwP_YPoeIy0Fw5ZA 
提取码：q4oy  /*案例*/
https://www.cfd-online.com/Tools/yplus.php  /*y plus online caculator*/

#批量建立平移平面
!$numsteps =31;#建立截面数
!$delta_z=10;#平移间距25mm
!$start_p=-312;#截面z轴起点 三点起始位置 

!for ($i=1; $i <= $numsteps; $i++) {
! $dis=$start_p+$delta_z*($i-1);

PLANE: Plane $i

  Apply Instancing Transform = On
  Apply Texture = Off
  Blend Texture = On
  Bound Radius = 0.5 [m]
  Colour = 0.75, 0.75, 0.75
  Colour Map = Default Colour Map
  Colour Mode = Constant
  Colour Scale = Linear
  Colour Variable = Pressure
  Colour Variable Boundary Values = Conservative
  Culling Mode = No Culling
  Direction 1 Bound = 10 [mm] #
  Direction 1 Orientation = 0 [degree]
  Direction 1 Points = 10
  Direction 2 Bound = 0.6 [mm]
  Direction 2 Points = 10
  Domain List = /DOMAIN GROUP:All Domains
  Draw Contours = Off
  Draw Faces = On
  Draw Lines = Off
  Instancing Transform = /DEFAULT INSTANCE TRANSFORM:Default Transform
  Invert Plane Bound = Off
  Lighting = On
  Line Colour = 0, 0, 0
  Line Colour Mode = Default
  Line Width = 1
  Max = 0.0 [Pa]
  Min = 0.0 [Pa]
  Normal = 0 , 0 , 1 #法向量
  Number of Contours = 11
  Option = Point and Normal
  Plane Bound = Rectangular
  Plane Type = Slice
  Point = $dis [mm], 0.3 [mm], -35 [mm] #点中心坐标
  Point 1 = 0 [mm], 0 [mm], 0 [mm]
  Point 2 = 1 [mm], 0 [mm], 0 [mm]
  Point 3 = 0 [mm], 1 [mm], 0 [mm]
  Range = Global
  Render Edge Angle = 0 [degree]
  Specular Lighting = On
  Surface Drawing = Smooth Shading
  Texture Angle = 0
  Texture Direction = 0 , 1 , 0
  Texture File = 
  Texture Material = Metal
  Texture Position = 0 , 0
  Texture Scale = 1
  Texture Type = Predefined
  Tile Texture = Off
  Transform Texture = Off
  Transparency = 0.0
  Visibility = On
  X = 0.0 [mm]
  Y = 0.0 [mm]
  Z = -55 [mm]
  OBJECT VIEW TRANSFORM: 
    Apply Reflection = Off
    Apply Rotation = Off
    Apply Scale = Off
    Apply Translation = Off
    Principal Axis = Z
    Reflection Plane Option = XY Plane
    Rotation Angle = 0.0 [degree]
    Rotation Axis From = 0 [mm], 0 [mm], 0 [mm]
    Rotation Axis To = 0 [mm], 0 [mm], 0 [mm]
    Rotation Axis Type = Principal Axis
    Scale Vector = 1 , 1 , 1
    Translation Vector = 0 [mm], 0 [mm], 0 [mm]
    X = 0.0 [mm]
    Y = 0.0 [mm]
    Z = 0.0 [mm]
  END
END

!}

