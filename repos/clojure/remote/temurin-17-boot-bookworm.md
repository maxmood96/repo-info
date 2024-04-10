## `clojure:temurin-17-boot-bookworm`

```console
$ docker pull clojure@sha256:d6d50fbab82c881ce46a9c29b5c8f98177d803b97eb95e98b4289e00e17e3ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7c644d7721eb25e77683f1b14aa290767f137223b9469a2e72f750b74522d8b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258793420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2247cd328b5831a339b5f3e3c3f5d4b3d72a10632588950cd5274eb37d87ae8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:10:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 03:06:12 GMT
COPY dir:88c5118aff6896f6ed535dcde576d68ef88ded459cca013e0f9beb3e430ebb52 in /opt/java/openjdk 
# Thu, 28 Mar 2024 03:06:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 03:06:13 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 03:06:13 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 03:06:13 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:06:20 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 03:06:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 03:06:20 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 03:06:37 GMT
RUN boot
# Thu, 28 Mar 2024 03:06:37 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 03:06:37 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 03:06:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd1d09ff668169a35ad1340a1e6c8ef47bc12ff42bb04e3501d7f507ad781a6`  
		Last Modified: Thu, 28 Mar 2024 03:24:17 GMT  
		Size: 144.9 MB (144893081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1619b5072313d2ea977227bf813f52c9cd057235def0bea81e05309afcc1045b`  
		Last Modified: Thu, 28 Mar 2024 03:24:07 GMT  
		Size: 5.5 MB (5527200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd2f05fbe986b148682a23d9df853619b0d673597e62d50b325bdb921e1b4ad`  
		Last Modified: Thu, 28 Mar 2024 03:24:09 GMT  
		Size: 58.8 MB (58820543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e2bfc1f8d32369c178df9b0750143042756b5ac3551ad58a4e9eae27e4a4d5`  
		Last Modified: Thu, 28 Mar 2024 03:24:06 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0d85e6ed00d8337c0e68f8ebc7b9b544660f4287535591d8391657fa68c3ae81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257487556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50468be07a0067a4b38bfb970483ec6d4e671d2ca4f42335ee8f1cc5ac193f69`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:37:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:48:10 GMT
COPY dir:a5d0039514ccd79689a0ea6094d70ca92113e8cbcc38d473b7c0fcc04a1f496a in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:48:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:48:14 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 04:48:14 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 04:48:14 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:48:19 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 04:48:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 04:48:20 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 04:48:37 GMT
RUN boot
# Wed, 10 Apr 2024 04:48:37 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 04:48:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 04:48:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9944fa1d82dffccbdecd6f3662116d2cade312ebe17866b01cd24bf860a8bcc`  
		Last Modified: Wed, 10 Apr 2024 05:04:25 GMT  
		Size: 143.7 MB (143720939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bb223a24324a000d626427b070d27a3fd9e3d9db7a59c00ff75fa8c30a4bde`  
		Last Modified: Wed, 10 Apr 2024 05:04:16 GMT  
		Size: 5.3 MB (5349417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a6c26d6a97949e65e7d304956ce6c0512be7b3f9159f1f8fbe6cb39919aa6b`  
		Last Modified: Wed, 10 Apr 2024 05:04:19 GMT  
		Size: 58.8 MB (58820536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e5c54695ca89fe8e4418545a5266d439bfcaed76549aff33847d82198106a7`  
		Last Modified: Wed, 10 Apr 2024 05:04:15 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
