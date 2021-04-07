```
# mlops scaffold <cloud platform> <name>

$ mlops scaffold azure mlppoc
```

```
ml/
	infra/
		deploy.json
		deploy.parameters.prod.json
		deploy.parameters.stage.json
		deploy.parameters.dev.json
	experiments/
		notebooks.ipynb
	<project>/
		config.json
		common/
		util/
		pipeline/
			preprocessing/
				- batch - input dataset, output dataset, register
				- mini-batch - input , output 
				- single - input json/dict, output json/dict
				__init__.py
			train/
				- at scale
				- single compute/parallel compute
				- custom training
				- hyperdrive training
				- input dataset, output model
				- validate
				__init__.py
					def train()
					def score()
						- batch
						- mini-batch
						-
		__init__.py
			def init()
			def run(data):
				from pipeline.score import something
				someting(data)
	test/
		pipeline/
			preprocessing/
				test_init.py
				...
			train/
				test_init.py
				...
		test_init.py
	integration_test/
		test_integration.py
```

resources:
- default storage account - for registered datasets
- various storage accounts - source of raw datasets
	- silver
	- bronze
	- gold
keyvault
app insights
