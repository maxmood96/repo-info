## `clojure:temurin-11-boot-bullseye`

```console
$ docker pull clojure@sha256:2fb0e6fe54856ce17399128f2a3d2db9086b4dc0fd00223d5b5d429d4e57cd0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5280af6dc85cb2c443b9af96db00723da2679c16af4215cdea6613778a479759
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314682063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fed1285aa2407197c91c5505bb8b7da33f025cd1744d27347d241a34790130`
-	Default Command: `["boot","repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:26 GMT
ADD file:cc6a56676703ec7ab5db8f2f7bc18a3169c0816d38703845b6b77ae5342ab41c in / 
# Sat, 04 Feb 2023 06:51:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:05:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 14:08:30 GMT
COPY dir:fdbc5e9dec2946fa124877176e92a68dd3fe3a70def5bb906a6040c4a1303a2d in /opt/java/openjdk 
# Sat, 04 Feb 2023 14:08:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 14:08:31 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 04 Feb 2023 14:08:31 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 04 Feb 2023 14:08:32 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 14:08:37 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 04 Feb 2023 14:08:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 04 Feb 2023 14:08:37 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 04 Feb 2023 14:08:54 GMT
RUN boot
# Sat, 04 Feb 2023 14:08:54 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:699c8a97647f5789e5850bcf1a3d5afe9730edb654e1ae0714d5bd198a67a3ed`  
		Last Modified: Sat, 04 Feb 2023 06:55:53 GMT  
		Size: 55.0 MB (55025312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f565856b829993d14340c31a3780b450c70735c0b120d09f383ea8f7d156617`  
		Last Modified: Sat, 04 Feb 2023 14:21:45 GMT  
		Size: 198.5 MB (198475546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcdc790b292770bf275667120221a3bcc2a5da2b60baa697c4a1d2fa858b6a9`  
		Last Modified: Sat, 04 Feb 2023 14:21:31 GMT  
		Size: 2.4 MB (2360715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbd3a590b7d3a57f3871fc65b47dd9c9bfa355f79e64cedea9551f6bc6c43e9`  
		Last Modified: Sat, 04 Feb 2023 14:21:34 GMT  
		Size: 58.8 MB (58820490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:43a6268677f01dbad4c41273f750d6bf1cdfafe6af202b9d99582f7a774f051b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310093377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362c82e298dbfe6e115332b0c508168192c75c2a6009899f3616ed43f1e9ad9f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:26 GMT
ADD file:c5a7c65d67685092faa3456c1a772550aa6d06ac07e1f98a95d39c31e304dbf8 in / 
# Sat, 04 Feb 2023 06:17:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:02:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 17:05:15 GMT
COPY dir:b661686bf8d434588756c45f2ef6e7f314f32f753cf180ef8fb45397388f098c in /opt/java/openjdk 
# Sat, 04 Feb 2023 17:05:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 17:05:19 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 04 Feb 2023 17:05:19 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 04 Feb 2023 17:05:19 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 17:05:25 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 04 Feb 2023 17:05:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 04 Feb 2023 17:05:25 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 04 Feb 2023 17:05:42 GMT
RUN boot
# Sat, 04 Feb 2023 17:05:42 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:fac7262b6510529638951e16807cf1758f42c892ed924e334c27bb8bbcf7d7c2`  
		Last Modified: Sat, 04 Feb 2023 06:21:01 GMT  
		Size: 53.7 MB (53681927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf390961218a64e5f08d8723e6ac559e53df82459981dd9ae968a11a901c3d63`  
		Last Modified: Sat, 04 Feb 2023 17:16:51 GMT  
		Size: 195.2 MB (195240318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff97ef0094bd04f359af617a1f4d8fe9d8adaf42725fa30a52465a40fcf50cab`  
		Last Modified: Sat, 04 Feb 2023 17:16:40 GMT  
		Size: 2.4 MB (2350653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b0cb6adeddf3fb4fd099e8dc0ebc11fea7755e7bda7b0bcbedf4084ed18aca`  
		Last Modified: Sat, 04 Feb 2023 17:16:42 GMT  
		Size: 58.8 MB (58820479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
