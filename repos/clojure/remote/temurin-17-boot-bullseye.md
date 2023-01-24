## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:6fce7e8c79ff45b3836b1efa9b593e8090be77bcb15f02fe9ff8d6c57370802c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5a644a3eaafa783a5fad538e5196770ffb768d12e3124ec8cb37e843c8381b18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308638032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c411b45a8ff0d4c590212fc8decd290ea9c4d2d6fbc2381cdd240ec30b9f5c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:29 GMT
ADD file:917750a82b29f8f7f88a121017bd9dfeb0fbcc8f0697a009f08b6b58246eff4b in / 
# Wed, 11 Jan 2023 02:34:30 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:18:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:25:39 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 11 Jan 2023 03:25:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 03:25:40 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 11 Jan 2023 03:25:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 11 Jan 2023 03:25:41 GMT
WORKDIR /tmp
# Wed, 11 Jan 2023 03:25:47 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 11 Jan 2023 03:25:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 11 Jan 2023 03:25:47 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 11 Jan 2023 03:26:06 GMT
RUN boot
# Wed, 11 Jan 2023 03:26:06 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 11 Jan 2023 03:26:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 11 Jan 2023 03:26:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bbeef03cda1f5d6c9e20c310c1c91382a6b0a1a2501c3436b28152f13896f082`  
		Last Modified: Wed, 11 Jan 2023 02:38:42 GMT  
		Size: 55.0 MB (55025206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2359afb593c01bca1799fd29c2d98e1da243e75a77e88c13d9c01c99d2d6472b`  
		Last Modified: Wed, 11 Jan 2023 03:38:12 GMT  
		Size: 192.4 MB (192431213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c8c4e7fb3237fb2b61f0dbf4078ab816bdec49e18f50f5c5b849bb0d0d9a05`  
		Last Modified: Wed, 11 Jan 2023 03:37:58 GMT  
		Size: 2.4 MB (2360651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c1c5c65beacbbff5f4b8ec727aa5dbbc1cf065073d5a8857f1330cdf9f67a1`  
		Last Modified: Wed, 11 Jan 2023 03:38:01 GMT  
		Size: 58.8 MB (58820563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31da7bf719fbe5315141ddfa2513362e8292bbb766e2a7307a10ee5f8350627b`  
		Last Modified: Wed, 11 Jan 2023 03:37:58 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2394b951ce1e8cb0c1f2cd23d3151f30e647a6449a3a695101dfab7f97e4879c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306113825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1f83c4231bdabdfe5619f52cfb768fe99debef7dba610118c5625a4cd4ed9f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:24 GMT
ADD file:9e185c2d9ca8a231a39ee2b1761fcdff75065252d25a65a207acb7a319c1cf23 in / 
# Wed, 11 Jan 2023 02:57:25 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 21:03:31 GMT
COPY dir:6138ae24df63cd8b909473221414960a006ae73d2e2f1e88f48051984c7a0e00 in /opt/java/openjdk 
# Tue, 24 Jan 2023 21:03:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:03:35 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 24 Jan 2023 21:03:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 24 Jan 2023 21:03:35 GMT
WORKDIR /tmp
# Tue, 24 Jan 2023 21:03:40 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 24 Jan 2023 21:03:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Jan 2023 21:03:41 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 24 Jan 2023 21:03:57 GMT
RUN boot
# Tue, 24 Jan 2023 21:03:58 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 24 Jan 2023 21:03:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Jan 2023 21:03:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c345c9e441f5f49235768af74b8ab37743652d38958afaa000edd56d7b2f0540`  
		Last Modified: Wed, 11 Jan 2023 03:00:56 GMT  
		Size: 53.7 MB (53681859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09dcb437b869e84fa1314bf4f1e61a77274341567bbec0caf4e4ea2237b3e69`  
		Last Modified: Tue, 24 Jan 2023 21:13:41 GMT  
		Size: 191.3 MB (191260425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a77992de3bd5a62d0fe5739b9fc2c910d5f028559a45e065ccfa2906ac34d7`  
		Last Modified: Tue, 24 Jan 2023 21:13:29 GMT  
		Size: 2.4 MB (2350678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd490233f402335d5134b25d48278f3431b40de0ce0dd4a8f092d7ce0849fe1`  
		Last Modified: Tue, 24 Jan 2023 21:13:32 GMT  
		Size: 58.8 MB (58820463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f0ad5479c9b83ab1610f276ad904a058417aa07ae7d9e63463849b659bb09b`  
		Last Modified: Tue, 24 Jan 2023 21:13:29 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
