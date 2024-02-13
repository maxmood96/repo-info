## `clojure:temurin-8-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:76c5380df1db9a29f06341ca3be79fd09f01c081b2a2ecaee6d4039e53a8bea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c0e33a9885684d74bc8b310cfe0fcc0bba2943cced44e501139676b31836541e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (195034682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7de0ce63d4c6987e0810f55a861452a8460b1ce08a6d4404051a847117e81f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:47:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:47:31 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:47:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:47:32 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 01:47:32 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 01:47:32 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:47:39 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 01:47:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 01:47:39 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 01:47:58 GMT
RUN boot
# Tue, 13 Feb 2024 01:47:58 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e1a9cbed5cc87e9380774cdf6c1211d2a3f6e261065440396d798b85e10c29`  
		Last Modified: Tue, 13 Feb 2024 02:09:40 GMT  
		Size: 103.6 MB (103591878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b8eba3750f982d6d856041374a351b737ba23e3867910aab409121368ca618`  
		Last Modified: Tue, 13 Feb 2024 02:09:33 GMT  
		Size: 3.5 MB (3498212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48995acffabb7d26d475d8e83aaad26fb0922fe4689bd4ad9c69fb2993bfa4c8`  
		Last Modified: Tue, 13 Feb 2024 02:09:35 GMT  
		Size: 58.8 MB (58820501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5796b1b825681370eb98cc713f274b33fa94ce1e009d0ba5d69355f148cf6944
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194002128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40bae3f0f722d28803ffa88d12371c3c2119926ef1acf3980c0a75cd8c84e61e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:55:02 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:55:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:55:05 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 01:55:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 01:55:05 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:55:10 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 01:55:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 01:55:10 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 01:55:28 GMT
RUN boot
# Tue, 13 Feb 2024 01:55:28 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d8cf35b6ab4ec7d12cf1c238b357320865b8bbeafb18d87da48bf11d86da22`  
		Last Modified: Tue, 13 Feb 2024 02:14:05 GMT  
		Size: 102.7 MB (102703044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad4f2fff22b8b0c94f119904ae4db6ed69b603eccc6a655ff910df16124c890`  
		Last Modified: Tue, 13 Feb 2024 02:13:58 GMT  
		Size: 3.3 MB (3322144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f9978f7d991f5d26eb4afda7481ee7ea30004361529461c9b6d94f62a65ec0e`  
		Last Modified: Tue, 13 Feb 2024 02:14:01 GMT  
		Size: 58.8 MB (58820577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
