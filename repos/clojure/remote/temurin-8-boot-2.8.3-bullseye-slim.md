## `clojure:temurin-8-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:49c21b3d23317b497303a79196177fa4e727f3054141ca1308075a547e80c6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:66ae5907457fa511c032d3e6ef766ee76d8aea47e4a20b49d2c1224c557cb5fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194912588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a38efea6e44d4039fe43f6c06af9503f55b83f7a92dcdd2bc50435481b84ca`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 06:12:55 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Tue, 12 Mar 2024 06:12:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 06:12:55 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 06:12:55 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 06:12:55 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 06:13:01 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 06:13:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 06:13:01 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 06:13:20 GMT
RUN boot
# Tue, 12 Mar 2024 06:13:21 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b714ceb7695c5119ff7513db7445ba5efd49ae5c2102b96d3001b8311d425af`  
		Last Modified: Tue, 12 Mar 2024 06:35:09 GMT  
		Size: 103.6 MB (103591873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0600a7cfd0fe7bcde42106b4a6da633a39d4f065286f50ffb6c3c8ead3041207`  
		Last Modified: Tue, 12 Mar 2024 06:35:00 GMT  
		Size: 1.1 MB (1077737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4416e24a52181a2e375e0c634e4efd920eb20bf54105f59a4a5539295507d844`  
		Last Modified: Tue, 12 Mar 2024 06:35:04 GMT  
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
