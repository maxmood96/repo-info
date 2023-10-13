## `clojure:temurin-11-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:5c7718372a7a2239c1080ec7daa9a01e09232fba075ab0425e2ebc18825b205f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d7ed6476c7818d6be19ba8e26715440840fe04f2fc990043526ccde1cdc799e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236297838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5880d5382599971392b4ebcb2851ee36f440253e4db10a8a8e46be5aa99a6ad`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:31:21 GMT
COPY dir:ac445271830068829c3bd23eb1c86ee02cd9bb1649e3c49d8839a5a364b933c2 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:31:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:31:22 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 01:31:22 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:31:22 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:31:28 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 01:31:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:31:28 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 01:31:46 GMT
RUN boot
# Fri, 13 Oct 2023 01:31:46 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412962c371ae01af0e4de74aef277a006799891be3a74648fb62d23a45c4bd12`  
		Last Modified: Fri, 13 Oct 2023 01:46:40 GMT  
		Size: 144.8 MB (144825953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bcc21f378626d86802de06e86e62f887f804e95d4b159736e06209ce0402581`  
		Last Modified: Fri, 13 Oct 2023 01:46:29 GMT  
		Size: 3.5 MB (3501459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce97cf70a738a0f6f25f9012a079f231df7c1fbb97b1f504a106495f0ebcee43`  
		Last Modified: Fri, 13 Oct 2023 01:46:32 GMT  
		Size: 58.8 MB (58820552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c176a162994140cc3aea3a775118a2249b6acc6bcca980b3daebca2b1a9ff74d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232895425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79c094a6b2e81694d94493baf56d3f7528a1d0decf007e7361164385149729e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:59:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 10:12:35 GMT
COPY dir:b4903e9e1c2782550c5bca9cb7b0f840b4fdb810848e07ca44af328ac9dd84f6 in /opt/java/openjdk 
# Fri, 13 Oct 2023 10:12:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 10:12:38 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 10:12:38 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 10:12:38 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 10:12:44 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 10:12:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 10:12:44 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 10:13:00 GMT
RUN boot
# Fri, 13 Oct 2023 10:13:00 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e7aa7d3902d954c470f86fe2b38acaf6172ca287d14a276c679a36a75e4824`  
		Last Modified: Fri, 13 Oct 2023 10:29:43 GMT  
		Size: 141.6 MB (141570614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef433121823e89ce82a0c156e8cfdf6614332d432f7e506af977e6e8252b0ec`  
		Last Modified: Fri, 13 Oct 2023 10:29:34 GMT  
		Size: 3.3 MB (3325234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2495e3abb88294236d2f859cbc190fd25636b2458b7471714ab20a81fcc581f4`  
		Last Modified: Fri, 13 Oct 2023 10:29:38 GMT  
		Size: 58.8 MB (58820293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
