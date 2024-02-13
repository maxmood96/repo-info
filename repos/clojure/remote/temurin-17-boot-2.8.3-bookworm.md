## `clojure:temurin-17-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:f454dc31bf7143d6cd174dced392e64f5012797f5de8e284d9a7f3abebc19036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7901cbeb1a9b0f3ec5a1b0cec5bd743aea0c5e0fa261762c15be3ce1f865788c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258793629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4273ed059eae9a8a8e19c628c0d0734304858e3b12427a37de5210cab06d182`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:58:26 GMT
COPY dir:2765b9c6732dde1d622a6314ea7119038a6031d832e1ec655de4889b7fd05a2e in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:58:27 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 01:58:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 01:58:28 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:58:34 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 01:58:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 01:58:34 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 01:58:52 GMT
RUN boot
# Tue, 13 Feb 2024 01:58:52 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 01:58:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 01:58:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2b2416bddbb63a5143aa0f8648683db64ee3be3e1734dd6322b14594ad178f`  
		Last Modified: Tue, 13 Feb 2024 02:16:23 GMT  
		Size: 144.9 MB (144893174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3350ba0d6961efdbad3aad46029bb46fff76fd112f4d380eab84eff778a9add`  
		Last Modified: Tue, 13 Feb 2024 02:16:12 GMT  
		Size: 5.5 MB (5527081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7044eeacac9f2e4f978c7de9be6d38bdceac027d84cdc3049746f296e3c01d6b`  
		Last Modified: Tue, 13 Feb 2024 02:16:15 GMT  
		Size: 58.8 MB (58820369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1b8763cc63a10546be1396b17c05dd56184d2718c66d8c5f738d70b82c5a6c`  
		Last Modified: Tue, 13 Feb 2024 02:16:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:274388da786032ee8f15ff3dc675f05d0432531de8a9d27a65521fd4e48bae61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257482231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a7748e0efe4aefcd2bb638bc1902540eb40428f3abef8c9bda8ee3bf8a48f3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:04:30 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:04:34 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Feb 2024 02:04:34 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 02:04:34 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:04:39 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Feb 2024 02:04:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 02:04:39 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Feb 2024 02:04:57 GMT
RUN boot
# Tue, 13 Feb 2024 02:04:57 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:04:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:04:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26243f51786db2e7088b824a2ea36718e48c26cd4fa4cb18d5b3c2d53b067358`  
		Last Modified: Tue, 13 Feb 2024 02:20:34 GMT  
		Size: 143.7 MB (143720886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0703dd56654d5f93851f7cdc6603175a3211572b3b0faf806657f038dcdae012`  
		Last Modified: Tue, 13 Feb 2024 02:20:25 GMT  
		Size: 5.3 MB (5349390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f85dc568386d619b9abbeefb1b63ed45f60f40736e603350e9369871ec23816`  
		Last Modified: Tue, 13 Feb 2024 02:20:28 GMT  
		Size: 58.8 MB (58820593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70b59fc148de9eebb86127a5d30c33f89258a51f581b403df861e9814465b34`  
		Last Modified: Tue, 13 Feb 2024 02:20:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
