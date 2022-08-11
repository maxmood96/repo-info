## `clojure:boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:e36e4d30d52044d345217387f37f988fcb77abcebb1e89936ce8eabbdf9213f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:b16f55207689c5a8dd0381fec6d5d394235fba09d11a3b2dca7d8e295e5fea11
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.0 MB (265986299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c424417bc0d2ca8a54e5171f3ef6f34de997cd1c22b00a9786c4bbbd880428b6`
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
# Thu, 11 Aug 2022 19:23:40 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 11 Aug 2022 19:24:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b356512c955f2d1a66b714ab3acaad942d04f80603af7dcd56e1fe5baeaeeda';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 11 Aug 2022 19:24:07 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 11 Aug 2022 19:24:07 GMT
CMD ["jshell"]
# Thu, 11 Aug 2022 20:09:15 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Aug 2022 20:09:15 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Aug 2022 20:09:15 GMT
WORKDIR /tmp
# Thu, 11 Aug 2022 20:09:17 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Thu, 11 Aug 2022 20:09:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Aug 2022 20:09:17 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Aug 2022 20:09:36 GMT
RUN boot
# Thu, 11 Aug 2022 20:09:37 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 11 Aug 2022 20:09:37 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Aug 2022 20:09:37 GMT
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
	-	`sha256:cdeb5c36e3987cc21fc57eda9f965b006f42903399b536e06aef37ff462fb27e`  
		Last Modified: Thu, 11 Aug 2022 19:35:23 GMT  
		Size: 191.4 MB (191449939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32867cbcebbe8d6d561e769be3ba911e76008280e8de56032b16a7b21538e5ba`  
		Last Modified: Thu, 11 Aug 2022 19:35:08 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe2d74d58dacd2a23969ce0a5fdb4c9c607ecccd717532b5bbabe6a76ff293b`  
		Last Modified: Thu, 11 Aug 2022 20:20:46 GMT  
		Size: 859.3 KB (859303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768d738beb534ca2b1695275ba75ac6af64c49fd32691e4bda485cc03615db52`  
		Last Modified: Thu, 11 Aug 2022 20:20:49 GMT  
		Size: 58.8 MB (58820351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1134e1a2f648f24223b06e878bd90aef50203b2ef1f0d3c6a5a7ae585c9a8cc`  
		Last Modified: Thu, 11 Aug 2022 20:20:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
