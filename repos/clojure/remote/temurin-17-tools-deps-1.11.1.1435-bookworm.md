## `clojure:temurin-17-tools-deps-1.11.1.1435-bookworm`

```console
$ docker pull clojure@sha256:3e423a6786e2012eac0ee5bb6e1235a6ed1a6df2a467129f0512c542730639bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1435-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3ef44b44019e3242980b2eda61ff094ed890bee33cceb76197b61f5cbe86b665
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275165633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a7b750726d0cada8e19f3a011fd6e12ce4a35ada8e707225b844918f6fb52a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:24:17 GMT
COPY dir:61bea833528044db01491107d8c3fb583322243082c7798fd60ade98f7eb7613 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:24:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:26:47 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:26:47 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:27:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 21:27:07 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:27:07 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:27:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:27:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46193795e372883da3b4657b2893b9eba1f1bb03039ac6400ad2fb37f30b611`  
		Last Modified: Wed, 24 Apr 2024 21:48:00 GMT  
		Size: 145.1 MB (145095353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306d8d4f8244d044b580fe83c5cf7be05a59a72c2d8f220277deabf1b6216232`  
		Last Modified: Wed, 24 Apr 2024 21:49:52 GMT  
		Size: 80.5 MB (80492981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cc9de56e79f9240fd268fcb6f066b9648a9d5a82a1a16bd71c10c6836ea5d7`  
		Last Modified: Wed, 24 Apr 2024 21:49:43 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bb1f28014a3cbfb9d2d22042640ec3cb762dd3e8b19aeb6a420e9d768ce3fe`  
		Last Modified: Wed, 24 Apr 2024 21:49:43 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1435-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ed159c4d65e39a5b0e73480113f6cfa3bb00a7ee3438b509df2d7c9888d1eda6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.8 MB (273764781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299a640d65711ce48eea2cde49ba0b9ab88fccacb021c561809d883c01e3d376`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:08:43 GMT
COPY dir:894420f494a8d73ff0a7e5986ef0142218654b95343c81b2b9fc9a9d3ea0c174 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:08:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:10:56 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 19:10:56 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:11:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 19:11:12 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 19:11:12 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:11:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:11:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fefe737023ec01887dd5a91b2358786392594133742c3e42b86e75cce6fa4c5`  
		Last Modified: Wed, 24 Apr 2024 19:28:15 GMT  
		Size: 143.9 MB (143891869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11701b770def54d0ff10b2ac8abd48ee958ee505e4b5ac27fb25b50e2a18d41`  
		Last Modified: Wed, 24 Apr 2024 19:29:50 GMT  
		Size: 80.3 MB (80258555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1379f2e6f4de35e274d0921f9264f87ddf6f7ee447578a53827173f08e17fd0`  
		Last Modified: Wed, 24 Apr 2024 19:29:40 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41abef654f0c47139f9f793f0c367d287d0f0b888f6c4a9c14d7ab8da306124d`  
		Last Modified: Wed, 24 Apr 2024 19:29:40 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
