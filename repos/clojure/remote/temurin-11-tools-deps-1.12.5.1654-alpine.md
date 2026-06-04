## `clojure:temurin-11-tools-deps-1.12.5.1654-alpine`

```console
$ docker pull clojure@sha256:8d6eb156dbc80b791a98f5bc3d88ff86846b5d2e5fd95bace5ccb14d75e83158
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.5.1654-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:2cd2936862c254b1205d85d3f03bb0a801639aeb956f7776a4b9c407ce371255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.1 MB (184077585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdd14b52480cd9e9eaa4a8f81647ca756618d74c00e933b0bf84e9e5f76ceb4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 29 Apr 2026 22:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 22:44:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 22:44:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Apr 2026 22:44:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 29 Apr 2026 22:44:05 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 22:44:16 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='ed06a4b8381786a6e8091c10539856675497d2b821cd2d0200cc5b65f453b982';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 29 Apr 2026 22:44:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 29 Apr 2026 22:44:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 29 Apr 2026 22:44:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 Apr 2026 22:44:17 GMT
CMD ["jshell"]
# Thu, 04 Jun 2026 17:43:15 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:43:15 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:43:19 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 04 Jun 2026 17:43:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:43:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c175c39880efd27b1b0b6f4b68db4424c3664c1899709c2068bc4301855817b`  
		Last Modified: Wed, 29 Apr 2026 22:44:33 GMT  
		Size: 16.8 MB (16837661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23b06a78b6e346324b4ccae7f54064e05cc8059b37b593caf9730186b81c6cd`  
		Last Modified: Wed, 29 Apr 2026 22:44:36 GMT  
		Size: 141.1 MB (141074590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b27e99b60546186d5398cb848761881034ad4a2495edd58778348608ab13b34`  
		Last Modified: Wed, 29 Apr 2026 22:44:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5cbe1f675378862d1c920e9f972f54caa6e00e0ef8bf232fd844c01fa839ac`  
		Last Modified: Wed, 29 Apr 2026 22:44:32 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192ae30c6d1a3fc191946e124f9c785ee41f497f389044a9c9a1d5d3635979b2`  
		Last Modified: Thu, 04 Jun 2026 17:43:29 GMT  
		Size: 22.3 MB (22298085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7fced235f0d5a86fe8f8e878f146b6dfdbfd3005bb1ec66bf8c9136dcac67b`  
		Last Modified: Thu, 04 Jun 2026 17:43:28 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1654-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:cccba0e157a90232837e8fbb08405b91541c90c5d655312dff9145614fe5a189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1221373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4462c460b28b881069880d93ced8a3ad27e98d036576ca357d6f20c1a6e1c410`

```dockerfile
```

-	Layers:
	-	`sha256:72d34a29c2b80498c24016d24701b7924415ff34187be5180f148c694aa9f7b3`  
		Last Modified: Thu, 04 Jun 2026 17:43:28 GMT  
		Size: 1.2 MB (1207977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:211da4f2e1d993fa851b02d97ac764e629a30af0739eafa3c28fef8164ca6e25`  
		Last Modified: Thu, 04 Jun 2026 17:43:28 GMT  
		Size: 13.4 KB (13396 bytes)  
		MIME: application/vnd.in-toto+json
