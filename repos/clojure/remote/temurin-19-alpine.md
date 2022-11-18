## `clojure:temurin-19-alpine`

```console
$ docker pull clojure@sha256:ea8292ab88e4ab99e5ede77fa9e6764b603f7c3db53f35d4dde345501e478a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-19-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:5ad36c79856820752fdca13fb98a4056ca747652ecf607b79d51589baf102f13
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 MB (245236268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f4c0378dbbd7a3675fbb71603c74a639af25ca81c3081f8136b4d242ef7af3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
# Sat, 12 Nov 2022 05:14:15 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Sat, 12 Nov 2022 05:14:35 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76cfcdf47cdf24331b51939fd2840fd387cf62471da99e4718e2e42b486a9270';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_alpine-linux_hotspot_19.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Sat, 12 Nov 2022 05:14:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 12 Nov 2022 05:14:38 GMT
CMD ["jshell"]
# Fri, 18 Nov 2022 22:27:33 GMT
ENV CLOJURE_VERSION=1.11.1.1200
# Fri, 18 Nov 2022 22:27:34 GMT
WORKDIR /tmp
# Fri, 18 Nov 2022 22:27:39 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "694381cb78d44f143bdcc38657507f012ebac4009bc57cec67abef1675447878 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Fri, 18 Nov 2022 22:27:39 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 18 Nov 2022 22:27:39 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 18 Nov 2022 22:27:39 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 18 Nov 2022 22:27:40 GMT
CMD ["-M" "--repl"]
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
	-	`sha256:f334dab74d0be632884d565506362427e88b3b8eda99949b482e665eb16228db`  
		Last Modified: Sat, 12 Nov 2022 05:19:12 GMT  
		Size: 200.3 MB (200303572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8636564591f925d6b7ffa028b7dfbfbf6a7350dc9a5aeb52d0597856e2c40a0`  
		Last Modified: Sat, 12 Nov 2022 05:18:57 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec154d1a747ee9164ddaa7fd49fe6995ee042ebcb2fca3c693b16759a093f0d7`  
		Last Modified: Fri, 18 Nov 2022 22:37:22 GMT  
		Size: 30.1 MB (30094593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd34468aa8c30e1c223a891b03a4917a7ddfa7d2ca23030d39d3ae13c537a806`  
		Last Modified: Fri, 18 Nov 2022 22:37:19 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c793b524a495a8acf9ff2db0f727bafe0b4ead5a586ce2b5c188eb297f41b94d`  
		Last Modified: Fri, 18 Nov 2022 22:37:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
