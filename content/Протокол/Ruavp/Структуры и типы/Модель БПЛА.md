```c
#define UAV_MODEL_UNKNOWN                0

/* TREX family */
#define UAV_MODEL_TREX_FAMILY_FIRST      (UAV_MODEL_UNKNOWN + 1)           // 1
#define UAV_MODEL_TREX450                (UAV_MODEL_TREX_FAMILY_FIRST + 0) // 1
#define UAV_MODEL_TREX600                (UAV_MODEL_TREX_FAMILY_FIRST + 1) // 2
#define UAV_MODEL_CTX5                   (UAV_MODEL_TREX_FAMILY_FIRST + 2) // 3
#define UAV_MODEL_TREX_FAMILY_LAST       (UAV_MODEL_TREX_FAMILY_FIRST + 2) // 3

/* VT45 family */
#define UAV_MODEL_VT45_FAMILY_FIRST      (UAV_MODEL_TREX_FAMILY_LAST + 1)  // 4
#define UAV_MODEL_VT45                   (UAV_MODEL_VT45_FAMILY_FIRST + 0) // 4
#define UAV_MODEL_LL1                    (UAV_MODEL_VT45_FAMILY_FIRST + 1) // 5
#define UAV_MODEL_LL2                    (UAV_MODEL_VT45_FAMILY_FIRST + 2) // 6
#define UAV_MODEL_VT45_KUPOL             (UAV_MODEL_VT45_FAMILY_FIRST + 3) // 7
#define UAV_MODEL_CH440                  (UAV_MODEL_VT45_FAMILY_FIRST + 4) // 8
#define UAV_MODEL_VT30                   (UAV_MODEL_VT45_FAMILY_FIRST + 5) // 9
#define UAV_MODEL_LL3                    (UAV_MODEL_VT45_FAMILY_FIRST + 6) // 10
#define UAV_MODEL_VT45_FAMILY_LAST       (UAV_MODEL_VT45_FAMILY_FIRST + 6) // 10

typedef uint32_t uav_model_t;
```

Список констант (определений препроцессора), определяющих тип БПЛА.


|            | Определение            | Значение |
| ---------- | ---------------------- | -------- |
| TREX450    | `UAV_MODEL_TREX450`    | 1        |
| TREX600    | `UAV_MODEL_TREX600`    | 2        |
| CTX5       | `UAV_MODEL_CTX5`       | 3        |
| **VT45**   | `UAV_MODEL_VT45`       | **4**    |
| LL1        | `UAV_MODEL_LL1`        | 5        |
| LL2        | `UAV_MODEL_LL2`        | 6        |
| VT45 KUPOL | `UAV_MODEL_VT45_KUPOL` | 7        |
| **VT440**  | `UAV_MODEL_CH440`      | **8**    |
| **VT30**   | `UAV_MODEL_VT30`       | **9**    |
| LL3        | `UAV_MODEL_LL3`        | 10       |

> [!warning]
> В протоколе Ruavp не существует способа узнать тип БПЛА по его телеметрии. Определение типа БПЛА происходит по косвенным признакам (например, по наличию структуры `zzq_battery_cut_t`)
> 