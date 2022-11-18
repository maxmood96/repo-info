## `clojure:temurin-8-tools-deps-1.11.1.1200-alpine`

```console
$ docker pull clojure@sha256:4fdf105a4660408ac05be1bd0d1234eb6e6fd7ef1e2c52a58826a79eb339b8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-8-tools-deps-1.11.1.1200-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:9f072abd2acc0d78aa91ce509e18d14f78adb1ba7751d75fd8f92ed07e31b8be
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146383733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1f7977957adf323fca78b903fd95de5ab36822be6b7173a51913179e2bdb26`
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
# Sat, 12 Nov 2022 05:12:06 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Sat, 12 Nov 2022 05:12:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='aa782e3c561b041a5730cbe728c210e234db71fa7222bd8b661f9f4df7799375';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Sat, 12 Nov 2022 05:12:16 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Fri, 18 Nov 2022 22:21:09 GMT
ENV CLOJURE_VERSION=1.11.1.1200
# Fri, 18 Nov 2022 22:21:10 GMT
WORKDIR /tmp
# Fri, 18 Nov 2022 22:21:15 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "694381cb78d44f143bdcc38657507f012ebac4009bc57cec67abef1675447878 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Fri, 18 Nov 2022 22:21:15 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 18 Nov 2022 22:21:15 GMT
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
	-	`sha256:4b09080cdf0f1bfc6de2b63e0d2002151f5d75cdf7abf67fdf79198614401955`  
		Last Modified: Sat, 12 Nov 2022 05:16:44 GMT  
		Size: 101.5 MB (101451502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57ea51d90384ab5a84e05b0af4fef16cf6e01763b43a0b2a1e18939a7a3a01a`  
		Last Modified: Sat, 12 Nov 2022 05:16:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6d5e8d1490832a6dceba723b62cd5fe42dd594b12b566b3d5a5695d2526d27`  
		Last Modified: Fri, 18 Nov 2022 22:32:03 GMT  
		Size: 30.1 MB (30094542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e144ca00b2c48cb3cd441576c4a20a45e686096c3b595eafb5ef495a943f1d`  
		Last Modified: Fri, 18 Nov 2022 22:32:01 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
