## `clojure:temurin-11-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:b65031bdb755fabbb3d5121f82d0ba70765245bdd27f5f9863251f97b2704a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5aa7683b2fc8839e34c1fae6d5fccc949cb488569f438101a12359975bcaf0a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236713862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ff5ac7bb87788d317b10c4c35b3196bf5dfe7219ff2a24a9982c80c3236b54`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:11:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:58:35 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:58:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:58:37 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 02:58:37 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:58:37 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:58:43 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 02:58:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:58:43 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 02:59:01 GMT
RUN boot
# Thu, 28 Mar 2024 02:59:01 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49a6ac31b34979fe9ad3cbc392d1e9236c7163db662ad2db2662f3d8c2227e1`  
		Last Modified: Thu, 28 Mar 2024 03:19:31 GMT  
		Size: 145.3 MB (145271203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76ae4313e02ca304686e027b7d873f321d116a379b4c382d704362518e7cf00`  
		Last Modified: Thu, 28 Mar 2024 03:19:21 GMT  
		Size: 3.5 MB (3498176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1e131b7458fbf7b51d4746b0e4cd1df4250fa1d74887af5a87acc0021ae7c6`  
		Last Modified: Thu, 28 Mar 2024 03:19:24 GMT  
		Size: 58.8 MB (58820302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f782bea79403fb899c59f6a1d29fec38596067cef7a13ee83e662426c7d113ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233305275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64988e07a4e8040a6f6e0f127d79fb9486115db75b1ec7ea970a7d489c7fa84`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:32:45 GMT
COPY dir:d5fb8d9a38dea7496f2aff176bc9a34bbca80551c2dc57109d2dae5907a339ee in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:32:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:32:49 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 02:32:49 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:32:49 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:32:54 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 02:32:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:32:54 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 02:33:11 GMT
RUN boot
# Thu, 28 Mar 2024 02:33:11 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7819794f44d5487fb5284f90132fb8e3a770cac3a81ff8a43630aa0ffcd999db`  
		Last Modified: Thu, 28 Mar 2024 02:49:43 GMT  
		Size: 142.0 MB (142006296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3f706cdf1e853b9b9001be26fc6e5e9debedc1b673e0935577ac20db1b949d`  
		Last Modified: Thu, 28 Mar 2024 02:49:35 GMT  
		Size: 3.3 MB (3322108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fb84813581ea89ff945382e9cb41ba79e875789e9be6e053b8313a2813f9c8`  
		Last Modified: Thu, 28 Mar 2024 02:49:37 GMT  
		Size: 58.8 MB (58820437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
