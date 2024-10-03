## `clojure:temurin-23-alpine`

```console
$ docker pull clojure@sha256:1d2f5bdb1d9f27bb68690b9758443755728ad41d9932f80989a79bebdbc13f08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-23-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:b2ec713357cf9df83cd3fb56842037ad2387512dd47cc33e9f9928ecdaf474d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208712083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15c6c0abcba3a439d0269f49c9aa2e6f919a483558770e07e40dd7f805f8593`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7e842c9b8a44a5a21d83a3e38ae3b141cfbdb429dde70ff264d3da4bff44e1c7';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='bff4c78f30d8d173e622bf2f40c36113df47337fc6d1ee5105ed2459841165aa';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c34627c847892ee87160ccb0488eb4484039dd04d400e9e86561f15459495`  
		Last Modified: Fri, 06 Sep 2024 22:44:13 GMT  
		Size: 14.0 MB (14032627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6515fe7a20d9848ae77a0dd2fe590ca44111e3a72a0696fa6b73e346b3514a4f`  
		Last Modified: Wed, 18 Sep 2024 21:24:27 GMT  
		Size: 165.5 MB (165476640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4108fead0afd7aed117dbfb1ae2a0bba1a6d4427cc8292f8fbc79e9bbcf4280`  
		Last Modified: Wed, 18 Sep 2024 21:24:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6363deaddf9a060529cefe0fdd8773e4a9daa37eff2e63cfdc5ccefed75bd5ff`  
		Last Modified: Wed, 18 Sep 2024 21:24:14 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251bb8710435fabd6ed41c801a407d6063c02543a1d3fd748721c041e1c4df2a`  
		Last Modified: Thu, 03 Oct 2024 19:00:37 GMT  
		Size: 25.6 MB (25575691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21910b4ab00dff7bf14a3fb187e88448c362a0f9a2f117acfedf1a69c9f1798c`  
		Last Modified: Thu, 03 Oct 2024 19:00:36 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c720d70915623e237dcd17e1d94b0b09d70480fd7c672fb66639afd56ea10`  
		Last Modified: Thu, 03 Oct 2024 19:00:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:62bbd62c5145e997270021f7958161d3bf2ac982b77d7da7db488ee6d1b43e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1167520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c748b1fe7f32f802666e6815890edee62f2264b51574f41169390b13838c5f54`

```dockerfile
```

-	Layers:
	-	`sha256:e9a81be1f669523e4e58e0a417bdd45b295ff4ab1236d42c2d95a8c51005e212`  
		Last Modified: Thu, 03 Oct 2024 19:00:37 GMT  
		Size: 1.2 MB (1152113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48cb8b0056ba0f797c0d79fbbb08d272beb176862d0a455701fce5291a6a7cd5`  
		Last Modified: Thu, 03 Oct 2024 19:00:37 GMT  
		Size: 15.4 KB (15407 bytes)  
		MIME: application/vnd.in-toto+json
