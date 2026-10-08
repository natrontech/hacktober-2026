# Hacktober 2026

Slides from our talk at Hacktober 2026.

## Breaking Out of CI: Container Isolation with Kata Containers

Nicolo Lüscher, Natron

If you run your own CI, you're running strangers' code on your own machines. Any job that builds a container image usually needs a privileged container or the host's Docker socket, which is root on the host by design. Most runners hand that code to runc, where it looks locked down but shares the host kernel, so a single escape means root on the runner and every other job's secrets. This talk is about that boundary, what container runtimes really isolate, where a shared kernel breaks down, and how Kata Containers gives each job its own VM and kernel instead. We run this on Kubernetes in production ourselves, so we also cover what it costs and when it's worth it.

Slides: [`breaking-out-of-ci/`](breaking-out-of-ci/)

## License

The slides and text are licensed under [CC BY 4.0](LICENSE).

The deck bundles [reveal.js](https://revealjs.com) (MIT) and the fonts Instrument Sans and JetBrains Mono (SIL OFL 1.1). Their licenses are in `breaking-out-of-ci/vendor/package/LICENSE` and `breaking-out-of-ci/assets/fonts/OFL.txt`.
