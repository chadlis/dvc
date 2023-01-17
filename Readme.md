git init
dvc init
dvc get https://github.com/iterative/dataset-registry get-started/data.xml -o data/data.xml
dvc remote add -d storage /Users/chadli/source/dvc_storage
dvc push

dvc stage add -n prepare \
                -p prepare.seed,prepare.split \
                -d src/prepare.py -d data/data.xml \
                -o data/prepared \
                python src/prepare.py data/data.xml
