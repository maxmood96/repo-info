## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:e80e2ecabf7af06161a8886b2cfb78f63dcd92a5e554d40f4bc30d7d800fa0ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:43698ddc678d6e27aef6e6b399fbfbbec73a588c7b4801fdbe5f5f0da9c32a5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194909862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a7a355ab63e3595e4e4479698dc4c09a4327bac16e5b49d1c0376457f88f39`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:01:32 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:01:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:01:33 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:01:33 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:01:33 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:01:39 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:01:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:01:39 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:01:59 GMT
RUN boot
# Wed, 24 Jan 2024 22:01:59 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a6c4425e06b5d5ddb335e03599626d9fceaea0e8b99f56638d1bf0a6d7f98b`  
		Last Modified: Wed, 24 Jan 2024 22:32:38 GMT  
		Size: 103.6 MB (103591877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b57c1c6cdefa8141d80d7421a8282ae4a77eae20bb82bc243f3f877e1ba1d1`  
		Last Modified: Wed, 24 Jan 2024 22:32:30 GMT  
		Size: 1.1 MB (1079475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da32ba87dc7447882980b55e92cbdcc02c8fac28d5be58095a8581d2393742e6`  
		Last Modified: Wed, 24 Jan 2024 22:32:34 GMT  
		Size: 58.8 MB (58820555 bytes)  
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
