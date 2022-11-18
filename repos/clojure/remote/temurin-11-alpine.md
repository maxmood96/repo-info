## `clojure:temurin-11-alpine`

```console
$ docker pull clojure@sha256:af6b9fb45881ad7820a66c78f76a34af817d967a096947095a3d0cba335cfcca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-11-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:4e3dc79cccd2e2f6529fc710de536c9530c6f06272f8276a733c2ed130384c91
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238744722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42fcbbe8ccd94f00817f9f73c5d98bcc7ff1f37f0a8a17e8f1ec9e5515b2492f`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:12:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 12 Nov 2022 05:12:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 05:12:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 12 Nov 2022 05:12:06 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Sat, 12 Nov 2022 05:12:49 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Sat, 12 Nov 2022 05:13:02 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='774d5955c09893dda14e3eb0fd3e239a6b2cec58615fcf4ec68747260b6e1cc1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Sat, 12 Nov 2022 05:13:05 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 12 Nov 2022 05:13:05 GMT
CMD ["jshell"]
# Fri, 18 Nov 2022 22:23:39 GMT
ENV CLOJURE_VERSION=1.11.1.1200
# Fri, 18 Nov 2022 22:23:39 GMT
WORKDIR /tmp
# Fri, 18 Nov 2022 22:23:44 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "694381cb78d44f143bdcc38657507f012ebac4009bc57cec67abef1675447878 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Fri, 18 Nov 2022 22:23:44 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 18 Nov 2022 22:23:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9822f87bb1185b1d8f81aa09fc8a20796bb3db4c90da28c6177e0fd8a3d8d3`  
		Last Modified: Sat, 12 Nov 2022 05:16:37 GMT  
		Size: 12.0 MB (12030631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec5de7441ae3d196472e565fe52f43eb0e27b60813e788d87440a3578ca867d`  
		Last Modified: Sat, 12 Nov 2022 05:17:32 GMT  
		Size: 193.8 MB (193812490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0dd61568d72d7bb5ed1797c90e222d6e5cd711c8339a9672cbf0a94378b103`  
		Last Modified: Sat, 12 Nov 2022 05:17:18 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ff5aa97bf98782680cbfe8a0e5acb47916011d2edf3d11c5f4c7d9d8232d81`  
		Last Modified: Fri, 18 Nov 2022 22:33:42 GMT  
		Size: 30.1 MB (30094528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd1c4da126b7946cfb5ecb4cabf072bdc27ee96a2b4819f4d7bab001990aaf7`  
		Last Modified: Fri, 18 Nov 2022 22:33:39 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
