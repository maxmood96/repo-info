## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:b4f763989ae1d0d84c0866255034505280ba60733be048642a1b08160f495e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1cd83b7ca42c139510476db84c47364ce6fdbb6193b9ffc966c8175fff09cb4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285495198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb42866dacdda52de1ca6b65bac0baba3e16cdfa867c89dd7fec90fbaa6f9fa4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Apr 2023 20:09:11 GMT
COPY dir:097a611561277927a8e367a60640ce12877b7a6373689dec24d5cfb76f99c807 in /opt/java/openjdk 
# Wed, 26 Apr 2023 20:09:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 20:12:27 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 26 Apr 2023 20:12:27 GMT
WORKDIR /tmp
# Wed, 26 Apr 2023 20:12:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 26 Apr 2023 20:12:43 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 26 Apr 2023 20:12:43 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 26 Apr 2023 20:12:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Apr 2023 20:12:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3dca630898b65b3e3d97ffce265d16549a24facef0348fd8a6d8d5aee0493b3`  
		Last Modified: Wed, 26 Apr 2023 20:24:23 GMT  
		Size: 192.6 MB (192580428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1e99d2c0e3a93ffede8d95b6a68f2ab7051cfa410b4851348eedd7d275a443`  
		Last Modified: Wed, 26 Apr 2023 20:26:52 GMT  
		Size: 61.5 MB (61495526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84040492425e5c1753f95d47ba5db903e0cc60921278c63b56e9367b7e7445d`  
		Last Modified: Wed, 26 Apr 2023 20:26:45 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d523daed056dd8074a6285b5377767422fd6343855361e5faa79fc6ba85e2852`  
		Last Modified: Wed, 26 Apr 2023 20:26:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8c4e1d6608655c7e559e8ebcc1fef6151487b5f7b24ef7802d8cae827541d059
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 MB (283051985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed3551e1dc25e32aeaa117a2114a68b02b9bca58e0285bb0ffa3770c949c13b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 17:49:05 GMT
COPY dir:d3d9f08d06fd1214b20f5d901cee398f498773bedf69f0d3cc795772967cfe44 in /opt/java/openjdk 
# Wed, 03 May 2023 17:49:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:50:36 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 03 May 2023 17:50:36 GMT
WORKDIR /tmp
# Wed, 03 May 2023 17:50:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 03 May 2023 17:50:50 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 03 May 2023 17:50:50 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 03 May 2023 17:50:50 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 03 May 2023 17:50:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6baebd3611c04da99c6391c894e4c5ba7eaa103bf201a26eba6d26bbdd244f42`  
		Last Modified: Wed, 03 May 2023 17:56:41 GMT  
		Size: 191.4 MB (191387733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c29ea17b74eb8018f990186af1199cf5d6b57d284c9e81ae4606fee11de2d4`  
		Last Modified: Wed, 03 May 2023 17:57:39 GMT  
		Size: 61.6 MB (61610508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d6dc48472448e945aa8d67c912964f343a5df58909677866b655bf086c1297`  
		Last Modified: Wed, 03 May 2023 17:57:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b0d923d1254a8b748574861e792682fd5a80099f821b8212d55642f2e76bcb`  
		Last Modified: Wed, 03 May 2023 17:57:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
