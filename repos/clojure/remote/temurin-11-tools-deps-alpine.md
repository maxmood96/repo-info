## `clojure:temurin-11-tools-deps-alpine`

```console
$ docker pull clojure@sha256:8215d61ac54becbe87b46fee5180cad9229980a38660e7463d53b15c90c41d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-11-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:e0e8a63d79a8ba3dbe0be38896285c1f483622c65590e34dee849e88d8f87984
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.2 MB (238173620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae01c2d3aca9d13c6b3db3249c07cedc9883d01ecee709a7bc99811e561e081`
-	Default Command: `["clj"]`

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
# Thu, 11 Aug 2022 19:22:05 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 11 Aug 2022 19:22:19 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='32a93bd824cf34ccdde0881699a41a12722b4d8ff1d57294b2add2102432759b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 11 Aug 2022 19:22:21 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 11 Aug 2022 19:22:21 GMT
CMD ["jshell"]
# Thu, 11 Aug 2022 20:07:45 GMT
ENV CLOJURE_VERSION=1.11.1.1149
# Thu, 11 Aug 2022 20:07:45 GMT
WORKDIR /tmp
# Thu, 11 Aug 2022 20:07:51 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "9aadc1a1840a458517a6efb111eba72be93c17bbdc874c833ef781e77aacc55e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Thu, 11 Aug 2022 20:07:51 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 11 Aug 2022 20:07:51 GMT
CMD ["clj"]
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
	-	`sha256:70c470bb6c75a97511cd4a515fd90f0d7502e6717113972f191c1a4f5dc892d5`  
		Last Modified: Thu, 11 Aug 2022 19:32:30 GMT  
		Size: 193.5 MB (193453440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d6d5d99e5b9142e729582ebacd318dedcb54f270e2386f0a8c1c0a3194b28b`  
		Last Modified: Thu, 11 Aug 2022 19:32:16 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7565f0a9cbc8e32edb40f20f14073db42191f3c9884df14f5d81cd76b9a7514`  
		Last Modified: Thu, 11 Aug 2022 20:20:33 GMT  
		Size: 29.9 MB (29863257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8df0859c02127ebfbbcb3720672ba11642157e822cdab2e71c78196381ebab`  
		Last Modified: Thu, 11 Aug 2022 20:20:31 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
