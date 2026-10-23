# [imapsync][h]
IMAP transfer tool.

## [Requirements][i]
Requires [r_pufky.srv][g] galaxy-ng collection. See
[additional documentation][m] and [reference documentation][h] for
troubleshooting and config variables.

* RAM: ~512MB
* Install size: ~100MB

## Role Variables
Detailed variable use documented in defaults. See usage for role operation.

* [defaults][j] - User configurable options.

## Usage
Role will automatically build imapsync from source and install to
**/usr/local/bin/imapsync**.

### Feature Flags
Tasks are gated by feature flags and executed in the following order.

  Step | Flag                 | Notes
 ------|----------------------|-------
  2    | imapsync_flg_install | Install required packages, users, etc.

### Example Playbooks

#### New Deployment
``` yaml
- name: 'Deploy imapsync.'
  ansible.builtin.include_role:
    name: 'r_pufky.srv.imapsync'
```

## Development
Configure [environment][a].

``` bash
# Run all tests.
molecule test --all
```

### [Releases][b]

  Release | Debian | Ansible | imapsync       | Notes
 ---------|--------|---------|----------------|-------
  1.x.x   | 13     | 2.20    | imapsync-2.314 | Initial release.

## Issues
Create a bug and provide as much information as possible.

Associate pull requests with a submitted bug.

## License
[AGPL-3.0 License][c] | [direct link][f]

## Author Information
PGP: [466EEC2B67516C7117C85CE3A0BC35D16698BAB9][d] | [github gist][e]

[a]: https://r-pufky.github.io/ansible_docs
[b]: https://semver.org/spec/v2.0.0
[c]: https://www.tldrlegal.com/license/gnu-affero-general-public-license-v3-agpl-3-0
[d]: https://keys.openpgp.org/vks/v1/by-fingerprint/466EEC2B67516C7117C85CE3A0BC35D16698BAB9
[e]: https://gist.github.com/r-pufky/a8df36977c55b5bb20829267c4c49d22

[f]: https://github.com/r-pufky/ansible_imapsync/blob/main/LICENSE
[g]: https://github.com/r-pufky/ansible_collection_srv
[h]: https://imapsync.lamiral.info/
[m]: https://r-pufky.github.io/docs/mail/imapsync
[i]: https://github.com/r-pufky/ansible_imapsync/blob/main/meta/main.yml
[j]: https://github.com/r-pufky/ansible_imapsync/tree/main/defaults/main/main.yml