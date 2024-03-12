## `clojure:temurin-8-boot-bullseye`

```console
$ docker pull clojure@sha256:cba70ee7f9b0da0a84bb72437b65c5232910791c7e12d4f1b7f106de913466b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:71a57afc195dff9e500c67aa04a3d90e8fe06f5719fa00164899916cdcd50ace
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219864705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f461a111066d3382457b6505ea01e199e9e4086cb798abd649776eaa3421267c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:11 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 12 Mar 2024 01:21:11 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 06:12:20 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Tue, 12 Mar 2024 06:12:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 06:12:21 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 06:12:21 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 06:12:21 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 06:12:27 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 06:12:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 06:12:27 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 06:12:46 GMT
RUN boot
# Tue, 12 Mar 2024 06:12:46 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6509d111e3d98c6926d5d0b8f8737955729a08a3305b0fb32251c8c04161be08`  
		Last Modified: Tue, 12 Mar 2024 06:34:52 GMT  
		Size: 103.6 MB (103591879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb3e7fbc64b06a5ed0f5ef286126a8e3e5bd7fc240f137d71ddaa54c7d40f1a`  
		Last Modified: Tue, 12 Mar 2024 06:34:44 GMT  
		Size: 2.4 MB (2367291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef5b08dc85bb8f3983ce2edb2c81600e3878cec3120729d9a8e627fc61eefa4`  
		Last Modified: Tue, 12 Mar 2024 06:34:48 GMT  
		Size: 58.8 MB (58820566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1013084f8779063e2f038b5182f1b700c06bec345b2c4138e05812b4e6c820b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217601417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f64b22a6525907cd209e7565bc9f303093c4a77c3237213fdfbbd03ea70292`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 01:44:39 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Tue, 12 Mar 2024 01:44:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 01:44:41 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 01:44:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 01:44:41 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 01:44:46 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 01:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 01:44:47 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 01:45:06 GMT
RUN boot
# Tue, 12 Mar 2024 01:45:06 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc111036e49950ea928d1514e89b3d66d1be636c914761d76aac3168d944166`  
		Last Modified: Tue, 12 Mar 2024 02:03:12 GMT  
		Size: 102.7 MB (102703020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e98ad901830b62474c175a6ca72d15eefd67c19c639cdcbab0d6cb1fed3f51`  
		Last Modified: Tue, 12 Mar 2024 02:03:05 GMT  
		Size: 2.4 MB (2355773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c669be8ad7597f1c86ef43b41f763b15b2f5e03636399388c52a839fc83244`  
		Last Modified: Tue, 12 Mar 2024 02:03:08 GMT  
		Size: 58.8 MB (58820525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
