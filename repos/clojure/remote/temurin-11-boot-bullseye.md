## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:f026dd1f83e0e7128bef859d2315086c4715dd43f3470b12e54875169420b952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

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

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e5b629c2fd3fa5e611a6ab79bdb3f2734af099433ad4deffbcc1aea3fba86d03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256906147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802c8c9af2d42a774f846f99fb555834f45469d2615aaf34899beb43a415ad16`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 13:16:46 GMT
COPY dir:774c748cac67d918432726696917d770e1c557a90a62f56899a68f5b5861f304 in /opt/java/openjdk 
# Wed, 06 Mar 2024 13:16:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 13:16:49 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 13:16:49 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 13:16:50 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 13:16:56 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 13:16:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 13:16:56 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 13:17:13 GMT
RUN boot
# Wed, 06 Mar 2024 13:17:13 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e0bf71df1188cd41163f875af3276d9ef7c286956d5d098df4a283431a3020`  
		Last Modified: Wed, 06 Mar 2024 13:34:10 GMT  
		Size: 142.0 MB (142008467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84a79907e533b752d6729c9563177676a9be301ec6402e794fb68155a582218`  
		Last Modified: Wed, 06 Mar 2024 13:34:01 GMT  
		Size: 2.4 MB (2355846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3544b3d61515495396a3b606f6e2bb71e565050913c83182fad6498975df8b8d`  
		Last Modified: Wed, 06 Mar 2024 13:34:04 GMT  
		Size: 58.8 MB (58820348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
