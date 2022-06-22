## `clojure:temurin-18-boot-alpine`

```console
$ docker pull clojure@sha256:290fa0725a8945e8fc06cdff5551b7cdfdd2f06825c42ad55065b2cdb9ef02ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-18-boot-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:7a7fe10655c96c8d3aea64ac95b4321e9319cd0d8893f939c93c4b63847563a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255810618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920a54c01cd178b1677ccbd12245d03263fb86ee958b9098922faed06e46daf2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 May 2022 19:19:30 GMT
ADD file:8e81116368669ed3dd361bc898d61bff249f524139a239fdaf3ec46869a39921 in / 
# Mon, 23 May 2022 19:19:31 GMT
CMD ["/bin/sh"]
# Tue, 21 Jun 2022 20:21:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 21 Jun 2022 20:21:36 GMT
RUN apk add --no-cache libretls musl-locales musl-locales-lang tzdata zlib     && rm -rf /var/cache/apk/*
# Tue, 21 Jun 2022 20:23:43 GMT
ENV JAVA_VERSION=jdk-18.0.1+10
# Tue, 21 Jun 2022 20:23:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ab72b28e1ce896e6b11e2b362c12c36007ebe9963d8954bc11e637be1f024dfe';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.1%2B10/OpenJDK18U-jdk_x64_alpine-linux_hotspot_18.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 21 Jun 2022 20:23:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jun 2022 20:23:58 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 21 Jun 2022 20:23:58 GMT
CMD ["jshell"]
# Tue, 21 Jun 2022 20:46:59 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Jun 2022 20:46:59 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Jun 2022 20:46:59 GMT
WORKDIR /tmp
# Tue, 21 Jun 2022 20:47:00 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Tue, 21 Jun 2022 20:47:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Jun 2022 20:47:00 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Jun 2022 20:47:21 GMT
RUN boot
# Tue, 21 Jun 2022 20:47:22 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 21 Jun 2022 20:47:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Jun 2022 20:47:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2408cc74d12b6cd092bb8b516ba7d5e290f485d3eb9672efc00f0583730179e8`  
		Last Modified: Mon, 23 May 2022 19:09:38 GMT  
		Size: 2.8 MB (2798889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4177d2591259bff2bae6f43f12721dbe4ed5aac24fb0991377a3d27cdd534e`  
		Last Modified: Tue, 21 Jun 2022 20:26:07 GMT  
		Size: 477.8 KB (477755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce063f20f3f48aa654699a8e40506412bceb1e805998d7959dd66d4b521af4b`  
		Last Modified: Tue, 21 Jun 2022 20:28:44 GMT  
		Size: 192.9 MB (192862501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0092728308d3b3e20f1e4fe1a4d2d7df28e4aaf1cf6c3e284e846452de11b684`  
		Last Modified: Tue, 21 Jun 2022 20:28:29 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a26c0e17c8e3c115c11f1c963a517c881cf3bd29327ba4ea7f98d0a1c69e7d4`  
		Last Modified: Tue, 21 Jun 2022 20:50:55 GMT  
		Size: 850.3 KB (850290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892bf085502befd0f3585c33d423f43af6cd639c13144a2f0259dd68e2c1ea34`  
		Last Modified: Tue, 21 Jun 2022 20:50:58 GMT  
		Size: 58.8 MB (58820622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7665d23f0df0610dbdb25dff39f383203182079cc6811a1c6845342908d856f`  
		Last Modified: Tue, 21 Jun 2022 20:50:55 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
