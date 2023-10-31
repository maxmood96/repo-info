## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:2c796048b1e900599e9f66ec46db226b72fe2126b7aba1d500127e4a2506a310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1c9f99ab1eae4770a1cec800f3b9c3bb14ae31a2ff17e61e3e254030a8bfeb9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261121562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dbf6df419037596f9e32b9ef1ac22f3caced851ad45b1ed00b60b756934eb2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:01 GMT
ADD file:8a9222387b89a9ac763fd72610ce01ab17f64387cbfde30a6af1861a82030aad in / 
# Wed, 11 Oct 2023 18:35:01 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:53:12 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 00:53:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 00:53:13 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 00:53:13 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 00:53:14 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 00:53:19 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 00:53:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 00:53:19 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 00:53:37 GMT
RUN boot
# Tue, 31 Oct 2023 00:53:37 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 31 Oct 2023 00:53:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 31 Oct 2023 00:53:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:69b3efbf67c2d9a46fdfdc8480b5a03ef73e9999a53aad57213447784f01eb6e`  
		Last Modified: Wed, 11 Oct 2023 18:39:54 GMT  
		Size: 55.1 MB (55058028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab53f257d3db68a71e02307f0e897bdec01076b53147c2e388fed341346c344f`  
		Last Modified: Tue, 31 Oct 2023 01:12:52 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1f81710613a9c681587c7d2fce108d26ee67c85b3beb45e288958af30bd9d6`  
		Last Modified: Tue, 31 Oct 2023 01:12:41 GMT  
		Size: 2.4 MB (2368740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b16307002e0378dd5c4e8e4c6e46165768f8b12b78b6e2e627ed85354a86abf`  
		Last Modified: Tue, 31 Oct 2023 01:12:44 GMT  
		Size: 58.8 MB (58820495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6bbf8e690762885514a7e476c48ce2d7da1defd0fd0780fdb25f2b341b6233c`  
		Last Modified: Tue, 31 Oct 2023 01:12:40 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9f623dc8397658200c44308550ceffec34ce378a2600d6ff374744d8554d7db2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258567934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc76eef32003845f4fa0aa9060a870354d5eb8a7dcb3180436c95fb40e0254f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:58 GMT
ADD file:e1a6c6c976e5e7c53eb2a7343a7a763b46e56828588535f4c79e63d6ec08198d in / 
# Wed, 11 Oct 2023 18:24:58 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:45:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:01 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 01:06:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 01:06:05 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 01:06:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 01:06:05 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 01:06:10 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 01:06:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 01:06:10 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 01:06:30 GMT
RUN boot
# Tue, 31 Oct 2023 01:06:31 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 31 Oct 2023 01:06:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 31 Oct 2023 01:06:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dd0dc10f921f4b3b65b17f20d367374079e6cb4e26531624ee64caaaf4adcc28`  
		Last Modified: Wed, 11 Oct 2023 18:28:45 GMT  
		Size: 53.7 MB (53707810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90039ec2f4fe2b5cdd7b80a6438242b4a123b1c3880a1f5babfa9b9b475835ae`  
		Last Modified: Tue, 31 Oct 2023 01:22:59 GMT  
		Size: 143.7 MB (143681710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7566ab1e852d59d8d1ab59156cd3e655c40542d25b9158b35db5b336046f46a0`  
		Last Modified: Tue, 31 Oct 2023 01:22:48 GMT  
		Size: 2.4 MB (2357465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8b1868cd16dd5662a7fb76ffda86a3824629dc7e8713c4abc80206a5b02033`  
		Last Modified: Tue, 31 Oct 2023 01:22:51 GMT  
		Size: 58.8 MB (58820548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d60807bcd8345a598d36514e6bea7c39fd8a0baa2d5696d30bdb8596b533b6`  
		Last Modified: Tue, 31 Oct 2023 01:22:48 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
