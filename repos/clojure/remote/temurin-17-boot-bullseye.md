## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:c0e5965172e2a96ad5581248401e31ca3713456093f9e02f5fb3ec64e663ef05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c6d7ed703b7972182b60f6ac018bb954a9d024ed92699c42be3b5f0b069ed055
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.4 MB (308365601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e58ca94383b815dcb3b7dc4b120543c631ce000dbd77f0540df065c2da3b26`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:30:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:56:02 GMT
COPY dir:09afbf947759009c57336c17f70cd71239c5d8b0170793151aec66483cdd0976 in /opt/java/openjdk 
# Thu, 06 Oct 2022 03:56:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 03:56:03 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 06 Oct 2022 03:56:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 03:56:04 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 03:56:10 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 06 Oct 2022 03:56:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 03:56:10 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 06 Oct 2022 03:56:32 GMT
RUN boot
# Thu, 06 Oct 2022 03:56:32 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 06 Oct 2022 03:56:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 06 Oct 2022 03:56:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acfce48843835d39fb569ba75ae523857fdae8d21d473e9152a27cb419979f2`  
		Last Modified: Thu, 06 Oct 2022 04:12:08 GMT  
		Size: 192.1 MB (192137601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11c114f4ba2f35cbdd982f2726c71489593df6f5a352fe746e451178979047a`  
		Last Modified: Thu, 06 Oct 2022 04:11:53 GMT  
		Size: 2.4 MB (2360728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d0c5362ae9efeab0a291efa0cd00b89a4eb727fbee26048577b7d742b914ea`  
		Last Modified: Thu, 06 Oct 2022 04:11:56 GMT  
		Size: 58.8 MB (58820625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed503815db206bcc11c58875ee60ac964d526787459bc0b6ad22e57c89ed3443`  
		Last Modified: Thu, 06 Oct 2022 04:11:52 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1c330fa7707749f016e4dd0f57d37108a6951e8f5feaf4cb71d61d3066cf3003
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305565854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d88df19f31445ddd2508c7a51e2d61e243a190680c999c8970d1b8cc638e603`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:38:34 GMT
COPY dir:dc2bc1e50ab42c5231433386b6bc2a9cff04b310112464fb4909efc66be10627 in /opt/java/openjdk 
# Thu, 06 Oct 2022 02:38:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 02:38:35 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 06 Oct 2022 02:38:36 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 02:38:37 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 02:38:43 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 06 Oct 2022 02:38:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 02:38:45 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 06 Oct 2022 02:39:33 GMT
RUN boot
# Thu, 06 Oct 2022 02:39:35 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 06 Oct 2022 02:39:35 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 06 Oct 2022 02:39:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b7798e9e43d2494af502b188de7bd161f67c7162a0b931a6e81e4e8d7c52d5`  
		Last Modified: Thu, 06 Oct 2022 03:01:09 GMT  
		Size: 190.9 MB (190904332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4ef412f00089f24b2edfc91068b2b7fb2abd52a500ecf9af694d54dfd33ca0`  
		Last Modified: Thu, 06 Oct 2022 03:00:53 GMT  
		Size: 2.1 MB (2144374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347d5a654856778a35001fcc471f22bed20431af15eb7ff73479937eece2bf86`  
		Last Modified: Thu, 06 Oct 2022 03:00:58 GMT  
		Size: 58.8 MB (58816124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc1af18a1013bb03aa53e4ab2657b977d2681f2ab9b44a4aebe4796d90eac21`  
		Last Modified: Thu, 06 Oct 2022 03:00:52 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
