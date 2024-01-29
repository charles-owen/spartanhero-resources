# The spartanhero-resources

In order to avoid student projects that are massive
on submission, we are providing most of the resources
for the project in this GitHub repository. These can be
added to a student project, but will not be uploaded
to the server on submit.

To use, add this content to the root CMakeLists.txt file:

```
# Fetch spartanhero-resources from Github
include(FetchContent)
FetchContent_Declare(
        spartanhero-resources
        GIT_REPOSITORY https://github.com/charles-owen/spartanhero-resources.git
        GIT_TAG origin/main
)

FetchContent_MakeAvailable(spartanhero-resources)

file(COPY ${spartanhero-resources_SOURCE_DIR}/resources/ DESTINATION ${CMAKE_CURRENT_BINARY_DIR}/)
```

This will automatically download the repository and 
add the contents to your project resources.
