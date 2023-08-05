## Usefull linting programs
```bash
yamllint <DIRECTORY>
ansible-lint
```

Exclude rules for yamllint:
```bash
yamllint <DIRECTORY> | grep -v "(line-length)\|(braces)\|(comments)\|(comments-indentation)"
```

Exclude rules for ansible-lint - set in `.ansible-lint`:
```bash
skip_list:
  - 'schema[playbook]'
  - 'name[casing]'
  - 'latest[git]'
  - 'yaml[comments]'
  - 'no-handler'
  - 'no-changed-when'
  - 'galaxy[no-changelog]'
  - 'galaxy[no-runtime]'
  - 'galaxy[tags]'
  - 'schema[galaxy]'
  - 'role-name'

  - 'fqcn[action-core]'
  - 'name[missing]'
```
