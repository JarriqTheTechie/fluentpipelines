FluentPipelines
FluentPipelines is a Python package that simplifies the creation and execution of data processing pipelines.

## Features

- **Pipeline Creation**: Easily create processing pipelines by chaining together operations.
- **Flexible Operations**: Define custom operations by subclassing `PipelineOperation`.
- **Convenient Interface**: Intuitive `send`, `through`, `then`, and `then_return` methods for building and executing pipelines.
- **Error Handling**: Robust error handling for smooth pipeline execution.

```
pip install fluentpipelines
```
# Usage


### Import PyPipeline
```
from fluentpipelines import pipeline
```

### Define custom operations by subclassing PipelineOperation
```
class MyOperation(PipelineOperation):
    def process(self, data):
        # Define processing logic here
        return processed_data
```

### Create a pipeline
```
pipeline = pipeline.send(initial_data).through([MyOperation, AnotherOperation]).then_return()
```

### Custom Operations
```
class MyOperation(PipelineOperation):
    def process(self, data):
        # Define processing logic here
        return processed_data
```


## Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
This package was inspired by the need for a simple and flexible data pipeline solution.