## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:2975e6c29fdf2fdbffe2f920f2e936d1dbac97bc349006b6eff98e8072053876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2ab3c2b6859f61e248a2ede86a7a5fce26b2f89ca6c81e9dad27d96ee2407667
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236192145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bcf31a4d5f852a91a3c6ba6ee6d3526db2efa3ee5a90afe3b7dc47ded81376c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:05:49 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:05:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:05:50 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 07:05:51 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 07:05:51 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:05:56 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 07:05:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 07:05:56 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 07:06:14 GMT
RUN boot
# Tue, 19 Dec 2023 07:06:14 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:06:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:06:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33083c2fa706ccf957a319c78e4544da4545d5fcc8d30f718d5eb0a8027dc84`  
		Last Modified: Tue, 19 Dec 2023 07:22:39 GMT  
		Size: 144.9 MB (144873991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02819a22bd08f9650a6e6b32cc022618f4553fea6a0e049f0594294a07cc749`  
		Last Modified: Tue, 19 Dec 2023 07:22:27 GMT  
		Size: 1.1 MB (1079490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77312a5070688aa91ca1f337b0e7dd0a0c45255e2826a3cddb9ee717bdf8e59`  
		Last Modified: Tue, 19 Dec 2023 07:22:30 GMT  
		Size: 58.8 MB (58820392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827d22624b2cd1a72e3bdf55bc56b89352e341e452ebd89855506af350da2759`  
		Last Modified: Tue, 19 Dec 2023 07:22:27 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:986bbf62de2e100ccb27b67344b18678a11acfcafb2681fe29fc2c5c42067e81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233633358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a0e020e8f25b29063a233dbe9730122eec6343db4396bf5a1796200b723c91`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:00:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 03:00:20 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:05:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:05:03 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 07:05:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 07:05:03 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:05:08 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 07:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 07:05:08 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 07:05:25 GMT
RUN boot
# Tue, 19 Dec 2023 07:05:25 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:05:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:05:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80ad0f784bba75d76206ff4e1034310f072851273c25fd54ef00422a8861cef`  
		Last Modified: Tue, 19 Dec 2023 03:03:38 GMT  
		Size: 143.7 MB (143681709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d05d52dfaf84bb91186b6faf838cd659cf404ca78d5c0cb497679c62fd4e78`  
		Last Modified: Tue, 19 Dec 2023 07:19:33 GMT  
		Size: 1.1 MB (1066820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd36bfb87b0cc093aad948085c468d8fb79aa5a16d5a89382f8c26a25bfcaed`  
		Last Modified: Tue, 19 Dec 2023 07:19:35 GMT  
		Size: 58.8 MB (58820377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb472ef7d071b954603b6fbd62684f6a296086ebdb25162e130923bd80920dcc`  
		Last Modified: Tue, 19 Dec 2023 07:19:32 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
