## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:5a692283c8561e3fd656784934a836b4b8685d980ee3d06262c36ef3714631b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e0220a8d445f94380d348a0929b3a96962c6183db4d12a9b2c81b71d7dcace1b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314684879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c88a2a5537ae704deafa781c9d3518561ea3da183965e08f659411cffc6087`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 01:11:42 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Sat, 05 Nov 2022 01:11:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:11:44 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 05 Nov 2022 01:11:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 05 Nov 2022 01:11:45 GMT
WORKDIR /tmp
# Sat, 05 Nov 2022 01:11:50 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 05 Nov 2022 01:11:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 05 Nov 2022 01:11:50 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 05 Nov 2022 01:12:10 GMT
RUN boot
# Sat, 05 Nov 2022 01:12:10 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888ca723db20161bd481e5a8af9ae7b9145b403d0fa3f2f444e7c6a21909570c`  
		Last Modified: Sat, 05 Nov 2022 01:25:58 GMT  
		Size: 198.5 MB (198455847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89052280c96745e6b7276e9d6a92bb668427b1e1ad4c6d6e9094f53de42ed1e3`  
		Last Modified: Sat, 05 Nov 2022 01:25:44 GMT  
		Size: 2.4 MB (2362167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28982c49d36bfea95914abcbaccd25cb397ccca89bbd8ad3b238952c8e6cc1e9`  
		Last Modified: Sat, 05 Nov 2022 01:25:48 GMT  
		Size: 58.8 MB (58820533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ba8b7109743f452edd8186d5a20756a662289f9a103aa340559014015da543d5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310075615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0139927831fbd680f555de7487719de34373e0e16614bfff85701ef23ec3991`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:55 GMT
ADD file:b16745ece8ef84c028d7e9ac4bf026ac64f885d4170bfcc9d435f237144a1b99 in / 
# Tue, 25 Oct 2022 05:45:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 23:53:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:12:15 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Fri, 04 Nov 2022 23:12:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Nov 2022 23:12:19 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 04 Nov 2022 23:12:19 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 04 Nov 2022 23:12:19 GMT
WORKDIR /tmp
# Fri, 04 Nov 2022 23:12:24 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 04 Nov 2022 23:12:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 04 Nov 2022 23:12:24 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 04 Nov 2022 23:12:41 GMT
RUN boot
# Fri, 04 Nov 2022 23:12:41 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:8e1d92e7d04d2a9a9880cb45dc3c32c2805912cd86abed96d0ada3ff28748205`  
		Last Modified: Tue, 25 Oct 2022 05:48:40 GMT  
		Size: 53.7 MB (53701966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89422e3bba4e9ae7d9df0676636eb6b1edefecaba3fbeccf62fea3f8a444364e`  
		Last Modified: Fri, 04 Nov 2022 23:23:14 GMT  
		Size: 195.2 MB (195201089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b64e30b70527d8ccb91eac49510de5433f79b79c79002abfe03b2eaa0e9a52`  
		Last Modified: Fri, 04 Nov 2022 23:23:02 GMT  
		Size: 2.4 MB (2352243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc438d6c17dbdd5f401b287010dbf191f07bc2c93f5943229a4a3fec853ff00`  
		Last Modified: Fri, 04 Nov 2022 23:23:05 GMT  
		Size: 58.8 MB (58820317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
