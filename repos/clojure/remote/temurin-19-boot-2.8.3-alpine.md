## `clojure:temurin-19-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:4ddad62f4c7244ccdc90ddc903fc7c1a0d86a7146b90baf60db57b4f61c42ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-19-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:5a66bea5bcf6f40bd1e253898fef950fa3125b2d75c0d275cd8fb0edcc9ff852
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274578312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614629655b9fada530220d15ace33cefdbb17a831892beb71496c214abb0fc06`
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
# Mon, 26 Sep 2022 23:20:38 GMT
ENV JAVA_VERSION=jdk-19+36
# Mon, 26 Sep 2022 23:20:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='2a073c3cc977317baf7c0c4995be38d33e3ed74e9fa4ac075933016e68f18252';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_alpine-linux_hotspot_19_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Mon, 26 Sep 2022 23:20:59 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 26 Sep 2022 23:20:59 GMT
CMD ["jshell"]
# Wed, 28 Sep 2022 00:25:22 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 28 Sep 2022 00:25:23 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 28 Sep 2022 00:25:23 GMT
WORKDIR /tmp
# Wed, 28 Sep 2022 00:25:24 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Wed, 28 Sep 2022 00:25:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 28 Sep 2022 00:25:24 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 28 Sep 2022 00:25:58 GMT
RUN boot
# Wed, 28 Sep 2022 00:25:59 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 28 Sep 2022 00:25:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Sep 2022 00:25:59 GMT
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
	-	`sha256:6ae12e307c9434ce280b5e193d9093d7c6be535d2c8b398c93a08cb53cc1a723`  
		Last Modified: Mon, 26 Sep 2022 23:25:17 GMT  
		Size: 200.0 MB (200041303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684feb0a923f6b8ea0137a7424fa76f492fa3646eb1305791ac45c0d44bed504`  
		Last Modified: Mon, 26 Sep 2022 23:25:00 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c20f41d391b3f30e96d501b353984f6a9d158f818b4e00bf0e371fa1a2268b5`  
		Last Modified: Wed, 28 Sep 2022 00:32:04 GMT  
		Size: 859.3 KB (859328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285fce38481cd38af6cf15b2167c1dc6acaa71b867f03b43338403091a507af0`  
		Last Modified: Wed, 28 Sep 2022 00:32:07 GMT  
		Size: 58.8 MB (58820975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00eca85220b443abf057abb25829c590eed8c4330e89ab77a87ac549d2940d0`  
		Last Modified: Wed, 28 Sep 2022 00:32:04 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
