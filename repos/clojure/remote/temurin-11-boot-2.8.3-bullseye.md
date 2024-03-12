## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:f7d5f27ad7ad3bbe58e0ee9956a4185d5abc320def20e7e1168f556e0faf88f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9787290f66d2bb293aa3b32bcca21a1f9bd64e870372e403dc3c6d352e424607
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261543814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48176fff4cee811dc2d4541c9209b8a45137410d994c30161121823546703bd`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 14:02:40 GMT
COPY dir:9807503b62b5ec57f5790350ba2323b4402a31264d57970336b28a606d7a3a68 in /opt/java/openjdk 
# Wed, 06 Mar 2024 14:02:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:02:41 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 14:02:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 14:02:41 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 14:02:49 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 14:02:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 14:02:49 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 14:03:09 GMT
RUN boot
# Wed, 06 Mar 2024 14:03:09 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee607ac86f3682133f1327bf9e4a5f8ae33688442179890807a04c59d80d532c`  
		Last Modified: Wed, 06 Mar 2024 14:23:37 GMT  
		Size: 145.3 MB (145271179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d16ace064c4338703ad233e100262a340b81e6a8b5026783fc5a735b81a3c5d`  
		Last Modified: Wed, 06 Mar 2024 14:23:25 GMT  
		Size: 2.4 MB (2367232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d983568cdc7759a4e30123aae9b9c20a2c9adf79852e29ff77842aca35b0f8cb`  
		Last Modified: Wed, 06 Mar 2024 14:23:29 GMT  
		Size: 58.8 MB (58820565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8803f9e627a95155fb22d23a84de103cfb532f08216975e17e34cdc0d79261c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256907056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95faac72e0449c3bba846387bf6f5901d2fb501d6f541a29e37eb915bb01f7c6`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 01:49:31 GMT
COPY dir:774c748cac67d918432726696917d770e1c557a90a62f56899a68f5b5861f304 in /opt/java/openjdk 
# Tue, 12 Mar 2024 01:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 01:49:34 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 01:49:34 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 01:49:34 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 01:49:39 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 01:49:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 01:49:39 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 01:49:57 GMT
RUN boot
# Tue, 12 Mar 2024 01:49:57 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d692135343f579bdc57767c8f81a05016412095194fd32989b78ccc8b60e927e`  
		Last Modified: Tue, 12 Mar 2024 02:06:17 GMT  
		Size: 142.0 MB (142008479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88dcb6152208b63f342b55f6cc0d7dc63e801873a968a908abab9699f1fa3853`  
		Last Modified: Tue, 12 Mar 2024 02:06:09 GMT  
		Size: 2.4 MB (2355725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5499c066df7b024df86397cbcbbff1a5ac4e976df05610224368c764a4f7b608`  
		Last Modified: Tue, 12 Mar 2024 02:06:11 GMT  
		Size: 58.8 MB (58820753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
