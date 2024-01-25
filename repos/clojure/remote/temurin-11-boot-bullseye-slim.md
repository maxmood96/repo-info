## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:ae884e78585a37760c021272990ea7ee28c00440d35260c7f0d8c045d666799f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:019ada23fec27c7995b887159ee01e5b1cd5e0b6f833887dfb505399c16d1a3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236588967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbce73e74d46f2568e2cb9677ec1e4d6cd42cc53079f093b3baa80389fe252a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:10:39 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:10:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:10:40 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:10:40 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:10:40 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:10:47 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:10:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:10:47 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:11:08 GMT
RUN boot
# Wed, 24 Jan 2024 22:11:08 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ca7d667a4ecdc7ffeb124470f85841423d14d5340d9a402d347b8dcab005f7`  
		Last Modified: Wed, 24 Jan 2024 22:37:46 GMT  
		Size: 145.3 MB (145270941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adc02171c4779fb6c61a5a6281ece011c75aa087243b12eaaecb143f8b99e9b`  
		Last Modified: Wed, 24 Jan 2024 22:37:35 GMT  
		Size: 1.1 MB (1079476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a45dfdf03c4781f7edd402f0593e5884346bd894ad9a178e6f14eeacfe13d62`  
		Last Modified: Wed, 24 Jan 2024 22:37:38 GMT  
		Size: 58.8 MB (58820595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

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
