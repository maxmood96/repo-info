## `clojure:temurin-8-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:217abdaeb30c320958bd96cdaba44b64d1903aa50f64eeb6ddd8ed82acaec0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bookworm` - linux; amd64

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

### `clojure:temurin-8-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9dae1c0a21dac39db75bfd81127bf0314b7dfb91a621fac3336acb8530554975
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216464015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5540754e8d00e7d78feeb14bd77d13097c06f7c393d1c8c96d4b75fb0720f45a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:54:30 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:54:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:54:32 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 01:54:32 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 01:54:32 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:54:38 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 01:54:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 01:54:38 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 01:54:57 GMT
RUN boot
# Tue, 13 Feb 2024 01:54:57 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2d4e3ded6ddd5ff92452771ec0295a8a94998dcf58890b6cbe30fea243fb95`  
		Last Modified: Tue, 13 Feb 2024 02:13:49 GMT  
		Size: 102.7 MB (102703043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5aa94285c8bc99d84af7db2772509f5dde7d8341e173448bb457ff0e7ced3ec`  
		Last Modified: Tue, 13 Feb 2024 02:13:42 GMT  
		Size: 5.3 MB (5349428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6544f55049d3ac7335b4a026d9d582a9af83aad230281fca076be27598919bbf`  
		Last Modified: Tue, 13 Feb 2024 02:13:44 GMT  
		Size: 58.8 MB (58820579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
