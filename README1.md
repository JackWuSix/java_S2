yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze$ git merge -s recursive -X theirs beumer-TMS 
Auto-merging yangtze/public/js/yangtze/form/multi_select_dialog.js
Auto-merging yangtze/hooks.py
Auto-merging yangtze/contacts/doctype/address/address.json
CONFLICT (add/add): Merge conflict in yangtze/api/test_s3_migration.py
Auto-merging yangtze/api/test_s3_migration.py
CONFLICT (add/add): Merge conflict in yangtze/api/s3_file_migration.py
Auto-merging yangtze/api/s3_file_migration.py
Merge made by the 'recursive' strategy.
 yangtze/api/s3_file_migration.py                              |  792 +++++++-------
 yangtze/api/test_s3_migration.py                              |  152 +--
 yangtze/automation/workspace/tools/tools.json                 |   12 +-
 yangtze/client.py                                             |    9 +-
 yangtze/contacts/doctype/address/address.json                 |  478 ++++----
 yangtze/contacts/doctype/address/address.py                   |   84 ++
 yangtze/core/doctype/file/file.js                             |   11 +
 yangtze/core/doctype/file/file.py                             |  114 +-
 yangtze/core/doctype/scheduled_job_type/scheduled_job_type.py |    4 +-
 yangtze/core/doctype/user/user.json                           |    2 +-
 yangtze/core/workspace/users/users.json                       |    8 +-
 yangtze/desk/form/save.py                                     |  113 +-
 yangtze/desk/notifications.py                                 |   41 +-
 yangtze/desk/query_report.py                                  |    2 +-
 yangtze/desk/reportview.py                                    |  215 ++++
 yangtze/email/doctype/newsletter/newsletter.py                |    8 +-
 yangtze/handler.py                                            |   35 +-
 yangtze/hooks.py                                              |  123 +--
 yangtze/model/db_query.py                                     | 3407 +++++++++++++++++++++++++++++++++------------------------
 yangtze/model/workflow.py                                     | 3848 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++---
 yangtze/public/js/yangtze/form/formatters.js                  |   15 +-
 yangtze/public/js/yangtze/form/layout.js                      |   17 +-
 yangtze/public/js/yangtze/form/multi_select_dialog.js         |    1 -
 yangtze/public/scss/desk/breadcrumb.scss                      |    7 +-
 yangtze/translations/zh.csv                                   |    2 +
 yangtze/utils/response.py                                     |    8 +-
 yangtze/www/generate_job_card_qr.html                         |   96 ++
 yangtze/www/generate_job_card_qr.py                           |   57 +
 yangtze/www/job_card_info.html                                |  520 +++++++++
 yangtze/www/job_card_info.py                                  |   54 +
 yangtze/www/job_card_view.html                                |  209 ++++
 yangtze/www/job_card_view.py                                  |   73 ++
 32 files changed, 8115 insertions(+), 2402 deletions(-)
 create mode 100644 yangtze/www/generate_job_card_qr.html
 create mode 100644 yangtze/www/generate_job_card_qr.py
 create mode 100644 yangtze/www/job_card_info.html
 create mode 100644 yangtze/www/job_card_info.py
 create mode 100644 yangtze/www/job_card_view.html
 create mode 100644 yangtze/www/job_card_view.py
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze$ git add .
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze$ git commit 
On branch beumer-upgrade
Your branch and 'upstream/beumer-upgrade' have diverged,
and have 88 and 1 different commits each, respectively.

Cherry-pick currently in progress.
  (run "git cherry-pick --continue" to continue)
  (use "git cherry-pick --skip" to skip this patch)
  (use "git cherry-pick --abort" to cancel the cherry-pick operation)

nothing to commit, working tree clean
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtze$ 
