# YAML
YAML (YAML Ain't Markup Language) is a human-readable data serialization format. It stands out for its simplicity and readability, making it popular for configuration files and data interchange between programming languages. YAML files typically use indentation to represent data structures like lists and dictionaries, making it easy for humans to understand and edit directly.

Here's a simple example of YAML:

```yaml
# Example YAML document
name: John Doe
age: 30
address:
  street: 123 Main St
  city: Anytown
  state: CA
  zip: 12345
```

In this example:

- `name` and `age` are scalar values (strings or integers).
- `address` is a mapping (similar to a dictionary or object in other languages), with keys (`street`, `city`, `state`, `zip`) and corresponding values.

# YAML in CodeBuild
In AWS CodeBuild, YAML (YAML Ain't Markup Language) is used for defining build spec files. A build spec file is a YAML-formatted file that contains information about the build process, such as the build phases, commands to run, environment variables, and more.

With YAML, you can define the steps your build process should take, specify dependencies, set environment variables, and configure various aspects of the build environment.

Here's a simple example of a YAML-based build spec file in CodeBuild:

```yaml
version: 0.2

phases:
  install:
    runtime-versions:
      nodejs: 12
  build:
    commands:
      - npm install
      - npm run build
  post_build:
    commands:
      - aws s3 sync dist/ s3://my-bucket
```

In this example:

- `version: 0.2` specifies the version of the build spec syntax being used.
- `phases` define different stages of the build process, such as `install`, `build`, and `post_build`.
- Under each phase, `commands` are specified, which contain the actual shell commands to be executed during that phase.
- In the `install` phase, it specifies the runtime version of Node.js to use.
- In the `build` phase, it installs dependencies using npm and then builds the project.
- In the `post_build` phase, it synchronizes the build artifacts with an S3 bucket.

This YAML file provides a clear and concise way to define the build process for your project within AWS CodeBuild.


# Example YAML
```yaml
my-course: "AWS MLOps"
version: 1.0
is_public: true
release_date: 2024-01-02
pre-enroll: null
category:
  - AWS
  - MLOps
  - AWS Certified
  - Gaurav
course_dev: ["hello","world","to","you"]
dev_details:
  - name: "Gaurav"
    email: "kandelgaurav7@gmail.com"
    role: "Data Scientist"
  - name: "Monika"
    email: "monikamalani5times@gmail.com"
    role: "Data Engineer"
  - {name: "Rahul", email: "rahulk@gmail.com", role: "Finance"}
```