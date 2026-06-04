## `clojure:temurin-17-alpine`

```console
$ docker pull clojure@sha256:b2ed116d2aa4afa393fb69919fa22a82c474e1181620de9feb4b8976a97f006b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-17-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:11e9b8aef5b0ad1948a2b0eba2f7153f2415d2900d9d05a69aef0f0ea47bea12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192475944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807a4d6b49b9632f92e6eddd3f5e38818e36cf846b2b0320997364610c3ebdfa`
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
# Thu, 04 Jun 2026 17:45:37 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:37 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:45:39 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 04 Jun 2026 17:45:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:45:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:45:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:45:40 GMT
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
	-	`sha256:6c88684b2d80a1843be3c0c05a3077f7e4d3aece1e4c73713522a9fed0b30494`  
		Last Modified: Thu, 04 Jun 2026 17:45:49 GMT  
		Size: 22.2 MB (22220341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0bc6409fd829ac4c0fe44e7156b364361133f39073547a5c8ecccc822ab289`  
		Last Modified: Thu, 04 Jun 2026 17:45:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a010939ddc41db1dcf685a2d28512d8c2d218a2bc2021037545ad7f1ce4b80c6`  
		Last Modified: Thu, 04 Jun 2026 17:45:49 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:c3a0b6a8dfa2588cd1025fbe324429b216b1a1f767fe6db5d0bd2c2505b22305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1319728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab5a10a6ced0a442b1908d6315474624a8aa68a45c94040f0da07e4ae6bb8a6`

```dockerfile
```

-	Layers:
	-	`sha256:a77454a0e15f2e6b2d38c6ed3c5308aa5844e7ce8eb9cdd30001e5698097ef03`  
		Last Modified: Thu, 04 Jun 2026 17:45:49 GMT  
		Size: 1.3 MB (1304296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cffbb22d6149b11e006723e5345066b2d204a25efa287f255d0674c5ce8107c`  
		Last Modified: Thu, 04 Jun 2026 17:45:48 GMT  
		Size: 15.4 KB (15432 bytes)  
		MIME: application/vnd.in-toto+json
