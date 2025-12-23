yangtze@ERP-Yangtze:~/yangtze-bench/apps$ bench --site beumer migrate
Migrating beumer
Updating DocTypes for yangtze       : [========================================] 100%
Updating DocTypes for yangtzeerp    : [========================================] 100%
Updating DocTypes for yangtze_invoice: [========================================] 100%
Updating DocTypes for hrms          : [=============                           ] 34%Failed to alter schema using query: ALTER TABLE `tabShift Type` MODIFY `flexible_schedules` int(1) not null default 0, MODIFY `working_hours_threshold_for_absent` decimal(21,9) not null default 0, MODIFY `working_hours_threshold_for_half_day` decimal(21,9) not null default 0, MODIFY `working_hours` decimal(21,9) not null default 0, MODIFY `duration_of_rest` decimal(21,9) not null default 0


There was an issue while migrating the DocType: Shift Type

Queued rebuilding of search index for beumer

Traceback with variables (most recent call last):
  File "<frozen runpy>", line 198, in _run_module_as_main
      mod_name = 'yangtze.utils.bench_helper'
      alter_argv = True
      mod_spec = ModuleSpec(name='yangtze.utils.bench_helper', loader=<_frozen_importlib_external.SourceFileLoader object at 0x7dfaf53ff3e0>, origin='/home/yangtze/yangtze-bench/apps/yangtze/yangtze/utils/bench_helper.py')
      code = <code object <module> at 0x1fbfe300, file "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/utils/bench_helper.py", line 1>
      main_globals = {'__name__': '__main__', '__doc__': None, '__package__': 'yangtze.utils', '__loader__': <_frozen_importlib_external.SourceFileLoader object at 0x7dfaf53ff3e0>, '__spec__': ModuleSpec(name='yangtze.utils.bench_helper', loader=<_frozen_importlib_external.SourceFileLoader object at 0x7dfaf53ff3e0>, origin='/home/yangtze/yangtze-bench/apps/yangtze/yangtze/utils/bench_helper.py'), '__annotations__': {}, '__builtins__': <module 'builtins' (built-in)>, '__file__': '/home/yangtze/yangtze-bench/apps/yangtze/yangtze/utils/bench_helper.py', '__cached__': '/home/yangtze/yangtze-bench/apps/yangtze/yangtze/utils/__pycache__/bench_helper.cpython-312.pyc', 'importlib': <module 'importlib' from '/usr/lib/python3.12/importlib/__init__.py'>, 'json': <module 'json' from '/usr/lib/python3.12/json/__init__.py'>, 'os': <module 'os' (frozen)>, 'traceback': <module 'traceback' from '/usr/lib/python3.12/traceback.py'>, 'warnings': <module 'warnings' from '/usr/lib/python3.12/warnings.py'>, 'Path': <class 'pathl...
  File "<frozen runpy>", line 88, in _run_code
      code = <code object <module> at 0x1fbfe300, file "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/utils/bench_helper.py", line 1>
      run_globals = {'__name__': '__main__', '__doc__': None, '__package__': 'yangtze.utils', '__loader__': <_frozen_importlib_external.SourceFileLoader object at 0x7dfaf53ff3e0>, '__spec__': ModuleSpec(name='yangtze.utils.bench_helper', loader=<_frozen_importlib_external.SourceFileLoader object at 0x7dfaf53ff3e0>, origin='/home/yangtze/yangtze-bench/apps/yangtze/yangtze/utils/bench_helper.py'), '__annotations__': {}, '__builtins__': <module 'builtins' (built-in)>, '__file__': '/home/yangtze/yangtze-bench/apps/yangtze/yangtze/utils/bench_helper.py', '__cached__': '/home/yangtze/yangtze-bench/apps/yangtze/yangtze/utils/__pycache__/bench_helper.cpython-312.pyc', 'importlib': <module 'importlib' from '/usr/lib/python3.12/importlib/__init__.py'>, 'json': <module 'json' from '/usr/lib/python3.12/json/__init__.py'>, 'os': <module 'os' (frozen)>, 'traceback': <module 'traceback' from '/usr/lib/python3.12/traceback.py'>, 'warnings': <module 'warnings' from '/usr/lib/python3.12/warnings.py'>, 'Path': <class 'pathl...
      init_globals = None
      mod_name = '__main__'
      mod_spec = ModuleSpec(name='yangtze.utils.bench_helper', loader=<_frozen_importlib_external.SourceFileLoader object at 0x7dfaf53ff3e0>, origin='/home/yangtze/yangtze-bench/apps/yangtze/yangtze/utils/bench_helper.py')
      pkg_name = 'yangtze.utils'
      script_name = None
      loader = <_frozen_importlib_external.SourceFileLoader object at 0x7dfaf53ff3e0>
      fname = '/home/yangtze/yangtze-bench/apps/yangtze/yangtze/utils/bench_helper.py'
      cached = '/home/yangtze/yangtze-bench/apps/yangtze/yangtze/utils/__pycache__/bench_helper.cpython-312.pyc'
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/utils/bench_helper.py", line 114, in <module>
    main()
      ...skipped... 27 vars
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/utils/bench_helper.py", line 20, in main
    click.Group(commands=commands)(prog_name="bench")
      commands = {'yangtze': <Group yangtze>, 'get-yangtze-commands': <Command get-yangtze-commands>, 'get-yangtze-help': <Command get-yangtze-help>}
  File "/home/yangtze/yangtze-bench/env/lib/python3.12/site-packages/click/core.py", line 1157, in __call__
    return self.main(*args, **kwargs)
      self = <Group None>
      args = ()
      kwargs = {'prog_name': 'bench'}
  File "/home/yangtze/yangtze-bench/env/lib/python3.12/site-packages/click/core.py", line 1078, in main
    rv = self.invoke(ctx)
      self = <Group None>
      args = ['yangtze', '--site', 'beumer', 'migrate']
      prog_name = 'bench'
      complete_var = None
      standalone_mode = True
      windows_expand_args = True
      extra = {}
      ctx = <click.core.Context object at 0x7dfaf530b080>
  File "/home/yangtze/yangtze-bench/env/lib/python3.12/site-packages/click/core.py", line 1688, in invoke
    return _process_result(sub_ctx.command.invoke(sub_ctx))
      self = <Group None>
      ctx = <click.core.Context object at 0x7dfaf530b080>
      _process_result = <function MultiCommand.invoke.<locals>._process_result at 0x7dfaf3749d00>
      args = ['migrate']
      cmd_name = 'yangtze'
      cmd = <Group yangtze>
      sub_ctx = <click.core.Context object at 0x7dfaf37c7860>
      __class__ = <class 'click.core.MultiCommand'>
  File "/home/yangtze/yangtze-bench/env/lib/python3.12/site-packages/click/core.py", line 1688, in invoke
    return _process_result(sub_ctx.command.invoke(sub_ctx))
      self = <Group yangtze>
      ctx = <click.core.Context object at 0x7dfaf37c7860>
      _process_result = <function MultiCommand.invoke.<locals>._process_result at 0x7dfaf3733b00>
      args = []
      cmd_name = 'migrate'
      cmd = <Command migrate>
      sub_ctx = <click.core.Context object at 0x7dfaf37e0950>
      __class__ = <class 'click.core.MultiCommand'>
  File "/home/yangtze/yangtze-bench/env/lib/python3.12/site-packages/click/core.py", line 1434, in invoke
    return ctx.invoke(self.callback, **ctx.params)
      self = <Command migrate>
      ctx = <click.core.Context object at 0x7dfaf37e0950>
  File "/home/yangtze/yangtze-bench/env/lib/python3.12/site-packages/click/core.py", line 783, in invoke
    return __callback(*args, **kwargs)
      _Context__self = <click.core.Context object at 0x7dfaf37e0950>
      _Context__callback = <function migrate at 0x7dfaf378d760>
      args = ()
      kwargs = {'skip_failing': False, 'skip_search_index': False}
      ctx = <click.core.Context object at 0x7dfaf37e0950>
  File "/home/yangtze/yangtze-bench/env/lib/python3.12/site-packages/click/decorators.py", line 33, in new_func
    return f(get_current_context(), *args, **kwargs)
      args = ()
      kwargs = {'skip_failing': False, 'skip_search_index': False}
      f = <function migrate at 0x7dfaf378d4e0>
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/commands/__init__.py", line 29, in _func
    ret = f(yangtze._dict(ctx.obj), *args, **kwargs)
      ctx = <click.core.Context object at 0x7dfaf37e0950>
      args = ()
      kwargs = {'skip_failing': False, 'skip_search_index': False}
      profile = False
      f = <function migrate at 0x7dfaf378d440>
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/commands/site.py", line 711, in migrate
    ).run(site=site)
      context = {'sites': ['beumer'], 'force': False, 'verbose': False, 'profile': False}
      skip_failing = False
      skip_search_index = False
      activate_by_import = <module 'traceback_with_variables.activate_by_import' from '/home/yangtze/yangtze-bench/env/lib/python3.12/site-packages/traceback_with_variables/activate_by_import.py'>
      SiteMigration = <class 'yangtze.migrate.SiteMigration'>
      site = 'beumer'
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/migrate.py", line 186, in run
    self.run_schema_updates()
      self = <yangtze.migrate.SiteMigration object at 0x7dfae3e88860>
      site = 'beumer'
      filelock = <function filelock at 0x7dfae3d187c0>
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/migrate.py", line 52, in wrapper
    raise e
      args = (<yangtze.migrate.SiteMigration object at 0x7dfae3e88860>,)
      kwargs = {}
      method = <function SiteMigration.run_schema_updates at 0x7dfae3d182c0>
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/migrate.py", line 44, in wrapper
    ret = method(*args, **kwargs)
      args = (<yangtze.migrate.SiteMigration object at 0x7dfae3e88860>,)
      kwargs = {}
      method = <function SiteMigration.run_schema_updates at 0x7dfae3d182c0>
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/migrate.py", line 120, in run_schema_updates
    yangtze.model.sync.sync_all()
      self = <yangtze.migrate.SiteMigration object at 0x7dfae3e88860>
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/model/sync.py", line 43, in sync_all
    sync_for(app, force, reset_permissions=reset_permissions)
      force = 0
      reset_permissions = False
      app = 'hrms'
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/model/sync.py", line 114, in sync_for
    import_file_by_path(
      app_name = 'hrms'
      force = 0
      reset_permissions = False
      files = ['/home/yangtze/yangtze-bench/apps/hrms/hrms/hr/doctype/appointment_letter/appointment_letter.json', '/home/yangtze/yangtze-bench/apps/hrms/hrms/hr/doctype/appointment_letter_content/appointment_letter_content.json', '/home/yangtze/yangtze-bench/apps/hrms/hrms/hr/doctype/appointment_letter_template/appointment_letter_template.json', '/home/yangtze/yangtze-bench/apps/hrms/hrms/hr/doctype/appraisal/appraisal.json', '/home/yangtze/yangtze-bench/apps/hrms/hrms/hr/doctype/appraisal_cycle/appraisal_cycle.json', '/home/yangtze/yangtze-bench/apps/hrms/hrms/hr/doctype/appraisal_goal/appraisal_goal.json', '/home/yangtze/yangtze-bench/apps/hrms/hrms/hr/doctype/appraisal_kra/appraisal_kra.json', '/home/yangtze/yangtze-bench/apps/hrms/hrms/hr/doctype/appraisal_template/appraisal_template.json', '/home/yangtze/yangtze-bench/apps/hrms/hrms/hr/doctype/appraisal_template_goal/appraisal_template_goal.json', '/home/yangtze/yangtze-bench/apps/hrms/hrms/hr/doctype/appraisee/appraisee.json', '/home/yangtze/...
      module_name = 'payroll'
      folder = '/home/yangtze/yangtze-bench/apps/hrms/hrms/payroll'
      l = 258
      i = 89
      doc_path = '/home/yangtze/yangtze-bench/apps/hrms/hrms/hr/doctype/shift_type/shift_type.json'
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/modules/import_file.py", line 146, in import_file_by_path
    import_doc(
      path = '/home/yangtze/yangtze-bench/apps/hrms/hrms/hr/doctype/shift_type/shift_type.json'
      force = 0
      data_import = False
      pre_process = None
      ignore_version = True
      reset_permissions = False
      docs = [{'actions': [], 'autoname': 'prompt', 'creation': '2018-04-13 16:22:52.954783', 'doctype': 'DocType', 'editable_grid': 1, 'engine': 'InnoDB', 'fields': [{'fieldname': 'start_time', 'fieldtype': 'Time', 'in_list_view': 1, 'label': 'Start Time', 'reqd': 1, 'doctype': 'DocField'}, {'fieldname': 'end_time', 'fieldtype': 'Time', 'in_list_view': 1, 'label': 'End Time', 'reqd': 1, 'doctype': 'DocField'}, {'fieldname': 'the_start_time_of_overtime_work', 'fieldtype': 'Time', 'in_list_view': 1, 'label': 'The Start Time Of Overtime Work', 'doctype': 'DocField'}, {'fieldname': 'the_end_time_of_overtime_work', 'fieldtype': 'Time', 'in_list_view': 1, 'label': 'The End Time Of Overtime Work', 'doctype': 'DocField'}, {'fieldname': 'column_break_3', 'fieldtype': 'Column Break', 'doctype': 'DocField'}, {'fieldname': 'holiday_list', 'fieldtype': 'Link', 'hidden': 1, 'label': 'Holiday List', 'options': 'Holiday List', 'doctype': 'DocField'}, {'default': '0', 'description': "Mark attendance based on 'Empl...
      calculated_hash = '7e1bee16fa85a038545fcbeff498d272'
      doc = {'actions': [], 'autoname': 'prompt', 'creation': '2018-04-13 16:22:52.954783', 'doctype': 'DocType', 'editable_grid': 1, 'engine': 'InnoDB', 'fields': [{'fieldname': 'start_time', 'fieldtype': 'Time', 'in_list_view': 1, 'label': 'Start Time', 'reqd': 1, 'doctype': 'DocField'}, {'fieldname': 'end_time', 'fieldtype': 'Time', 'in_list_view': 1, 'label': 'End Time', 'reqd': 1, 'doctype': 'DocField'}, {'fieldname': 'the_start_time_of_overtime_work', 'fieldtype': 'Time', 'in_list_view': 1, 'label': 'The Start Time Of Overtime Work', 'doctype': 'DocField'}, {'fieldname': 'the_end_time_of_overtime_work', 'fieldtype': 'Time', 'in_list_view': 1, 'label': 'The End Time Of Overtime Work', 'doctype': 'DocField'}, {'fieldname': 'column_break_3', 'fieldtype': 'Column Break', 'doctype': 'DocField'}, {'fieldname': 'holiday_list', 'fieldtype': 'Link', 'hidden': 1, 'label': 'Holiday List', 'options': 'Holiday List', 'doctype': 'DocField'}, {'default': '0', 'description': "Mark attendance based on 'Emplo...
      db_modified_timestamp = datetime.datetime(2025, 12, 23, 9, 56, 25, 692352)
      is_db_timestamp_latest = True
      stored_hash = None
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/modules/import_file.py", line 239, in import_doc
    doc.insert()
      docdict = {'actions': [], 'autoname': 'prompt', 'creation': '2018-04-13 16:22:52.954783', 'doctype': 'DocType', 'editable_grid': 1, 'engine': 'InnoDB', 'fields': [{'fieldname': 'start_time', 'fieldtype': 'Time', 'in_list_view': 1, 'label': 'Start Time', 'reqd': 1, 'doctype': 'DocField'}, {'fieldname': 'end_time', 'fieldtype': 'Time', 'in_list_view': 1, 'label': 'End Time', 'reqd': 1, 'doctype': 'DocField'}, {'fieldname': 'the_start_time_of_overtime_work', 'fieldtype': 'Time', 'in_list_view': 1, 'label': 'The Start Time Of Overtime Work', 'doctype': 'DocField'}, {'fieldname': 'the_end_time_of_overtime_work', 'fieldtype': 'Time', 'in_list_view': 1, 'label': 'The End Time Of Overtime Work', 'doctype': 'DocField'}, {'fieldname': 'column_break_3', 'fieldtype': 'Column Break', 'doctype': 'DocField'}, {'fieldname': 'holiday_list', 'fieldtype': 'Link', 'hidden': 1, 'label': 'Holiday List', 'options': 'Holiday List', 'doctype': 'DocField'}, {'default': '0', 'description': "Mark attendance based on 'Emplo...
      data_import = False
      pre_process = None
      ignore_version = True
      reset_permissions = False
      path = '/home/yangtze/yangtze-bench/apps/hrms/hrms/hr/doctype/shift_type/shift_type.json'
      controller = <class 'yangtze.core.doctype.doctype.doctype.DocType'>
      doc = <DocType: Shift Type>
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/model/document.py", line 315, in insert
    self.run_post_save_methods()
      self = <DocType: Shift Type>
      ignore_permissions = None
      ignore_links = None
      ignore_if_duplicate = False
      ignore_mandatory = None
      set_name = None
      set_child_names = True
      d = <DocPerm: 0af9f9fee7 parent=Shift Type>
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/model/document.py", line 1128, in run_post_save_methods
    self.run_method("on_update")
      self = <DocType: Shift Type>
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/model/document.py", line 962, in run_method
    out = Document.hook(fn)(self, *args, **kwargs)
      self = <DocType: Shift Type>
      method = 'on_update'
      args = ()
      kwargs = {}
      fn = <function Document.run_method.<locals>.fn at 0x7dfae366bb00>
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/model/document.py", line 1322, in composer
    return composed(self, method, *args, **kwargs)
      self = <DocType: Shift Type>
      args = ()
      kwargs = {}
      hooks = [<function build_domain_restriced_doctype_cache at 0x7dfaf362a980>, <function clear_doctype_notifications at 0x7dfaf16aab60>, <function process_workflow_actions at 0x7dfae3789a80>, <function attach_files_to_document at 0x7dfaf23d3060>, <function apply at 0x7dfae360c720>, <function update_due_date at 0x7dfae360c7c0>, <function apply_permissions_for_non_standard_user_type at 0x7dfae360df80>]
      method = 'on_update'
      doc_events = {'*': {'on_update': ['yangtze.desk.notifications.clear_doctype_notifications', 'yangtze.workflow.doctype.workflow_action.workflow_action.process_workflow_actions', 'yangtze.core.doctype.file.utils.attach_files_to_document', 'yangtze.automation.doctype.assignment_rule.assignment_rule.apply', 'yangtze.automation.doctype.assignment_rule.assignment_rule.update_due_date', 'yangtze.core.doctype.user_type.user_type.apply_permissions_for_non_standard_user_type'], 'after_rename': ['yangtze.desk.notifications.clear_doctype_notifications'], 'on_cancel': ['yangtze.desk.notifications.clear_doctype_notifications', 'yangtze.workflow.doctype.workflow_action.workflow_action.process_workflow_actions', 'yangtze.automation.doctype.assignment_rule.assignment_rule.apply'], 'on_trash': ['yangtze.desk.notifications.clear_doctype_notifications', 'yangtze.workflow.doctype.workflow_action.workflow_action.process_workflow_actions'], 'on_update_after_submit': ['yangtze.workflow.doctype.workflow_action.workflow_act...
      handler = 'yangtze.core.doctype.user_type.user_type.apply_permissions_for_non_standard_user_type'
      composed = <function Document.hook.<locals>.compose.<locals>.runner at 0x7dfae366b4c0>
      compose = <function Document.hook.<locals>.compose at 0x7dfae366bba0>
      f = <function Document.run_method.<locals>.fn at 0x7dfae366bb00>
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/model/document.py", line 1304, in runner
    add_to_return_value(self, fn(self, *args, **kwargs))
      self = <DocType: Shift Type>
      method = 'on_update'
      args = ()
      kwargs = {}
      add_to_return_value = <function Document.hook.<locals>.add_to_return_value at 0x7dfae366bf60>
      fn = <function Document.run_method.<locals>.fn at 0x7dfae366bb00>
      hooks = (<function build_domain_restriced_doctype_cache at 0x7dfaf362a980>, <function clear_doctype_notifications at 0x7dfaf16aab60>, <function process_workflow_actions at 0x7dfae3789a80>, <function attach_files_to_document at 0x7dfaf23d3060>, <function apply at 0x7dfae360c720>, <function update_due_date at 0x7dfae360c7c0>, <function apply_permissions_for_non_standard_user_type at 0x7dfae360df80>)
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/model/document.py", line 959, in fn
    return method_object(*args, **kwargs)
      self = <DocType: Shift Type>
      args = ()
      kwargs = {}
      method_object = <bound method DocType.on_update of <DocType: Shift Type>>
      method = 'on_update'
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/core/doctype/doctype/doctype.py", line 509, in on_update
    raise e
      self = <DocType: Shift Type>
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/core/doctype/doctype/doctype.py", line 506, in on_update
    yangtze.db.updatedb(self.name, Meta(self))
      self = <DocType: Shift Type>
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/database/mariadb/database.py", line 439, in updatedb
    db_table.sync()
      self = <yangtze.database.mariadb.database.MariaDBDatabase object at 0x7dfaf0c8e3c0>
      doctype = 'Shift Type'
      meta = <Meta: Shift Type>
      res = ((0,),)
      db_table = <yangtze.database.mariadb.schema.MariaDBTable object at 0x7dfae3740fb0>
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/database/schema.py", line 44, in sync
    self.alter()
      self = <yangtze.database.mariadb.schema.MariaDBTable object at 0x7dfae3740fb0>
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/database/mariadb/schema.py", line 111, in alter
    yangtze.db.sql_ddl(query)
      self = <yangtze.database.mariadb.schema.MariaDBTable object at 0x7dfae3740fb0>
      col = <yangtze.database.schema.DbColumn object at 0x7dfae36a75f0>
      add_column_query = []
      columns_to_modify = {<yangtze.database.schema.DbColumn object at 0x7dfae36a6840>, <yangtze.database.schema.DbColumn object at 0x7dfae36a7170>, <yangtze.database.schema.DbColumn object at 0x7dfae36a7b30>, <yangtze.database.schema.DbColumn object at 0x7dfae36a5340>, <yangtze.database.schema.DbColumn object at 0x7dfae36a6b70>}
      modify_column_query = ['MODIFY `flexible_schedules` int(1) not null default 0', 'MODIFY `working_hours_threshold_for_absent` decimal(21,9) not null default 0', 'MODIFY `working_hours_threshold_for_half_day` decimal(21,9) not null default 0', 'MODIFY `working_hours` decimal(21,9) not null default 0', 'MODIFY `duration_of_rest` decimal(21,9) not null default 0']
      add_index_query = []
      drop_index_query = []
      query_parts = ['MODIFY `flexible_schedules` int(1) not null default 0', 'MODIFY `working_hours_threshold_for_absent` decimal(21,9) not null default 0', 'MODIFY `working_hours_threshold_for_half_day` decimal(21,9) not null default 0', 'MODIFY `working_hours` decimal(21,9) not null default 0', 'MODIFY `duration_of_rest` decimal(21,9) not null default 0']
      query_body = 'MODIFY `flexible_schedules` int(1) not null default 0, MODIFY `working_hours_threshold_for_absent` decimal(21,9) not null default 0, MODIFY `working_hours_threshold_for_half_day` decimal(21,9) not null default 0, MODIFY `working_hours` decimal(21,9) not null default 0, MODIFY `duration_of_rest` decimal(21,9) not null default 0'
      query = 'ALTER TABLE `tabShift Type` MODIFY `flexible_schedules` int(1) not null default 0, MODIFY `working_hours_threshold_for_absent` decimal(21,9) not null default 0, MODIFY `working_hours_threshold_for_half_day` decimal(21,9) not null default 0, MODIFY `working_hours` decimal(21,9) not null default 0, MODIFY `duration_of_rest` decimal(21,9) not null default 0'
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/database/database.py", line 419, in sql_ddl
    self.sql(query, debug=debug)
      self = <yangtze.database.mariadb.database.MariaDBDatabase object at 0x7dfaf0c8e3c0>
      query = 'ALTER TABLE `tabShift Type` MODIFY `flexible_schedules` int(1) not null default 0, MODIFY `working_hours_threshold_for_absent` decimal(21,9) not null default 0, MODIFY `working_hours_threshold_for_half_day` decimal(21,9) not null default 0, MODIFY `working_hours` decimal(21,9) not null default 0, MODIFY `duration_of_rest` decimal(21,9) not null default 0'
      debug = False
  File "/home/yangtze/yangtze-bench/apps/yangtze/yangtze/database/database.py", line 236, in sql
    self._cursor.execute(query, values)
      self = <yangtze.database.mariadb.database.MariaDBDatabase object at 0x7dfaf0c8e3c0>
      query = 'ALTER TABLE `tabShift Type` MODIFY `flexible_schedules` int(1) not null default 0, MODIFY `working_hours_threshold_for_absent` decimal(21,9) not null default 0, MODIFY `working_hours_threshold_for_half_day` decimal(21,9) not null default 0, MODIFY `working_hours` decimal(21,9) not null default 0, MODIFY `duration_of_rest` decimal(21,9) not null default 0'
      values = None
      as_dict = 0
      as_list = 0
      debug = False
      ignore_ddl = 0
      auto_commit = 0
      update = None
      explain = False
      run = True
      pluck = False
      as_iterator = False
      trace_id = None
  File "/home/yangtze/yangtze-bench/env/lib/python3.12/site-packages/pymysql/cursors.py", line 153, in execute
    result = self._query(query)
      self = <pymysql.cursors.Cursor object at 0x7dfaee1fae70>
      query = 'ALTER TABLE `tabShift Type` MODIFY `flexible_schedules` int(1) not null default 0, MODIFY `working_hours_threshold_for_absent` decimal(21,9) not null default 0, MODIFY `working_hours_threshold_for_half_day` decimal(21,9) not null default 0, MODIFY `working_hours` decimal(21,9) not null default 0, MODIFY `duration_of_rest` decimal(21,9) not null default 0'
      args = None
  File "/home/yangtze/yangtze-bench/env/lib/python3.12/site-packages/pymysql/cursors.py", line 322, in _query
    conn.query(q)
      self = <pymysql.cursors.Cursor object at 0x7dfaee1fae70>
      q = 'ALTER TABLE `tabShift Type` MODIFY `flexible_schedules` int(1) not null default 0, MODIFY `working_hours_threshold_for_absent` decimal(21,9) not null default 0, MODIFY `working_hours_threshold_for_half_day` decimal(21,9) not null default 0, MODIFY `working_hours` decimal(21,9) not null default 0, MODIFY `duration_of_rest` decimal(21,9) not null default 0'
      conn = <pymysql.connections.Connection object at 0x7dfae3dfba70>
  File "/home/yangtze/yangtze-bench/env/lib/python3.12/site-packages/pymysql/connections.py", line 558, in query
    self._affected_rows = self._read_query_result(unbuffered=unbuffered)
      self = <pymysql.connections.Connection object at 0x7dfae3dfba70>
      sql = b'ALTER TABLE `tabShift Type` MODIFY `flexible_schedules` int(1) not null default 0, MODIFY `working_hours_threshold_for_absent` decimal(21,9) not null default 0, MODIFY `working_hours_threshold_for_half_day` decimal(21,9) not null default 0, MODIFY `working_hours` decimal(21,9) not null default 0, MODIFY `duration_of_rest` decimal(21,9) not null default 0'
      unbuffered = False
  File "/home/yangtze/yangtze-bench/env/lib/python3.12/site-packages/pymysql/connections.py", line 822, in _read_query_result
    result.read()
      self = <pymysql.connections.Connection object at 0x7dfae3dfba70>
      unbuffered = False
      result = <pymysql.connections.MySQLResult object at 0x7dfae36a75c0>
  File "/home/yangtze/yangtze-bench/env/lib/python3.12/site-packages/pymysql/connections.py", line 1200, in read
    first_packet = self.connection._read_packet()
      self = <pymysql.connections.MySQLResult object at 0x7dfae36a75c0>
  File "/home/yangtze/yangtze-bench/env/lib/python3.12/site-packages/pymysql/connections.py", line 772, in _read_packet
    packet.raise_for_error()
      self = <pymysql.connections.Connection object at 0x7dfae3dfba70>
      packet_type = <class 'pymysql.protocol.MysqlPacket'>
      buff = bytearray(b"\xff\xf1\x04#01000Data truncated for column \'flexible_schedules\' at row 1")
      packet_header = b'@\x00\x00\x01'
      btrl = 64
      btrh = 0
      packet_number = 1
      bytes_to_read = 64
      recv_data = b"\xff\xf1\x04#01000Data truncated for column 'flexible_schedules' at row 1"
      packet = <pymysql.protocol.MysqlPacket object at 0x7dfae36a5420>
  File "/home/yangtze/yangtze-bench/env/lib/python3.12/site-packages/pymysql/protocol.py", line 221, in raise_for_error
    err.raise_mysql_exception(self._data)
      self = <pymysql.protocol.MysqlPacket object at 0x7dfae36a5420>
      errno = 1265
  File "/home/yangtze/yangtze-bench/env/lib/python3.12/site-packages/pymysql/err.py", line 143, in raise_mysql_exception
    raise errorclass(errno, errval)
      data = b"\xff\xf1\x04#01000Data truncated for column 'flexible_schedules' at row 1"
      errno = 1265
      errval = "Data truncated for column 'flexible_schedules' at row 1"
      errorclass = <class 'pymysql.err.DataError'>
pymysql.err.DataError: (1265, "Data truncated for column 'flexible_schedules' at row 1")
yangtze@ERP-Yangtze:~/yangtze-bench/apps$ 
