## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:3c4c126bb5f8f56fd3a4054a65ebdb15730513b3b6d24437b1ef971e914eff3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d77876351a3debe1f7ece59a68025de522985b13359f3a244c634ad41346c8a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283896353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953a5d1a03d029cc98aba42118d7dfe24d06e13d3c465e6266ed34c836cadc68`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:00:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 11:24:32 GMT
COPY dir:4f02f3c240ecc691ff41263b0454f619d51a2ba11a57fe51c0e31e7ff62a9194 in /opt/java/openjdk 
# Wed, 05 Jul 2023 11:24:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 11:24:34 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Jul 2023 11:24:34 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Jul 2023 11:24:34 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 11:24:39 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Jul 2023 11:24:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Jul 2023 11:24:39 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Jul 2023 11:24:56 GMT
RUN boot
# Wed, 05 Jul 2023 11:24:56 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 05 Jul 2023 11:24:56 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Jul 2023 11:24:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fafbbd507c7f35e198981926b1a326f224d7e89d5a693df01bea8a92ba4e7d1b`  
		Last Modified: Wed, 05 Jul 2023 11:36:02 GMT  
		Size: 192.6 MB (192580435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576cfae513c3806cf2c252e0ad27ac0c2f0020829145a355b2bca624c41c8fac`  
		Last Modified: Wed, 05 Jul 2023 11:35:49 GMT  
		Size: 1.1 MB (1077536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5454bd671bdf9f23a8eef1ff97444082a775dff7b010d8da75f98aa030e18100`  
		Last Modified: Wed, 05 Jul 2023 11:35:52 GMT  
		Size: 58.8 MB (58820595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a37c483dd932dce0d4f07339301bb8d8ea0ead46a213cd3cde32b2f1e3b6f70`  
		Last Modified: Wed, 05 Jul 2023 11:35:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bdb5ce44b837f8aa980e041f1a123b4cba1d03847ccca7d8f0b6792c67fa05e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233486794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06fec8a2233f7ff1814b138ae72bf1c1e1df3dd8a11b31b2d474f4b915049c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Jul 2023 22:58:45 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Tue, 25 Jul 2023 22:58:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 22:58:49 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 25 Jul 2023 22:58:49 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 25 Jul 2023 22:58:49 GMT
WORKDIR /tmp
# Tue, 25 Jul 2023 22:58:53 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 25 Jul 2023 22:58:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 25 Jul 2023 22:58:54 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 25 Jul 2023 22:59:09 GMT
RUN boot
# Tue, 25 Jul 2023 22:59:10 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 25 Jul 2023 22:59:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 25 Jul 2023 22:59:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c798e6c54e318dbfe8b5b1325d38da64ea5e5a387b26c620cc1f0c2820d0f70a`  
		Last Modified: Tue, 25 Jul 2023 23:05:13 GMT  
		Size: 143.5 MB (143538051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f022df721f2161c242aa45b07dc22205fc76e3559c0466ed45ffd4ddbce623`  
		Last Modified: Tue, 25 Jul 2023 23:05:04 GMT  
		Size: 1.1 MB (1064810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eba96a071a612739c8d84d122c715ccfecb08d311e419ac7832f9b70fa72b57`  
		Last Modified: Tue, 25 Jul 2023 23:05:06 GMT  
		Size: 58.8 MB (58820577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f22dfb66f5c14b092e76da1a03fd02feb77aff2da8418662db15f26d37f47bf`  
		Last Modified: Tue, 25 Jul 2023 23:05:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
