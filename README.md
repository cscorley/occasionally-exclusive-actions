# occasionally-exclusive-actions

Two example actions where:

- action `A` is skipped when there are only changes in the `b/` directory
- action `A` runs whenever there are changes anywhere else outside of `b/`, but is not skipped just because there are some changes in `b/`
- action `B` is "skipped" when there are not only changes in the `b/` directory
  - "skipped" here because the action runs whenever there are changes in `b/`, but the actual job in the example is skipped if there are ALSO other changes outside of `b/`
  - You can also achieve this with the built-in `paths`, but requires knowing what paths should be excluded ahead-of-time.
