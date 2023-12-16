## `clojure:temurin-17-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:4eeb7510c64bc3964dab49380994115e2c077d8f66029e00d899999a5dceb0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:70540fec22a9d23d7316793bc9b222cc31fa5516591baae3b68380470868bb26
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236346280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc08476b643b5a114b4717c64ecce694d85a69382d8dd60a1e0d1f6aef05861`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:37 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Tue, 21 Nov 2023 05:21:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:08:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 15:33:00 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Sat, 16 Dec 2023 15:33:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 15:33:01 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 16 Dec 2023 15:33:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 16 Dec 2023 15:33:01 GMT
WORKDIR /tmp
# Sat, 16 Dec 2023 15:33:07 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 16 Dec 2023 15:33:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 16 Dec 2023 15:33:08 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 16 Dec 2023 15:33:24 GMT
RUN boot
# Sat, 16 Dec 2023 15:33:25 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 16 Dec 2023 15:33:25 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Dec 2023 15:33:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3245e9463990d9e0c965bd9734c2af1ca019b79fe90798edef5dc2e096986e`  
		Last Modified: Sat, 16 Dec 2023 15:49:04 GMT  
		Size: 144.9 MB (144873974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3b386ab5d93ef7c8f06dbf2afa7531637353d03805418464920ed6d5bc86bb`  
		Last Modified: Sat, 16 Dec 2023 15:48:53 GMT  
		Size: 3.5 MB (3501674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308c2a95811854830c03b6d4c14c1ee10e9e225263d8587b16f3fb703d018eda`  
		Last Modified: Sat, 16 Dec 2023 15:48:56 GMT  
		Size: 58.8 MB (58820322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c4d77d5f21109ed17150e18e509da86dd00e3e9b773371f7a1f801145125df`  
		Last Modified: Sat, 16 Dec 2023 15:48:53 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d7a719a6ff16014c1c1cee436e04e5becc7add3f8d186375ee8b09a37280e08e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235006809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a78fb225db6818448704571b2a7e0f45ea351a84384d20fa1d008e5b81254389`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 08:53:31 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Sat, 02 Dec 2023 08:53:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 08:53:35 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Dec 2023 08:53:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Dec 2023 08:53:35 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 08:53:40 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Dec 2023 08:53:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Dec 2023 08:53:40 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Dec 2023 08:53:56 GMT
RUN boot
# Sat, 02 Dec 2023 08:53:57 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 02 Dec 2023 08:53:57 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 02 Dec 2023 08:53:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5174505a545417ed296a7213ad24367c7222fd420ece7b5f7b0bd62c3811e57`  
		Last Modified: Sat, 02 Dec 2023 09:08:12 GMT  
		Size: 143.7 MB (143681757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e37bf8024f8af2ad7371f20dc897038ea349c3e3ae82e03109bf62c01ee1f9a`  
		Last Modified: Sat, 02 Dec 2023 09:08:03 GMT  
		Size: 3.3 MB (3324877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fb6c60c5411387f48e0828bc66c65a041d406527832079e5bfb1c007c53208`  
		Last Modified: Sat, 02 Dec 2023 09:08:05 GMT  
		Size: 58.8 MB (58820498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d85c2c212c6bcc4b56978cb9aa977ba9a3a968182b06214fe391d6139832060`  
		Last Modified: Sat, 02 Dec 2023 09:08:02 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
