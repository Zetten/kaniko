# v0.4.0 Release - 10/01/2018

## New Features
* Add a benchmark package to store and monitor timings. [#367](https://github.com/GoogleContainerTools/kaniko/pull/367)
* Add layer caching to kaniko [#353](https://github.com/GoogleContainerTools/kaniko/pull/353)
* Update issue templates [#340](https://github.com/GoogleContainerTools/kaniko/pull/340)
* Separate --insecure-skip-tls-verify flag into two separate flags [#311](https://github.com/GoogleContainerTools/kaniko/pull/311)
* Updated created by time for built image [#328](https://github.com/GoogleContainerTools/kaniko/pull/328)
* Add Flag to Disable Push to Container Registry [#292](https://github.com/GoogleContainerTools/kaniko/pull/292)
* Add a new flag to cleanup the filesystem at the end [#370](https://github.com/GoogleContainerTools/kaniko/pull/370)

## Updates
* Update README to add information about layer caching [#364](https://github.com/GoogleContainerTools/kaniko/pull/364)
* Suppress usage upon Run error [#356](https://github.com/GoogleContainerTools/kaniko/pull/356)
* Refactor build into stageBuilder type [#343](https://github.com/GoogleContainerTools/kaniko/pull/343)
* Replace gometalinter with GolangCI-Lint [#349](https://github.com/GoogleContainerTools/kaniko/pull/349)
* Add Key() to LayeredMap and Snapshotter [#337](https://github.com/GoogleContainerTools/kaniko/pull/337)
* Add CacheCommand to DockerCommand interface [#336](https://github.com/GoogleContainerTools/kaniko/pull/336)
* Extract filesystem in order rather than in reverse [#326](https://github.com/GoogleContainerTools/kaniko/pull/326)
* Configure logs to show colors [#327](https://github.com/GoogleContainerTools/kaniko/pull/327)
* Enable shared config for s3 [#321](https://github.com/GoogleContainerTools/kaniko/pull/321)
* Update go-containerregistry. [#305](https://github.com/GoogleContainerTools/kaniko/pull/305)
* Tag latest in cloudbuild.yaml [#287](https://github.com/GoogleContainerTools/kaniko/pull/287)
* Set default home value [#281](https://github.com/GoogleContainerTools/kaniko/pull/281)
* Update deps [#265](https://github.com/GoogleContainerTools/kaniko/pull/265)
* Update go-containerregistry dep and remove unnecessary Options [#376](https://github.com/GoogleContainerTools/kaniko/pull/376)
* Add a bit more context to layer offset failures [#264](https://github.com/GoogleContainerTools/kaniko/pull/264)

## Bug Fixes
* Whitelist /busybox in the debug image [#369](https://github.com/GoogleContainerTools/kaniko/pull/369)
* Check --cache-repo is provided with --cache and --no-push [#374](https://github.com/GoogleContainerTools/kaniko/pull/374)
* Fixes a whitelist issue when untarring files in ADD commands. [#371](https://github.com/GoogleContainerTools/kaniko/pull/371)
* set default HOME env properly [#341](https://github.com/GoogleContainerTools/kaniko/pull/341)
* Review config for cmd/entrypoint after building a stage [#348](https://github.com/GoogleContainerTools/kaniko/pull/348)
* Enable overwriting of links (solves #351) [#360](https://github.com/GoogleContainerTools/kaniko/pull/360)
* Only return stdout when running commands for integration tests [#363](https://github.com/GoogleContainerTools/kaniko/pull/363)
* Whitelist /etc/mtab [#347](https://github.com/GoogleContainerTools/kaniko/pull/347)
* Added a KanikoStage type for each stage of a Dockerfile [#320](https://github.com/GoogleContainerTools/kaniko/pull/320)
* Make sure paths are absolute before matching files to wildcard sources [#330](https://github.com/GoogleContainerTools/kaniko/pull/330)
* Build each kaniko image separately [#324](https://github.com/GoogleContainerTools/kaniko/pull/324)
* support multiple tags when writing to a tarfile [#323](https://github.com/GoogleContainerTools/kaniko/pull/323)
* Snapshot only specific files for COPY [#319](https://github.com/GoogleContainerTools/kaniko/pull/319)
* Remove some constraints from our Gopkg.toml. [#318](https://github.com/GoogleContainerTools/kaniko/pull/318)
* Always snapshot files in COPY and RUN commands [#289](https://github.com/GoogleContainerTools/kaniko/pull/289)
* Refactor command line arguments and the executor [#306](https://github.com/GoogleContainerTools/kaniko/pull/306)
* Fix bug in SaveStage function for multistage builds [#295](https://github.com/GoogleContainerTools/kaniko/pull/295)
* Get absolute path of file before checking whitelist [#293](https://github.com/GoogleContainerTools/kaniko/pull/293)
* Fix support for insecure registry [#169](https://github.com/GoogleContainerTools/kaniko/pull/169)
* ignore sockets when adding to tar [#288](https://github.com/GoogleContainerTools/kaniko/pull/288)
* fix add command bug when adding remote URLs [#277](https://github.com/GoogleContainerTools/kaniko/pull/277)
* Environment variables with multiple '=' are not parsed correctly [#278](https://github.com/GoogleContainerTools/kaniko/pull/278)
* Ensure cmd.SysProcAttr is set before modifying it [#275](https://github.com/GoogleContainerTools/kaniko/pull/275)
* Don't copy same files twice in copy integration tests [#273](https://github.com/GoogleContainerTools/kaniko/pull/273)
* Extract intermediate stages to filesystem [#266](https://github.com/GoogleContainerTools/kaniko/pull/266)
* Fix process group handling. [#271](https://github.com/GoogleContainerTools/kaniko/pull/271)
* Only add whiteout files once [#270](https://github.com/GoogleContainerTools/kaniko/pull/270)
* Fix handling of the volume directive [#334](https://github.com/GoogleContainerTools/kaniko/pull/334)


# v0.3.0 Release - 7/31/2018
New Features
* Local integration testing [#256](https://github.com/GoogleContainerTools/kaniko/pull/256)
* Add --target flag for multistage builds [#255](https://github.com/GoogleContainerTools/kaniko/pull/255)
* Look for on cluster credentials using k8s chain [#243](https://github.com/GoogleContainerTools/kaniko/pull/243)

Bug Fixes
* Kill grandchildren spun up by child processes [#247](https://github.com/GoogleContainerTools/kaniko/issues/247)
* Fix bug in copy command [#221](https://github.com/GoogleContainerTools/kaniko/issues/221)
* Multi-stage errors when referencing earlier stages [#233](https://github.com/GoogleContainerTools/kaniko/issues/233)


# v0.2.0 Release - 7/09/2018

New Features
* Support for adding different source contexts, including Amazon S3 [#195](https://github.com/GoogleContainerTools/kaniko/issues/195)
* Added --reproducible [#205](https://github.com/GoogleContainerTools/kaniko/pull/205) and --single-snapshot [#204](https://github.com/GoogleContainerTools/kaniko/pull/204) flags
* Documented running kaniko in gVisor [#194](https://github.com/GoogleContainerTools/kaniko/pull/194)
* Update go-containerregistry so kaniko works better with Harbor and Gitlab[#227](https://github.com/GoogleContainerTools/kaniko/pull/227)
* Push image to multiple destinations [#184](https://github.com/GoogleContainerTools/kaniko/pull/184)

# v0.1.0 Release - 5/17/2018

New Features
* The majority of Dockerfile commands are feature complete [#1](https://github.com/GoogleContainerTools/kaniko/issues/1)
* Support for multi-stage Dockerfile builds [#141](https://github.com/GoogleContainerTools/kaniko/pull/141)
* Refactored integration tests [#126](https://github.com/GoogleContainerTools/kaniko/pull/126)
* Added debug image with a busybox shell [#171](https://github.com/GoogleContainerTools/kaniko/pull/1710)
* Added credential helper for Amazon ECR [#167](https://github.com/GoogleContainerTools/kaniko/pull/167)
 
