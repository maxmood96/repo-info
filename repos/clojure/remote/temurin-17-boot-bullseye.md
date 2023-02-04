## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:36a67768735e410b78c8d1bfd97350d2dd07784489e3f886b7e7d54fed0fbd95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e5dadf40bf15990cd1deb0cad97e340461c38a473c34d83383eb084d5524fca7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308644979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f962a24b4952f08bdfccca0bdaaebba1854367d6553d91c323be468d85afd0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:26 GMT
ADD file:cc6a56676703ec7ab5db8f2f7bc18a3169c0816d38703845b6b77ae5342ab41c in / 
# Sat, 04 Feb 2023 06:51:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:05:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 14:11:32 GMT
COPY dir:5cf52f938fe415b0022fbccb8cf978562c503c0b8313cc9dedf46c1c4edb35cf in /opt/java/openjdk 
# Sat, 04 Feb 2023 14:11:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 14:11:34 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 04 Feb 2023 14:11:34 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 04 Feb 2023 14:11:34 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 14:11:40 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 04 Feb 2023 14:11:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 04 Feb 2023 14:11:40 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 04 Feb 2023 14:11:57 GMT
RUN boot
# Sat, 04 Feb 2023 14:11:57 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 04 Feb 2023 14:11:57 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 04 Feb 2023 14:11:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:699c8a97647f5789e5850bcf1a3d5afe9730edb654e1ae0714d5bd198a67a3ed`  
		Last Modified: Sat, 04 Feb 2023 06:55:53 GMT  
		Size: 55.0 MB (55025312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727bcccdff75985595c8badff46162a5d28d33fbf14058510d50197d1c3640f5`  
		Last Modified: Sat, 04 Feb 2023 14:23:37 GMT  
		Size: 192.4 MB (192438147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a2c58ed2b090ac998c98a374b84df0621457692a3f6d76ebe8ede4eb626dbe`  
		Last Modified: Sat, 04 Feb 2023 14:23:23 GMT  
		Size: 2.4 MB (2360646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6da79164107778fc5a27d80eb410c48f3fb784bc7a725b46406159139249698`  
		Last Modified: Sat, 04 Feb 2023 14:23:26 GMT  
		Size: 58.8 MB (58820476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32ca9ea2ae6721ff2c6e9f24f827375a805845ac05ac1316d81d08a13504a2b`  
		Last Modified: Sat, 04 Feb 2023 14:23:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8beba5c1c0189e1fb24523ab32bdf9eb4bba848546bf485e0552d3fd590e7e6a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306113829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11980674f8a513fbff1a257a25a98cb1cc1ce68731c6dfa681402fcefec6fc0b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:26 GMT
ADD file:c5a7c65d67685092faa3456c1a772550aa6d06ac07e1f98a95d39c31e304dbf8 in / 
# Sat, 04 Feb 2023 06:17:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:02:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 17:07:48 GMT
COPY dir:a1bd99c3d82513db94430c73467e1e5c69ea4624d0489571d594afe503e15dc5 in /opt/java/openjdk 
# Sat, 04 Feb 2023 17:07:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 17:07:52 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 04 Feb 2023 17:07:52 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 04 Feb 2023 17:07:52 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 17:07:57 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 04 Feb 2023 17:07:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 04 Feb 2023 17:07:58 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 04 Feb 2023 17:08:15 GMT
RUN boot
# Sat, 04 Feb 2023 17:08:15 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 04 Feb 2023 17:08:15 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 04 Feb 2023 17:08:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fac7262b6510529638951e16807cf1758f42c892ed924e334c27bb8bbcf7d7c2`  
		Last Modified: Sat, 04 Feb 2023 06:21:01 GMT  
		Size: 53.7 MB (53681927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4587f5b0b6cc201c66ee925b97cb22125be9119fe7913e0b278683e5374d83`  
		Last Modified: Sat, 04 Feb 2023 17:18:23 GMT  
		Size: 191.3 MB (191260431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def203447547b0b94c7b85936967447f75c232bae2459436d67051c6d3420fc3`  
		Last Modified: Sat, 04 Feb 2023 17:18:12 GMT  
		Size: 2.4 MB (2350636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4c7d24fecd6ce9bb8d39a9b51e43e717c74b67268e130beea3e359e752108f`  
		Last Modified: Sat, 04 Feb 2023 17:18:14 GMT  
		Size: 58.8 MB (58820436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e211cf78f123b1b6fd37196dbd13e03ccde09cd56c628eb7b0fb8f3e4b402e7`  
		Last Modified: Sat, 04 Feb 2023 17:18:11 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
