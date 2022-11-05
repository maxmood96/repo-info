## `clojure:temurin-11-tools-deps-alpine`

```console
$ docker pull clojure@sha256:85006dfce5db2c6dc7432e1a24eee154846a237db10ca6b3f9d8a47b0399af73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-11-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:fbf23c657f3ef58126719fbeb1d54edfb983fd4620cfe6ffaef99f9135753d27
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238744722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b57600b8243ed799d4982c8a2b62e7b4ff1bf2e94dbb39542bb5a996f5e56f`
-	Default Command: `["clj"]`

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
# Sat, 05 Nov 2022 01:16:33 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Sat, 05 Nov 2022 01:16:33 GMT
WORKDIR /tmp
# Sat, 05 Nov 2022 01:16:38 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Sat, 05 Nov 2022 01:16:38 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 05 Nov 2022 01:16:38 GMT
CMD ["clj"]
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
	-	`sha256:e4180fd9e76989e3ea72b8cb989ab89a94242190cf94cb921f9d378144439a12`  
		Last Modified: Sat, 05 Nov 2022 01:27:57 GMT  
		Size: 30.1 MB (30083953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf338432f42b2c4361ef2c72e263eac2ae774bf6546f0036e06a843706ccb873`  
		Last Modified: Sat, 05 Nov 2022 01:27:55 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
