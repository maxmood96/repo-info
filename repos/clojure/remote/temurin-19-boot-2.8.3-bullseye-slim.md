## `clojure:temurin-19-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:0195aecd742def102ea319870534fc326550354e2b5e536abe49d81dda653558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6e02f788ca467fcb4726fe535b08ad240bd842bee563d6c7e26b7439c9378384
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292408151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673a6ab77f7927ab3ded3479de4c7b6a16290790fc4940f2f94d212f7d44306a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:06:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 14:15:02 GMT
COPY dir:94cb5af8175285c10c94286222d8a35302f3f8c290e00011a75c67156659d6ab in /opt/java/openjdk 
# Sat, 04 Feb 2023 14:15:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 14:15:04 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 04 Feb 2023 14:15:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 04 Feb 2023 14:15:04 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 14:15:10 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 04 Feb 2023 14:15:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 04 Feb 2023 14:15:10 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 04 Feb 2023 14:15:26 GMT
RUN boot
# Sat, 04 Feb 2023 14:15:27 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 04 Feb 2023 14:15:27 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 04 Feb 2023 14:15:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300431c7a62af0031d946dcb4bce1afaa7937b894471d1bac4795c1091262f26`  
		Last Modified: Sat, 04 Feb 2023 14:26:05 GMT  
		Size: 201.1 MB (201112956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed23ba4a02d9f1175b6711c651f8e28ce5677560b51e8b6434371a7e3071162`  
		Last Modified: Sat, 04 Feb 2023 14:25:50 GMT  
		Size: 1.1 MB (1077383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38398f4616f00010161a96ded0ca178b4ba36ec5dca6421f2d00e49bbd7effc`  
		Last Modified: Sat, 04 Feb 2023 14:25:53 GMT  
		Size: 58.8 MB (58820495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed69cecf44e5ceb26159cb54be14fb4307f548bb411576ad3a66bf14b6c90430`  
		Last Modified: Sat, 04 Feb 2023 14:25:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:25f21980dc7813397d061af6473dc28d8264794ffb81567cd971b8ff2d4acd2a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289785519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397987fe231eb94a85b93991f167d687d07752607915ca834b7c7b1deeb6bd8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:44:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 17:10:54 GMT
COPY dir:9a6a873ca11063f6f04e7f088397a1fce771e2b1aa8590b72eb07158cfac883f in /opt/java/openjdk 
# Sat, 04 Feb 2023 17:10:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 17:10:57 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 04 Feb 2023 17:10:57 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 04 Feb 2023 17:10:57 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 17:11:02 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 04 Feb 2023 17:11:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 04 Feb 2023 17:11:02 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 04 Feb 2023 17:11:18 GMT
RUN boot
# Sat, 04 Feb 2023 17:11:19 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 04 Feb 2023 17:11:19 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 04 Feb 2023 17:11:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd6a2c95889ff1bf974c1d3aa8d9648da50dd043fb5c120824cf6fb0944985e`  
		Last Modified: Sat, 04 Feb 2023 17:20:30 GMT  
		Size: 199.9 MB (199855200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fcbbd397c16bf512ec59d811403d7e61fc9da11286b4d7adbc2960c7169f197`  
		Last Modified: Sat, 04 Feb 2023 17:20:18 GMT  
		Size: 1.1 MB (1064646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4c1ec9371f060dcd6baa74da6b538135aab8eff1cdf88fabf23b216500e4f3`  
		Last Modified: Sat, 04 Feb 2023 17:20:21 GMT  
		Size: 58.8 MB (58820482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacd9a3bf6d5f5e8d0437c1060a44e6819c93843d3a5e42760934da098fc0551`  
		Last Modified: Sat, 04 Feb 2023 17:20:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
