## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:1bdc3ca867dba68f36aa335eddb05992a84eb2d866dc29bc08b9dad39b76355f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:05c7475d49a6a59b4c2a6a161f8d5fab9e1c401fd71fafe7a9fabac870a2d35f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261166150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3a56b82ad74f4715a4677a8952800e6619d91e2271f467412e173ccafa3666`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:59:34 GMT
COPY dir:2765b9c6732dde1d622a6314ea7119038a6031d832e1ec655de4889b7fd05a2e in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:59:35 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 01:59:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 01:59:36 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:59:41 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 01:59:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 01:59:41 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 01:59:59 GMT
RUN boot
# Tue, 13 Feb 2024 02:00:00 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:00:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:00:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7038720c6253652e061d4b6f774aaf3955e68140b3088439919b8db57fbd91`  
		Last Modified: Tue, 13 Feb 2024 02:17:09 GMT  
		Size: 144.9 MB (144893168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d457e20d7ffca82e792ae1f3aa1c21f9b698c02555a41ace7824c312827bbf1`  
		Last Modified: Tue, 13 Feb 2024 02:16:58 GMT  
		Size: 2.4 MB (2367236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34102f8e33cd2def8eae8c4716d25b3fdbba313bc57780cc1fe76a0e0a18ee93`  
		Last Modified: Tue, 13 Feb 2024 02:17:01 GMT  
		Size: 58.8 MB (58820509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b461e0c621b7301eb87e7fbe75eaf326935159dc6bea94f6d0bd0700fcbff52`  
		Last Modified: Tue, 13 Feb 2024 02:16:57 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:53563b0e6d02b564ebe23156d6d3ed44bd4d8608b055ef3fc8701675d48bd5a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258618982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee8cc1def97537936bf13ef29927029c5e8fd39d802063379a7774f61e31c61`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:05:36 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:05:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:05:39 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 02:05:39 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 02:05:40 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:05:44 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 02:05:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 02:05:45 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 02:06:01 GMT
RUN boot
# Tue, 13 Feb 2024 02:06:01 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:06:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:06:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b93abada80d7a4cca39f20b2fb149ebf7e2868c862d216131fb6c28cc287e7`  
		Last Modified: Tue, 13 Feb 2024 02:21:10 GMT  
		Size: 143.7 MB (143720884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2ec2c2c63d8048964bfaedae65b44bf02ce09599184abc894ec53294fc8ac0`  
		Last Modified: Tue, 13 Feb 2024 02:21:01 GMT  
		Size: 2.4 MB (2355782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d50f41954c30ba61b08c94e980cac35f4538d8f3f8b8834f23bd5b71bb4c203`  
		Last Modified: Tue, 13 Feb 2024 02:21:04 GMT  
		Size: 58.8 MB (58820431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9954c933941db6bedd1a25b0c09a2d718adc581178d971abb564e840344a57`  
		Last Modified: Tue, 13 Feb 2024 02:21:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
