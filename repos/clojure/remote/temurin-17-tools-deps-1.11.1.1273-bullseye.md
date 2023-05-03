## `clojure:temurin-17-tools-deps-1.11.1.1273-bullseye`

```console
$ docker pull clojure@sha256:6180877efadc64c548cfd908b105963ce5f486e7c3ad67e72837d650e9eb70a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1273-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:df17c08816696f95b9ac1d466e6b0aeb37532e5711b33c8e736e13cccd8f7a09
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319510433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea3687c3a955bbb4d8b9a6be194294ee1410290be24ce320cc9802673c904f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 02 May 2023 23:46:50 GMT
ADD file:fc290cf8ddb984325474583faa79c5a98c5ea0ec7f606bf360251f63acecf389 in / 
# Tue, 02 May 2023 23:46:51 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 20:29:34 GMT
COPY dir:097a611561277927a8e367a60640ce12877b7a6373689dec24d5cfb76f99c807 in /opt/java/openjdk 
# Wed, 03 May 2023 20:29:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:31:36 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 03 May 2023 20:31:36 GMT
WORKDIR /tmp
# Wed, 03 May 2023 20:31:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 03 May 2023 20:31:52 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 03 May 2023 20:31:52 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 03 May 2023 20:31:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 03 May 2023 20:31:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:918547b9432687b1e1d238e82dc1e0ea0b736aafbf3c402eea98c6db81a9cb65`  
		Last Modified: Tue, 02 May 2023 23:49:58 GMT  
		Size: 55.0 MB (55049070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4691a7487ede1e6dd3accb93b84f63e7ba0a18afb5a6dde1cb2605bdef6cce`  
		Last Modified: Wed, 03 May 2023 20:38:14 GMT  
		Size: 192.6 MB (192580399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b948fa5bac2d445fd7c6c55aca1e130a19941fdbc0fcff7f0a2013a73433e4dd`  
		Last Modified: Wed, 03 May 2023 20:39:18 GMT  
		Size: 71.9 MB (71879956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9da316c43f862e11f4fced4492065d8e265cbcbd966e99687330e79cf9a8fb2`  
		Last Modified: Wed, 03 May 2023 20:39:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76204b05ea84e3e122f916abb8baffa29c6693fdef94612b7fb72e09ba97d37c`  
		Last Modified: Wed, 03 May 2023 20:39:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1273-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d2347115ad51e39bdc612eb6b3d34481fef09ea2978facbb99f3f2012ccd0a87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317078147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02574811dc15bb17b131908444fc02b9eff0a4f3002ca0015fd4ee3e4680d645`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:43:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 17:48:34 GMT
COPY dir:d3d9f08d06fd1214b20f5d901cee398f498773bedf69f0d3cc795772967cfe44 in /opt/java/openjdk 
# Wed, 03 May 2023 17:48:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:50:20 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 03 May 2023 17:50:20 GMT
WORKDIR /tmp
# Wed, 03 May 2023 17:50:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 03 May 2023 17:50:34 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 03 May 2023 17:50:34 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 03 May 2023 17:50:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 03 May 2023 17:50:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54e3dfe953384be82597fea580dc9ef9ebb8b53e65fc436e07311295d7e9202`  
		Last Modified: Wed, 03 May 2023 17:56:22 GMT  
		Size: 191.4 MB (191387699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c6ba92ee17a5cb76a13f0bd62679a4c815a62db1d5069ff99b799d2e3ab9d2`  
		Last Modified: Wed, 03 May 2023 17:57:22 GMT  
		Size: 72.0 MB (71996728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd9359668f28b1826964c8abfa6ba1833a6c7387dda4ff0f1948a1ec7df699f`  
		Last Modified: Wed, 03 May 2023 17:57:16 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43abc36873969757ad2678a9ac3fd005622909b4b716295ad43c31917ff4ee3`  
		Last Modified: Wed, 03 May 2023 17:57:16 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
