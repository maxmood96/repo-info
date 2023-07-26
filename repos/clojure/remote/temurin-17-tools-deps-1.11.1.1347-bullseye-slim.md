## `clojure:temurin-17-tools-deps-1.11.1.1347-bullseye-slim`

```console
$ docker pull clojure@sha256:094acac7a4690eb3bb8707eee2aff626a9de55aedf164bd5fd0966673b62fdb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1347-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8be5d34471c632a0954a75e69208650aa8edb94a8b920a71313b8ea9a43c8aea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285495432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39989f63e3d231b9398a6b7d356ae4c0ca22be3a4c1bbf3f6d583ab3f08caa34`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:00:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 11:24:32 GMT
COPY dir:4f02f3c240ecc691ff41263b0454f619d51a2ba11a57fe51c0e31e7ff62a9194 in /opt/java/openjdk 
# Wed, 05 Jul 2023 11:24:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 11:27:20 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Wed, 05 Jul 2023 11:27:20 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 11:27:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Jul 2023 11:27:36 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Jul 2023 11:27:36 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 05 Jul 2023 11:27:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Jul 2023 11:27:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fafbbd507c7f35e198981926b1a326f224d7e89d5a693df01bea8a92ba4e7d1b`  
		Last Modified: Wed, 05 Jul 2023 11:36:02 GMT  
		Size: 192.6 MB (192580435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062744121a547ddef9530c299df1b3fdb2a602c17473298f6c41bc964682f69c`  
		Last Modified: Wed, 05 Jul 2023 11:38:16 GMT  
		Size: 61.5 MB (61496595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5048307abd6949cebb745f8321992b79d813c40352f171c93e7da7da97d0abbf`  
		Last Modified: Wed, 05 Jul 2023 11:38:09 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92c02ed7f2604660c22073eb1306a19fbf106e52530e51087bcfb926d1f3bd8`  
		Last Modified: Wed, 05 Jul 2023 11:38:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1347-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:49360e1f9b2e5e48863f28f324abe26cd0bbf33c9572fc680b61ddde1a989494
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235217178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de69fb2da41285d651d06de0fb2526c0ca512ec2b5ec43e1f75610dd4fa211d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Jul 2023 22:58:45 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Tue, 25 Jul 2023 22:58:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:01:44 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Tue, 25 Jul 2023 23:01:45 GMT
WORKDIR /tmp
# Tue, 25 Jul 2023 23:01:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 25 Jul 2023 23:01:58 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 25 Jul 2023 23:01:58 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 25 Jul 2023 23:01:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 25 Jul 2023 23:01:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c798e6c54e318dbfe8b5b1325d38da64ea5e5a387b26c620cc1f0c2820d0f70a`  
		Last Modified: Tue, 25 Jul 2023 23:05:13 GMT  
		Size: 143.5 MB (143538051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83832eac0161537daf790610e6490c4fc09e476b436f56958c942f39f33c972a`  
		Last Modified: Tue, 25 Jul 2023 23:07:16 GMT  
		Size: 61.6 MB (61615155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aeeb3d36742c1633a50bcaff6dc028561490229375e514329f77a1ca8ae17c`  
		Last Modified: Tue, 25 Jul 2023 23:07:10 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1103e25289a6bddb16f7b5782b8312ea8300aa29ea53a8691a54cd0ca43278e8`  
		Last Modified: Tue, 25 Jul 2023 23:07:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
