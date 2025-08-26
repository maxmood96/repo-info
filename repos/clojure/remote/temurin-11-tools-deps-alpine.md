## `clojure:temurin-11-tools-deps-alpine`

```console
$ docker pull clojure@sha256:345e88dec9b62076dfa0309079af97bb7a18f76adba640da0a019a945e406c8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:1859b31b1bf90f956b8a8b114f9896aaac49146b48c9c09b40588ac63ead18b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.4 MB (186399290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3337dc1c6033596825bc01f546a6a37720b20995885e7d7c71c753956c9e541e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7e9e5241d1378d75ae70e9b216d0d51d3aa2e61e187e92e09d117cb613e16ee4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32368a88ab88c011f9799e221ffa3a76a0557d8f869cb207cb6f61e0a1955762`  
		Last Modified: Mon, 04 Aug 2025 19:11:15 GMT  
		Size: 16.3 MB (16280183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d648ad0c3205513ffbb1e09ea89959604157e09c4cc8d981f5fa1b1e777c4f0`  
		Last Modified: Mon, 04 Aug 2025 20:12:02 GMT  
		Size: 140.8 MB (140841600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593271197e067f9172951dae5461f06c964edf69c2598534299fed88688fb565`  
		Last Modified: Mon, 04 Aug 2025 19:11:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79e640d46de60752e85b9c04c3a723384b01154acc6635a1cda3176da6ada69`  
		Last Modified: Mon, 04 Aug 2025 19:11:16 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f7992e26af63b1e90c26a71494045e17303939f9c479359758e74e8b355e01`  
		Last Modified: Tue, 26 Aug 2025 17:27:24 GMT  
		Size: 25.5 MB (25474756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2054300f7f0f15bf6bf734c14d541f7cb432faafc6161b84498d54edfd4ac73`  
		Last Modified: Tue, 26 Aug 2025 17:27:22 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:83e287dd5d1aee3407633b52704d043f46703905935d13c5e6162e9225546b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1210005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c058abf9270599230dfa6eca4b365e622440ce3f3fa61fadecb29979dbf3b3c`

```dockerfile
```

-	Layers:
	-	`sha256:2726a1274274bda7e43efd974e662cb3eeee66ee7f68450f9265e29ba83d500b`  
		Last Modified: Tue, 26 Aug 2025 18:34:53 GMT  
		Size: 1.2 MB (1196567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a789a9c8901f0e62723a7b17d2e5b7dee674d653acdcfb9664ed0742aeba1a4`  
		Last Modified: Tue, 26 Aug 2025 18:34:54 GMT  
		Size: 13.4 KB (13438 bytes)  
		MIME: application/vnd.in-toto+json
