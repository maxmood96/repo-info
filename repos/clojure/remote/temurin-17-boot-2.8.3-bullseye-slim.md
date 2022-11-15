## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:ff1709322f6351e96cebfe5951e29d7fa63f0afe34e9b7c3246e87dec03bcea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5be6cbdff2ed9f382ef961f1555ef60c66acb4ada4a4d82c65b756eab903cc44
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283743899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3213ac99ff541a4dac1bcb2c1526793ddbdd24dfd984cd5233da1494211eed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:05:21 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Tue, 15 Nov 2022 17:57:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 17:57:46 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 15 Nov 2022 17:57:46 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 17:57:46 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 17:57:52 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 15 Nov 2022 17:57:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 17:57:52 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 15 Nov 2022 17:58:13 GMT
RUN boot
# Tue, 15 Nov 2022 17:58:13 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 15 Nov 2022 17:58:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 15 Nov 2022 17:58:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e2f15985394be21a4e4a010fbea73bcb4ac9c162a40582171119a45451824`  
		Last Modified: Tue, 15 Nov 2022 13:08:12 GMT  
		Size: 192.4 MB (192431277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719b6df3ba7b60afdb41abd77d4057072c67d557f32b0668de4d952c5c45aba1`  
		Last Modified: Tue, 15 Nov 2022 18:10:33 GMT  
		Size: 1.1 MB (1079025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d73691b61fcced909773e5a161fab9cfa0614e44b4cad42f1115c90932358e`  
		Last Modified: Tue, 15 Nov 2022 18:10:36 GMT  
		Size: 58.8 MB (58820570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de39c1ed90d0f907b98c199cc6499eb273c5188a2adbcb7b10a96eb4d5f88de4`  
		Last Modified: Tue, 15 Nov 2022 18:10:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:007b89247b8b1faa5a7c7d5731ac95694034e287f4936fe0ec13154fd0a2a0e8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281162984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80f35e39bc4a867d9ed103f6429d239d20140295775207256132181545d396f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:49:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:54:33 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:54:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:54:38 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 15 Nov 2022 05:54:38 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 05:54:38 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:54:42 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 15 Nov 2022 05:54:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 05:54:42 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 15 Nov 2022 05:54:59 GMT
RUN boot
# Tue, 15 Nov 2022 05:54:59 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 15 Nov 2022 05:54:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 15 Nov 2022 05:54:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0032fd948a5495fec37e26e9d086c7c0fa24d0623f43f8ad0471aac3350e5f61`  
		Last Modified: Tue, 15 Nov 2022 06:05:10 GMT  
		Size: 191.2 MB (191215234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd82123c314640caf9ef70a6ff9cbd22dbab52e98b8e3d189af14846e2c7dbf9`  
		Last Modified: Tue, 15 Nov 2022 06:04:59 GMT  
		Size: 1.1 MB (1066314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f662c395e477b14935738e6eaa21409f06fbe49b5563949f6acc552e7b84c4`  
		Last Modified: Tue, 15 Nov 2022 06:05:02 GMT  
		Size: 58.8 MB (58820433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12376f6ae0880f69c35b83c4c956bf256285e159ff7bd127fbb4c0e78584dd13`  
		Last Modified: Tue, 15 Nov 2022 06:04:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
