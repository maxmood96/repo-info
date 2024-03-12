## `clojure:temurin-8-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:6f570ccdf23d85dc4bd3e3d16b3b816dbfb68302c011568aeb233aad4f17171e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:34a9912925b817f4471034818e4aa8e93bdd47bb4126914e3bbd1f5b5a2b2a57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194912477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b759d3a8c8cef1fb7682b2aa9ebac6ba13c64bf8183c28e634ad12e25a98e0`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:48:40 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:48:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:48:41 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 01:48:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 01:48:41 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:48:47 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 01:48:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 01:48:47 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 01:49:06 GMT
RUN boot
# Tue, 13 Feb 2024 01:49:06 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41190a3d826a196367bcb15e909443c6b1b2fc4d1bedc92ad3a5af7d1024b2f0`  
		Last Modified: Tue, 13 Feb 2024 02:10:21 GMT  
		Size: 103.6 MB (103591873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5833b632753489d9fb42950d3a16d1b2615988e6ae360c6113e41bd913550078`  
		Last Modified: Tue, 13 Feb 2024 02:10:13 GMT  
		Size: 1.1 MB (1077690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f487a7b5ce06bffb75b7af806830a50a87417593087c61a56b0e2487d1fb701`  
		Last Modified: Tue, 13 Feb 2024 02:10:16 GMT  
		Size: 58.8 MB (58820489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b79129e5d2a1f03ccdf24353edbcdcc436118cb32b9734360bda6ecc70678c8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192659434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cbee9e10e0c75bd530a6522339832fdfeb1724bdab27718b6f643b9bd0a665`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:45:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 01:45:12 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Tue, 12 Mar 2024 01:45:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 01:45:15 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 01:45:15 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 01:45:15 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 01:45:20 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 01:45:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 01:45:20 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 01:45:38 GMT
RUN boot
# Tue, 12 Mar 2024 01:45:38 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb35a23c2857877f105c7b0bb770a8af7e1a757d2375be42f9d12c0f5ecb1fc`  
		Last Modified: Tue, 12 Mar 2024 02:03:27 GMT  
		Size: 102.7 MB (102703020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec55edae8032224de0aef566119bb5b611dbf99155051c477f546af9b4b3cec`  
		Last Modified: Tue, 12 Mar 2024 02:03:20 GMT  
		Size: 1.1 MB (1064977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471bc4e380426502d71aa8e8cb3fbddfb0983fee9d7705033edcffea123a1a7b`  
		Last Modified: Tue, 12 Mar 2024 02:03:30 GMT  
		Size: 58.8 MB (58820321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
