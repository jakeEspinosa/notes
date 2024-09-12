# Internals
## `<script setup>`
- `:is` binding is for dynamic components
	- `<component :is="someCondition ? foo : bar" />`
### Scope
`<script>` runs once in the module scope
`<script setup>` runs in its own scope PER INSTANCE
