# pipelines-generic

some pipeline definitions for my projects

## Folder structure

### `presets/`

The definitions of full pipelines.  
Typically the place where most pipelines reference to.

#### Presets

- Dotnet Libraries
  > packages as class library and publishes to packages
- Dotnet Tools
  > packages as executable and publishes to releases

### `pipelines/`

The definitions of pipeline building blocks.  
Used by `presets/` to define full pipelines.  
Custom pipelines can be made by referencing to specific parts of these building blocks.

#### Definitions

- dotnet
  - libraries (mainly class libraries)
    - build
    - test (might skip)
    - publish (one or both)
      - **package**
      - release
  - tools (full executables)
    - build
    - test (might skip)
    - publish (one or both)
      - package
      - **release**
