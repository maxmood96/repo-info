## `eclipse-temurin:26-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:10421f30dc851c0f71dce54628083d22ef0cce51ab1fc02bf902de56fd953688
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:26-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f782bbc00cd6e905f9aa37394827b1e45caa91127aba4e8d94c95923b1e73ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77072546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0ff0240a15e35d5556c0ae5d6cdc3621b5d0e34b7a8d9970f364f3d4a7d5c5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:34:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:20 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:34:20 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 15 Apr 2026 20:34:54 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f3c21f425f9e9f53ab8a19aed6a25cedee662be19fa221696c1450eb67470905';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_alpine-linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='4f0866bd8aa88eb6dfd0489793f8b2fb3eb0f6c20aadb27cae1b140f10897f8e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_alpine-linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Wed, 15 Apr 2026 20:34:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af76732d1c87ea83d225c5f6a2bf4fa407c04df7ac0d6690f5edd0cebf5d443`  
		Last Modified: Wed, 15 Apr 2026 20:34:38 GMT  
		Size: 9.4 MB (9437820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda0ef767c71517d7b4111ff279bdce7f223bd73772a3d72f12f58bb16cb5f03`  
		Last Modified: Wed, 15 Apr 2026 20:35:08 GMT  
		Size: 63.8 MB (63768128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ebb84038a37b01134bc5531b569fd697ab42b9aedcad472437345326d8c9c0`  
		Last Modified: Wed, 15 Apr 2026 20:35:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc27638916d2e266082323745d2dd8fa8a569aef22680acc5e3998a045c25a`  
		Last Modified: Wed, 15 Apr 2026 20:35:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:fef68082ad9ad0492809c24a62e635ed5d2604c1a67e63c38448098a8f0862d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **819.5 KB (819540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a592f0f42412d5db584d94ff4733877444bb65485bf4e2a030acbda5ba9fa807`

```dockerfile
```

-	Layers:
	-	`sha256:19b10cfca6cf07ef377d03ff6b617f65203da6867ac397fb1c943cf9cae5ab32`  
		Last Modified: Wed, 15 Apr 2026 20:35:06 GMT  
		Size: 799.8 KB (799797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecbae04ed028ca55acf9c223c95b013fc491cdc0b817e980625a0e76cc76184d`  
		Last Modified: Wed, 15 Apr 2026 20:35:06 GMT  
		Size: 19.7 KB (19743 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:4b24f10196565c2e3c64cfa232dfe98c3400b89192978c11c4a1acca7cfafb15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76321666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd86ab71063e1b7b136ec99a7b50aa0ebf2da6e07780b2e92ef32df6cee6b561`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:34:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:55 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:34:55 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 15 Apr 2026 20:35:01 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f3c21f425f9e9f53ab8a19aed6a25cedee662be19fa221696c1450eb67470905';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_aarch64_alpine-linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='4f0866bd8aa88eb6dfd0489793f8b2fb3eb0f6c20aadb27cae1b140f10897f8e';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jre_x64_alpine-linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Wed, 15 Apr 2026 20:35:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:35:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:35:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcf42d082e09ab51aac7c11051319c43611d1e3962a3d571b81b0659bfd6264`  
		Last Modified: Wed, 15 Apr 2026 20:35:14 GMT  
		Size: 9.5 MB (9468202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930146b5f321a3df1c2db57a474ab607b4adc8522970751f707e9ee9698ef23f`  
		Last Modified: Wed, 15 Apr 2026 20:35:15 GMT  
		Size: 62.7 MB (62651184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eb5080e01c7bb136aa6df68c313294f8e1f97532be44e532168c39062488b9`  
		Last Modified: Wed, 15 Apr 2026 20:35:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d30ced8e7b88cd55977112773f04f0d117dc90a7a0396b4373b9a1b7add66bd`  
		Last Modified: Wed, 15 Apr 2026 20:35:13 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:887a363b84bfb904a9bb73d1b139275d645ccbb7ed70aad50f8707bde8cc3fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **818.5 KB (818458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbf9515889bc4fc705396ad7b0b5572e7b2bf1b8e05ced990edc9edb97354e0`

```dockerfile
```

-	Layers:
	-	`sha256:1ca4055e04d0fda2e771ee85d598ba9d9473f8d997b92f802d1bea564137e709`  
		Last Modified: Wed, 15 Apr 2026 20:35:13 GMT  
		Size: 798.6 KB (798582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60db6cd09379ea37d193c26f97e0f72bfebae38247142dd0ece49ae8b417aad`  
		Last Modified: Wed, 15 Apr 2026 20:35:13 GMT  
		Size: 19.9 KB (19876 bytes)  
		MIME: application/vnd.in-toto+json
