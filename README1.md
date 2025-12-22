yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtzeerp$ git status 
On branch beumer-TMS
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   yangtzeerp/assets/dashboard_chart/asset_value_analytics/asset_value_analytics.json
        modified:   yangtzeerp/buying/dashboard_chart/purchase_order_trends/purchase_order_trends.json
        modified:   yangtzeerp/selling/dashboard_chart/sales_order_trends/sales_order_trends.json

no changes added to commit (use "git add" and/or "git commit -a")
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtzeerp$ git cherry-pick --quit
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtzeerp$ git status 
On branch beumer-TMS
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   yangtzeerp/assets/dashboard_chart/asset_value_analytics/asset_value_analytics.json
        modified:   yangtzeerp/buying/dashboard_chart/purchase_order_trends/purchase_order_trends.json
        modified:   yangtzeerp/selling/dashboard_chart/sales_order_trends/sales_order_trends.json

no changes added to commit (use "git add" and/or "git commit -a")
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtzeerp$ git cherry-pick --abort
error: no cherry-pick or revert in progress
fatal: cherry-pick failed
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtzeerp$ git cherry-pick --quit
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtzeerp$ git status
On branch beumer-TMS
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   yangtzeerp/assets/dashboard_chart/asset_value_analytics/asset_value_analytics.json
        modified:   yangtzeerp/buying/dashboard_chart/purchase_order_trends/purchase_order_trends.json
        modified:   yangtzeerp/selling/dashboard_chart/sales_order_trends/sales_order_trends.json

no changes added to commit (use "git add" and/or "git commit -a")
yangtze@ERP-Yangtze-Test:~/yangtze-bench/apps/yangtzeerp$ 
