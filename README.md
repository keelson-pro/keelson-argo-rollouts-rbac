# Keelson ArgoCD Rollouts RBAC

An optional add-on for [Keelson](https://github.com/keelson-pro/keelson). It
grants the Keelson ServiceAccount read, watch and update access to Argo Rollouts
custom resources so Keelson can bump the image on a `Rollout` the same way it
does on a Deployment or StatefulSet.

Apply it only if you run [Argo Rollouts](https://argo-rollouts.readthedocs.io/)
and have added `Rollout` to `KEELSON_WATCHED_KINDS`.


# License

Keelson is MIT licensed except for `*.md` Markdown docs which are CC-BY-SA-4.0
For more detail see [LICENSE.md](https://github.com/keelson-pro/.github/blob/main/LICENSE.md).
