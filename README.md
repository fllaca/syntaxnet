# SyntaxNet Docker Image

## Using universal parser

### Download the corpus

```shell

# Assuming we have a /fer directory 
wget http://download.tensorflow.org/models/parsey_universal/Spanish-AnCora.zip
unzip Spanish-AnCora.zip

MODEL_DIRECTORY=/fer/Spanish-AnCora
```

### Run the parser

```shell
echo "Alfredo, pon una alarma a las 15:30" | syntaxnet/models/parsey_universal/parse.sh $MODEL_DIRECTORY | bazel-bin/syntaxnet/conll2tree
```

## Useful Links

* Syntaxnet: https://github.com/tensorflow/models/tree/master/syntaxnet
* Parsey Universal: https://github.com/tensorflow/models/blob/master/syntaxnet/g3doc/universal.md
* Similar project: http://www.whycouch.com/2016/07/how-to-install-and-use-syntaxnet-and.html
