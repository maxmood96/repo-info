## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:1102a0c0d42b9505a4bfc1e4496f0dfbc563ed98cf149576cc0e745839bca236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5c60446ff0996cceb1d27d06445574cef5378a2f3bb3051aac77ea792cb9c155
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283895889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d98f946fd3a8731df2edacbbc795dff7af6b9cdfbeec89c55b9cb25f7e535bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:00:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 04:06:23 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Tue, 04 Jul 2023 04:06:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 04:06:24 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 04 Jul 2023 04:06:24 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 04 Jul 2023 04:06:24 GMT
WORKDIR /tmp
# Tue, 04 Jul 2023 04:06:29 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 04 Jul 2023 04:06:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Jul 2023 04:06:30 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 04 Jul 2023 04:06:46 GMT
RUN boot
# Tue, 04 Jul 2023 04:06:46 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 04 Jul 2023 04:06:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Jul 2023 04:06:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22f472fa461196b4d0768628e3eee647b25cc27072e8bad3c89810bdd847134`  
		Last Modified: Tue, 04 Jul 2023 04:15:28 GMT  
		Size: 192.6 MB (192580306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91efe5ddf3644d6cd5b1aa3406a5bd97c0d687a8acf643b18bfbba5f677fb8a7`  
		Last Modified: Tue, 04 Jul 2023 04:15:15 GMT  
		Size: 1.1 MB (1077529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb38398b52ce7d4f26ef217968c10a23b2b23eecd90c1a4b75f748f6cab2661d`  
		Last Modified: Tue, 04 Jul 2023 04:15:19 GMT  
		Size: 58.8 MB (58820267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd062b3c2009c8ee14a202f450d829b0c338b248658d44a6e7471188e9a4e5aa`  
		Last Modified: Tue, 04 Jul 2023 04:15:15 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4183c22e49dc1565433adc0efc77833f833feb7e560d6f3c1422e2d88a0d4ba8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281336051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5046c757a694813546d82f4446f14167412a13ad0296cb56b84860d142e3d467`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:28:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 04:47:00 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Fri, 16 Jun 2023 04:47:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:47:05 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Jun 2023 04:47:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Jun 2023 04:47:05 GMT
WORKDIR /tmp
# Fri, 16 Jun 2023 04:47:10 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Jun 2023 04:47:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jun 2023 04:47:10 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Jun 2023 04:47:26 GMT
RUN boot
# Fri, 16 Jun 2023 04:47:26 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 16 Jun 2023 04:47:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jun 2023 04:47:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589855d0c7aebd4ca2b50aaf622d291cd44875676cdd56512b687b47b80c59ad`  
		Last Modified: Fri, 16 Jun 2023 04:57:17 GMT  
		Size: 191.4 MB (191387665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e2f8c0fd65919012d69d90edf7df4c7cf1d74c57c24ce0d1ed009618a042f4`  
		Last Modified: Fri, 16 Jun 2023 04:57:06 GMT  
		Size: 1.1 MB (1064832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86eeebd25e09e7fb8175ed4be36d909a841ada725a3039740b084f3cc0e71b7f`  
		Last Modified: Fri, 16 Jun 2023 04:57:09 GMT  
		Size: 58.8 MB (58820321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e190aea293b31f11a1e45a6e116e55ddfed37f09b9c265262fa9c47c9c40e0`  
		Last Modified: Fri, 16 Jun 2023 04:57:06 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
