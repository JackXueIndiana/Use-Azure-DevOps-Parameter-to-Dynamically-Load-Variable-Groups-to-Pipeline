# Use-Azure-DevOps-Parameter-to-Dynamically-Load-Variable-Groups-to-PipeLine
This demo is to show how to use Azure DevOps parameter to select desired variable group pipeline at runtime. Assume you have two variable groups in library and have granted the permission to the pipeline (picture var_grp_1):
- prod_var_grp with a variable name='region' value='westus'
- test_var_grp with a variable name='region' value='eastus'

If you run the yaml file with the selection of (picture var_grp_2)
image='ubuntu-latest'
deploy_region='prod_var_grp'

Then the three CmdLine will echo the following:
- building 20240227.19 with ubuntu-latest
- deploy_region = prod_var_grp
- westus
