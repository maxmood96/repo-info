## `clojure:temurin-18-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:7885abda9be9ab6f126c7a736b1ac6065127f25bb2da8ab6af5240ec65e969ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-18-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:3f6d729864b0d03c44d7e35bdd0711844c6e621c762c5acb6cd21b8347e57c79
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267448539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eaa030b3a7de9e2ea26b913bf87448b28eeb06a7945e004e53c69ad629fdaf4`
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
# Mon, 29 Aug 2022 18:27:26 GMT
ENV JAVA_VERSION=jdk-18.0.2.1+1
# Mon, 29 Aug 2022 18:27:42 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='478c8f56dec7378ed8c687e8d7d0fbf729973c62c497cfc8cf58bd621849d764';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2.1%2B1/OpenJDK18U-jdk_x64_alpine-linux_hotspot_18.0.2.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Mon, 29 Aug 2022 18:27:45 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 29 Aug 2022 18:27:45 GMT
CMD ["jshell"]
# Mon, 29 Aug 2022 18:52:48 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 29 Aug 2022 18:52:48 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 29 Aug 2022 18:52:48 GMT
WORKDIR /tmp
# Mon, 29 Aug 2022 18:52:50 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Mon, 29 Aug 2022 18:52:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 29 Aug 2022 18:52:50 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 29 Aug 2022 18:53:24 GMT
RUN boot
# Mon, 29 Aug 2022 18:53:24 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Mon, 29 Aug 2022 18:53:24 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 29 Aug 2022 18:53:24 GMT
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
	-	`sha256:740e3cdadfebcaafba907a9fba5363e7b2da3e4636a0340e58c190daa0667e08`  
		Last Modified: Mon, 29 Aug 2022 18:31:41 GMT  
		Size: 192.9 MB (192911706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71f0ae6ae71d4a6dd24382195739038e7f96208259eb6100971cd8eed81943a`  
		Last Modified: Mon, 29 Aug 2022 18:31:26 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5356b9bbc41a559a103f3656a95237a0adb525aacb054e5dbab21e9fa2dccb2`  
		Last Modified: Mon, 29 Aug 2022 18:59:28 GMT  
		Size: 859.3 KB (859317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c8b6cadb16161fd042d71f1ef36686349fa21b7008d6ef9b17645efb0111c2`  
		Last Modified: Mon, 29 Aug 2022 18:59:31 GMT  
		Size: 58.8 MB (58820811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e416854800ccc0ada7708cac212db0e5e0d2e99bd96ec6c78e13ee3e7db8fc`  
		Last Modified: Mon, 29 Aug 2022 18:59:28 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
