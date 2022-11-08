## `clojure:temurin-17-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:208af8bfb8c67a0b470c358e7580018058d5be5799dd99f8b63e33462caac3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-17-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:4ef4102e61f086b41421841f3814b423ba8224ba43a0aed08e2f2ce8988e7f2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266264507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f63c99b4e20d00d2ed7937a8ab6f2e1d634e02472623dd33a2f30b3d93013d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Mon, 07 Nov 2022 20:20:20 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Mon, 07 Nov 2022 20:20:45 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='cb154396ff3bfb6a9082e3640c564643d31ecae1792fab0956149ed5258ad84b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.5%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.5_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Mon, 07 Nov 2022 20:20:48 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 07 Nov 2022 20:20:48 GMT
CMD ["jshell"]
# Mon, 07 Nov 2022 20:46:56 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 07 Nov 2022 20:46:57 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 07 Nov 2022 20:46:57 GMT
WORKDIR /tmp
# Mon, 07 Nov 2022 20:46:58 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Mon, 07 Nov 2022 20:46:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 07 Nov 2022 20:46:59 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 07 Nov 2022 20:47:20 GMT
RUN boot
# Mon, 07 Nov 2022 20:47:20 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Mon, 07 Nov 2022 20:47:20 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 07 Nov 2022 20:47:20 GMT
CMD ["repl"]
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
	-	`sha256:11c1d96634150955afe088fe282afe9245e873ff0ae4e04b9279c56b67f9d1f0`  
		Last Modified: Mon, 07 Nov 2022 20:24:39 GMT  
		Size: 191.7 MB (191737167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d6368dfb564164f6091c1e3b40fd2c57c89c558a6d7ed91b8796208629ce41`  
		Last Modified: Mon, 07 Nov 2022 20:24:24 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd3855d854432096e01e0138c1a451787dd849ae5a486872ef5f2a7edaff220`  
		Last Modified: Mon, 07 Nov 2022 20:57:00 GMT  
		Size: 858.8 KB (858813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93f411c1db3f4944e52b9f87dca029082cf85250abdbf4d18caad4d42590fc7`  
		Last Modified: Mon, 07 Nov 2022 20:57:03 GMT  
		Size: 58.8 MB (58820553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab02f4eeaabfc36d52414fee6aa59d0fe92f40b7c7f2a3adfac9ad5ff61bbeb`  
		Last Modified: Mon, 07 Nov 2022 20:57:00 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
