## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:db934abd70c7125b23dd00353e151a9e608bec90fa363362ef9ebcd19f2246ba
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
$ docker pull clojure@sha256:cbffae2af09f57c139a571df1c4d9d197a7d8f5ba00a4e0c2641517c4e19142c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258429481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5551fe2768e834922eee694465ed0b7a960fa79ad746f89513bb1f1bd27cad80`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:58 GMT
ADD file:e1a6c6c976e5e7c53eb2a7343a7a763b46e56828588535f4c79e63d6ec08198d in / 
# Wed, 11 Oct 2023 18:24:58 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:45:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Oct 2023 18:50:47 GMT
COPY dir:9add47918f86acac35c907520d4811042633ac78a65fb2fbf0acc7586100f57a in /opt/java/openjdk 
# Wed, 11 Oct 2023 18:50:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:50:51 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 11 Oct 2023 18:50:51 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 11 Oct 2023 18:50:51 GMT
WORKDIR /tmp
# Wed, 11 Oct 2023 18:50:56 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 11 Oct 2023 18:50:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 11 Oct 2023 18:50:56 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 11 Oct 2023 18:51:13 GMT
RUN boot
# Wed, 11 Oct 2023 18:51:13 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 11 Oct 2023 18:51:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 11 Oct 2023 18:51:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dd0dc10f921f4b3b65b17f20d367374079e6cb4e26531624ee64caaaf4adcc28`  
		Last Modified: Wed, 11 Oct 2023 18:28:45 GMT  
		Size: 53.7 MB (53707810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a1f8b3759a1839cb8073a249d154141146ae4412f22a174f43a763f9d6c8c7`  
		Last Modified: Wed, 11 Oct 2023 18:59:29 GMT  
		Size: 143.5 MB (143543483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c641ef8d53d2a977a08514971df538d91c2f5c3119a35c99e9b9e841e7078b4e`  
		Last Modified: Wed, 11 Oct 2023 18:59:20 GMT  
		Size: 2.4 MB (2357353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660e958dfca0b00a4a67e99a5f563657864a4b45f08ae2ebaeac0d7c10bcc685`  
		Last Modified: Wed, 11 Oct 2023 18:59:27 GMT  
		Size: 58.8 MB (58820436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4552e934ae056f7d2bfbdc94d18bfcec7a6e5956208a605b07ea05191d522e1`  
		Last Modified: Wed, 11 Oct 2023 18:59:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
