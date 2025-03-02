```md README.md (1-15)
# test_v-model_type

This repository is used to provide a minimal demo for testing v-model type detection.

I originally wanted to test the ts2322 error in the case of `<InputText v-model="value" />`. However, after switching the display language in VSCode once to copy the English error message, I could no longer reproduce the error!!!

I initially thought that the above code was equivalent to this code `<InputText :model-value="value" @update:model-value="value = $event" />`, so it was reasonable for Volar to prompt the same error. But now I'm not so sure.

```log
Type 'string | undefined' is not assignable to type 'string'.
  Type 'undefined' is not assignable to type 'string'.ts-plugin(2322)
(property) value: string
```

The situation I encountered earlier was that `<InputText v-model="value" />` would also report the above error, but now I can no longer reproduce it. So I want to know whether `<InputText v-model="value" />` should actually report the error ts-plugin(2322).
```