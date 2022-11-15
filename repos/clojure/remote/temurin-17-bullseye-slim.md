## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:52952933982c20d21eb0d8007fe3d07307b60c54f551e840d40442eab7d7f901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:23ac82a4d1c5c4109a0d30bbfd28ada3d53e63d8164e2675eeb7a79d9306e78c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285318784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415c17ca3485b3d9c6a4246271c426562e0cfde072606e7322e37892a591f824`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:05:21 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Tue, 15 Nov 2022 17:57:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 17:59:43 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Tue, 15 Nov 2022 17:59:43 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 18:00:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Nov 2022 18:00:01 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Nov 2022 18:00:01 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 15 Nov 2022 18:00:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 15 Nov 2022 18:00:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e2f15985394be21a4e4a010fbea73bcb4ac9c162a40582171119a45451824`  
		Last Modified: Tue, 15 Nov 2022 13:08:12 GMT  
		Size: 192.4 MB (192431277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e5d17e525064da9a34caca8db8dcaf9a278a126967e78ce2e3f3f233e982dd`  
		Last Modified: Tue, 15 Nov 2022 18:11:51 GMT  
		Size: 61.5 MB (61473863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad353feaa50207dfeadc350888ed5ca938f7e7f0e9247d0e87334fbefda0714c`  
		Last Modified: Tue, 15 Nov 2022 18:11:43 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e6cac461ea60471782c4cc4f71686d0ff0eed897ae781cae7eb6aa78968572`  
		Last Modified: Tue, 15 Nov 2022 18:11:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a84262be49a49037906aab2429619732b12addb2ee15c5f616aa562136f2819f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282869843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f9dd9a9f54d6bdb3363100c55d148ffa9a05c7a1f2c66251bc487be501fb54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:49:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:54:33 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:54:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:56:13 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Tue, 15 Nov 2022 05:56:13 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:56:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Nov 2022 05:56:27 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Nov 2022 05:56:27 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 15 Nov 2022 05:56:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 15 Nov 2022 05:56:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0032fd948a5495fec37e26e9d086c7c0fa24d0623f43f8ad0471aac3350e5f61`  
		Last Modified: Tue, 15 Nov 2022 06:05:10 GMT  
		Size: 191.2 MB (191215234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d260aa1617d409fcbf5c40a1baddeafa09d9b6d425a2adcf2fb62a660b5b4a0f`  
		Last Modified: Tue, 15 Nov 2022 06:06:08 GMT  
		Size: 61.6 MB (61592990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67ceca4358722c5be603275b07b93e4b53a4939965ce7183fc2e23cb1355753`  
		Last Modified: Tue, 15 Nov 2022 06:06:02 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e269d18efbe652f7bd9f8e113ac3be5851eefca2423de5442fe717ca099b203`  
		Last Modified: Tue, 15 Nov 2022 06:06:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
