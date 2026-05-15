## `clojure:temurin-17-tools-deps-alpine`

```console
$ docker pull clojure@sha256:2714eaacd3bca2a2faf796ef168fa1d4cef7dbc06d6eb87b7857aebe666ddc2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:88dc1ba9eac0306d84b5f38e4c9d3d61b442d119a4b2cfba4894bce8cb7b32c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195650444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6905930e9dbbf8c5010b49fda57257a7534ef2c55ad2322cc7d998e7259fd34`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 23:58:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:58:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:58:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:58:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 07 May 2026 23:58:34 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Thu, 07 May 2026 23:58:42 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='960b4090b75a887bb21a915a294bee3a97cd11876967c95e5bd29d9ec4812e17';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 07 May 2026 23:58:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:58:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:58:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 May 2026 23:58:43 GMT
CMD ["jshell"]
# Thu, 14 May 2026 23:34:39 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:39 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:42 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 14 May 2026 23:34:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:34:42 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:34:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b50ae58d435408a9b026fe52e1670bc1fa8333eabfe9bf8732808b503921e21`  
		Last Modified: Thu, 07 May 2026 23:58:58 GMT  
		Size: 21.3 MB (21336223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede0d10cee20aac36e35f4a5f8b5277bf42d4cb4c8d9a9d4fcdccdc80bc721a6`  
		Last Modified: Thu, 07 May 2026 23:59:01 GMT  
		Size: 145.1 MB (145051725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97e55ba8d37d6d0466dfc5f33fb9646c28947c3dc8386294a7f1f12a35edc2c`  
		Last Modified: Thu, 07 May 2026 23:58:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665e255b26ac403ea595f439a3807b4421a1347f75ad3570ce930c2ea8a8a4a6`  
		Last Modified: Thu, 07 May 2026 23:58:57 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4563c43a4060ab4f22b32e4a7cd0fff16912ffb79181dff8ecf0012d096d85a`  
		Last Modified: Thu, 14 May 2026 23:34:52 GMT  
		Size: 25.4 MB (25394842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4506cd4e6a489fa29d5d46a990a7d484c40fecadfe92d277b4ae9ac45b70ab28`  
		Last Modified: Thu, 14 May 2026 23:34:51 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d734467164494ce1a0ee2ede81184a3da5bc9eaa9d2a6d6073b4a424680d95`  
		Last Modified: Thu, 14 May 2026 23:34:52 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:4171b238b0be24e10a6da9bfad68b00e8a073b60b338ecb4b6fda9a3239a5da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eec9235e64b7be72f6cf0cd4624f6d7106236ede087b0373a4176a68bc35c13`

```dockerfile
```

-	Layers:
	-	`sha256:25dc78f4e5d339ebce4a5aaf1b9e47f1b012e2c105126530a27bfca7bd1ba4ff`  
		Last Modified: Thu, 14 May 2026 23:34:51 GMT  
		Size: 1.3 MB (1308723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd70f9805866dd533c27cc4f4f6b078b9b64ade946e72d26870c391cde173ea2`  
		Last Modified: Thu, 14 May 2026 23:34:51 GMT  
		Size: 15.4 KB (15432 bytes)  
		MIME: application/vnd.in-toto+json
