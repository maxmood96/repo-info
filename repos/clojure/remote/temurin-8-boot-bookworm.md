## `clojure:temurin-8-boot-bookworm`

```console
$ docker pull clojure@sha256:f7371b5d4a94ec1ec9685a79dba0073bd5338b6625816585aec41b6e05a895be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b4cd341ea38b098b1d8db315904fe318e6d8c23cd7167f91269d68671978ebf9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217492238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99d923c8d08e2ee19a0b77adcb9a5a715afefb41dae0ef6016259eaf6f129d1`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:46:51 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:46:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:46:52 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 01:46:52 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 01:46:52 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:46:58 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 01:46:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 01:46:58 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 01:47:27 GMT
RUN boot
# Tue, 13 Feb 2024 01:47:27 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fa82103c6b10ff303cbdb75dd172bcb17a9cea1c3239cb231b5ac7cde39c33`  
		Last Modified: Tue, 13 Feb 2024 02:09:22 GMT  
		Size: 103.6 MB (103591911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c839cb54fc24c4e6e37aad84d26302f052be65e49dc4bc65e46a285bdcce88b`  
		Last Modified: Tue, 13 Feb 2024 02:09:15 GMT  
		Size: 5.5 MB (5527031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8a9a6f8fe12ead732fdb204b963b18e77da7cc23e773c7f316cac6484f5bfb`  
		Last Modified: Tue, 13 Feb 2024 02:09:17 GMT  
		Size: 58.8 MB (58820691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:559c2dc2c52f3d0b77428cd11ab7f07f9f632c8d36ffde538b9021949755031b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216464737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85350a330ed5cb3675fdb7c2845bdede55afbb27a366e1ec550c59069af9c00b`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:42:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 01:42:58 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Tue, 12 Mar 2024 01:42:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 01:42:59 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 01:43:00 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 01:43:00 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 01:43:05 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 01:43:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 01:43:05 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 01:43:58 GMT
RUN boot
# Tue, 12 Mar 2024 01:43:58 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1f067e69dadc5cc2c2ed5898b9d04f2ab2b78246ccfd096e8de3302a96c807`  
		Last Modified: Tue, 12 Mar 2024 02:02:41 GMT  
		Size: 102.7 MB (102703043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1264b2e4138fe82751939c065c595614d2e516a29eca22f88473bd2a2f461fbf`  
		Last Modified: Tue, 12 Mar 2024 02:02:35 GMT  
		Size: 5.3 MB (5349396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974a076573ef01bd12d41fc3ac6944f4819085fcf043386f8b5753d86228fd8e`  
		Last Modified: Tue, 12 Mar 2024 02:02:36 GMT  
		Size: 58.8 MB (58821314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
