## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:8b2f88a10c338504b968bbcb34100106a0218104b8fda011ce0fc1b6d97c464b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:10d0ccbdc63d256c733021a32c81f82021244e779cb7da72b3a3cfe502c04f85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314703469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377c52835be7e4a6dbe3c22f32311aa12b1274cf663c8016e96ca370bee8e542`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:40:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 07:43:44 GMT
COPY dir:fdbc5e9dec2946fa124877176e92a68dd3fe3a70def5bb906a6040c4a1303a2d in /opt/java/openjdk 
# Wed, 01 Mar 2023 07:43:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 07:43:46 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 07:43:46 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 07:43:46 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 07:43:52 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 07:43:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 07:43:52 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 07:44:11 GMT
RUN boot
# Wed, 01 Mar 2023 07:44:11 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0b29cc6adaf6091151573ab5a4ba12f03dcfaea1402985879aea0d535da14c`  
		Last Modified: Wed, 01 Mar 2023 07:56:45 GMT  
		Size: 198.5 MB (198475588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ae233260f61fbc119660e2b4a3d274be78160fdce5c91ac58cd4250913a827`  
		Last Modified: Wed, 01 Mar 2023 07:56:31 GMT  
		Size: 2.4 MB (2361542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c675b009ac0b3345f8254cfeff9deb48d31b4620d513d1e51c13368a972eea3a`  
		Last Modified: Wed, 01 Mar 2023 07:56:34 GMT  
		Size: 58.8 MB (58820417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:130aaf071f79b651096a84bf25f9fc177ca7b08e3f9e9ae0f0969553e0fd1976
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310115048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65df673505500c92ee3463f50a242d08d3b99bfa2e21c8ce0c239b3a57dadf57`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:04:01 GMT
COPY dir:b661686bf8d434588756c45f2ef6e7f314f32f753cf180ef8fb45397388f098c in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:04:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:04:06 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 03:04:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 03:04:06 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:04:10 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 03:04:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 03:04:11 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 03:04:28 GMT
RUN boot
# Wed, 01 Mar 2023 03:04:28 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db5f99a046fb93d70e363d58ebe237b913e09a889f35b330f65e0bfa4627f3c`  
		Last Modified: Wed, 01 Mar 2023 03:15:41 GMT  
		Size: 195.2 MB (195240319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10e8ed13cb2c61cc3df0df1f561ffb2ea74ef7bcad3057e758d7a954993350b`  
		Last Modified: Wed, 01 Mar 2023 03:15:30 GMT  
		Size: 2.4 MB (2351022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be609b0d2928b4f0b0f06c0305df464086a410a6084ef30c091859939f298456`  
		Last Modified: Wed, 01 Mar 2023 03:15:32 GMT  
		Size: 58.8 MB (58820492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
