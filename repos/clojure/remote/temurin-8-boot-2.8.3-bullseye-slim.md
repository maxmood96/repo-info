## `clojure:temurin-8-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:345242b63df0b1e82f100a721d8add65ae8f6310b376e11df909d96a5f4dd71d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:76dd71be58d5d5e55d30755384577da084981fe117b0a95db4554a72629855c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194916254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2aaecbb9be144c4a46611b8b9e14c8b85fb5568a61f4efa096e9b9d3fd8fa6`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:54:00 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:54:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 04:54:01 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 04:54:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 04:54:01 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 04:54:07 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 04:54:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 04:54:07 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 04:54:28 GMT
RUN boot
# Thu, 11 Jan 2024 04:54:28 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174aa11106f2d3d4da01484fac2da5df4e3ce9ec4196afe1ba0d6908551deaf2`  
		Last Modified: Thu, 11 Jan 2024 05:15:12 GMT  
		Size: 103.6 MB (103598261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8a2edf9d38b86b998b45d47df1284a64099e053932b3d71fee8174589c6fe5`  
		Last Modified: Thu, 11 Jan 2024 05:15:04 GMT  
		Size: 1.1 MB (1079493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15109adb220834a2f05b4d7784c3b8feaf114b9d2c9c55564b1b9e90c31017ef`  
		Last Modified: Thu, 11 Jan 2024 05:15:07 GMT  
		Size: 58.8 MB (58820545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4d743538d576228bae2597adc986b5bb9ccecd13dc209ffa813575627aaa58d3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192652935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44939e4ae49d3415b6969c3265c4f95a171c0e929ccf2fb18da92623a9c3e62c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 08:00:34 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Thu, 11 Jan 2024 08:00:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 08:00:37 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 08:00:37 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 08:00:37 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 08:00:42 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 08:00:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 08:00:42 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 08:01:02 GMT
RUN boot
# Thu, 11 Jan 2024 08:01:02 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366d659c3c292f2bc2e093f2ff5fe19bc591d3988f74e4d0a7c85be379fc8c40`  
		Last Modified: Thu, 11 Jan 2024 08:18:46 GMT  
		Size: 102.7 MB (102701538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eabae97d7dc51fcb1a1dcfed8a67631b167fe0f2143390287c8239facf3d9cd`  
		Last Modified: Thu, 11 Jan 2024 08:18:39 GMT  
		Size: 1.1 MB (1066826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f88a2805a45a0e9cfb49495aa3f50a7a0fa1df15a5710965da81c725db54025`  
		Last Modified: Thu, 11 Jan 2024 08:18:42 GMT  
		Size: 58.8 MB (58820561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
