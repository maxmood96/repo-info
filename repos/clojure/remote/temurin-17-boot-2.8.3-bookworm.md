## `clojure:temurin-17-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:a70a70ef168e3d01f5fd01e07ddac51e0c759524fa12cfae49e1058b22aa7bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:2626ca93ce8dea52a2e5ce0ace373e77c72f154891e3a03c3a8c9971da13a5ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258793786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f80dd7dd69034c423b8d6bb8dafaff6fc009baf2bd2da6a25690a3dbf7cf147`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 14:09:55 GMT
COPY dir:3be96ae7faea81e90455993c99b71c9b45986c7e71f70fc577ab97699c92b508 in /opt/java/openjdk 
# Wed, 06 Mar 2024 14:09:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:09:56 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 14:09:57 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 14:09:57 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 14:10:04 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 14:10:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 14:10:04 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 14:10:24 GMT
RUN boot
# Wed, 06 Mar 2024 14:10:25 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 14:10:25 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 14:10:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16509130f52dbe6d465329f39db40d29a6c2c14281e633450baff6de75121859`  
		Last Modified: Wed, 06 Mar 2024 14:28:11 GMT  
		Size: 144.9 MB (144893104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c14849b23f9db43fc95aa23f3f0277e5a6374746f72c350bba0da6c21c48abb`  
		Last Modified: Wed, 06 Mar 2024 14:28:00 GMT  
		Size: 5.5 MB (5527203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d83f5107ffae2406a3101cedea5d23e44551d7cbf663455d149b9c4c6fc487`  
		Last Modified: Wed, 06 Mar 2024 14:28:02 GMT  
		Size: 58.8 MB (58820474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd9fa4b06c932a45000534d7e73ecb6b9fc5ddd2d7b27a81e98033d6e6d4597`  
		Last Modified: Wed, 06 Mar 2024 14:27:59 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2facaa2d403fa7f3081edc8ccc18318d71709226838b3bf6b4ac9675ad4765a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257482009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a08b7f0a7a5d18bda19d3bda926399cb078821c9145a8f4b187a77d2550e39`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 13:22:48 GMT
COPY dir:4a8c697909e89d854b955537d3c80fbcec33336dd00fb9805f3c0a9edf3861db in /opt/java/openjdk 
# Wed, 06 Mar 2024 13:22:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 13:22:52 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 13:22:52 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 13:22:52 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 13:22:58 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 13:22:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 13:22:58 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 13:23:14 GMT
RUN boot
# Wed, 06 Mar 2024 13:23:14 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 13:23:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 13:23:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd9e4d0e4feed501f9183f335a260b7c3ffdfd6dc1fd1de88bd150909f9355e`  
		Last Modified: Wed, 06 Mar 2024 13:37:56 GMT  
		Size: 143.7 MB (143720890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f68adce7335fa788a5d1514542f455a59a78f2c43eb0a93e8d3602d6fbb4164`  
		Last Modified: Wed, 06 Mar 2024 13:37:48 GMT  
		Size: 5.3 MB (5349514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75abcd4390f6fa49452f58d2bd4d1e0818029a15176e775a37d4176820a96c04`  
		Last Modified: Wed, 06 Mar 2024 13:37:50 GMT  
		Size: 58.8 MB (58820239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7b382ddb7313d83bef8e859d96dad141ef44f85375252a8e7a2d7b4372114f`  
		Last Modified: Wed, 06 Mar 2024 13:37:47 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
