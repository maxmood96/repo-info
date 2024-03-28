## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:f8022dd64e14f8f28cec4d3aeb89c0a5734c2c0e6fd11f4ed0ea5e819c4b22b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:40c810f58bf67e74136f86c99a760c3f0f3a6ab739d738e435139f28feeb6592
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261544011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d6785b5b8b3691ba7c0a098bf1fc5efc24047411c51e644ca9b9e05ac1949c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:11 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 12 Mar 2024 01:21:11 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 06:18:04 GMT
COPY dir:9807503b62b5ec57f5790350ba2323b4402a31264d57970336b28a606d7a3a68 in /opt/java/openjdk 
# Tue, 12 Mar 2024 06:18:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 06:18:06 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 06:18:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 06:18:06 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 06:18:12 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 06:18:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 06:18:12 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 06:18:31 GMT
RUN boot
# Tue, 12 Mar 2024 06:18:31 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f608604393368f518f031d9a8951c541e3f9fc9b1b2523354c649adf7baa69`  
		Last Modified: Tue, 12 Mar 2024 06:38:01 GMT  
		Size: 145.3 MB (145271155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d035e79425cfac1f35e9d6b815a4da915da55c2894287a0394c5e7a7a8215026`  
		Last Modified: Tue, 12 Mar 2024 06:37:49 GMT  
		Size: 2.4 MB (2367261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6358cb8d49715f838a517ec7fd4dcae3978a7ba4e6ae4b00ad00bc3a511583`  
		Last Modified: Tue, 12 Mar 2024 06:37:52 GMT  
		Size: 58.8 MB (58820626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1f737b430779c0f9ee31fd2d51f2b12776ae59cafd5e188e9a0965caf1c890d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256904821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7799d8287845e36bf1c8fb88fa1a6597a1d49a8da4251eafc919894640d3048b`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:33:19 GMT
COPY dir:d5fb8d9a38dea7496f2aff176bc9a34bbca80551c2dc57109d2dae5907a339ee in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:33:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:33:22 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 02:33:22 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:33:22 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:33:28 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 02:33:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:33:28 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 02:33:44 GMT
RUN boot
# Thu, 28 Mar 2024 02:33:44 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1fdda8e4da6bde8ae6730609d8d2464cbd336e3514cb984622194caa155ea73`  
		Last Modified: Thu, 28 Mar 2024 02:50:00 GMT  
		Size: 142.0 MB (142006317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1576a827f0821e7833bdf36fd9f1e4b5e559fd5cf38a20e1536880a1aedcdf`  
		Last Modified: Thu, 28 Mar 2024 02:49:52 GMT  
		Size: 2.4 MB (2355852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a46d82bae598ae3418ce3a7951ac66dd612a563ca4936d91cb2c8554984d199`  
		Last Modified: Thu, 28 Mar 2024 02:49:54 GMT  
		Size: 58.8 MB (58820553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
