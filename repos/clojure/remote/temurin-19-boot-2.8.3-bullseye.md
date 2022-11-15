## `clojure:temurin-19-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:7fba651cbabe3abc4f4280f435a3105e38bdc342e7615306d875877ad0c74fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5c26c81df87b1b11d4e20e630d4d0dcaa9070729d7bd3a19bf9d141d207b5598
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317325061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79fb867ae55be8007444a626effbc971d60206ca97497e0cbf395aeaf1e04aa3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:43 GMT
ADD file:abc6873c98339a3c496cb75ec2528e65ebe1f20d2cea777033f86dcd55d73da5 in / 
# Tue, 15 Nov 2022 04:04:43 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 17:50:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 18:00:19 GMT
COPY dir:fef581854733ec7202f8c807463b9e1952aeb6c7a002719c7e54987e50ea4dcb in /opt/java/openjdk 
# Tue, 15 Nov 2022 18:00:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 18:00:20 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 15 Nov 2022 18:00:21 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 18:00:21 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 18:00:27 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 15 Nov 2022 18:00:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 18:00:27 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 15 Nov 2022 18:00:45 GMT
RUN boot
# Tue, 15 Nov 2022 18:00:45 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 15 Nov 2022 18:00:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 15 Nov 2022 18:00:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a8ca11554fce00d9177da2d76307bdc06df7faeb84529755c648ac4886192ed1`  
		Last Modified: Tue, 15 Nov 2022 04:08:24 GMT  
		Size: 55.0 MB (55038615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255e73ee1e6eea684a2802365781fb7b0537b3dd818cb1ce939242a8029132be`  
		Last Modified: Tue, 15 Nov 2022 18:12:23 GMT  
		Size: 201.1 MB (201103445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d407f671f4346d214726b50ec7b59aed230e60ca7ab5f410d79f56c5c26c605`  
		Last Modified: Tue, 15 Nov 2022 18:12:08 GMT  
		Size: 2.4 MB (2362026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab8d4ff4b2f4588d8807cfaea42547f7e3fc7901e93a14f7ba612dbf87f9f4f`  
		Last Modified: Tue, 15 Nov 2022 18:12:12 GMT  
		Size: 58.8 MB (58820575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caaf59c459d4b3ff660621208a995e7a3186700bf3f489957e3bfafbca458058`  
		Last Modified: Tue, 15 Nov 2022 18:12:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ddfea431bf33184abb96d8f9c5b822bf0dad9ec7cb8a641f21860de8b41979ef
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314737379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36c703f0c870e7362985588e161943246ebf3ab6c127f3a26efa8373c412106`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:12 GMT
ADD file:1f3a7177f64e1adda3e7a541c93dd4322c6ecb4f00f7b015665df2c0c08b59a5 in / 
# Tue, 15 Nov 2022 01:41:12 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:48:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:56:38 GMT
COPY dir:4138443eebfda1a2a245638d5bb568645bd34d79b66d39a3be31b5ac6b823d6d in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:56:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:56:43 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 15 Nov 2022 05:56:43 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 05:56:43 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:56:48 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 15 Nov 2022 05:56:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 05:56:48 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 15 Nov 2022 05:57:06 GMT
RUN boot
# Tue, 15 Nov 2022 05:57:06 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 15 Nov 2022 05:57:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 15 Nov 2022 05:57:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:077c13527d405646e2f6bb426e04716ae4f8dd2fdd8966dcb0194564a2b57896`  
		Last Modified: Tue, 15 Nov 2022 01:44:12 GMT  
		Size: 53.7 MB (53699862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fdef0df9660bc53c8d91dc032dd6670451891d34a69da37129f03671d76128`  
		Last Modified: Tue, 15 Nov 2022 06:06:38 GMT  
		Size: 199.9 MB (199864458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b8b4b231d2e30251684fcc71ca75a52b86ab480facfcb30808d88fbf5e226a`  
		Last Modified: Tue, 15 Nov 2022 06:06:26 GMT  
		Size: 2.4 MB (2352212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b91518133088d18a7cc5869421aaf12313f2291b0f9ce36dca2bd86b215c50c`  
		Last Modified: Tue, 15 Nov 2022 06:06:29 GMT  
		Size: 58.8 MB (58820448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2a883b8b9488e369d55ca91402b725b25d4c2a0e157888f7e1ac3cdf6cb8a5`  
		Last Modified: Tue, 15 Nov 2022 06:06:25 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
