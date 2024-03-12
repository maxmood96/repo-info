## `clojure:temurin-17-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:94dce9dc088cf0da5c05b8c9267aed60b91b6c0d18978714e72dbff9ee6d6289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7b7d373cf25a5759133c7ef9fd3f126c8a4b4f8018fde46ac6b90e46be112f5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236336250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6136644dbe3192f3d8f031d312cf494d7aa67ee451cf394f0003d907c1fd6065`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:11:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 06:23:06 GMT
COPY dir:3be96ae7faea81e90455993c99b71c9b45986c7e71f70fc577ab97699c92b508 in /opt/java/openjdk 
# Tue, 12 Mar 2024 06:23:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 06:23:07 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 06:23:07 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 06:23:07 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 06:23:13 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 06:23:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 06:23:14 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 06:23:31 GMT
RUN boot
# Tue, 12 Mar 2024 06:23:31 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 12 Mar 2024 06:23:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 12 Mar 2024 06:23:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdab3494cdaf5946d15fe4624cb49b52470aafe67e35adf4bcaeef7a1db50f8`  
		Last Modified: Tue, 12 Mar 2024 06:40:51 GMT  
		Size: 144.9 MB (144893191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a1597534a1271109beffae6fefbffd7f1957c4c9b6c6a6af84bb4e3239a604`  
		Last Modified: Tue, 12 Mar 2024 06:40:41 GMT  
		Size: 3.5 MB (3498163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ee005d6c283e9c3061ed33ea7dca0d099c1a6d213bc74091c1ab877bd891d8`  
		Last Modified: Tue, 12 Mar 2024 06:40:43 GMT  
		Size: 58.8 MB (58820317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4066822990b8894ccf62358405b26e08d3f35361c2de23bf8dcf3a2ca4700f`  
		Last Modified: Tue, 12 Mar 2024 06:40:40 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:609db4795898a81584570227410ca8a9b248547c37f3d49a1e50504ca8df7093
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235020452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4554058dda5dad05f98ea0901fac4b9b49b810f2ed65f95f54455c3443004ecc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 01:53:54 GMT
COPY dir:4a8c697909e89d854b955537d3c80fbcec33336dd00fb9805f3c0a9edf3861db in /opt/java/openjdk 
# Tue, 12 Mar 2024 01:53:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 01:53:58 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 01:53:58 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 01:53:58 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 01:54:03 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 01:54:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 01:54:03 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 01:54:20 GMT
RUN boot
# Tue, 12 Mar 2024 01:54:21 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 12 Mar 2024 01:54:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 12 Mar 2024 01:54:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc56412027ee59e7ee15cd13a8ab482381595108513644a75ffc9f30cd96cf7`  
		Last Modified: Tue, 12 Mar 2024 02:09:01 GMT  
		Size: 143.7 MB (143720928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0842ba81f9e69a761ad47903886e7ac56ab3068441e0a83fad72b2222c21b7a2`  
		Last Modified: Tue, 12 Mar 2024 02:08:52 GMT  
		Size: 3.3 MB (3322111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7504ab80642f8b9212b8452dedbcf0737d5204542737c631e138852d53c6a4d8`  
		Last Modified: Tue, 12 Mar 2024 02:08:54 GMT  
		Size: 58.8 MB (58820580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6378f5b1c21efaea889f2e9252865654472c312fe1896d46083bf7400e4f1f`  
		Last Modified: Tue, 12 Mar 2024 02:08:51 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
