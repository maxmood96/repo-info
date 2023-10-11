## `clojure:temurin-8-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:f6d900fb6a78de58d2c5f875f4b9e7523079ea60f14a2c7bae847ad42dfc1cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e8cf00bda9902f2a05f17d382175c2fd42696ffbcb84e0db345c7c339592f949
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219832289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66571236c488cf1fe45ca6a46c7768a6176ae3e93af467d131144b0fba002d4`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:01 GMT
ADD file:8a9222387b89a9ac763fd72610ce01ab17f64387cbfde30a6af1861a82030aad in / 
# Wed, 11 Oct 2023 18:35:01 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Oct 2023 18:51:27 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Wed, 11 Oct 2023 18:51:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:51:27 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 11 Oct 2023 18:51:28 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 11 Oct 2023 18:51:28 GMT
WORKDIR /tmp
# Wed, 11 Oct 2023 18:51:33 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 11 Oct 2023 18:51:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 11 Oct 2023 18:51:34 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 11 Oct 2023 18:51:52 GMT
RUN boot
# Wed, 11 Oct 2023 18:51:52 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:69b3efbf67c2d9a46fdfdc8480b5a03ef73e9999a53aad57213447784f01eb6e`  
		Last Modified: Wed, 11 Oct 2023 18:39:54 GMT  
		Size: 55.1 MB (55058028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0484593b15ad8725a3c8408b36968a6a2a8c9374979f21ea8472663545e4cab2`  
		Last Modified: Wed, 11 Oct 2023 19:03:25 GMT  
		Size: 103.6 MB (103585043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29eeb7ada75951bbe18e5915d04067e54d0c6d47cb28219737fc19ad300dd6d`  
		Last Modified: Wed, 11 Oct 2023 19:03:16 GMT  
		Size: 2.4 MB (2368721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c7ba676aa783071d46496a2d89d496a82d75af7b7abb669c9dc26b943a7842`  
		Last Modified: Wed, 11 Oct 2023 19:03:21 GMT  
		Size: 58.8 MB (58820497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5bb3be96982f759da6dd05fd695c6b7d80013ab780ae2a9f6e528ea349480304
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217576631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b90ccd92272cd6c39e75c7fb27e9cf81a13d0b38ab11520371e0924816125f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:58 GMT
ADD file:e1a6c6c976e5e7c53eb2a7343a7a763b46e56828588535f4c79e63d6ec08198d in / 
# Wed, 11 Oct 2023 18:24:58 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:45:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Oct 2023 18:45:22 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Wed, 11 Oct 2023 18:45:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:45:24 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 11 Oct 2023 18:45:24 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 11 Oct 2023 18:45:25 GMT
WORKDIR /tmp
# Wed, 11 Oct 2023 18:45:30 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 11 Oct 2023 18:45:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 11 Oct 2023 18:45:30 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 11 Oct 2023 18:46:06 GMT
RUN boot
# Wed, 11 Oct 2023 18:46:06 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:dd0dc10f921f4b3b65b17f20d367374079e6cb4e26531624ee64caaaf4adcc28`  
		Last Modified: Wed, 11 Oct 2023 18:28:45 GMT  
		Size: 53.7 MB (53707810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9023335902a8e4a34ef793a0035a716a10c893a34643861db03f1be029c9a229`  
		Last Modified: Wed, 11 Oct 2023 18:56:11 GMT  
		Size: 102.7 MB (102690464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a6c1e2627e751b53cb51ba0b7e179bf95c2c5cf9aa0a95d638a2d80d4a8f15`  
		Last Modified: Wed, 11 Oct 2023 18:56:04 GMT  
		Size: 2.4 MB (2357466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f69a4d20a4147d1e13e47eb42b57803a93e8daa869e3a1527529a2fb122b3e`  
		Last Modified: Wed, 11 Oct 2023 18:56:07 GMT  
		Size: 58.8 MB (58820891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
