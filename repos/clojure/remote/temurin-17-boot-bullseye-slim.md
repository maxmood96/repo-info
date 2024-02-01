## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:37c4fd71500658af3db67e770438f33446667fdd209cfa8d3d7409b716bf8f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:245d85c8ac41d505eb896fc09ef6ef699cccf8d3e0e92b1357b52ee99e648b18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236210776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb42d6d4ff1c932498584091de2aceb8e796611180848b6bc597ab777785e0e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:55:44 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:55:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:55:45 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:55:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:55:45 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:55:51 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:55:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:55:51 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:56:09 GMT
RUN boot
# Wed, 31 Jan 2024 23:56:09 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 31 Jan 2024 23:56:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 31 Jan 2024 23:56:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada2cf41cb8c5a69262cd16ed219afecfb15a02b85a90f3f7b04709e0dc6dd35`  
		Last Modified: Thu, 01 Feb 2024 00:13:12 GMT  
		Size: 144.9 MB (144892503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2754ed8628a6e8ce037c32b542b3de59cfaa897f7ec2621d1b728b718cf119`  
		Last Modified: Thu, 01 Feb 2024 00:12:59 GMT  
		Size: 1.1 MB (1079493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6116485c8782a79dd201601ec3070eb3d8582de0f100b8c112264de6383c3bc2`  
		Last Modified: Thu, 01 Feb 2024 00:13:09 GMT  
		Size: 58.8 MB (58820550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec037ae86e991d7bba6fee6591177dbf6e3d4b524498b2ae183b2d655b57a97f`  
		Last Modified: Thu, 01 Feb 2024 00:12:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:084981b127db64e8b051954cc56fb60e9f952df9ad40c62a5f12ff2cb0fa81a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233672522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d00bfe8412f3acf08735279d2f95c4e6469797d3f0f65e9a9ca785a9acdece`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:22:09 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:22:09 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:22:09 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:22:13 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:22:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:22:14 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:22:28 GMT
RUN boot
# Wed, 24 Jan 2024 22:22:29 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 24 Jan 2024 22:22:29 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jan 2024 22:22:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788e0490d2b2fa8b837175a198776ee16acffd004eae1a6bf332246b5de097e`  
		Last Modified: Wed, 24 Jan 2024 22:42:11 GMT  
		Size: 1.1 MB (1066838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0ab61a6ca8b90ab0060400c12dbd77f2f9ff54ad084f52319d23e5916d9fc2`  
		Last Modified: Wed, 24 Jan 2024 22:42:14 GMT  
		Size: 58.8 MB (58820403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d96ee137699e7345e7a26c20bfa9516a78d65e491d4c77980bd20b3e64196ab`  
		Last Modified: Wed, 24 Jan 2024 22:42:10 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
