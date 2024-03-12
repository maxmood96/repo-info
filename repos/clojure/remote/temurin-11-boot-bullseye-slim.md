## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:31030412ccf0a224a9ad8ea7b74f371e12f43f5b6896c0c99aebac73b1c365cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6f6403c68819d6ae4b2f82aa7523b11f0de80b10c20e1368d0e7e2a407c6ee83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236591872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a57a2f18faf054e7871eb71a5e6c047ebaa090031f074f7e318f9ec20114c6`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 06:18:39 GMT
COPY dir:9807503b62b5ec57f5790350ba2323b4402a31264d57970336b28a606d7a3a68 in /opt/java/openjdk 
# Tue, 12 Mar 2024 06:18:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 06:18:40 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 06:18:40 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 06:18:40 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 06:18:46 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 06:18:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 06:18:46 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 06:19:05 GMT
RUN boot
# Tue, 12 Mar 2024 06:19:05 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b61eedf4152e446c791ad3f45ad9ce7e0dd61af7bf4b12af581b20940300b28`  
		Last Modified: Tue, 12 Mar 2024 06:38:20 GMT  
		Size: 145.3 MB (145271154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850dc483b78825b3111d52e9d16576bad8aacd660236468450c30d05cc7694ae`  
		Last Modified: Tue, 12 Mar 2024 06:38:09 GMT  
		Size: 1.1 MB (1077735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4382f69046392ad8cb1e4ed334f0198599c6874b7b2195e82819cc0ae309c61a`  
		Last Modified: Tue, 12 Mar 2024 06:38:12 GMT  
		Size: 58.8 MB (58820494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1d12b0094d5949d746a8486d502643770e2f36c342a6379da63ff14a0ec4b1cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231965018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2171b8f31314d73ea892efa419fdd66bd280b3295d2f9e2ee68a07a2a5aa20b8`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:45:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 01:50:05 GMT
COPY dir:774c748cac67d918432726696917d770e1c557a90a62f56899a68f5b5861f304 in /opt/java/openjdk 
# Tue, 12 Mar 2024 01:50:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 01:50:08 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 01:50:08 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 01:50:08 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 01:50:13 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 01:50:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 01:50:13 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 01:50:31 GMT
RUN boot
# Tue, 12 Mar 2024 01:50:31 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb450795f7ec7c9a3f449d4b89a1813bc06e338a4ccecb2a734b6e798364b28a`  
		Last Modified: Tue, 12 Mar 2024 02:06:35 GMT  
		Size: 142.0 MB (142008478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb498ff3e7f054097bf8efaa59b55a2af4ce44011a3966cf1f39d886c06d0474`  
		Last Modified: Tue, 12 Mar 2024 02:06:25 GMT  
		Size: 1.1 MB (1064958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d867fa9417d560678297c363c1216bda3b605aa61370657ac87f5267ddd7ca66`  
		Last Modified: Tue, 12 Mar 2024 02:06:28 GMT  
		Size: 58.8 MB (58820466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
