## `clojure:temurin-8-boot-bullseye`

```console
$ docker pull clojure@sha256:72b41154243c7e05392fd19a87db3ff2438c73f4f2a242c7b2e7faaab374e7a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye` - linux; amd64

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

### `clojure:temurin-8-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:557eb60c4a3ee8747a0405797745c8cb79f2f93133f6ebbef55e67a76221124a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217589223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089010530d1ee4add5336af7e0c51627d3994d7033c97fc0cb7782649dede6c6`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:20:40 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:20:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:20:42 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 01 Feb 2024 06:20:42 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 06:20:42 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:20:48 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 01 Feb 2024 06:20:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 06:20:48 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 01 Feb 2024 06:21:07 GMT
RUN boot
# Thu, 01 Feb 2024 06:21:07 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd92bb115e3bc72c588dcd8f8f7038498cebfb63f1a8dad90091554d6b14c21`  
		Last Modified: Thu, 01 Feb 2024 06:39:35 GMT  
		Size: 102.7 MB (102703041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2177cc184fa371c4676bbe403b1daeb9f2ff706b500611b3d1bbcadce6d9e3`  
		Last Modified: Thu, 01 Feb 2024 06:39:29 GMT  
		Size: 2.4 MB (2357402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b267734dfc79dd3d56b892036f1985f5cef96a9227fa548a1819d1a5086271a`  
		Last Modified: Thu, 01 Feb 2024 06:39:31 GMT  
		Size: 58.8 MB (58820513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
