## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:94d21acc494343fd361ff7e55469b01e972c2c0dbaca53f126701164c1e776b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:40e50da65f83473a92bb00e02f2cfd8590d2449199cf832496f8a9a63ac65405
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261543521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615a9e0b2bb0555d5462dce6a2720cae1e30fe8082a995217d960ccb74b6c6ba`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 05:15:18 GMT
COPY dir:95f5b1bebae6bba6ca961eb10c7982ff1efe410622f69bd5e96558adc723ec83 in /opt/java/openjdk 
# Fri, 16 Feb 2024 05:15:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 05:15:20 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Feb 2024 05:15:20 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Feb 2024 05:15:20 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 05:15:27 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Feb 2024 05:15:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Feb 2024 05:15:27 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Feb 2024 05:15:47 GMT
RUN boot
# Fri, 16 Feb 2024 05:15:47 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84a8644a343d4e99709030fd0959289f32549436480f2512f939201a1f39bcb`  
		Last Modified: Fri, 16 Feb 2024 05:32:54 GMT  
		Size: 145.3 MB (145270856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ccb0502b359ba6efb5231b8b6ef024ce8ccd4622c994b334bedc5b5a934313`  
		Last Modified: Fri, 16 Feb 2024 05:32:43 GMT  
		Size: 2.4 MB (2367304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e87973993ee08b1689d0a75d38fff77017757886c57bdcd63f69c83569e3d97`  
		Last Modified: Fri, 16 Feb 2024 05:32:47 GMT  
		Size: 58.8 MB (58820523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c2975de418b498cb2e7c0692438f03704e74fc2b53e0d105dd1e03e5eb43209a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256904391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552c8c01557f4268cf82a5e0e71b9d804445efefe94649416826e47919311ac0`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 07:53:01 GMT
COPY dir:0419d7bc8c60addce41546593a3de80cd02ee9001351a641f9cf113402b5fb20 in /opt/java/openjdk 
# Fri, 16 Feb 2024 07:53:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 07:53:04 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Feb 2024 07:53:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Feb 2024 07:53:04 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 07:53:11 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Feb 2024 07:53:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Feb 2024 07:53:11 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Feb 2024 07:53:30 GMT
RUN boot
# Fri, 16 Feb 2024 07:53:31 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648b28c7b0b1b882a71e9849233f4ab02acfab37c54f47808d97c101efa9ef70`  
		Last Modified: Fri, 16 Feb 2024 08:08:08 GMT  
		Size: 142.0 MB (142006410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8323e28f3349b08c700183910ef28576a9fb5fecdbec1b55354906037084e7fb`  
		Last Modified: Fri, 16 Feb 2024 08:07:59 GMT  
		Size: 2.4 MB (2355804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b33c31d028b74fe4b5dc6cac1b2c3bf823a340b96c911f305cf063ca5c052c`  
		Last Modified: Fri, 16 Feb 2024 08:08:02 GMT  
		Size: 58.8 MB (58820691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
