## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:34e710763a87114321ca462b4e6cee29f435396e3302465b11e5be21a01a5bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9ec6aa9f0fd6d080df6e83d7f1dcad78942dc09ad698b302273f2c33b61eb5e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261071132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7020ded373b5750421614bb43c857a0d3fd14af9cff0544e064e24c45ae5c1fd`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:57 GMT
ADD file:20f89ff93bfbd6c9fb1a97058a1f3de4485a8974e8a83892072c511fbd2e4134 in / 
# Wed, 16 Aug 2023 00:59:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 18:04:32 GMT
COPY dir:72d046f3e284b8eca8066a837ab8a68f91b4cf5355de7f6803a8ee9b7ce3d682 in /opt/java/openjdk 
# Wed, 16 Aug 2023 18:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 18:04:34 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 16 Aug 2023 18:04:34 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 16 Aug 2023 18:04:34 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 18:04:40 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 16 Aug 2023 18:04:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 16 Aug 2023 18:04:40 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 16 Aug 2023 18:05:00 GMT
RUN boot
# Wed, 16 Aug 2023 18:05:00 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:6a70103cc499a199e10e379794c60aa524d9598587cc2bdfe2995642c2da8df7`  
		Last Modified: Wed, 16 Aug 2023 01:04:50 GMT  
		Size: 55.1 MB (55056621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802f7c61301eef1eb08be64b58b246c8d0994f99e572b694d6cd34c52442c978`  
		Last Modified: Wed, 16 Aug 2023 18:15:30 GMT  
		Size: 144.8 MB (144831648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479b28809ed0340065e641f6dcc0ddb935a9dc9366b74e41f286f8aeac030d85`  
		Last Modified: Wed, 16 Aug 2023 18:15:19 GMT  
		Size: 2.4 MB (2362163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3d4b03292749b775267aa46f0781d6ca420f0352dafffb2af0d60810418b34`  
		Last Modified: Wed, 16 Aug 2023 18:15:23 GMT  
		Size: 58.8 MB (58820700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2840d090921648bf8e1fdd028d371fd69dbb8418918cd2d30264154e684354f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256442050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f62ce9df5c0b6a3fc6db81f319f82f763fc8310c3f3d431d1c6ea602ce90549`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:21:45 GMT
COPY dir:6acc55ac013a722a8db4af8f0ce8de9270cd9aeb372e6c734b449d15adcc5218 in /opt/java/openjdk 
# Wed, 16 Aug 2023 17:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 17:21:49 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 16 Aug 2023 17:21:49 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 16 Aug 2023 17:21:49 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 17:21:55 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 16 Aug 2023 17:21:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 16 Aug 2023 17:21:55 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 16 Aug 2023 17:22:14 GMT
RUN boot
# Wed, 16 Aug 2023 17:22:14 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175ec2cb09b3952032a7dbf0cdc9f641b1c5035ea846b712b44240d849a2979f`  
		Last Modified: Wed, 16 Aug 2023 17:31:34 GMT  
		Size: 141.6 MB (141565216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfd7675a9c3b06328335936000a3057d2d514992f3b36b9efc0b53b946322b2`  
		Last Modified: Wed, 16 Aug 2023 17:31:25 GMT  
		Size: 2.4 MB (2351376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f3283b47edb3205a492de536e949c7b3eacfa102e07497a7245328efe4ec7d`  
		Last Modified: Wed, 16 Aug 2023 17:31:29 GMT  
		Size: 58.8 MB (58820679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
