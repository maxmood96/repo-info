## `clojure:temurin-8-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:52320773023c16b478181bb44f7241748f00942b92f6d5b949470673d89bb3dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:15bdc032558acd1f76bf675d1f79556c397133a60515ee59054e39684f4dd604
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219864477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe9ea51d7f4abd5a0b1afe70941abd9578ede8d89efea5d87c2879b81cbeb3d`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:48:06 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:48:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:48:07 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 01:48:07 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 01:48:07 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:48:13 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 01:48:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 01:48:13 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 01:48:32 GMT
RUN boot
# Tue, 13 Feb 2024 01:48:33 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a05fe09067b798061f2f5ff13d43b55c21280d92138631ea76436b0d3bb4b93`  
		Last Modified: Tue, 13 Feb 2024 02:09:59 GMT  
		Size: 103.6 MB (103591878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a728c6a80fc49b01796f30a440e3a28d73b3923d6ba1b08381a31a3ec99eb54e`  
		Last Modified: Tue, 13 Feb 2024 02:09:51 GMT  
		Size: 2.4 MB (2367250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3e16d207d3e9b4b57b60b4911fc728d521e6a3a5892f62acf233402518d4c6`  
		Last Modified: Tue, 13 Feb 2024 02:09:53 GMT  
		Size: 58.8 MB (58820511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a46a40a90984e03afdcfa05138b247f0ff0e3d63fbcf83839d8fc45d74ad3781
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217600688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc865ab955fee77b89532512a0b13ea8159feaa257e3cf72fef9e51b6d2c6d36`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:55:36 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:55:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:55:38 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 01:55:38 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 01:55:38 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:55:43 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 01:55:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 01:55:43 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 01:56:02 GMT
RUN boot
# Tue, 13 Feb 2024 01:56:02 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d68b1bf2f42bce59bf4decb76d0f247ec7fed28033d5cde59aeadda6872a1c`  
		Last Modified: Tue, 13 Feb 2024 02:14:20 GMT  
		Size: 102.7 MB (102703018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f7190d5059066cfb7bbd2ca664717485a5c72a75c699d7c7b9ae27dded4fe4`  
		Last Modified: Tue, 13 Feb 2024 02:14:13 GMT  
		Size: 2.4 MB (2355773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efb5f2f84bd70313ff204d9b47812542a887532095d9a51e8d1aaa5af30e62a`  
		Last Modified: Tue, 13 Feb 2024 02:14:16 GMT  
		Size: 58.8 MB (58820411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
