## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:ed05a4a9e2a19d221e34058271fdc99a1474940aff5f03d1d28c0be93a1c9097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6283c0e9e50119e1b983b29b3f759f3572fdb7fc51b4ed5ca7790d9a2b4fc205
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261065341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a57434f5ec5743a5a47e2430169fa8fb807296dbad7f4a95a75cf6dc047d51`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:57 GMT
ADD file:20f89ff93bfbd6c9fb1a97058a1f3de4485a8974e8a83892072c511fbd2e4134 in / 
# Wed, 16 Aug 2023 00:59:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 04:04:41 GMT
COPY dir:3e9b1d3d54369337872a2b8aa8c30068d69b28c2def3ec3bf07ba34bd69d48a0 in /opt/java/openjdk 
# Sat, 02 Sep 2023 04:04:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 04:04:43 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Sep 2023 04:04:43 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Sep 2023 04:04:43 GMT
WORKDIR /tmp
# Sat, 02 Sep 2023 04:04:49 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Sep 2023 04:04:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Sep 2023 04:04:49 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Sep 2023 04:05:09 GMT
RUN boot
# Sat, 02 Sep 2023 04:05:10 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:6a70103cc499a199e10e379794c60aa524d9598587cc2bdfe2995642c2da8df7`  
		Last Modified: Wed, 16 Aug 2023 01:04:50 GMT  
		Size: 55.1 MB (55056621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f23cc16f2ead19268424e28613dfc3458e746552d2cc3bfd0a72d3334cb9b4`  
		Last Modified: Sat, 02 Sep 2023 04:15:34 GMT  
		Size: 144.8 MB (144825994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd906e95cb81f2a6783bb1b15e87d827a6992cd214b13d65085f77ddd7c11323`  
		Last Modified: Sat, 02 Sep 2023 04:15:22 GMT  
		Size: 2.4 MB (2362214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9241ea5486d0bffbcbb06f0e32bb28016caf9394caa679a56dae8eafc1392f`  
		Last Modified: Sat, 02 Sep 2023 04:15:25 GMT  
		Size: 58.8 MB (58820512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:180dc85a5c5617b5cb68447f7887c6a8ebe42fafab2f283dbb1003d62abb2aac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256447187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1784c706dc867f4aea147072f33baeb54a8cfa232c7962ebcc8aa050c99ea33`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 01:43:53 GMT
COPY dir:68819d2d348aedadecb99120d7ca4a63dcc1e3aa0bb526ecbd9925396c38234c in /opt/java/openjdk 
# Sat, 02 Sep 2023 01:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 01:43:56 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Sep 2023 01:43:56 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Sep 2023 01:43:56 GMT
WORKDIR /tmp
# Sat, 02 Sep 2023 01:44:02 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Sep 2023 01:44:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Sep 2023 01:44:03 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Sep 2023 01:44:21 GMT
RUN boot
# Sat, 02 Sep 2023 01:44:22 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e4e3a8bbfd2bdf093ae59fc74ef766b5e27c2748069f457d192d1719121d34`  
		Last Modified: Sat, 02 Sep 2023 01:53:12 GMT  
		Size: 141.6 MB (141570380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c5d1cd432757a32b7e23e3061b5bb2748eaa9dfedf7497d88be9e5e34540ca`  
		Last Modified: Sat, 02 Sep 2023 01:53:04 GMT  
		Size: 2.4 MB (2351483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb07bb527fd33975fe235895f466438f89f0ae1fbdb69eb8a00ee2d745c094c0`  
		Last Modified: Sat, 02 Sep 2023 01:53:06 GMT  
		Size: 58.8 MB (58820545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
