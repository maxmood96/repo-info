## `clojure:temurin-8-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:a70e45cab3262d67ffab4ef3925d21e6586adbe4f440fb4b1c33ac709d04b533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7481b68fc84c516e25d60748eccede4f5fed32594c69fae9556c211020facb4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (195041827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5f04a8369ac9ac99c88e5a0afa3c3c7815d2041aad0003adc20aaf749ae7cb`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:17:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:17:28 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:17:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:17:29 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 06:17:29 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 06:17:29 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:17:35 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 06:17:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 06:17:35 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 06:17:55 GMT
RUN boot
# Wed, 10 Apr 2024 06:17:56 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749f37dbf9d4dfdd37d7f198529a3e48fdf4dae1c886dfea29b00eebcd72ee5b`  
		Last Modified: Wed, 10 Apr 2024 06:39:20 GMT  
		Size: 103.6 MB (103591906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12de39d84b7db7631b5ee8d78af7416641b1bb2f8d1ba6f3cdf8612a970697aa`  
		Last Modified: Wed, 10 Apr 2024 06:39:12 GMT  
		Size: 3.5 MB (3498209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1c7153d120f64807f09294c42b3b099b46b88f84370e3ef398fb58d866fbdc`  
		Last Modified: Wed, 10 Apr 2024 06:39:15 GMT  
		Size: 58.8 MB (58820354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c74397b2734d9020636e6a4284df002fe76ed0d099662299ccff81b8549c59c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194007880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e259269f6ce3ea16a20c66b678bff5e7006b63c990a65637f457730abefa7fdb`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:38:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:38:51 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:38:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:38:53 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 04:38:53 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 04:38:53 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:38:58 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 04:38:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 04:38:58 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 04:39:18 GMT
RUN boot
# Wed, 10 Apr 2024 04:39:18 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fd11889651ce9cfe92f9a1350b046c825698b9cb23aa47fd46c345c9df41b2`  
		Last Modified: Wed, 10 Apr 2024 04:58:07 GMT  
		Size: 102.7 MB (102703040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def991de3517a967d7f8338ffe24032a007106f41e519ac32d6d8422af60ad4f`  
		Last Modified: Wed, 10 Apr 2024 04:58:00 GMT  
		Size: 3.3 MB (3322181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3e7274076bf2b430b0648390b44c5ac1e9842d1eb1d74b7f78539197bf5bb3`  
		Last Modified: Wed, 10 Apr 2024 04:58:03 GMT  
		Size: 58.8 MB (58820502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
