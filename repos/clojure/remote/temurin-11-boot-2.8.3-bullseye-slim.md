## `clojure:temurin-11-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:4845bac22ca4bfd86911d93d50b55f6a374100bb4151a001ad116813199bd5e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2c3519d27544d9650e2c03ab3c0645e8b61b008f78b6e08e7f512a4101f6a5aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236141867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13380c1c3ac7495c12708c05f177468dc04ef83c8358704d44a9bae44f11f660`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Aug 2023 20:50:14 GMT
COPY dir:9c2351d5d5cdf669213a7cfcfa52bd6bd8e9fc36b0a8e93328276d7280e1bab3 in /opt/java/openjdk 
# Thu, 31 Aug 2023 23:22:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2023 23:22:59 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 31 Aug 2023 23:22:59 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 31 Aug 2023 23:22:59 GMT
WORKDIR /tmp
# Thu, 31 Aug 2023 23:23:05 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 31 Aug 2023 23:23:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 31 Aug 2023 23:23:05 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 31 Aug 2023 23:23:24 GMT
RUN boot
# Thu, 31 Aug 2023 23:23:24 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d08bb3cc4c5f5565aedec30d167dd9f4534631431ccf2ef52db66770488b231`  
		Last Modified: Thu, 31 Aug 2023 20:54:04 GMT  
		Size: 144.8 MB (144826071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3cb6ad466ce885faf5048f936b61e36769c0a28b486edc05d0dacb2c2fa27a`  
		Last Modified: Thu, 31 Aug 2023 23:41:12 GMT  
		Size: 1.1 MB (1077567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653439b772b1a890046b63fdbd2c04f59a7e6d6d87cbec4b50c31b6bc08f3f9f`  
		Last Modified: Thu, 31 Aug 2023 23:41:15 GMT  
		Size: 58.8 MB (58820551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:42b4cc50b57d9e7a1baf7a17abe0306c266107fcaa6b11e55d9f5a57305aacaf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231518495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b226fec133da2d3a2956b7de796f2bf74081208409530dd2aff0735d255ebb4e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Aug 2023 21:25:45 GMT
COPY dir:5893aa8259c326023fbed778b793e0c69a0437031d8da5faa0a285cd6e549029 in /opt/java/openjdk 
# Thu, 31 Aug 2023 22:20:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2023 22:20:36 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 31 Aug 2023 22:20:36 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 31 Aug 2023 22:20:37 GMT
WORKDIR /tmp
# Thu, 31 Aug 2023 22:20:41 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 31 Aug 2023 22:20:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 31 Aug 2023 22:20:41 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 31 Aug 2023 22:21:00 GMT
RUN boot
# Thu, 31 Aug 2023 22:21:00 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248227e1f62c9722645138bcad60e493e720e54e2d54cfdb500dfba94f41b12a`  
		Last Modified: Thu, 31 Aug 2023 21:28:59 GMT  
		Size: 141.6 MB (141570400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e045f70d487a40bdc8a99f8dcf2a0cf32650992a498d2978265d5a1ace216b`  
		Last Modified: Thu, 31 Aug 2023 22:30:00 GMT  
		Size: 1.1 MB (1064839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f85a326f8b9dd2c93cf69fc3d05cc9f5042cc573f5e90feaa8b48b6524be492`  
		Last Modified: Thu, 31 Aug 2023 22:30:04 GMT  
		Size: 58.8 MB (58820440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
