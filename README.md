# Minimal repro of RBE symlinking issue

`bazel build //:css --remote_exector=YOUR_REMOTE_EXECUTOR`

Will generate output of the form

```
ERROR: /usr/local/home/mrmeku/minimal_repro/BUILD:8:14: Sass styles.css failed: (Exit 34): Remote Execution Failure:
Unknown: symlink ../../normalize-path@3.0.0/node_modules/normalize-path normalize-path: file exists
Target //:css failed to build
Use --verbose_failures to see the command lines of failed build steps.
```