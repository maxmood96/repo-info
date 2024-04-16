## `clojure:temurin-11-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:7b0fb472fe6e3531d89a95e1329bcfd8bb182050f157813aa8097d8d740e95b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4ed4e7ba64a924de0471cabad9039f7bd33fb0218ae74330a0accce2d790382a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259179085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5448e290b78a6c718b97325ae7b02bb8962449242fac2deffcf60078e02b751f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:16:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 10:54:44 GMT
COPY dir:daac410d49a992b5ee309816020a7ba772f8c0edbe3557815c30b5c2d8f8820a in /opt/java/openjdk 
# Tue, 16 Apr 2024 10:54:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 10:54:45 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 16 Apr 2024 10:54:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 16 Apr 2024 10:54:45 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 10:54:53 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 16 Apr 2024 10:54:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Apr 2024 10:54:54 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 16 Apr 2024 10:55:13 GMT
RUN boot
# Tue, 16 Apr 2024 10:55:13 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0244ce4938d8394376413762e06d05ca1857940950519a989eecd73ca7ba467f`  
		Last Modified: Tue, 16 Apr 2024 11:16:45 GMT  
		Size: 145.3 MB (145271008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d0cd945565ab7f6eada6edbefd197b58427efcbf5ce05bdce48a72c4817dc1`  
		Last Modified: Tue, 16 Apr 2024 11:16:34 GMT  
		Size: 5.5 MB (5527236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6c97c6a7bd014d4f17db0dffc0950234ec673e4280d8111c4c33b14803b7e4`  
		Last Modified: Tue, 16 Apr 2024 11:16:37 GMT  
		Size: 58.8 MB (58820481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:297c13208951a6bba594f9fa49b174a39f6e908bc294ab337d04e784bca603e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255772557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3961fb5febb3d15261981dafa0df3185a29e282182a96e972a5bd3ee2390af`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:37:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 06:32:39 GMT
COPY dir:337eb37873e2fe424b3d62c18ff2640cf50898156a884981e9e10924759441c3 in /opt/java/openjdk 
# Tue, 16 Apr 2024 06:32:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 06:32:42 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 16 Apr 2024 06:32:42 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 16 Apr 2024 06:32:43 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:32:49 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 16 Apr 2024 06:32:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Apr 2024 06:32:50 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 16 Apr 2024 06:33:07 GMT
RUN boot
# Tue, 16 Apr 2024 06:33:07 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc51715a24a46140347f8e42a20868b5d5df2b6fc903958ad67dda303c34ee6`  
		Last Modified: Tue, 16 Apr 2024 06:52:13 GMT  
		Size: 142.0 MB (142006321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7f58c376daba620ae0b4ae33a76a5b161092d303d6163edb4695a7a962a7bc`  
		Last Modified: Tue, 16 Apr 2024 06:52:05 GMT  
		Size: 5.3 MB (5349519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901300a64318a84dd3ed67110f33b647247f725f677ea8aeced62eb9534baa2f`  
		Last Modified: Tue, 16 Apr 2024 06:52:07 GMT  
		Size: 58.8 MB (58820452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
