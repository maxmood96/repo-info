## `clojure:temurin-20-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:ba6f5027fbf0df8582761d5983a5b24923a778a5ee8c9a6873416039ebe54169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:854e9c4f55993b6a8a36a07bdb63720135140e67a16737f69a8886f7c23c97ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246706759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d710814bc0077551bde55752a036b91a9c96345c8253e860dbadeccf09eeb18a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:00:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Jul 2023 00:38:26 GMT
COPY dir:6a540db71f2a37db361084aee8addd6817cd7c4f18237e6f852a38e98bdb4182 in /opt/java/openjdk 
# Tue, 25 Jul 2023 00:38:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 00:39:45 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Tue, 25 Jul 2023 00:39:45 GMT
WORKDIR /tmp
# Tue, 25 Jul 2023 00:40:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 25 Jul 2023 00:40:01 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 25 Jul 2023 00:40:01 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 25 Jul 2023 00:40:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 25 Jul 2023 00:40:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd8dcabc383354545f1dd362a5a95eb6d392af95b3bedee879be058834a43e9`  
		Last Modified: Tue, 25 Jul 2023 00:43:21 GMT  
		Size: 153.8 MB (153791699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f8149d4de9aa085258cbffe7e9fcf86930ea5dbd0b52a6a95bfdf7dbf2ecd6`  
		Last Modified: Tue, 25 Jul 2023 00:44:18 GMT  
		Size: 61.5 MB (61496662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6cd806793534b5e6be5335f3920e09f579130f54628e8b24ce98777447a9f79`  
		Last Modified: Tue, 25 Jul 2023 00:44:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c62d2b0723d89479a1f2d136600b49f5e4184f68a234ccb47fd7bcf847c6f0`  
		Last Modified: Tue, 25 Jul 2023 00:44:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:08df48e245240fc10c970742ffd90b794f6b552d6c49b86764df7e927b05753d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243798837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b871888c3da545329c552d641870ade761eeb1f6fa8eeb3ef47a5b25c8beadf8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Jul 2023 00:45:52 GMT
COPY dir:d35c6357dd030960bb6081f48b2bc10afb3da11efc1525ff916214b03be70ddf in /opt/java/openjdk 
# Tue, 25 Jul 2023 00:45:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 00:47:08 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Tue, 25 Jul 2023 00:47:08 GMT
WORKDIR /tmp
# Tue, 25 Jul 2023 00:47:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 25 Jul 2023 00:47:22 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 25 Jul 2023 00:47:22 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 25 Jul 2023 00:47:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 25 Jul 2023 00:47:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7904f1e95e8cb22ce337c6df82fdcf6243ba5c312c817a19ddb6c438d9c701b2`  
		Last Modified: Tue, 25 Jul 2023 00:50:07 GMT  
		Size: 152.1 MB (152120075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8c433e22c9330d2b24a1b7ca630badfb6d6dec56bc7e6258b25ed5ce486c2a`  
		Last Modified: Tue, 25 Jul 2023 00:50:52 GMT  
		Size: 61.6 MB (61614790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd78c2cabc3c65cff83823bb46ab84df056a7a95eb78b9a9e5942757813c11dd`  
		Last Modified: Tue, 25 Jul 2023 00:50:46 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0e6ee992c7d0dcd184410b03e64351291c90da771960a1e0fdc9c6f4d2f4cd`  
		Last Modified: Tue, 25 Jul 2023 00:50:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
