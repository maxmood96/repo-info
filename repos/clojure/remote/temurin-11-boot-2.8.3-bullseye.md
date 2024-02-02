## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:caef96762b089b2232cc9b42f1e8f99830d22d81bd68f7e31e96b3665da95bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6206bab9bad9837178bbb657d719b96dfa6cc46eedf6c39eaf961190dfe7ad9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261517336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81061b58f400bb75eb85dd28bfc232ac23989b60045554d381fc16be941150f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 17:11:09 GMT
COPY dir:b67fa5b31406358a1c40465f439a0fe28f2585d2aa41aff7249c3c30b266c578 in /opt/java/openjdk 
# Fri, 02 Feb 2024 17:11:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 17:11:09 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Feb 2024 17:11:09 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 17:11:09 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:11:17 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 17:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 17:11:17 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Feb 2024 17:11:36 GMT
RUN boot
# Fri, 02 Feb 2024 17:11:37 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605d7fef2171261d35cbe76cea836569a7106d2a9523d9a32c74193df8b83e18`  
		Last Modified: Fri, 02 Feb 2024 17:31:44 GMT  
		Size: 145.3 MB (145271036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e6d2d7a46691ce3b3952f326643d284ae212f7949006083ba017b712f64c59`  
		Last Modified: Fri, 02 Feb 2024 17:31:32 GMT  
		Size: 2.4 MB (2368743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480457ae31d8e83020bf1180a7dccc78a518122041bf78609156bcfd00201a9e`  
		Last Modified: Fri, 02 Feb 2024 17:31:36 GMT  
		Size: 58.8 MB (58820594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8a9c14c192bccc26a6923b4027e4aa11aa7f495befb968333cd9ae9bf0eb8429
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256892624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885e40c60fca7f70980443806e74d252778bb7508b98bd49276b35b571dfb342`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:20:51 GMT
COPY dir:66e2d93ab60a4ef1bb1a1f0fa29608c8835186fbe657955fddda78ed144821fc in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:20:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:20:54 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 02 Feb 2024 08:20:54 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 08:20:54 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:21:00 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 02 Feb 2024 08:21:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 08:21:01 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 02 Feb 2024 08:21:19 GMT
RUN boot
# Fri, 02 Feb 2024 08:21:19 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b439db64bcde69fb388115b6850434c56a98c6d0d363997cfa20eb0a1fb35d9`  
		Last Modified: Fri, 02 Feb 2024 08:38:45 GMT  
		Size: 142.0 MB (142006376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2646619f4f50dcccae1b5b7bd9b3b66ea4a632826066da1b6233d1163ab5a41a`  
		Last Modified: Fri, 02 Feb 2024 08:38:35 GMT  
		Size: 2.4 MB (2357451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdda7cb4ffdd5732113a3d02282c4308c11cd7da3636de39556868d65c4edf89`  
		Last Modified: Fri, 02 Feb 2024 08:38:37 GMT  
		Size: 58.8 MB (58820530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
