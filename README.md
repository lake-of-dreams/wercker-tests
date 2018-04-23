# wercker-tests
A  repository for testing pipelines in wercker
 
To run these tests fork this repository and add it as an applicaiton in Wercker. Then set up the following workflow:

```
build --> test-docker-build1        --> test-docker-build2           Tests internal/docker-build
          test-docker-push-classic1 --> test-docker-push-classic2    Tests internal/docker-push (committing and pushing pipeline container)
          test-docker-scratch-push1 --> test-docker-scratch-push2    Tests internal/docker-scratch-push
```

Then run the `build` pipeline,  either manually (easier) or by making a token edit to your clone of this repo and pushing it.

See the [latest runs on app.wercker.com](https://app.wercker.com/nigeldeakin/wercker-tests/runs)

See the [latest runs on dev.wercker.com](https://dev.wercker.com/nigeldeakin/wercker-tests/runs)
