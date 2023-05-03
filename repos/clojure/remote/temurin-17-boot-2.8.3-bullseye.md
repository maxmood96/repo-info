## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:3c24b28ad50167deec7ce77171e5096d0ca5a7076cbd8e31b596fcb73d57c15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6de03649fcca0c35c55205e7efe7df28b6e16b44a22537560aa6159e1b60afc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308812052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c5e323ebc385cec24cbfe6ec209ab50383d227b32e3d1629d93ecf9ff110bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 02 May 2023 23:46:50 GMT
ADD file:fc290cf8ddb984325474583faa79c5a98c5ea0ec7f606bf360251f63acecf389 in / 
# Tue, 02 May 2023 23:46:51 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 20:29:34 GMT
COPY dir:097a611561277927a8e367a60640ce12877b7a6373689dec24d5cfb76f99c807 in /opt/java/openjdk 
# Wed, 03 May 2023 20:29:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:29:35 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 03 May 2023 20:29:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 03 May 2023 20:29:36 GMT
WORKDIR /tmp
# Wed, 03 May 2023 20:29:41 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 03 May 2023 20:29:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 03 May 2023 20:29:42 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 03 May 2023 20:29:59 GMT
RUN boot
# Wed, 03 May 2023 20:30:00 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 03 May 2023 20:30:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 03 May 2023 20:30:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:918547b9432687b1e1d238e82dc1e0ea0b736aafbf3c402eea98c6db81a9cb65`  
		Last Modified: Tue, 02 May 2023 23:49:58 GMT  
		Size: 55.0 MB (55049070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4691a7487ede1e6dd3accb93b84f63e7ba0a18afb5a6dde1cb2605bdef6cce`  
		Last Modified: Wed, 03 May 2023 20:38:14 GMT  
		Size: 192.6 MB (192580399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428dc42a680a1e1f8c3e719c59d3d86272ce3afdc2ea44b2fdb6d6685d62e922`  
		Last Modified: Wed, 03 May 2023 20:38:01 GMT  
		Size: 2.4 MB (2361718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780bc7725ec1f70c6b58089979d8a67693a26466fba7a2f0aa31ba65294b55c9`  
		Last Modified: Wed, 03 May 2023 20:38:04 GMT  
		Size: 58.8 MB (58820468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34bff871ca29bf662ff7bf15656ded977a1a63d0cd35621165a8d1dd55269f00`  
		Last Modified: Wed, 03 May 2023 20:38:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:961829c966f3772d8998541564a16cfa205e2020af55e543060d7bc51bc16e31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.3 MB (306252448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3806c51cc54c9cc1c752882b06119b0baf146aa827a982bd6c5d21e0ccc50476`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:43:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 17:48:34 GMT
COPY dir:d3d9f08d06fd1214b20f5d901cee398f498773bedf69f0d3cc795772967cfe44 in /opt/java/openjdk 
# Wed, 03 May 2023 17:48:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:48:38 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 03 May 2023 17:48:38 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 03 May 2023 17:48:38 GMT
WORKDIR /tmp
# Wed, 03 May 2023 17:48:43 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 03 May 2023 17:48:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 03 May 2023 17:48:43 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 03 May 2023 17:49:00 GMT
RUN boot
# Wed, 03 May 2023 17:49:01 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 03 May 2023 17:49:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 03 May 2023 17:49:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54e3dfe953384be82597fea580dc9ef9ebb8b53e65fc436e07311295d7e9202`  
		Last Modified: Wed, 03 May 2023 17:56:22 GMT  
		Size: 191.4 MB (191387699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd4b1a528a6756262ae18bfebc7321d523a29039035a4fec5b98ee7e7cac436`  
		Last Modified: Wed, 03 May 2023 17:56:11 GMT  
		Size: 2.4 MB (2351082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaedb0f1cc218bde23edc38fa6de75c51f70bb89d07c5ff1e5052f5a6670725c`  
		Last Modified: Wed, 03 May 2023 17:56:14 GMT  
		Size: 58.8 MB (58820564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332d9619a6ec17c14d3cb3801d792cf4b1820ddb3bd4b19af06c36f9a52c6646`  
		Last Modified: Wed, 03 May 2023 17:56:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
