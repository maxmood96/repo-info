## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:84288739f746678887642009ba7a828ef46241fc3e9dbb928db67210f8ac0c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:cd8a35b6c95227f4ca79bc36a85626aac5801fc3902ea5c0ba3184ef59c011a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261513452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2fb396285fdb3e7bb5d079fbc5551b7fad23fbb10c480cfc56ee36af03e791`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 14:13:19 GMT
COPY dir:c80966d54ee599fa5b16f964e9342a0dab00f0ed4f5d18b7bebc8a71278b8b40 in /opt/java/openjdk 
# Wed, 17 Jan 2024 14:13:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 14:13:20 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 17 Jan 2024 14:13:20 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 17 Jan 2024 14:13:20 GMT
WORKDIR /tmp
# Wed, 17 Jan 2024 14:13:27 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 17 Jan 2024 14:13:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jan 2024 14:13:27 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 17 Jan 2024 14:13:46 GMT
RUN boot
# Wed, 17 Jan 2024 14:13:47 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ac175da1b9b628db28e4e12e9b90c12de8324b914a482fbe71788fb27c22e1`  
		Last Modified: Wed, 17 Jan 2024 14:49:42 GMT  
		Size: 145.3 MB (145266471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dee73baae73dfcd6a07e7712acc9dc000d5877c437a0e76622d62b58d6afe5`  
		Last Modified: Wed, 17 Jan 2024 14:49:31 GMT  
		Size: 2.4 MB (2368774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad14162a1b99fe7bf34987c3254a66d9e5ae5823099e5aebd3a0b2abda10139d`  
		Last Modified: Wed, 17 Jan 2024 14:49:34 GMT  
		Size: 58.8 MB (58820484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e2ec6bd026ff83ab77b80586dba5aea0af8c70309394325ee9f261fb39b37308
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256887733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f1ee2ea325cb250c5d5471fe6110cf100ccb73c4162ef4fd67929c5856e1c6`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:00:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:23:25 GMT
COPY dir:de5568efb2f4de409b0bbafecabebfd7b12106c4b1a8ded40ebb723247056709 in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:23:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:23:28 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 17 Jan 2024 09:23:28 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 17 Jan 2024 09:23:28 GMT
WORKDIR /tmp
# Wed, 17 Jan 2024 09:23:33 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 17 Jan 2024 09:23:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jan 2024 09:23:34 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 17 Jan 2024 09:23:51 GMT
RUN boot
# Wed, 17 Jan 2024 09:23:51 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25597194bb48f15c10f255c31d5eb54b9c2f17e3873288cbacf71f9289c10a90`  
		Last Modified: Wed, 17 Jan 2024 09:38:51 GMT  
		Size: 142.0 MB (142002057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d72639153d860d27b61582bd718970e44789e0b05b74560fa420ddf1df94771`  
		Last Modified: Wed, 17 Jan 2024 09:38:42 GMT  
		Size: 2.4 MB (2357382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f987eabe6e00f88f01424451db49c79160725e0a0f5975f7fbce2cbc024454`  
		Last Modified: Wed, 17 Jan 2024 09:38:45 GMT  
		Size: 58.8 MB (58820447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
