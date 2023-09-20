## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:d8e3004313bfd1d168cac174e28b5fe5fb5afeff89e35f398728eaeefb239a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d1f303e2160e707d55c6fd1ba823f119ce09c54b4870e7559ec225f103f8159b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261065358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eecffec0ce5812305f759d2dfebb565a889c702ea81b7f50b4bfabf8bf798748`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:51 GMT
ADD file:85db4f4c5016f51f7112a5d09cb7d4620f565a1379ae4b8a03c5ffc23886a876 in / 
# Wed, 20 Sep 2023 04:55:51 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:21:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 07:24:52 GMT
COPY dir:3e9b1d3d54369337872a2b8aa8c30068d69b28c2def3ec3bf07ba34bd69d48a0 in /opt/java/openjdk 
# Wed, 20 Sep 2023 07:24:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:24:53 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 20 Sep 2023 07:24:54 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 20 Sep 2023 07:24:54 GMT
WORKDIR /tmp
# Wed, 20 Sep 2023 07:24:59 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 20 Sep 2023 07:25:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 Sep 2023 07:25:00 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 20 Sep 2023 07:25:20 GMT
RUN boot
# Wed, 20 Sep 2023 07:25:20 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:ddf874abf16cc990e0fd75a154a34ca0a03ee310ad895a18fb62ae15bf4171fb`  
		Last Modified: Wed, 20 Sep 2023 05:00:41 GMT  
		Size: 55.1 MB (55056714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d2593b379fff1802970ddf266f34d6bd5d13fda962a549ac1b0e11020096b1`  
		Last Modified: Wed, 20 Sep 2023 07:35:34 GMT  
		Size: 144.8 MB (144826046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bc3c67b3eba7c868eecee43a21f6efd25eb2b00f4c47ea902a459a050be28e`  
		Last Modified: Wed, 20 Sep 2023 07:35:23 GMT  
		Size: 2.4 MB (2362085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a21e8dadd7bb670003a0e2be43047dfdc2d13ac0cd3d815edd9b289c41a7a7`  
		Last Modified: Wed, 20 Sep 2023 07:35:27 GMT  
		Size: 58.8 MB (58820513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fbdd6cd9b433fedfd80f5f8fb655266b20c5202e5281b82c36442cf567293110
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256447096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb5f26c92396ee1dc9ff412fa219f22fa69a92c70ff28ac2ce65faf2ed70b1e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:45 GMT
ADD file:6bc001e951ef1280f566a92e65fcff57aefb8a280aa3510b7cd4b4e0a54c5cff in / 
# Thu, 07 Sep 2023 00:39:46 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:03:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 09:06:37 GMT
COPY dir:68819d2d348aedadecb99120d7ca4a63dcc1e3aa0bb526ecbd9925396c38234c in /opt/java/openjdk 
# Thu, 07 Sep 2023 09:06:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:06:41 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 07 Sep 2023 09:06:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 09:06:41 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 09:06:46 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 07 Sep 2023 09:06:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 09:06:46 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 07 Sep 2023 09:07:05 GMT
RUN boot
# Thu, 07 Sep 2023 09:07:05 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:61c16b7975697b00760ff9536c09eed29b6a76923d4d98be38e9cdc749506417`  
		Last Modified: Thu, 07 Sep 2023 00:43:21 GMT  
		Size: 53.7 MB (53704716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0526516c15ab59c896bde61f8cbcc3d733f5b792e340106528fab44ad40477`  
		Last Modified: Thu, 07 Sep 2023 09:16:03 GMT  
		Size: 141.6 MB (141570385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89be6054ec9a349911a290811063e164bffcfbf4dd2ccf846a4a710b060e1a2`  
		Last Modified: Thu, 07 Sep 2023 09:15:54 GMT  
		Size: 2.4 MB (2351423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6afd7f87c288246a0c560e2dec0586c394cc4f421020f39bb4883c0dc8399c2`  
		Last Modified: Thu, 07 Sep 2023 09:15:57 GMT  
		Size: 58.8 MB (58820572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
