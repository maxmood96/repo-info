## `clojure:temurin-17-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:0fa2df2fb58a48d7b707d1f28b71c42b9365718b9b182bc82f761a1b3195038a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4431cd7134b63a253d881bac8e801479e9dd1c6b63eb1fdd16a9158110de768a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.4 MB (236365687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e7d506fc3947ccd9226d3bec4db4ed345adf49d5b137dc97f616db6b56780a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:43:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:54:34 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:54:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:54:36 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:54:36 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:54:36 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:54:42 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:54:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:54:42 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:55:01 GMT
RUN boot
# Wed, 31 Jan 2024 23:55:01 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 31 Jan 2024 23:55:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 31 Jan 2024 23:55:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f958f51a0d7ee5eda8bc3fd3d244ea755a14a4ce5fc81c38ce16b8f68abf581`  
		Last Modified: Thu, 01 Feb 2024 00:12:29 GMT  
		Size: 144.9 MB (144892493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da7d919311dbe3c81801e65e5425d85c9c11959b754120a0b54c052c35f3b20`  
		Last Modified: Thu, 01 Feb 2024 00:12:09 GMT  
		Size: 3.5 MB (3501736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6379a15f831eb7017152eb869afa938b876aef5a4406446857b8184bfe7875`  
		Last Modified: Thu, 01 Feb 2024 00:12:12 GMT  
		Size: 58.8 MB (58820591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f286a5f1c152deb82c54b097afd05e222b0ffe6761a98dcff8ef84ca8cd2a5`  
		Last Modified: Thu, 01 Feb 2024 00:12:09 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b075986e4aa6cdebcde304e3fd132da6535a62441353db1aa386219ef8a4e5bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235047691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de5347e4ccaeabb03f39ebf459d91113636f2c4be79d65e1f544039e14525fb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:30:04 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:30:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:30:08 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 01 Feb 2024 06:30:08 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 06:30:08 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:30:13 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 01 Feb 2024 06:30:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 06:30:13 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 01 Feb 2024 06:30:31 GMT
RUN boot
# Thu, 01 Feb 2024 06:30:31 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 06:30:31 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 06:30:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8541bec30ce62241d4247e43427e2cfb0f0dd456024f3b7c2bc64e85374f9c`  
		Last Modified: Thu, 01 Feb 2024 06:45:48 GMT  
		Size: 143.7 MB (143720887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fe42ef2cd31ea4fd38429ab8ce18f3d30ecfd58ab59ab4b4f60ed0c1efb69d`  
		Last Modified: Thu, 01 Feb 2024 06:45:39 GMT  
		Size: 3.3 MB (3324922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ef63e8147d91655d760adf61a1904f57e8e9f2f5c5c5004367d408351700d6`  
		Last Modified: Thu, 01 Feb 2024 06:45:41 GMT  
		Size: 58.8 MB (58820650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79e9974c1721c162ac83c2ffd178a153bdc3c17dfc8fa31bc34326564bc3015`  
		Last Modified: Thu, 01 Feb 2024 06:45:38 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
