## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:1e55c531ea217e465c934283b832543250f8637f2436ea40568762215f8fdb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:20566a0be5d359b284468a4f000bbea92e0fa3b7d85071d05f5b1fd33a8677de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314703715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b327c0077d26e8f4fc8722424bd3b79ee57cc1938e46bc8aab3705ba23b3ce`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:16:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 Mar 2023 06:19:58 GMT
COPY dir:e649a995635d4b28f1458e8ccc09f5f71440b52479cfda5ea11e99ab14d0ce82 in /opt/java/openjdk 
# Thu, 23 Mar 2023 06:20:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Mar 2023 06:20:00 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 23 Mar 2023 06:20:00 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 23 Mar 2023 06:20:00 GMT
WORKDIR /tmp
# Thu, 23 Mar 2023 06:20:06 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 23 Mar 2023 06:20:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 23 Mar 2023 06:20:06 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 23 Mar 2023 06:20:23 GMT
RUN boot
# Thu, 23 Mar 2023 06:20:23 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab656fe58b67db3e6051a8b99a09ffa77a9d8123326d18547c28803ea6e0439`  
		Last Modified: Thu, 23 Mar 2023 06:30:46 GMT  
		Size: 198.5 MB (198476073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9134c860de795517c920387f54f89973cd2cbff11b205254d1db12eac1784b4`  
		Last Modified: Thu, 23 Mar 2023 06:30:33 GMT  
		Size: 2.4 MB (2361568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea413de62dc105ccbfd7f7a8e07773f57769ccefc747f463b869d1e17be75c6`  
		Last Modified: Thu, 23 Mar 2023 06:30:35 GMT  
		Size: 58.8 MB (58820466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:58692a3b56a89dcd88ebc25ebbb69e4afe4129d454cc3f38a982287afe402140
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310119637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61fb9dae5bbde82a98288cc9a64a796e6c661dc7c08dcafa3fa0fc2a9af17c1`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:42 GMT
ADD file:dd3d4e5fe819950e7d01b44a29dbd790438cd722ba76198910e2597448ab0c6f in / 
# Wed, 12 Apr 2023 00:39:43 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:20:38 GMT
COPY dir:d446509417048b798354227404c222c2c6031477a91cb1b64eded33f5e598adf in /opt/java/openjdk 
# Wed, 12 Apr 2023 01:20:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 01:20:43 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 12 Apr 2023 01:20:43 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 12 Apr 2023 01:20:43 GMT
WORKDIR /tmp
# Wed, 12 Apr 2023 01:20:47 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 12 Apr 2023 01:20:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 12 Apr 2023 01:20:48 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 12 Apr 2023 01:21:05 GMT
RUN boot
# Wed, 12 Apr 2023 01:21:05 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:dc80b8cdbfd36cb20231d807a50d704945d1df4da8f6e23197ccfcb629970491`  
		Last Modified: Wed, 12 Apr 2023 00:42:14 GMT  
		Size: 53.7 MB (53705529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e34d229c4186d9e7e7ce0aee26abda131ebcee8bee99be5af11bfc1bf391db`  
		Last Modified: Wed, 12 Apr 2023 01:29:24 GMT  
		Size: 195.2 MB (195242537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ee64c8bc6746b8da9e35d0eaac1f05cc6f88126dfde0cd2200960514ff0f54`  
		Last Modified: Wed, 12 Apr 2023 01:29:13 GMT  
		Size: 2.4 MB (2351079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a0924add50f5bf4fac17b84dbc91d24a420b88f61a6154442afbd591f23ff7`  
		Last Modified: Wed, 12 Apr 2023 01:29:15 GMT  
		Size: 58.8 MB (58820492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
