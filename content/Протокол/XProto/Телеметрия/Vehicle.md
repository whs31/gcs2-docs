```protobuf
enum Vehicle {
  option allow_alias = true;
  
  VEHICLE_UNSPECIFIED = 0;
  VEHICLE_VT30 = 1;
  VEHICLE_VT45 = 2;
  VEHICLE_VT440 = 3;
  VEHICLE_VT550 = 3;
}
```

Перечисление, содержащее тип БПЛА в соответствии с протоколом `ruavp` (см. [[UAV Model]]).