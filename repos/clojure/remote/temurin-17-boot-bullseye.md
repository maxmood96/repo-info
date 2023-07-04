## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:dc1bf6cde27aa0f0240e7491648be4b2afa1a68ae97317b7f9e837c5a60ab846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7d83fbbdd3eb52d58a26edbd5e5bc4b9f52ef5904193d6dd04bbfbc4a14dfa02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308818555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f509d593bfffadbec94a2ee801b67871761b3a08d34cbdee31e0b40953dbd3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:59:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 04:05:49 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Tue, 04 Jul 2023 04:05:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 04:05:51 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 04 Jul 2023 04:05:51 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 04 Jul 2023 04:05:51 GMT
WORKDIR /tmp
# Tue, 04 Jul 2023 04:05:56 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 04 Jul 2023 04:05:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Jul 2023 04:05:57 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 04 Jul 2023 04:06:14 GMT
RUN boot
# Tue, 04 Jul 2023 04:06:14 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 04 Jul 2023 04:06:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Jul 2023 04:06:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d5749ce62c0fb43ce9ee4298e4f571f0584facdde1f4b6b77b68dcf21129c2`  
		Last Modified: Tue, 04 Jul 2023 04:15:06 GMT  
		Size: 192.6 MB (192580329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867a42286c8fd64788bcca9ecdbc386ad3706ec5ab9af2f0b17a4c49597bce42`  
		Last Modified: Tue, 04 Jul 2023 04:14:54 GMT  
		Size: 2.4 MB (2361998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f131ac5030f2260ecf46ebac6600983427ef72bf57ed714fb3e3e3f068a602`  
		Last Modified: Tue, 04 Jul 2023 04:14:56 GMT  
		Size: 58.8 MB (58820530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86200f2de86cafe4a518ec081a6f7b8d8286bbba1570314c826c5a43e6d629f3`  
		Last Modified: Tue, 04 Jul 2023 04:14:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a11e441ebbe97be2c42f8bea1817dbed6bc657a28df2e8901aa0b15c544c489c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.3 MB (306263811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9670c7f39aec2a4fa578c08742274cf41df9dc50b9e76ab963d8d4eae102e8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:43:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:48:38 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:48:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:48:42 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 04 Jul 2023 06:48:42 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 04 Jul 2023 06:48:42 GMT
WORKDIR /tmp
# Tue, 04 Jul 2023 06:48:48 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 04 Jul 2023 06:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Jul 2023 06:48:48 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 04 Jul 2023 06:49:04 GMT
RUN boot
# Tue, 04 Jul 2023 06:49:04 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 04 Jul 2023 06:49:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Jul 2023 06:49:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810f3cbd7d4c2c14a5785455f4c5304087407ef091338c76582566ea8b195d1d`  
		Last Modified: Tue, 04 Jul 2023 06:56:43 GMT  
		Size: 191.4 MB (191387711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630768a0a4621b3d7adf4929b94af66acfd802c033f8ebfc53c523510bd5674b`  
		Last Modified: Tue, 04 Jul 2023 06:56:32 GMT  
		Size: 2.4 MB (2351401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9badc3695de44b25819cde1655e82a934982e6ea5260b8bcfa17720df7e86791`  
		Last Modified: Tue, 04 Jul 2023 06:56:34 GMT  
		Size: 58.8 MB (58820324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2fc0a2dd3f002e87bd1e3ab5717a41c4f6a271452f6f9ec186ec988149b0e5`  
		Last Modified: Tue, 04 Jul 2023 06:56:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
