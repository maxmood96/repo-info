## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:9911b88823a628fa4ff9e023c027195afc5b6fa8473325ed03c66667eeee2b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8bf5efa3ef235b1a8533833514016dea5b2f0739876de424100ab1cbcf6efaca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (261013492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8e7154cad51db6565690e80242214608a0eb009abed1613a0a19adaaf8b639`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:57 GMT
ADD file:20f89ff93bfbd6c9fb1a97058a1f3de4485a8974e8a83892072c511fbd2e4134 in / 
# Wed, 16 Aug 2023 00:59:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 18:08:24 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Wed, 16 Aug 2023 18:08:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 18:08:25 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 16 Aug 2023 18:08:25 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 16 Aug 2023 18:08:26 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 18:08:31 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 16 Aug 2023 18:08:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 16 Aug 2023 18:08:31 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 16 Aug 2023 18:08:50 GMT
RUN boot
# Wed, 16 Aug 2023 18:08:50 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 16 Aug 2023 18:08:50 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 16 Aug 2023 18:08:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a70103cc499a199e10e379794c60aa524d9598587cc2bdfe2995642c2da8df7`  
		Last Modified: Wed, 16 Aug 2023 01:04:50 GMT  
		Size: 55.1 MB (55056621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fbbfc9003ff6a7a7db701f4c4c225eecdff24e8d91f37e9d447417a6e458b2`  
		Last Modified: Wed, 16 Aug 2023 18:17:54 GMT  
		Size: 144.8 MB (144773721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c83c58593293395bf83b16b13284ce9bab4d114f1d4c4893fd2239efdef0d5`  
		Last Modified: Wed, 16 Aug 2023 18:17:43 GMT  
		Size: 2.4 MB (2362212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8b6567434c6e8a05349d2251741c0344c5db80767c471208372a741a3fb19a`  
		Last Modified: Wed, 16 Aug 2023 18:17:46 GMT  
		Size: 58.8 MB (58820539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e10ef1ec0c18cf589572bb6d2f8e6adb0f830004ceda58a32468a6649080960`  
		Last Modified: Wed, 16 Aug 2023 18:17:42 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0bfe62c6c52706867c6a0e46fc98c682736e409634b60f27f2937be2c6f7de15
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258415268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a048a7b183f0aaf952d98c76ac24b6d706f8d7ce3e947e8eb3286d8e97a8a1db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:20 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Wed, 16 Aug 2023 17:25:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 17:25:24 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 16 Aug 2023 17:25:24 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 16 Aug 2023 17:25:24 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 17:25:29 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 16 Aug 2023 17:25:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 16 Aug 2023 17:25:29 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 16 Aug 2023 17:25:46 GMT
RUN boot
# Wed, 16 Aug 2023 17:25:46 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 16 Aug 2023 17:25:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 16 Aug 2023 17:25:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407f1b0394be128a63af2359d89c3282164b67cd2fac29716c6f2f5e348ec07a`  
		Last Modified: Wed, 16 Aug 2023 17:34:01 GMT  
		Size: 143.5 MB (143538089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34182b71af18636282320505be3e3a3c8c1c354c995613212e4c8ed93f2b5c28`  
		Last Modified: Wed, 16 Aug 2023 17:33:51 GMT  
		Size: 2.4 MB (2351416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5548432b5120e8d40e85d209d5cd022dfa3af54d333b41e6470a87c8558b1c1`  
		Last Modified: Wed, 16 Aug 2023 17:33:54 GMT  
		Size: 58.8 MB (58820583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab80fe62f299714184c58674ec1c97dd892bef68413b7792bb93fcac6b3460c0`  
		Last Modified: Wed, 16 Aug 2023 17:33:51 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
