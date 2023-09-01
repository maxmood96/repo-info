## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:17f6f7a29457abe5eee0a70ab35f82cb56a245a1ff7f3939065627043443e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5872499d4479874a2ed7aaabaa1e1e36d6d5fa1e32fa39deee10174621a1694e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236092013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82ea8433faaa6c86e7646178f3b8a08b0267f8b2c8ed4c8ffbf1c47d5cad96b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Aug 2023 20:48:51 GMT
COPY dir:6777d1f77166c2ecdd8f4eb23f5fd82574aa8a90fd65d6dff981fbb31778a3d1 in /opt/java/openjdk 
# Thu, 31 Aug 2023 23:31:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2023 23:31:49 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 31 Aug 2023 23:31:49 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 31 Aug 2023 23:31:49 GMT
WORKDIR /tmp
# Thu, 31 Aug 2023 23:31:54 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 31 Aug 2023 23:31:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 31 Aug 2023 23:31:54 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 31 Aug 2023 23:32:13 GMT
RUN boot
# Thu, 31 Aug 2023 23:32:14 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 31 Aug 2023 23:32:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 31 Aug 2023 23:32:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65006a4851e206ccc53a9bf891b081e6fefbdbe0fcb897d670970fc7f2eff9ea`  
		Last Modified: Thu, 31 Aug 2023 20:51:41 GMT  
		Size: 144.8 MB (144775820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da35ef5d3ba3f1252a68755d0ce1a97b682682fedaa79a100eb40ba9f34bb3a9`  
		Last Modified: Thu, 31 Aug 2023 23:44:30 GMT  
		Size: 1.1 MB (1077543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad62d6d787003da538724e450fa06ddf7484b999164234d6983ef71a44a6598b`  
		Last Modified: Thu, 31 Aug 2023 23:44:33 GMT  
		Size: 58.8 MB (58820573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa86b440bd8ee4a418cd069ee84f98f4022f58f2e36c433f7e6e808aaf64bda`  
		Last Modified: Thu, 31 Aug 2023 23:44:29 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d4dc1e26edfb02cc95ede1d59f9bc776a0e9b9a368e6e8d423045fd6fbb21a24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233491887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd42f9a0c0eaad98cd7f73fa00b070e2564cf1b44a7eaa36c6be04766cc1eeb3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Aug 2023 21:24:25 GMT
COPY dir:544cc8a0b662cd03d0780bbc88fa0ab8d4ff7ef38b3da70f9f97f586944edbe6 in /opt/java/openjdk 
# Thu, 31 Aug 2023 22:25:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2023 22:25:01 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 31 Aug 2023 22:25:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 31 Aug 2023 22:25:01 GMT
WORKDIR /tmp
# Thu, 31 Aug 2023 22:25:06 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 31 Aug 2023 22:25:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 31 Aug 2023 22:25:06 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 31 Aug 2023 22:25:23 GMT
RUN boot
# Thu, 31 Aug 2023 22:25:23 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 31 Aug 2023 22:25:23 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 31 Aug 2023 22:25:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db320ad0aabde9ef892d611629818359b8a0e753d16e7c3cb1a7c4ef14730d6`  
		Last Modified: Thu, 31 Aug 2023 21:26:45 GMT  
		Size: 143.5 MB (143543485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a903d5b0888917bc948103876abb32214255b0c42239cb88e97e8e7e8d923a`  
		Last Modified: Thu, 31 Aug 2023 22:32:56 GMT  
		Size: 1.1 MB (1064808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3247879b7e58209e72be6f3ce4846f8c99384045c270f060e2b0219fd1a0331`  
		Last Modified: Thu, 31 Aug 2023 22:32:59 GMT  
		Size: 58.8 MB (58820379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194f68851d9e5cd4d2ab74998fb8f650c0bcd82499a0b5cae8a50fa3d72d2ebd`  
		Last Modified: Thu, 31 Aug 2023 22:32:55 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
