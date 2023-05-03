## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:f8ba56c9eb1c4f6d818a57b476d734e6448159f910463dabf48a9508d1f3d3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cf2613f6199a9c6d7b8d26d5ad062d695990a92707fc31d440eb6707c7beeeb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283897032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a91118f7ba56e0b7c091c116bd3d1aee023dac6d36fe82550e23e3a73a86c21`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Apr 2023 20:09:11 GMT
COPY dir:097a611561277927a8e367a60640ce12877b7a6373689dec24d5cfb76f99c807 in /opt/java/openjdk 
# Wed, 26 Apr 2023 20:09:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 20:09:12 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Apr 2023 20:09:12 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Apr 2023 20:09:12 GMT
WORKDIR /tmp
# Wed, 26 Apr 2023 20:09:18 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Apr 2023 20:09:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Apr 2023 20:09:18 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Apr 2023 20:09:35 GMT
RUN boot
# Wed, 26 Apr 2023 20:09:35 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 26 Apr 2023 20:09:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Apr 2023 20:09:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3dca630898b65b3e3d97ffce265d16549a24facef0348fd8a6d8d5aee0493b3`  
		Last Modified: Wed, 26 Apr 2023 20:24:23 GMT  
		Size: 192.6 MB (192580428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8dc93ac75a348ee7b4ec2fcec25ac191d749da2df80e06bcc4b3c06bdacd58`  
		Last Modified: Wed, 26 Apr 2023 20:24:09 GMT  
		Size: 1.1 MB (1077506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4a7af206e939d030d987e720113a9f4f88ec2b19f2f34a207691e1c67208f4`  
		Last Modified: Wed, 26 Apr 2023 20:24:13 GMT  
		Size: 58.8 MB (58820470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6112ceb4a38c0a1ac3a31a84d5605072db5f292d75882b658f54d2ee444df74e`  
		Last Modified: Wed, 26 Apr 2023 20:24:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f9634f9ca86d5b9bd19c892dd991878d07b5540dfeed99e9709feb0b4bbfff81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281326170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55a2a7862042c08d5a4b3fcad1f344f5b64fafbc3652ef989c5c41996590cd6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 17:49:05 GMT
COPY dir:d3d9f08d06fd1214b20f5d901cee398f498773bedf69f0d3cc795772967cfe44 in /opt/java/openjdk 
# Wed, 03 May 2023 17:49:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:49:10 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 03 May 2023 17:49:10 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 03 May 2023 17:49:10 GMT
WORKDIR /tmp
# Wed, 03 May 2023 17:49:14 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 03 May 2023 17:49:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 03 May 2023 17:49:15 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 03 May 2023 17:49:32 GMT
RUN boot
# Wed, 03 May 2023 17:49:32 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 03 May 2023 17:49:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 03 May 2023 17:49:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6baebd3611c04da99c6391c894e4c5ba7eaa103bf201a26eba6d26bbdd244f42`  
		Last Modified: Wed, 03 May 2023 17:56:41 GMT  
		Size: 191.4 MB (191387733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0fc846c08b7318ea63b766820855ed70be5ce95dba9c685160c156359d7f627`  
		Last Modified: Wed, 03 May 2023 17:56:31 GMT  
		Size: 1.1 MB (1064804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316f11328c8bf81cb038d73c86d5c032342697e1670a0660aec36ddde5aa5795`  
		Last Modified: Wed, 03 May 2023 17:56:33 GMT  
		Size: 58.8 MB (58820503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b047eb4a1923d574a295d5e702b2ca2a59525b080f6200e43e7b78aef0ef3188`  
		Last Modified: Wed, 03 May 2023 17:56:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
