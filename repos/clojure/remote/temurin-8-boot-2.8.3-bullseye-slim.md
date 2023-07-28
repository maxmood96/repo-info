## `clojure:temurin-8-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:46c67d503e5d28f3f5f6af3f1f513bdbe3cb8e9032f31c41d28c53e5f0c1b81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:71fdff0f1eab1e96775925b78aa0a31f4ec2c76fd4e5eac7bcef8f663da41aef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (145957724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1925ae99c9919877f5331b78f976c0b67874341dfc869e71e5df36287a8cb3`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 03:14:47 GMT
COPY dir:715eb4123a1bd94a1f232c902a6f3cdcc4011195a3e566c0f0ddc35dd1e83095 in /opt/java/openjdk 
# Fri, 28 Jul 2023 03:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 03:14:47 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 28 Jul 2023 03:14:48 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 28 Jul 2023 03:14:48 GMT
WORKDIR /tmp
# Fri, 28 Jul 2023 03:14:53 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 28 Jul 2023 03:14:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 28 Jul 2023 03:14:53 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 28 Jul 2023 03:15:12 GMT
RUN boot
# Fri, 28 Jul 2023 03:15:12 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ba5371a0abebe830bcea6b9222d076c8228ded98370c272f71596d172e2a49`  
		Last Modified: Fri, 28 Jul 2023 03:28:13 GMT  
		Size: 54.6 MB (54642102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ee254c577f2d981a17fe81a1627f2ae3158b8237e058870edf410f064591dd`  
		Last Modified: Fri, 28 Jul 2023 03:28:06 GMT  
		Size: 1.1 MB (1077548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98590bbb5b46c3eafe41e7443b46318c587d2e74755dff4c4fe7c4dfbc080aeb`  
		Last Modified: Fri, 28 Jul 2023 03:28:10 GMT  
		Size: 58.8 MB (58820472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:38bdd86bae12e660726672e12085d586a595710a6d0e1af5ef5b815c23dcb559
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143690995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a5c26a309381bd3eb8fea1b979e2198c18a769f371d13487d8b8a0c57495a5`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:25:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 14:30:43 GMT
COPY dir:f6bbe63c81e220d954915791686219263d8c45918fd81b238f7c9f6b21f076f8 in /opt/java/openjdk 
# Fri, 28 Jul 2023 14:30:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 14:30:45 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 28 Jul 2023 14:30:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 28 Jul 2023 14:30:45 GMT
WORKDIR /tmp
# Fri, 28 Jul 2023 14:30:49 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 28 Jul 2023 14:30:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 28 Jul 2023 14:30:50 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 28 Jul 2023 14:31:10 GMT
RUN boot
# Fri, 28 Jul 2023 14:31:10 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb91ed9165432810d4f91e7d6139695bd8c5c470b47b0aea2b6e5334cc599318`  
		Last Modified: Fri, 28 Jul 2023 14:40:20 GMT  
		Size: 53.7 MB (53742686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e71cfd6f7f02eddc2decc394a8baf7f092b156be4f37b07d6dab92565c93585`  
		Last Modified: Fri, 28 Jul 2023 14:40:15 GMT  
		Size: 1.1 MB (1064818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126b4511122c132566ede44fc6bd168e8609a87f826dc8851503533890c7067a`  
		Last Modified: Fri, 28 Jul 2023 14:40:19 GMT  
		Size: 58.8 MB (58820660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
