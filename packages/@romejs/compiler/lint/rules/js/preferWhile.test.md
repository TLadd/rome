# `preferWhile.test.ts`

**DO NOT MODIFY**. This file has been autogenerated. Run `rome test packages/@romejs/compiler/lint/rules/js/preferWhile.test.ts --update-snapshots` to update.

## `prefer while`

### `0`

```

 unknown:1 lint/js/preferWhile FIXABLE ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  ✖ Use while loops instead of for loops.

  > 1 │ for (; x.running;) {
      │ ^^^^^^^^^^^^^^^^^^^^
  > 2 │   x.step();
  > 3 │ }

  ℹ Recommended fix

      │ - for (;·x.running;) {
    1 │ + while (x.running) {
      │ - ··x.step();
    2 │ + ↹x.step();
    3 │   }

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✖ Found 1 problem

```

### `0: formatted`

```
while (x.running) {
	x.step();
}

```

### `1`

```

 unknown:1 lint/js/preferWhile FIXABLE ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

  ✖ Use while loops instead of for loops.

  > 1 │ for (;;) {
      │ ^^^^^^^^^^
  > 2 │   doSomething();
  > 3 │ }

  ℹ Recommended fix

      │ - for (;;) {
    1 │ + while (true) {
      │ - ··doSomething();
    2 │ + ↹doSomething();
    3 │   }

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✖ Found 1 problem

```

### `1: formatted`

```
while (true) {
	doSomething();
}

```
