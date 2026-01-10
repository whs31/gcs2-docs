Идентификатор команды. Представляет собой 64-битное беззнаковое значение статического счетчика, инкрементируемого на единицу при каждом вызове функции (см. ниже).

Счетчик обнуляется при перезапуске программы.

Генерируется с помощью функции `ruavp_generate_cid`:
```c
static uint64_t g_cid_counter;

uint64_t ruavp_generate_cid() {
    return ++g_cid_counter;
}
```

В Rust (крейт `vt45`) доступен в виде функции `vt45::util::generate_cid`:
```rust
pub fn generate_cid() -> u64 {
  unsafe { vt45::sys::ruavp_generate_cid() }
}
```