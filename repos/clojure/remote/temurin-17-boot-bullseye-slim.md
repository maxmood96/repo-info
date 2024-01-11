## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:677000cb80a6aa07bc406d22efa5a0826c249d30ce4c436dd932ab305c139494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:42b7ed0a3261327fd9e55c89cd3d1ced47b915885b3f8640843e76a6f1ffba4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236192238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32ab78859cfa7306d4ce5d4ec65a26ded114897cf199694d3a2ada0625ed237`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 05:05:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:05:27 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 05:05:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 05:05:27 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 05:05:32 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 05:05:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 05:05:33 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 05:05:52 GMT
RUN boot
# Thu, 11 Jan 2024 05:05:53 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 11 Jan 2024 05:05:53 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jan 2024 05:05:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50dfbeec8990bbac2cb741dc563a8091b2267af161a2851bf3ed2578c72f4b4e`  
		Last Modified: Thu, 11 Jan 2024 05:22:01 GMT  
		Size: 1.1 MB (1079449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a857476d9d82c817e77b59473b5475f755bb1fbd202e854b902d99375ea82a`  
		Last Modified: Thu, 11 Jan 2024 05:22:05 GMT  
		Size: 58.8 MB (58820531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1b2031d15444a208a509813af3bff715444f6e5eccb90cadb2ecb6e2166fc7`  
		Last Modified: Thu, 11 Jan 2024 05:22:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

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
