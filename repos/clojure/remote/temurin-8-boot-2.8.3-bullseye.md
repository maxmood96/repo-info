## `clojure:temurin-8-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:2b8390cf2532d285477e734ce08047ff72b22e65e53e2f160c9f4d789033d225
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
