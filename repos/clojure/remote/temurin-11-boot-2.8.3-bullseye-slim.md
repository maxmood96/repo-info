## `clojure:temurin-11-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:1142789117a952481736b1b45f80f07659000a260c32d5f7a9db9646bad023b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b6635ac40869b5ffa8b3282e0bf0c1dcd85d28d28830be84c3fe4ed420feb114
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236596761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e4b0d3278029be193af6b67d0944e4c28e3e3dec7b9f4fe16242eadd40b2c1`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 10:56:33 GMT
COPY dir:daac410d49a992b5ee309816020a7ba772f8c0edbe3557815c30b5c2d8f8820a in /opt/java/openjdk 
# Tue, 16 Apr 2024 10:56:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 10:56:34 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 16 Apr 2024 10:56:34 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 16 Apr 2024 10:56:34 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 10:56:41 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 16 Apr 2024 10:56:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Apr 2024 10:56:41 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 16 Apr 2024 10:57:00 GMT
RUN boot
# Tue, 16 Apr 2024 10:57:00 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1285df439becc98660f5ac5dff9e2cfb5f4dce86559d91d1883529a9b8730d6f`  
		Last Modified: Tue, 16 Apr 2024 11:17:44 GMT  
		Size: 145.3 MB (145271004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7496dd2cd68a4fe320225e637d6d6dd25c4455cbb0a7b10e014bdcd7d5f9e598`  
		Last Modified: Tue, 16 Apr 2024 11:17:33 GMT  
		Size: 1.1 MB (1077708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292e1c4a6cc693acb3d4329f52bcce21cb421fb4c6e07cf1eb086eef9439d055`  
		Last Modified: Tue, 16 Apr 2024 11:17:36 GMT  
		Size: 58.8 MB (58820311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a2cd9bf1608eac0aef88e48fd52d09458e2440f2fbf790590242cc57bd80040e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231968278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930aacb6610b5123578db481f8e37b17ed5b17a05cd8ca432a226cf1f774fc0c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 06:34:19 GMT
COPY dir:337eb37873e2fe424b3d62c18ff2640cf50898156a884981e9e10924759441c3 in /opt/java/openjdk 
# Tue, 16 Apr 2024 06:34:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 06:34:22 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 16 Apr 2024 06:34:22 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 16 Apr 2024 06:34:22 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:34:27 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 16 Apr 2024 06:34:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Apr 2024 06:34:27 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 16 Apr 2024 06:34:45 GMT
RUN boot
# Tue, 16 Apr 2024 06:34:45 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff05a7b30a1c1c5b0e61fdf5d3f92a4bba15507b0cd3761604069982b2384477`  
		Last Modified: Tue, 16 Apr 2024 06:53:05 GMT  
		Size: 142.0 MB (142006376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52aa1a3d1fe0d75ededcc907eb692d668cdb3080819fe8b94338644e82719e04`  
		Last Modified: Tue, 16 Apr 2024 06:52:56 GMT  
		Size: 1.1 MB (1064952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd941598d3d089c19a6cb8787519e8bc7331a0679b1212280c4c946bc8af577`  
		Last Modified: Tue, 16 Apr 2024 06:52:59 GMT  
		Size: 58.8 MB (58820644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
