## `eclipse-temurin:21-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:5aa38709814b18631e665fe87b8ac471c4bd4271f88fe16ccda6000cd2a2d644
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d985dfb7da9d989b5531f77e8d43b494966358f9309f4d9dc818ef53e1849efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72821909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160f7501189a950bbccd6c852579f11d61bd9df614b0ddd9f67e63554d3434c0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:59:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:27 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:59:27 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:30 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7f8c230ba505b418e4288e2b34758a6e4da32470944740e5ba0cfaae02271c22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='17aca4ecc1600f70ec88ea0f8bf3a06ba6806bdae8c96d03c07683c800f0d4e8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sat, 08 Nov 2025 17:59:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23d8a4ba3b4016db3ef9e5cce26605b0de5de9c21384874dcae00cfe7e60ea0`  
		Last Modified: Sat, 08 Nov 2025 17:59:43 GMT  
		Size: 16.0 MB (16023415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ed217d5fa76a5aa6435590113b0933dec7250e6440c65d3445e1fb514dfe31`  
		Last Modified: Sat, 08 Nov 2025 17:59:44 GMT  
		Size: 53.2 MB (53169030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff01f4fab586a80e65f0f2f326a5f42b287d1c292b487054bd1a4c40ec5c1ec7`  
		Last Modified: Sat, 08 Nov 2025 17:59:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9243b0f232d7db4adb939eaa4764f919367fc61513ac8d1e78f0ebaf013487c4`  
		Last Modified: Wed, 07 Jan 2026 19:24:40 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:dccb3e9248c52cbaf1489570407d80455a938a0c735e1a3a99ed11118d981ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **909.8 KB (909763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00b4f3c0571836918d80201cceeacc32d332d330fe178de3111ba4b9c91fa81`

```dockerfile
```

-	Layers:
	-	`sha256:ad55fdd4e9986e60f30ca5bad5a943fa84c8c7e5610de5ed9565c5d33fd4d13c`  
		Last Modified: Sat, 08 Nov 2025 17:59:42 GMT  
		Size: 890.7 KB (890739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:363fa442ec1aed266d0984cc474332becfef4074f7a85212e80fe2775a5d167d`  
		Last Modified: Sat, 08 Nov 2025 17:59:42 GMT  
		Size: 19.0 KB (19024 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-alpine-3.20` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:5fe315f89c3024e26780e13c61717284189661966b6671ff32c6761a8e67e9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72509601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ff0cab2ef8c71751fa79ba46fe732f7a6cbf42280678c2b7097156052f3fa5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:58:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:55 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:58:55 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:58:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7f8c230ba505b418e4288e2b34758a6e4da32470944740e5ba0cfaae02271c22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='17aca4ecc1600f70ec88ea0f8bf3a06ba6806bdae8c96d03c07683c800f0d4e8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sat, 08 Nov 2025 17:58:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Sun, 07 Dec 2025 13:54:57 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffb7401ec152f9c57cb2b2c3718360c16c8b8d67fd42ba68ddf6997ecf1df5b`  
		Last Modified: Sat, 08 Nov 2025 17:59:11 GMT  
		Size: 16.2 MB (16191339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec617d251e2e1228975488ffac1e12b22ac6132a9fba5a221ce1413dbca3f66b`  
		Last Modified: Mon, 12 Jan 2026 05:22:32 GMT  
		Size: 52.2 MB (52226477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26355bcf44b4bf296a8048d48c95ac241dbe71257822053d4f1113f536b11e49`  
		Last Modified: Sat, 08 Nov 2025 17:59:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027e40558c1085e7d054cca0c0c284a4f277a5919752f77e5a85f55ee335ad22`  
		Last Modified: Sat, 08 Nov 2025 17:59:10 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d87cb564b1ecc84dd83730abcdd1aa1fc2eaa7d49391fbb848dd544fe0ea26c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **909.3 KB (909288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad298371aa590b1a0ae7a37cf28da244a4411089ef8d7c5347b27f349f3b72e`

```dockerfile
```

-	Layers:
	-	`sha256:ca435aba59ad17b3273881dbc78a457eade9c554fda1e37d4ac2c4c79e74a2f7`  
		Last Modified: Sat, 08 Nov 2025 17:59:10 GMT  
		Size: 890.2 KB (890153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c838039ba7dd0defa36a561995cce3a64e5122e13aa40e2240d330ef6cb86e4`  
		Last Modified: Sat, 08 Nov 2025 17:59:10 GMT  
		Size: 19.1 KB (19135 bytes)  
		MIME: application/vnd.in-toto+json
