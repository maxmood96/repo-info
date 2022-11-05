## `clojure:temurin-11-boot-alpine`

```console
$ docker pull clojure@sha256:2de7a5f89c82e1612e21b6ea727ad69961907a74caa4b5921ca7bff18639d8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-11-boot-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:bfea33f577767d1fdac85113814e17d186191820b3399c7ac2adb8fa973ff5a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 MB (268339547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b933a8b4e3d1a59910732443bb54083add3d499918acb4377148f0e3d0933b3`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 16:53:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 07 Oct 2022 16:53:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Oct 2022 16:53:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Oct 2022 16:53:21 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Fri, 04 Nov 2022 23:20:57 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:21:21 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='774d5955c09893dda14e3eb0fd3e239a6b2cec58615fcf4ec68747260b6e1cc1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Fri, 04 Nov 2022 23:21:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 04 Nov 2022 23:21:24 GMT
CMD ["jshell"]
# Sat, 05 Nov 2022 01:11:12 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 05 Nov 2022 01:11:12 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 05 Nov 2022 01:11:12 GMT
WORKDIR /tmp
# Sat, 05 Nov 2022 01:11:14 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Sat, 05 Nov 2022 01:11:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 05 Nov 2022 01:11:14 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 05 Nov 2022 01:11:35 GMT
RUN boot
# Sat, 05 Nov 2022 01:11:36 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5835cc7e6eb64b728c9694dd72d8aede877af0a2ec44f981847853af9abbf5`  
		Last Modified: Fri, 07 Oct 2022 16:57:51 GMT  
		Size: 12.0 MB (12041341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326222305ee7ba2cd4c5b9421222ea3b98c1fcdf5614f10686612cd9e48d4944`  
		Last Modified: Fri, 04 Nov 2022 23:27:19 GMT  
		Size: 193.8 MB (193812570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f17b778e5911ba3c3e61d32e7eeb30f4b62bf95d1ced95b7cf7c1f152fe40da`  
		Last Modified: Fri, 04 Nov 2022 23:27:05 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c40aeba0d2c5d8f4b48d24e39c20df19f6ab3b00ebfa074546e280b7222a9d`  
		Last Modified: Sat, 05 Nov 2022 01:25:31 GMT  
		Size: 858.8 KB (858813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04162c201affc01cf1d43637f5008a891ecd0646cff99085669bc70e28be39e4`  
		Last Modified: Sat, 05 Nov 2022 01:25:34 GMT  
		Size: 58.8 MB (58820589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
