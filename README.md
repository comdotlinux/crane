# crane
A Composite Github Action that eases the usage of google/go-containerregistry in your project

### What
- https://github.com/google/go-containerregistry has some interesting things to use (See Readme for usage)
- After using this action you should have a crane command available for you to use installed for that github workflow.
    

### Why
- Mostly when workign with different remote docker registries, it is difficult to move docker images between two registries.
    - When docker image registries are separated fro dev and prod, you need to move the docker image before the deployment.
    - When using the default docker commandline, the only way to do this is
        1. Pull the docker image
        1. Tag the local docker image with the name of the destination docker image registry
        1. Push the new docker image
        - This is fine but wastes time and network resources, as we cannot benefit from the docker layer caching becuase before pushing (i.e. when pulling) you cannot know if any layers exist in the desination.

#### Roadmap
* See the Issues / Milestones