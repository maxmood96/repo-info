## `clojure:temurin-17-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:4bbdd0b9feba75e9f2bab45f095d2837a09696bbfe299c982402a0e75ee093a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:369608d470e0f2c06b469bf3147ad495c17d4a66266e0c9d33a0976a4b64e3c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236335770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2272ea0651a2c0d311783e111791d6964543727d2c1d14f64a64e5a6d0e1b5d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:47:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 05:21:53 GMT
COPY dir:6673b976fb9ccd391df2de00f5738789bfa84c9bc068b98b869cb1d7436fd333 in /opt/java/openjdk 
# Fri, 16 Feb 2024 05:21:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 05:21:55 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Feb 2024 05:21:55 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Feb 2024 05:21:55 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 05:22:02 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Feb 2024 05:22:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Feb 2024 05:22:02 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Feb 2024 05:22:22 GMT
RUN boot
# Fri, 16 Feb 2024 05:22:22 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 16 Feb 2024 05:22:22 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Feb 2024 05:22:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954503457635d4984fa02d42e6a7fe96adb6ed04ec63bd42b5805de30d4f95ba`  
		Last Modified: Fri, 16 Feb 2024 05:36:46 GMT  
		Size: 144.9 MB (144892562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449ebc0c6a76c29d7255738fd71818f5f3dea4c48d505fc9303b6fddd74f39b1`  
		Last Modified: Fri, 16 Feb 2024 05:36:34 GMT  
		Size: 3.5 MB (3498232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af79193a04b622c6fdf9c9e31a22defc359174195b1515744657cc2632887630`  
		Last Modified: Fri, 16 Feb 2024 05:36:37 GMT  
		Size: 58.8 MB (58820485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153e9461e98f139041fd674e57f6098a514ad2a8b355de775b6da74cbb5e6b63`  
		Last Modified: Fri, 16 Feb 2024 05:36:34 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e6d7fbeb19e3fa67fe41003d57fbb387dacc775c947359e170d9bbc106852d12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235020415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f03751caff4506e30fc607f71290a64096135823cb8d56774e3f53fe808889f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 07:58:42 GMT
COPY dir:868002d69a8870cfd22502db6415e3cd8591d5271a62d90057620eefd5ce7d20 in /opt/java/openjdk 
# Fri, 16 Feb 2024 07:58:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 07:58:46 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Feb 2024 07:58:46 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Feb 2024 07:58:46 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 07:58:51 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Feb 2024 07:58:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Feb 2024 07:58:51 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Feb 2024 07:59:11 GMT
RUN boot
# Fri, 16 Feb 2024 07:59:11 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 16 Feb 2024 07:59:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Feb 2024 07:59:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d97e501642634b434e8ba4d34ad6efdf8610fdb932f46517563cd65f1b26a51`  
		Last Modified: Fri, 16 Feb 2024 08:11:43 GMT  
		Size: 143.7 MB (143720920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b918ff8748504ccb8096d6842daeb30ec4f57ffff3c1ea1cb9fef72e9052ff`  
		Last Modified: Fri, 16 Feb 2024 08:11:34 GMT  
		Size: 3.3 MB (3322111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac04b06d7713011a2129210086f9f01483155a0e8380cbc48f186ab969424540`  
		Last Modified: Fri, 16 Feb 2024 08:11:36 GMT  
		Size: 58.8 MB (58820621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1534f639c4d64008c309824248952d41d8afdf09d218314770b700bd397aaa10`  
		Last Modified: Fri, 16 Feb 2024 08:11:33 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
