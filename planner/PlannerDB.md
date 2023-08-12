---

database-plugin: basic

---

```yaml:dbfolder
name: new database
description: new description
columns:
  __file__:
    key: __file__
    id: __file__
    input: markdown
    label: File
    accessorKey: __file__
    isMetadata: true
    skipPersist: false
    isDragDisabled: false
    csvCandidate: true
    position: 1
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: true
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      wrap_content: true
  subject:
    input: select
    key: subject
    accessorKey: subject
    label: Subject
    position: 2
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "CD", value: "CD", color: "hsl(320, 95%, 90%)"}
      - { label: "MATH", value: "MATH", color: "hsl(358, 95%, 90%)"}
      - { label: "DM", value: "DM", color: "hsl(4, 95%, 90%)"}
      - { label: "CN", value: "CN", color: "hsl(331, 95%, 90%)"}
      - { label: "DS", value: "DS", color: "hsl(296, 95%, 90%)"}
      - { label: "DAA", value: "DAA", color: "hsl(128, 95%, 90%)"}
      - { label: "APTI", value: "APTI", color: "hsl(82, 95%, 90%)"}
      - { label: "COA", value: "COA", color: "hsl(271, 95%, 90%)"}
      - { label: "C", value: "C", color: "hsl(124, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      option_source: manual
  Topic:
    input: tags
    accessorKey: Topic
    key: Topic
    id: Topic
    label: Topic
    position: 3
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 133
    options:
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      option_source: manual
  __created__:
    key: __created__
    id: __created__
    input: metadata_time
    label: Created
    accessorKey: __created__
    isMetadata: true
    isDragDisabled: false
    skipPersist: false
    csvCandidate: true
    position: 4
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
config:
  remove_field_when_delete_column: false
  cell_size: normal
  sticky_first_column: false
  group_folder_column: 
  remove_empty_folders: false
  automatically_group_files: false
  hoist_files_with_empty_attributes: true
  show_metadata_created: true
  show_metadata_modified: false
  show_metadata_tasks: false
  show_metadata_inlinks: false
  show_metadata_outlinks: false
  show_metadata_tags: false
  source_data: current_folder
  source_form_result: 
  source_destination_path: /
  row_templates_folder: /templates
  current_row_template: templates/Planner Template.md
  pagination_size: 10
  font_size: 16
  enable_js_formulas: false
  formula_folder_path: /
  inline_default: false
  inline_new_position: last_field
  date_format: yyyy-MM-dd
  datetime_format: "yyyy-MM-dd HH:mm:ss"
  metadata_date_format: "yyyy-MM-dd HH:mm:ss"
  enable_footer: false
  implementation: default
filters:
  enabled: false
  conditions:
```