## `clojure:temurin-17-tools-deps-1.11.1.1413-bullseye-slim`

```console
$ docker pull clojure@sha256:2eddcc298b8174e862645a4eceec2e5f42e9fe5e588faf2c573bdf7ef356f80b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1413-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6b65758812cd90db237349d06832725a5048812119548cf6fdc862779a29a271
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237688074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d3321ddb2dba2948effdc11a726359b6d9dad7b8ec3f0f7e1b2d1fa5a9c70b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Aug 2023 20:48:51 GMT
COPY dir:6777d1f77166c2ecdd8f4eb23f5fd82574aa8a90fd65d6dff981fbb31778a3d1 in /opt/java/openjdk 
# Thu, 31 Aug 2023 23:31:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2023 23:38:04 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 31 Aug 2023 23:38:04 GMT
WORKDIR /tmp
# Thu, 31 Aug 2023 23:38:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 31 Aug 2023 23:38:20 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 31 Aug 2023 23:38:20 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 31 Aug 2023 23:38:20 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 31 Aug 2023 23:38:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65006a4851e206ccc53a9bf891b081e6fefbdbe0fcb897d670970fc7f2eff9ea`  
		Last Modified: Thu, 31 Aug 2023 20:51:41 GMT  
		Size: 144.8 MB (144775820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5044695fd17bf3f973e31581a2e8b9aba6ffae8a40434ff241ac30305d9e0b`  
		Last Modified: Thu, 31 Aug 2023 23:47:09 GMT  
		Size: 61.5 MB (61493559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a9da5e7b90344baa0cd3afe316d7e7b261298d41c2aebe2fbec7e1042aa158`  
		Last Modified: Thu, 31 Aug 2023 23:47:01 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0083784da58fdcbd300f81a2c9976afde929e5ba9ea112091cc13d29b46ff0`  
		Last Modified: Thu, 31 Aug 2023 23:47:01 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1413-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:68731d8cd1e4be897a88e8010916cc2df609aa18320cbc231088be3c58038e2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235218922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5750c5b0b36b9bd72f285248b32abc4a49727ccc2e874e5b2cee9cc6a7fddd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Aug 2023 21:24:25 GMT
COPY dir:544cc8a0b662cd03d0780bbc88fa0ab8d4ff7ef38b3da70f9f97f586944edbe6 in /opt/java/openjdk 
# Thu, 31 Aug 2023 22:25:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2023 22:27:32 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 31 Aug 2023 22:27:33 GMT
WORKDIR /tmp
# Thu, 31 Aug 2023 22:27:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 31 Aug 2023 22:27:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 31 Aug 2023 22:27:47 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 31 Aug 2023 22:27:47 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 31 Aug 2023 22:27:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db320ad0aabde9ef892d611629818359b8a0e753d16e7c3cb1a7c4ef14730d6`  
		Last Modified: Thu, 31 Aug 2023 21:26:45 GMT  
		Size: 143.5 MB (143543485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513da619cb3ffeef6f8d3e5e465330e4d57a1aa6d379374e849e091daa96d9b2`  
		Last Modified: Thu, 31 Aug 2023 22:35:07 GMT  
		Size: 61.6 MB (61611605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b048bb5b4847b337ee6e0d571d0372673069e324ddf957a68b6acd9d933a79e`  
		Last Modified: Thu, 31 Aug 2023 22:35:01 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baff7a2d0df913754bc236717d15983ec310120e3888c7288a8d06ac20d8543f`  
		Last Modified: Thu, 31 Aug 2023 22:35:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
