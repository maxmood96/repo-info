## `clojure:temurin-8-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:844adb1f3f19c8a1c3266f6cf61ccd924308fa36304f13095daa850909558c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d3221ea4da03d14ab81ddfd779a44a33e93b636af84acbafdcc297cf35ea68d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219838125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d237fd82ab28368710d86a845155c9d5f7605d5d3f1ecd5823e17f5a1f7d5b`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:44:01 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:44:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:44:02 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:44:02 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:44:02 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:44:08 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:44:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:44:08 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:44:27 GMT
RUN boot
# Wed, 31 Jan 2024 23:44:27 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500d15a4f25ce821641fe8d270f770fe1b9b8e9269c49b164d7ef1c7db3dddde`  
		Last Modified: Thu, 01 Feb 2024 00:05:47 GMT  
		Size: 103.6 MB (103591895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6be1c1e5f94d044d747f02b6295a37773d94b9cf09410e0217ee65070452de`  
		Last Modified: Thu, 01 Feb 2024 00:05:39 GMT  
		Size: 2.4 MB (2368751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc2614c3aff116fd135f2c3baf8ff2ddd0f2214ea21c0c83125293cead675df`  
		Last Modified: Thu, 01 Feb 2024 00:05:42 GMT  
		Size: 58.8 MB (58820516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:658bc223560faf01d19485b5ebcac70db2f7c5fcbed78119f5d8bfb88c20d1c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217588778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cd9dbaad11e869edf1519e5f8daa5020f5b3635b40fbee98b9d4dbe90e68d1`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:00:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:07:41 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:07:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:07:43 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:07:43 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:07:44 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:07:49 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:07:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:07:49 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:08:05 GMT
RUN boot
# Wed, 24 Jan 2024 22:08:05 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519231c3e78c50a52cebbf1587bc354f0818d8934ef2453de9dce3979beff28f`  
		Last Modified: Wed, 24 Jan 2024 22:32:40 GMT  
		Size: 102.7 MB (102703032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9539b9bef8850475174b55253efcff00723a711151f269fbaf610182b23799aa`  
		Last Modified: Wed, 24 Jan 2024 22:32:34 GMT  
		Size: 2.4 MB (2357476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4155096bf5ed5105add0b1339f1cefe5e65032c3a6002b3c2192a246556f5b`  
		Last Modified: Wed, 24 Jan 2024 22:32:37 GMT  
		Size: 58.8 MB (58820423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
