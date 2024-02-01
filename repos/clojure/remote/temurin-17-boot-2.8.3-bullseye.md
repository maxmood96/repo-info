## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:084abbd494fbe286f4a4c2130786422851344d0c4a8224fca02778b54e8153d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:537df2c17f6c13b61d5a635a5f8a55bee0cb89bc3a15e33b50d5e5d35a8a0005
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261139161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50bd3a9d50f5c9d118ce082612be8f369cb4a50eb4af0d15dda1cd6a25ce82a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:55:09 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:55:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:55:10 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:55:10 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:55:10 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:55:16 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:55:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:55:16 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:55:35 GMT
RUN boot
# Wed, 31 Jan 2024 23:55:35 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 31 Jan 2024 23:55:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 31 Jan 2024 23:55:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a56f94c4ac8cf1517e75f20daa59713855b2a987cde3f5a473b73b8fca109c`  
		Last Modified: Thu, 01 Feb 2024 00:12:50 GMT  
		Size: 144.9 MB (144892488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4f4c3ff8947ca24726a619dac2b2aecc3370a14051399e92ddc42713524794`  
		Last Modified: Thu, 01 Feb 2024 00:12:39 GMT  
		Size: 2.4 MB (2368750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a794919da05b7033fdb34852494594c7bb3686cc938954ebdb2fb2aadb6b90c3`  
		Last Modified: Thu, 01 Feb 2024 00:12:41 GMT  
		Size: 58.8 MB (58820562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f11a7810235ef2bc7a1b438a7b1f5416edef7bcecba3ed91f9e250518a6f44`  
		Last Modified: Thu, 01 Feb 2024 00:12:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

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
