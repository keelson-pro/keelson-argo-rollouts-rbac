# Keelson Argo Rollouts RBAC

An optional add-on for [Keelson](https://github.com/keelson-pro/keelson). It
grants the Keelson ServiceAccount read, watch and update access to Argo Rollouts
custom resources so Keelson can bump the image on a `Rollout` the same way it
does on a Deployment or StatefulSet.

Apply it only if you run [Argo Rollouts](https://argo-rollouts.readthedocs.io/)
and have added `Rollout` to `KEELSON_WATCHED_KINDS`.

This bundle contains an overlapping `Role` and `ClusterRole` one of which
should be removed depending on how you're using Keelson. Keelson docs cover
this in its [security through least privilege](https://github.com/keelson-pro/keelson/blob/main/README.md#security-through-least-privilege)
section. Please read the main section and appropriate deployment method part.


## Configuration

| Kaptain Config Token                       | Default        | Purpose                                                               |
|--------------------------------------------|----------------|-----------------------------------------------------------------------|
| `KeelsonArgoRolloutsRbac/KeelsonNamespace` | none, required | The namespace Keelson itself runs in and where its ServiceAccount is. |

This value is required by both the `RoleBinding` and `ClusterRoleBinding`.


# License

Keelson is MIT licensed except for `*.md` Markdown docs which are CC-BY-SA-4.0
For more detail see [LICENSE.md](https://github.com/keelson-pro/.github/blob/main/LICENSE.md).
