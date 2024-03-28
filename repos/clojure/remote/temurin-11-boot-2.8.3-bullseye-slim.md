## `clojure:temurin-11-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:ae9c5b2c5a7e082462ec340f406118145037583fd08a45486c8107e8fe37ddf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1ca7fe1dc83cf80545bfe9c0d64dbc32f4fdae2ecc7ecdfbe683602dcd0a9f47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236591933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a24768b21e23a2d84ff4967d4b19f50f25520518682eadb43672e541081c538`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:59:44 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:59:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:59:46 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 02:59:46 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:59:46 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:59:51 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 02:59:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:59:52 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 03:00:10 GMT
RUN boot
# Thu, 28 Mar 2024 03:00:10 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765e80b34419cc4d75a074af22d808e72a16040aef302be6b97f83f87c3cea68`  
		Last Modified: Thu, 28 Mar 2024 03:20:12 GMT  
		Size: 145.3 MB (145271223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fd5998556eee427dc0ce457543ff6eca088bc940cfc3c75591c9e7d93821d4`  
		Last Modified: Thu, 28 Mar 2024 03:20:00 GMT  
		Size: 1.1 MB (1077705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1a40ecb5418168b5c7cc3cf7edeeae7decfe7bc12d3ac7c9a66c9f34b7795c`  
		Last Modified: Thu, 28 Mar 2024 03:20:04 GMT  
		Size: 58.8 MB (58820516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2aced85049e99a3322de3fe8fd77d658149559f4a710c92e72d274efeeed5a49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231962906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a717334d5a2061b7a6ffbb119c0308d6f6f83b96524a341fc54a4556b9cc124`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:45:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:33:52 GMT
COPY dir:d5fb8d9a38dea7496f2aff176bc9a34bbca80551c2dc57109d2dae5907a339ee in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:33:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:33:56 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 02:33:56 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:33:56 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:34:01 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 02:34:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:34:01 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 02:34:17 GMT
RUN boot
# Thu, 28 Mar 2024 02:34:18 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff8a31a2022acad9a6b7593ce2e2b45a1ce4aeb662d6311f16bc5d6ea9a4339`  
		Last Modified: Thu, 28 Mar 2024 02:50:17 GMT  
		Size: 142.0 MB (142006322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba68aed36e969d8c25702822f2c3a51392d330c1d3895fcef1351239cf9c29b`  
		Last Modified: Thu, 28 Mar 2024 02:50:09 GMT  
		Size: 1.1 MB (1065030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba651653c0fb10b8b2c113b7f6f748bdcab8b663a51abbd869811b2c11e577bf`  
		Last Modified: Thu, 28 Mar 2024 02:50:11 GMT  
		Size: 58.8 MB (58820438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
