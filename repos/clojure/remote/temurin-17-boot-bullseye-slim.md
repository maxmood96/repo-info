## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:2d8ad26c0cd00f0e697559995eec3f3ce78c1d088a7506cb49e1558b980009bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bf5fb1cc141ffbe28287c5fb026831366dfa7da6cbf9574fd8516decbde9eb3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236213536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8fa0a31b9bd2f027d9ac2e6ab77a033cdbc5a58086e7b37fd28a7366d62510`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 05:23:02 GMT
COPY dir:6673b976fb9ccd391df2de00f5738789bfa84c9bc068b98b869cb1d7436fd333 in /opt/java/openjdk 
# Fri, 16 Feb 2024 05:23:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 05:23:04 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Feb 2024 05:23:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Feb 2024 05:23:04 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 05:23:10 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Feb 2024 05:23:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Feb 2024 05:23:10 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Feb 2024 05:23:29 GMT
RUN boot
# Fri, 16 Feb 2024 05:23:29 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 16 Feb 2024 05:23:29 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Feb 2024 05:23:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f0fc78b66d4b42be2ff0a23e21d3d64cf400961852ccf277b2f8c893c9409d`  
		Last Modified: Fri, 16 Feb 2024 05:37:27 GMT  
		Size: 144.9 MB (144892535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739508b4b7052949441060a1a73d27bf4866126123850d6ec10d9a915e21adf3`  
		Last Modified: Fri, 16 Feb 2024 05:37:15 GMT  
		Size: 1.1 MB (1077660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d996b3d4ea369eb7440392388dcb01231e90eaf93ea017a4f95001d1069614`  
		Last Modified: Fri, 16 Feb 2024 05:37:18 GMT  
		Size: 58.8 MB (58820516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3926c4ae70847a6f32415a590c808ee62f2b80ffa0d6120323968bbc48b968f`  
		Last Modified: Fri, 16 Feb 2024 05:37:15 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b9ef235cf0385ef948d720fea3253aa55d02b811fc6787cf5bb5085d933ad34c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233677889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec4d1a72f9be649497a940706874827a9df5ab964052bc4a1750e041eb2e598`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:56:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 07:59:49 GMT
COPY dir:868002d69a8870cfd22502db6415e3cd8591d5271a62d90057620eefd5ce7d20 in /opt/java/openjdk 
# Fri, 16 Feb 2024 07:59:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 07:59:53 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Feb 2024 07:59:53 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Feb 2024 07:59:53 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 07:59:58 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Feb 2024 07:59:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Feb 2024 07:59:58 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Feb 2024 08:00:17 GMT
RUN boot
# Fri, 16 Feb 2024 08:00:17 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 16 Feb 2024 08:00:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Feb 2024 08:00:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95db6848a5501ac6095ba49011e465a0c3ee89a48c93cee11d5d41a74651ab43`  
		Last Modified: Fri, 16 Feb 2024 08:12:19 GMT  
		Size: 143.7 MB (143720860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fe1fcb00d6381dfdd6a93e658d5cc8fe59bdcbceddbd32c542055bf92c4e79`  
		Last Modified: Fri, 16 Feb 2024 08:12:10 GMT  
		Size: 1.1 MB (1065006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed15dc41dbbe37618ce53d9d5edfece3f235fe7202e4e37cdfae0c6fc2dec61b`  
		Last Modified: Fri, 16 Feb 2024 08:12:12 GMT  
		Size: 58.8 MB (58820545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1004fffa006e86e06a78c8e8da6e9a9a362481ae6566aef6cdadc64f2d193864`  
		Last Modified: Fri, 16 Feb 2024 08:12:09 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
