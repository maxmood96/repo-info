## `clojure:temurin-8-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:86d76005433f352a3da076f2c01b8de391b4ce631c3943ab2da9aea8a9db4391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-8-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:82ad64ba17735f2a9620e9a85b0fc0eeab4e222318df85e810f802c271336ee3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.0 MB (175972495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7604e9b6b7dcd57e5cb1f680ee1d0f22849bc1eb05ae20d050418ca53f0cd3a3`
-	Default Command: `["boot","repl"]`

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
# Thu, 11 Aug 2022 19:19:40 GMT
ENV JAVA_VERSION=jdk8u345-b01
# Thu, 11 Aug 2022 19:19:49 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='e5dcb8f947b687597f92fa80c008a2a17ce86f739dd6dce7ca741921621acb21';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u345-b01/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u345b01.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 11 Aug 2022 19:19:50 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 11 Aug 2022 20:01:50 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Aug 2022 20:01:50 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Aug 2022 20:01:50 GMT
WORKDIR /tmp
# Thu, 11 Aug 2022 20:01:52 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Thu, 11 Aug 2022 20:01:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Aug 2022 20:01:52 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Aug 2022 20:02:10 GMT
RUN boot
# Thu, 11 Aug 2022 20:02:11 GMT
CMD ["boot" "repl"]
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
	-	`sha256:0785c5e3ab89a9dfa7638fd78c1fc211af4fab5cc276025f6f0bd09e13f0581c`  
		Last Modified: Thu, 11 Aug 2022 19:29:59 GMT  
		Size: 101.4 MB (101436564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758050903e3eb20e7b6f221721deaa4ec312c37440aec34aa44fdf73788659b0`  
		Last Modified: Thu, 11 Aug 2022 19:29:50 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180158ef62348b72b48478e731fc4fa5a6307bfe60c1433795dc530c17cdb77e`  
		Last Modified: Thu, 11 Aug 2022 20:17:30 GMT  
		Size: 859.3 KB (859317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0032c0cc7ddf05b5091cf848d8816fc9d52505c50689b289bdb497d305f5960a`  
		Last Modified: Thu, 11 Aug 2022 20:17:33 GMT  
		Size: 58.8 MB (58820327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
