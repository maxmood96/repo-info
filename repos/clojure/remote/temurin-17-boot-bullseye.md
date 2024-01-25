## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:ff82d830e097cf60fbac0db29d16ccf18e426cc9d9b3a71c00447a4f0b8e0802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ea0cc6f272f32ee7aad68318a873c3ca68f40e65572d3fd673b1417adf54227c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261139600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a098d968db03c611194cb0eef7e0028f97110d377b02e857717bd1c5b80e9751`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:18:34 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:18:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:18:35 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:18:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:18:35 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:18:41 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:18:42 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:18:58 GMT
RUN boot
# Wed, 24 Jan 2024 22:18:58 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 24 Jan 2024 22:18:58 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jan 2024 22:18:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4bf5d96b49c211bade1ddaef953c1483674323e75b82e60d87009d59260f9fb`  
		Last Modified: Wed, 24 Jan 2024 22:42:34 GMT  
		Size: 144.9 MB (144892491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11215c2ade2f232e05f6c7ac63fe797f2851606f6931cea9bca3c74de04e526e`  
		Last Modified: Wed, 24 Jan 2024 22:42:23 GMT  
		Size: 2.4 MB (2368732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be58a863aea302e5d9606364c6bf403fb269aa54cedab3080e9d15aafa4dce97`  
		Last Modified: Wed, 24 Jan 2024 22:42:25 GMT  
		Size: 58.8 MB (58820253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab73f1b36a2260300752ecf14ae9bc6650a39a594897095e7d095777d9e1fcc`  
		Last Modified: Wed, 24 Jan 2024 22:42:22 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:feba61360007b03109adf40d10fcf0b48af4f768658474dbf207aaf6a3884e2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258607051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae677f8872c76b308141c2bb8156b87cf09c470526c21052814867598a8f49c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 08:00:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:21:37 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:21:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:21:41 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:21:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:21:41 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:21:46 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:21:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:21:46 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:22:01 GMT
RUN boot
# Wed, 24 Jan 2024 22:22:01 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 24 Jan 2024 22:22:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jan 2024 22:22:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f386e67e1668f87b7933f75c2901d37ecd3d8df2a7c9b8a37df606b4e9ce911`  
		Last Modified: Wed, 24 Jan 2024 22:41:59 GMT  
		Size: 143.7 MB (143720872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca992a946c9d564831911635a412b9c4c4de37f516bef67caddba5353ff0e898`  
		Last Modified: Wed, 24 Jan 2024 22:41:50 GMT  
		Size: 2.4 MB (2357489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909b43c36e09a4543f60e02bcf7fd5eeeb4aee56cd9c0319877ea7d48c6e21c4`  
		Last Modified: Wed, 24 Jan 2024 22:41:53 GMT  
		Size: 58.8 MB (58820443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1207ebcba6595776a244bc84b264d18f3c4a42dc9530c99d4c07520832796240`  
		Last Modified: Wed, 24 Jan 2024 22:41:49 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
