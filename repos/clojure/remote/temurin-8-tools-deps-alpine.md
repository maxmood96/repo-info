## `clojure:temurin-8-tools-deps-alpine`

```console
$ docker pull clojure@sha256:994338726b8dfbe8b85c9d29fc77129cdad59b3ab62151b82b6ea428b9596757
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:1728d2933ca14c9d6e99d7d0f99aef9c6f143dd857e988374d85bf8bd7dea006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97613081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9563ce2a0893532126d006520d1f4886cc047d8537ad3c5e58e3b8561e6dcd2f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='be8abae7586c328ceb3252aefed9e51c29be91616968c0130b41e7e57c846f0f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7141be485741d41116a845b669643de63ccceb87c3be707c0a7eaa7f5ccf8f0`  
		Last Modified: Thu, 08 May 2025 17:18:28 GMT  
		Size: 16.2 MB (16176532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d22b184abfb23338db1ce2eec5f2b1c5299eec68ec533ba9f0c96eb50f94d86`  
		Last Modified: Thu, 08 May 2025 17:18:35 GMT  
		Size: 52.6 MB (52621858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3726fa4c4e4f7f6fac67f7e4a3b9f88a7697235d9144aea259a488250ea6a4`  
		Last Modified: Thu, 08 May 2025 17:18:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267111b8758c00ce54358fe646f25d46e043fc0ee6173035ede38ede1c1aaddb`  
		Last Modified: Thu, 08 May 2025 17:18:27 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa932d5b5b173a902aff105177ee4d19ddd3eb542b813d7ce67fcfbb74245c56`  
		Last Modified: Mon, 28 Apr 2025 20:51:29 GMT  
		Size: 25.2 MB (25169360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2623a0872f21d26f037b524357b0f9de74f2fd77a6e0ed5760946b611ee0b10c`  
		Last Modified: Mon, 28 Apr 2025 20:51:28 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:318c9652c3d855b24e9d86a017f837eaa775c8ae4f95cb94d3806860a99c052d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1266533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bff5e704998e48f4d18f994bca53db2a79300e06d5f8e25611aa4d9ffd9b20b`

```dockerfile
```

-	Layers:
	-	`sha256:4332346204a8c71513bad08f3dbda7ae21270f52d75e8ba8307258b50444566e`  
		Last Modified: Mon, 28 Apr 2025 20:51:28 GMT  
		Size: 1.3 MB (1253125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d30cd4410882bad7582a59a1e86490c0a884a3d6bdf2545ded01a154cd4f91d`  
		Last Modified: Mon, 28 Apr 2025 20:51:28 GMT  
		Size: 13.4 KB (13408 bytes)  
		MIME: application/vnd.in-toto+json
