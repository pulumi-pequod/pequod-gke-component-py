# pequod-gke-component-py
Implements GKE component provider (components as components) in Python that can be used across languages.

## References
* Docs: https://github.com/pulumi/pulumi/blob/master/sdk/python/lib/pulumi/provider/experimental/ComponentProvider.md
* Examples:
  * https://github.com/julienp/cloudrun/tree/main
  * https://github.com/mikhailshilkov/comp-as-comp/tree/main/py 

# Usage
To use the component, make sure your pulumi CLI is at version 3.149.0 or later. 
```bash
pulumi version
```

Then, in the folder that contains the Pulumi program (regardless of language) that is using the component, run
```bash
pulumi package add https://github.com/pulumi-pequod/pequod-gke-component-py
```

This will generate the SDK for the language the Pulumi project is written in and provide the import statement.

Can also specify a given release as follows:
`pulumi package add https://github.com/pulumi-pequod/pequod-gke-component-py@v1.0.0`
