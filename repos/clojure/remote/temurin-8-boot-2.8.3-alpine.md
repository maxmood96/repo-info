## `clojure:temurin-8-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:bca5bb899ef2a2a3a474d8275170d785b64c3f45c1b3a6204bc4f9b946f9f91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-8-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:a458e5b37af43a36b630cba099e388e5c043a26190d9b8e8ce0c6a95f9c1d338
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164381206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3557a0088d0e77aff0d11ba3d17f8b4f68514998d81559ece0bc4f4f99154be6`
-	Default Command: `["boot","repl"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:20:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 18 Jul 2022 22:20:08 GMT
RUN apk add --no-cache libretls musl-locales musl-locales-lang tzdata zlib     && rm -rf /var/cache/apk/*
# Mon, 18 Jul 2022 22:20:08 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Mon, 18 Jul 2022 22:20:25 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='29705d2b619b40b0f3dbb05fa497b74851e872e4db6496c2b9b358e1dad967ff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 18 Jul 2022 22:20:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Jul 2022 22:20:26 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 26 Jul 2022 22:21:30 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 26 Jul 2022 22:21:30 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 26 Jul 2022 22:21:30 GMT
WORKDIR /tmp
# Tue, 26 Jul 2022 22:21:32 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Tue, 26 Jul 2022 22:21:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 26 Jul 2022 22:21:32 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 26 Jul 2022 22:21:52 GMT
RUN boot
# Tue, 26 Jul 2022 22:21:52 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d31e16dc1b50d804a50e80381050a90d4dc55a110eae65cd1cef937d3dc18d3`  
		Last Modified: Mon, 18 Jul 2022 22:24:55 GMT  
		Size: 477.8 KB (477762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3079c391c0fc9c44446b64c2e90f79b25c3f7d970a0b0c7c9948b8bc4039867a`  
		Last Modified: Mon, 18 Jul 2022 22:25:04 GMT  
		Size: 101.4 MB (101433768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd7ad4e378d30632e06e883ca8783dbe81f637d5789cc57aca1965d31a541c2`  
		Last Modified: Mon, 18 Jul 2022 22:24:55 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fb7a6107586090efe92012ac57a9638b4b5ae7735309c8e32abd790f1e8029`  
		Last Modified: Tue, 26 Jul 2022 22:32:02 GMT  
		Size: 850.3 KB (850313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd178a8015b6b8dbaf7920d57bcbf2f80fd368e54ac9813a0acb2c13452f547`  
		Last Modified: Tue, 26 Jul 2022 22:32:05 GMT  
		Size: 58.8 MB (58820396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
