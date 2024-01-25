## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:f0995e3449afb5b50814866e99ec8c7d0681c86ed5fe0276208d638e313c220c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a95f81c362d2a54dcefba330572896e56efd377d2229066337800150121b6d6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261517791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61b4bff15e916876fed5e491c81e3c3071482340194b44f889514ae0424e47a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:10:04 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:10:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:10:06 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:10:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:10:06 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:10:12 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:10:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:10:12 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:10:30 GMT
RUN boot
# Wed, 24 Jan 2024 22:10:30 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d2777753c6e802d3f0a823c3e3720d828d6a8db23bb61b593090e0ca659c5a`  
		Last Modified: Wed, 24 Jan 2024 22:37:27 GMT  
		Size: 145.3 MB (145270941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251b163f4014cd586b7622be65061f734b80676d929f3ab70d2c29b54397dced`  
		Last Modified: Wed, 24 Jan 2024 22:37:15 GMT  
		Size: 2.4 MB (2368741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2ae94f5288bb1dd4cb45376d1e571141fb83b9f29070d3ab63057120a5f946`  
		Last Modified: Wed, 24 Jan 2024 22:37:18 GMT  
		Size: 58.8 MB (58820386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4c683b28c65856d4e4e88ea7ea6a608792dd11a83ceb21bb4685a130ae96ac6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256892076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2273236f974cda4f650254758f0bbd9ae7fe42e3a7cc5279002537c0f1a7635`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:00:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:15:18 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:15:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:15:22 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:15:22 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:15:22 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:15:26 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:15:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:15:27 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:15:42 GMT
RUN boot
# Wed, 24 Jan 2024 22:15:42 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4784242628146db6fb7c6468a1ce206df42dc47a858378c4c1f685782f5c44a`  
		Last Modified: Wed, 24 Jan 2024 22:37:23 GMT  
		Size: 142.0 MB (142006473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6806a166b89367b0cc2e936b35204961b83f58860f2609abb0c1802c46459fc0`  
		Last Modified: Wed, 24 Jan 2024 22:37:06 GMT  
		Size: 2.4 MB (2357352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90fc987a5fb03facea72b1bae7508b07d52b452e4d569e308bebaf79117ce3f`  
		Last Modified: Wed, 24 Jan 2024 22:37:09 GMT  
		Size: 58.8 MB (58820404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
