## `clojure:temurin-11-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:31482e61e57a1f97dfa719560afa7596ec931bc275ffb81fb090d33c3355e438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:92bc5add4cf3c67e9a13fdae239f155c5382f91832254f3b8a3d9dca0b29f624
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236588834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de74cc4666b21da743b5fd4e065a3bab0c95b1ad85ac74c483ae21660ec5e3fc`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:50:14 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:50:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:50:15 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:50:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:50:16 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:50:21 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:50:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:50:21 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:50:41 GMT
RUN boot
# Wed, 31 Jan 2024 23:50:41 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237cb6d9dedd71662d3dfef2792a61299af8d4b495bbb2a1e8f51c6f89c22ddd`  
		Last Modified: Thu, 01 Feb 2024 00:09:34 GMT  
		Size: 145.3 MB (145270936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a0fd4a1b29914c5528747a90854647fa44175561142158b4fe1e10d818e4e5`  
		Last Modified: Thu, 01 Feb 2024 00:09:23 GMT  
		Size: 1.1 MB (1079474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95edbefb260db8c5c5d1b253640d906e4ad30669eae43d777cf1da26794c887`  
		Last Modified: Thu, 01 Feb 2024 00:09:26 GMT  
		Size: 58.8 MB (58820597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:60d7a489067d18f940fd6f535f69089b145d27aac917c833b246c784e5415d4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231957685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a72143eaf8188979c494303d308c15d47562880c720b10d3c9d5c8aadb736b5`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:15:46 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:15:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:15:50 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:15:50 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:15:50 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:15:55 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:15:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:15:55 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:16:10 GMT
RUN boot
# Wed, 24 Jan 2024 22:16:11 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526ebc7d46b758eaa180a9fe8c8d3e11a382c71f0c0f80f26cbea876285218d4`  
		Last Modified: Wed, 24 Jan 2024 22:37:42 GMT  
		Size: 142.0 MB (142006475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a246ce555b24f9323467b9bbaf36fcbe511baf6e28baf465c5a842e73f575f5`  
		Last Modified: Wed, 24 Jan 2024 22:37:33 GMT  
		Size: 1.1 MB (1066844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53183eae750a1d5e16604efe18aee93390b4268143ce31f1c115e0ec35ce3b3`  
		Last Modified: Wed, 24 Jan 2024 22:37:35 GMT  
		Size: 58.8 MB (58820356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
