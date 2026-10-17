# 2.0 构建：未完成，请勿使用 / 2.0 build: incomplete, do not use

`air-logistics-tower_0.12.72.zip` 是同一份代码的 Factorio 2.0 构建，**只验证了能加载，运行时会崩溃**，因此从正式发布中撤下。

已确认的 2.0 缺陷（都属于 2.1 专有 API，缺失时需要逐个适配）：

| 现象 | 缺失的 API |
|---|---|
| 加载即报 `First argument must be a table or LuaEventType` | `defines.events.on_gui_inventory_action` |
| 建塔时报 `doesn't contain key output_networks` | `LuaControlBehavior.output_networks` |
| 建塔时报 `could not set fluid filter` | `LuaEntity.get_fluid_filter / set_fluid_filter` |
| 接口搬运时报 `doesn't contain key transfer_from_stack` | `LuaInventory.transfer_from_stack` |
| 配置时报 `LuaLogisticContainerControlBehavior doesn't contain key read_contents` | `LuaLogisticContainerControlBehavior.read_contents` |

**请使用 2.1 版本（`release/air-logistics-tower_0.12.71.zip`）**，那是经过完整功能测试的分支。

2.0 支持需要一次系统性的移植：枚举全部 2.1 专有 API → 逐个加兼容层 → 在 2.0.77 上跑完整测试套件。在完成之前不会再提供 2.0 包。

---

`air-logistics-tower_0.12.72.zip` is a Factorio 2.0 build of the same code. Only loading was verified; it **crashes at runtime**, so it is withdrawn from the official releases. Missing 2.1-only APIs are listed in the table above. Use the 2.1 release (`release/air-logistics-tower_0.12.71.zip`), which is fully tested. 2.0 support needs a systematic port before any 2.0 package is offered again.
