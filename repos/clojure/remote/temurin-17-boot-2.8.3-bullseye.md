## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:50d5a71a83b3da868fcced175d4d7b483da35c47a88ab8bb9c6a4f01a9718836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6520a2b8319612285efad7252e723489f8c348f6a6d5d2f067fd7df310de7c49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (261023298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3a48231f293733454a74721840f449693aca8f68102f564c470a398ae324ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:01 GMT
ADD file:8a9222387b89a9ac763fd72610ce01ab17f64387cbfde30a6af1861a82030aad in / 
# Wed, 11 Oct 2023 18:35:01 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Oct 2023 18:57:16 GMT
COPY dir:762e280751e9eaacf2bfae42d6a8cb2a49846426bd7c5675b21a4c0c8ae8fb71 in /opt/java/openjdk 
# Wed, 11 Oct 2023 18:57:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:57:17 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 11 Oct 2023 18:57:17 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 11 Oct 2023 18:57:17 GMT
WORKDIR /tmp
# Wed, 11 Oct 2023 18:57:23 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 11 Oct 2023 18:57:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 11 Oct 2023 18:57:23 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 11 Oct 2023 18:57:40 GMT
RUN boot
# Wed, 11 Oct 2023 18:57:40 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 11 Oct 2023 18:57:40 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 11 Oct 2023 18:57:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:69b3efbf67c2d9a46fdfdc8480b5a03ef73e9999a53aad57213447784f01eb6e`  
		Last Modified: Wed, 11 Oct 2023 18:39:54 GMT  
		Size: 55.1 MB (55058028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365667dfd219fc4fab7a6f4d836814d811216a8ec52ecad3b816c65e8644c142`  
		Last Modified: Wed, 11 Oct 2023 19:07:13 GMT  
		Size: 144.8 MB (144775739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855d813d070f07db8ee8a33f68563ddbdf2a13ef58ebee3f47edb51a00cf0d74`  
		Last Modified: Wed, 11 Oct 2023 19:07:01 GMT  
		Size: 2.4 MB (2368751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465c250b7ddabaf0542f98ac8f52fd652476752d248626ce7f63edf7c1dd4214`  
		Last Modified: Wed, 11 Oct 2023 19:07:06 GMT  
		Size: 58.8 MB (58820383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f53700a9ad1ebc4dca06cf2a9965671958fe73a10f5032d6f493a48f61f4b59`  
		Last Modified: Wed, 11 Oct 2023 19:07:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9b672c08527dc47922f179d0c622a9add0683b458c187778100fa28e3830a7f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258429494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e700c8141f0f435e8c356ec2134200c6855c1600dbda40803cde0e48570f1a19`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:58 GMT
ADD file:e1a6c6c976e5e7c53eb2a7343a7a763b46e56828588535f4c79e63d6ec08198d in / 
# Wed, 11 Oct 2023 18:24:58 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:45:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 10:19:41 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Fri, 13 Oct 2023 10:19:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 10:19:45 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 10:19:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 10:19:45 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 10:19:50 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 10:19:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 10:19:50 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 10:20:06 GMT
RUN boot
# Fri, 13 Oct 2023 10:20:06 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 10:20:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 10:20:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dd0dc10f921f4b3b65b17f20d367374079e6cb4e26531624ee64caaaf4adcc28`  
		Last Modified: Wed, 11 Oct 2023 18:28:45 GMT  
		Size: 53.7 MB (53707810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684313f418d9fed6660cbe779ae6207c2a9b882041837ba794aa69652458352d`  
		Last Modified: Fri, 13 Oct 2023 10:34:41 GMT  
		Size: 143.5 MB (143543484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da60352a9f31e0c080776335d61eb207da21cad73cb5e7b60f8c40f62c498749`  
		Last Modified: Fri, 13 Oct 2023 10:34:31 GMT  
		Size: 2.4 MB (2357366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c74605fe579f98c0132eb85153d5c7e716ceb0bcdcab5c5ae1d713e86b1e71`  
		Last Modified: Fri, 13 Oct 2023 10:34:35 GMT  
		Size: 58.8 MB (58820433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11153a68437f34f8f000448e9c2e032deb6e75f914e8656ac06449c9468234b`  
		Last Modified: Fri, 13 Oct 2023 10:34:31 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
