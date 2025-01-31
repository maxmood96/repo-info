## `clojure:temurin-8-tools-deps-alpine`

```console
$ docker pull clojure@sha256:4aa357224d9fdc011dbd8d902470c94f7d12429b7a408114042b2fa85b5d784a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:410615910c98f45378104e3645a9eb9405a53a3f99110d7b7985b9d464c681c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97563669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14038a1f3994e0d89b37f9cb148b9295d9353c9fcd0fdb1c53d2baa0a7d739d8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Jan 2025 01:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 01:19:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='86071bc98901cae80c62745a64bb4486212985fe5b66b5aec36ce92e8a036a9d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
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
	-	`sha256:f03d02a1a038083f4bc30ab747d341a6591063fe0585ea9cbb1a6f466d15fb0d`  
		Last Modified: Wed, 29 Jan 2025 20:27:11 GMT  
		Size: 25.2 MB (25172827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69641a27932e895575d3c86ab9cd3d5f34bbf4ab5f76cc5d781035e1c8c14fb`  
		Last Modified: Wed, 29 Jan 2025 20:27:10 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:ffb82e848ce54a0928896481748b989b0aff8fe41bfbffd7b0a09979fe777a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1265904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a019f9c99c17cbea36fea780e9096f8abac360b630de9bab29fcd7c1aed9ceb`

```dockerfile
```

-	Layers:
	-	`sha256:725e8997462c3a5c0dd8a60d24dc86e557271759ea59d02a6fe4a10df9ffb2bd`  
		Last Modified: Wed, 29 Jan 2025 20:27:10 GMT  
		Size: 1.3 MB (1252497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fcaf890e469d69ad548e60b2aedc282b1c889347cb8f2b3c24ef20b2d49f47d`  
		Last Modified: Wed, 29 Jan 2025 20:27:10 GMT  
		Size: 13.4 KB (13407 bytes)  
		MIME: application/vnd.in-toto+json
