## `eclipse-temurin:25-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:775fe7002dab25049ad49318a77e3469bd5ef6e8fa738a9df467ed1faef4d7ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:25-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:43444540186b6756070bd01a80eff7a171ce0733ab31aeaf03454b9b596ee735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75030408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9ec8bdf9c1d6fd9c5990d732e24376542465118f36463313657ee1a4a12754`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:21:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:21:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:21:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:21:03 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:21:03 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:21:09 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='159099235c536b152f86111a694a8a03392948924736f354c79e95532dcfc1f8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='2cbb356c6923f89814b892561e6f0377ecf035ab0577e3162d2cf4e202d38ee7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Thu, 05 Feb 2026 22:21:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:21:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:21:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba792fd087fa800dff5983d8e3d2e4861e61d575c6d8db97a16acf36c3f1b05`  
		Last Modified: Thu, 05 Feb 2026 22:21:21 GMT  
		Size: 9.4 MB (9393337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1117e03ad2f3ef282afc31ab99db1d7704287b64dbd1e0013c9d37b0fe79463`  
		Last Modified: Thu, 05 Feb 2026 22:21:23 GMT  
		Size: 62.0 MB (61990923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b7e16ede81088fa81d7e19a173979c0de76f02e5362629f4386dd207d41216`  
		Last Modified: Thu, 05 Feb 2026 22:21:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a4af20b6b2b1f286534df8cabc3306d7a8e4e76a2e8696ab41cab9c2d9ef86`  
		Last Modified: Thu, 05 Feb 2026 22:21:21 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3bc6d8a55b787f89fcdfd20dbbc355be913c6034bd6550d5ded715970a95f108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **818.2 KB (818178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcde2ec88b86a2ab0fa4bf193f69aa2b7825380b7f2a9deec457721d051d75a`

```dockerfile
```

-	Layers:
	-	`sha256:017a30deb34823a4049b5876a6f59b53d61a25e243f0448987cbacf4305f93c9`  
		Last Modified: Thu, 05 Feb 2026 22:21:21 GMT  
		Size: 799.0 KB (799041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3db003703eaf271adcf3968fb787c0fef68bdd2106fb9d5f1bcb9d941ec6c9`  
		Last Modified: Thu, 05 Feb 2026 22:21:21 GMT  
		Size: 19.1 KB (19137 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-alpine-3.21` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:5943278ae2f956c62d918896c426498d001ab0a2126a9a7c3de03d108f5bd3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74319175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd97d94739cf638405ed1dad93821b742d5e5f13506bf02676dd37ef85bae2f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:20:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:20:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:20:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:20:02 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:20:02 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:20:07 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='159099235c536b152f86111a694a8a03392948924736f354c79e95532dcfc1f8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='2cbb356c6923f89814b892561e6f0377ecf035ab0577e3162d2cf4e202d38ee7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Thu, 05 Feb 2026 22:20:07 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:20:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:20:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece5d6c86bd8a8d30a9cee9aa735e43c69c2ab71015a22715dd25edef1cb8ef3`  
		Last Modified: Thu, 05 Feb 2026 22:20:21 GMT  
		Size: 9.4 MB (9412231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ed13b516f0fe7016d8f91aced8ff93f38f7547d75a5b51400f52c8f5d5b6c1`  
		Last Modified: Thu, 05 Feb 2026 22:20:22 GMT  
		Size: 60.9 MB (60911655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c9ff6ab3726b31e86e8342396cfbfe304555de0b046e595eb63cc412a77f58`  
		Last Modified: Thu, 05 Feb 2026 22:20:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390793da90a60a6048f8d56aa8338dc5c1aee6cc8c200aebeef3d4a4967163a5`  
		Last Modified: Thu, 05 Feb 2026 22:20:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a1d8bc23ec57b3e64de756cd244826cf7b3fb1732786f89c7a9d1c7c11677ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **817.7 KB (817699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8532293cf4f19e8d7e527baf40ba05ae7346760e894e48f2cefdf21d26ef2f04`

```dockerfile
```

-	Layers:
	-	`sha256:42d13a7286698f1aec4cab87de4e0d2d9ae99e6e74ddd176bfa71ebed89b7e3e`  
		Last Modified: Thu, 05 Feb 2026 22:20:20 GMT  
		Size: 798.5 KB (798452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e3febf779bb58eae092734ec3274d3eee5e8e58f2f8c92269aa7ec30aa93b57`  
		Last Modified: Thu, 05 Feb 2026 22:20:20 GMT  
		Size: 19.2 KB (19247 bytes)  
		MIME: application/vnd.in-toto+json
