## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:844380262573f6f793a6b2bde66c479c74eebf0c7b6ac3f4d75412ca5c8e8fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ec3df9b9a0e63cb7a6d9fb9213acc5f54473548868712eab6149d029a7c6b36b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.7 MB (308652855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39802242619afaa5dc7efc180876a880d65b15b5800156a7dc31f58acf8ecc16`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:43 GMT
ADD file:abc6873c98339a3c496cb75ec2528e65ebe1f20d2cea777033f86dcd55d73da5 in / 
# Tue, 15 Nov 2022 04:04:43 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 17:50:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 17:57:09 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Tue, 15 Nov 2022 17:57:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 17:57:11 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 15 Nov 2022 17:57:11 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 17:57:11 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 17:57:17 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 15 Nov 2022 17:57:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 17:57:17 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 15 Nov 2022 17:57:37 GMT
RUN boot
# Tue, 15 Nov 2022 17:57:37 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 15 Nov 2022 17:57:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 15 Nov 2022 17:57:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a8ca11554fce00d9177da2d76307bdc06df7faeb84529755c648ac4886192ed1`  
		Last Modified: Tue, 15 Nov 2022 04:08:24 GMT  
		Size: 55.0 MB (55038615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac501d2f56220af0989f4867ddcb859a8c615b98ef9c55c1ea816f6a6ce37930`  
		Last Modified: Tue, 15 Nov 2022 18:10:20 GMT  
		Size: 192.4 MB (192431251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa61314b430b408323c99ce1089e434742b8a07686c0b6ba0d68b486e1ce3978`  
		Last Modified: Tue, 15 Nov 2022 18:10:06 GMT  
		Size: 2.4 MB (2362114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f791cdf16293f2f0cfaaa9d8cb7fed1051d851814a96bc2f2fa956fcfb309d82`  
		Last Modified: Tue, 15 Nov 2022 18:10:09 GMT  
		Size: 58.8 MB (58820476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132bdf1169e495ed4afdb70ba300e6d204b220777b8e9b7ac0451e27a9a04bf2`  
		Last Modified: Tue, 15 Nov 2022 18:10:06 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cc1e08844008faceea6cd83ca9f344d7ceb370c1a174d991a5481b46f88a5538
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306088222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6d900da21e3d9af2ec4b0f9b11428a7706e9ce1eaab1f7a2e938ca9c8e3100`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:12 GMT
ADD file:1f3a7177f64e1adda3e7a541c93dd4322c6ecb4f00f7b015665df2c0c08b59a5 in / 
# Tue, 15 Nov 2022 01:41:12 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:48:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:54:01 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:54:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:54:05 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 15 Nov 2022 05:54:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 05:54:05 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:54:10 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 15 Nov 2022 05:54:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 05:54:10 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 15 Nov 2022 05:54:27 GMT
RUN boot
# Tue, 15 Nov 2022 05:54:28 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 15 Nov 2022 05:54:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 15 Nov 2022 05:54:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:077c13527d405646e2f6bb426e04716ae4f8dd2fdd8966dcb0194564a2b57896`  
		Last Modified: Tue, 15 Nov 2022 01:44:12 GMT  
		Size: 53.7 MB (53699862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee604ee1c814449c1e8223fcbca2cf78c6ba906a0de869dc5ae852d237e22604`  
		Last Modified: Tue, 15 Nov 2022 06:04:50 GMT  
		Size: 191.2 MB (191215218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039f1d577246462e461a235787c393f1c378a61f37f505632ce33cb8c612f982`  
		Last Modified: Tue, 15 Nov 2022 06:04:39 GMT  
		Size: 2.4 MB (2352200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06eba7a89179cb7f9c0684af2e2c130e0f32262253510e1fe193574d2e81190e`  
		Last Modified: Tue, 15 Nov 2022 06:04:42 GMT  
		Size: 58.8 MB (58820542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb11aed458b4d88cbb9eb5cc01b9331794d7dfc45d7c91e672b8701b1c9fa9b`  
		Last Modified: Tue, 15 Nov 2022 06:04:38 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
