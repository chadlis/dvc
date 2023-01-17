git init
dvc init
dvc get https://github.com/iterative/dataset-registry get-started/data.xml -o data/data.xml

dvc remote add -d storage gdrive://1ClPp0GWxaLNqDfII7RJS4Vxr4LSvmsTq
