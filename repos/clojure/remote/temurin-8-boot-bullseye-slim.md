## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:4de6b67863a01b396d75dc64e91148b403f7ff69b8851a95e9da9a0bc3086280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a1d5c7aae48eb73159010407864b2a0cdd831b556d103f72acd76986d0aee46f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194909655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89394b7207b2b8360899a29b8c4ad83cef949492234d800d6a9c056b153501d3`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:44:36 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:44:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:44:37 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:44:37 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:44:37 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:44:42 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:44:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:44:42 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:45:02 GMT
RUN boot
# Wed, 31 Jan 2024 23:45:03 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f1c7bfdaddc71e83c67b85b893fc8356c320085ad7fd07d8155f9936128564`  
		Last Modified: Thu, 01 Feb 2024 00:06:04 GMT  
		Size: 103.6 MB (103591889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d94d1e922b6270e9142d3637660872c8fd85701a03c68957add4f38f6eb650d`  
		Last Modified: Thu, 01 Feb 2024 00:05:56 GMT  
		Size: 1.1 MB (1079453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a131cfac0c5f903f871c34b93b6a7f9ea331f090771a9824af28bf16bde331ca`  
		Last Modified: Thu, 01 Feb 2024 00:06:00 GMT  
		Size: 58.8 MB (58820486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d73657ccc2e68b3332c5d33b10ae6bb0d89d1d752d788d9b3f4b5f0bd5b2a1f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192654217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3dd82aa232ee49714f642403b9a1587eeb50b8ed49a218162a3369162b22540`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:08:09 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:08:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:08:12 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:08:12 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:08:12 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:08:16 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:08:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:08:17 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:08:33 GMT
RUN boot
# Wed, 24 Jan 2024 22:08:33 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05dcc0e0197cd1663367a24ef26acebe43e8cf5f6e2398a0f0ce82dd0cf7aacc`  
		Last Modified: Wed, 24 Jan 2024 22:32:58 GMT  
		Size: 102.7 MB (102703041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac99a81dea99338a05455d17074cfca18496154618c9fb031a670c897637f4d0`  
		Last Modified: Wed, 24 Jan 2024 22:32:51 GMT  
		Size: 1.1 MB (1066840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cde3ad8150cd0f545bbb54a0b3fdbb5d6a76a6ccedc0817aef0a755baceaf29`  
		Last Modified: Wed, 24 Jan 2024 22:32:54 GMT  
		Size: 58.8 MB (58820326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
