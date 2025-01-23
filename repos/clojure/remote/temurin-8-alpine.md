## `clojure:temurin-8-alpine`

```console
$ docker pull clojure@sha256:81be876b3462e19a4ced2df8479d4da166506a0c88df4d543bfdb95ab0eb366c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-8-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:20ff604adfadd7083e0f9fa67229dd3f44a5a5afbedf30c4298eced169cec0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97556585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460b035c6b7030114ce405c395c6ae1a3b0ed55e9a1a4ffeee0f61376f9c2d09`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["/bin/sh"]
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 06 Jan 2025 23:07:46 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Mon, 06 Jan 2025 23:07:46 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='86071bc98901cae80c62745a64bb4486212985fe5b66b5aec36ce92e8a036a9d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c424ce528b8a969200c72fb8dd59bb4245ca7ceca1e0338e8e20243cf13105`  
		Last Modified: Wed, 22 Jan 2025 18:27:34 GMT  
		Size: 16.1 MB (16135176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5d45ed21cb09747b5d1c53aae5f27c01da74be5d9248b1c3d518e31692af6f`  
		Last Modified: Wed, 22 Jan 2025 18:27:35 GMT  
		Size: 52.6 MB (52610867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227d4657ee96815baf764041d2d3803f17f8dd8a87a828071f83b176b68fcb19`  
		Last Modified: Wed, 22 Jan 2025 18:27:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073cdb653eb72896613ee4b3625fbc727fa740f7dc1aed1d4d10d218bafbaf0f`  
		Last Modified: Wed, 22 Jan 2025 18:27:33 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671e7c109bee4be3a675621f5194524f16eac33fe2504ce86008e3f6dc042ffe`  
		Last Modified: Wed, 22 Jan 2025 19:41:06 GMT  
		Size: 25.2 MB (25165743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635a227bd4ae7f526467df846e121a987cf757206b69d2cee1cbf05874f33407`  
		Last Modified: Wed, 22 Jan 2025 19:41:05 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:a92034588c942330038fd06a6380c6eaa4b9d9f282becda52dd6dcb384cf51fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1265905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b564763088b33131e0cdb21a1801608d4930eb85448cba043f0d0eeb842dccca`

```dockerfile
```

-	Layers:
	-	`sha256:c944e7466810757e6310b6193ba844335e4c689f33bcac23d4049a72f12afdb5`  
		Last Modified: Wed, 22 Jan 2025 19:41:05 GMT  
		Size: 1.3 MB (1252497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a14a641c4ded355b78d0b6c7ce528431e3ba21c58c414f774571fe936efaf5f`  
		Last Modified: Wed, 22 Jan 2025 19:41:05 GMT  
		Size: 13.4 KB (13408 bytes)  
		MIME: application/vnd.in-toto+json
