## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:490b4835a43b35076752ec5b943a270955acc102a58c18288e30339c15ca3a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0431e3fdc67dd263718d3ffb83c7ede9134b20e6a411c9658e61d4456ebe99b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261543738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db582cf608bbf8588b5dfa36a50c5267a85da6973c84a40e9b9da8b0a29cc20c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:53:54 GMT
COPY dir:b67fa5b31406358a1c40465f439a0fe28f2585d2aa41aff7249c3c30b266c578 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:53:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:53:55 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 01:53:55 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 01:53:56 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:54:01 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 01:54:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 01:54:01 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 01:54:20 GMT
RUN boot
# Tue, 13 Feb 2024 01:54:20 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281fd91f06e23fb8bb875dacdbb6833a4d72153ad3b5edf098143c2f04ff19a3`  
		Last Modified: Tue, 13 Feb 2024 02:13:32 GMT  
		Size: 145.3 MB (145271028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8e47417daf7de8a9bbc4047fd1f6ccac7810804c992de088f996567c7479c6`  
		Last Modified: Tue, 13 Feb 2024 02:13:21 GMT  
		Size: 2.4 MB (2367251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d08c6e8f0e8f164161588e359c86dda2e84464b158ce6a58e769c45e352b86`  
		Last Modified: Tue, 13 Feb 2024 02:13:24 GMT  
		Size: 58.8 MB (58820621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bc0f247dc3f5ddc7e260b40b710245270cdcb927a6005ba7051a9a06af6c9f43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256904032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79033f997f51f8f5afde3f4c65d2a68dff5f388ce1afc746227cb190a86cdc78`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:00:36 GMT
COPY dir:66e2d93ab60a4ef1bb1a1f0fa29608c8835186fbe657955fddda78ed144821fc in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:00:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:00:39 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 02:00:39 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 02:00:40 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:00:44 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 02:00:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 02:00:45 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 02:01:02 GMT
RUN boot
# Tue, 13 Feb 2024 02:01:02 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c186ed2a4be59e96efae471350e604eb9aeb2c333085eb5710177787530416b`  
		Last Modified: Tue, 13 Feb 2024 02:17:46 GMT  
		Size: 142.0 MB (142006384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260f6242fcf1e6c0dc5e088d30a27b7394ba5ed87a0eadf835015454f45b96ac`  
		Last Modified: Tue, 13 Feb 2024 02:17:37 GMT  
		Size: 2.4 MB (2355787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876ddddc10d676194a6566dfe402e5a1008396252b3af44e35a316671b989d50`  
		Last Modified: Tue, 13 Feb 2024 02:17:40 GMT  
		Size: 58.8 MB (58820375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
