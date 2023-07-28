## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:39ae786e0d0355503361e2f4aecba6dad57a9917432e316a2798233466cb382a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6f6c7494d397c017e2cc08fd91eb913313f90af84bcef2c8eab3a10fdea485c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236089806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92176b5342c2cda6adf3168421f634f3b68f843d2fe07c2029fb651692842bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 02:22:08 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 03:20:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 03:20:17 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 28 Jul 2023 03:20:17 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 28 Jul 2023 03:20:17 GMT
WORKDIR /tmp
# Fri, 28 Jul 2023 03:20:22 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 28 Jul 2023 03:20:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 28 Jul 2023 03:20:23 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 28 Jul 2023 03:20:40 GMT
RUN boot
# Fri, 28 Jul 2023 03:20:40 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 28 Jul 2023 03:20:41 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 28 Jul 2023 03:20:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b29ed6597331035398011b2e89cfefc617fdebf9bddaf2ac7d5c40d25859a6f`  
		Last Modified: Fri, 28 Jul 2023 02:24:18 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c1c70a7ac8bc54ff659f2ceaf683594cacd02becd9af99e4ea650af52d7806`  
		Last Modified: Fri, 28 Jul 2023 03:31:30 GMT  
		Size: 1.1 MB (1077550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9cb564a6b38c79d51f3007b9affeeeb6bbf036c89c7c8e7eb3381236bd8991`  
		Last Modified: Fri, 28 Jul 2023 03:31:34 GMT  
		Size: 58.8 MB (58820505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f01fb20c53284e4a349aa80ca8985aef5b88e5ee19c77aeef95b6ef16561d7`  
		Last Modified: Fri, 28 Jul 2023 03:31:30 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fa8ea5dcc771d0960e0f51902177fca400c777d985a251ea52c07ecb0a2e9eb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233486698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69563954d885bf6feee30e2330b253784ac91e05d37aae1f1681795fab0bbcc0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:25:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 14:25:26 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 14:35:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 14:35:35 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 28 Jul 2023 14:35:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 28 Jul 2023 14:35:35 GMT
WORKDIR /tmp
# Fri, 28 Jul 2023 14:35:40 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 28 Jul 2023 14:35:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 28 Jul 2023 14:35:40 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 28 Jul 2023 14:35:59 GMT
RUN boot
# Fri, 28 Jul 2023 14:35:59 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 28 Jul 2023 14:35:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 28 Jul 2023 14:35:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc8dfc50ad1a93c8652ce31df19291350dca86cc2b7462fbd67c78d39e53aca`  
		Last Modified: Fri, 28 Jul 2023 14:27:39 GMT  
		Size: 143.5 MB (143538104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c46ce4b0b545db2a2d1e4fbab8d22ca721f1b69515cc5ef57b30101e6e0254`  
		Last Modified: Fri, 28 Jul 2023 14:43:20 GMT  
		Size: 1.1 MB (1064842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d97c695a299359994c84af5e6e5bbcdcec584db37fb703b30e6a4acd1c0cbf5`  
		Last Modified: Fri, 28 Jul 2023 14:43:23 GMT  
		Size: 58.8 MB (58820521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f5cda9bee94254c7133f24b91598a7e694f182808e58f32adeb4d343518d34`  
		Last Modified: Fri, 28 Jul 2023 14:43:20 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
