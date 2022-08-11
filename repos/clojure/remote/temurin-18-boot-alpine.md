## `clojure:temurin-18-boot-alpine`

```console
$ docker pull clojure@sha256:3eb028be3dc7a1d53205d5a5c84ab2798e97f6faf6dd9ac87b372e792ede4676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-18-boot-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:d19bb3c41f3a14538a7b10854e468af741735d9e963120530eb0fe881bd5664e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267433917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3484dd42456e99e9df5334efc585e36e84c63bd7db0ea02a3246668d99116e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 11 Aug 2022 19:19:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 19:19:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 19:19:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Aug 2022 19:19:40 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Thu, 11 Aug 2022 19:26:26 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Thu, 11 Aug 2022 19:26:46 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='045670342a036fff98b2ee90279ed923dc8c92bebe6227a2a60f64ca84f4f7c8';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_alpine-linux_hotspot_18.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 11 Aug 2022 19:26:48 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 11 Aug 2022 19:26:48 GMT
CMD ["jshell"]
# Thu, 11 Aug 2022 20:12:27 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Aug 2022 20:12:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Aug 2022 20:12:27 GMT
WORKDIR /tmp
# Thu, 11 Aug 2022 20:12:29 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Thu, 11 Aug 2022 20:12:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Aug 2022 20:12:29 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Aug 2022 20:12:52 GMT
RUN boot
# Thu, 11 Aug 2022 20:12:53 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 11 Aug 2022 20:12:53 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Aug 2022 20:12:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107abfa4a9656cc98051eebaf02de090526191f4d53ab3733605b34f84513224`  
		Last Modified: Thu, 11 Aug 2022 19:29:52 GMT  
		Size: 12.1 MB (12050073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e679a78d83de61b5d0ed95e8ee0bdd2eaa0d7f7c320f381f9c5f66b63a3715f5`  
		Last Modified: Thu, 11 Aug 2022 19:38:17 GMT  
		Size: 192.9 MB (192897589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e0855aa0b135a5077a832ca2d50c73d5ea07687225d09966878018473d37aa`  
		Last Modified: Thu, 11 Aug 2022 19:38:03 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f85d8886cec13cefc4e0cb175e2908dd9819d1907c035e49ccb359149404be`  
		Last Modified: Thu, 11 Aug 2022 20:23:02 GMT  
		Size: 859.3 KB (859323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25989e5a8386f9cee3302e1e3e04cacd26747d180a2a80923b642bb57c82b09`  
		Last Modified: Thu, 11 Aug 2022 20:23:05 GMT  
		Size: 58.8 MB (58820300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da9d955ce541d254fd56dd7ab7b0283f655b5d815f1e948a20cc039113b7e59`  
		Last Modified: Thu, 11 Aug 2022 20:23:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
