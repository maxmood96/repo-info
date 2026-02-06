## `eclipse-temurin:25-jre-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:2bf0db425c0f387e91530a223e18525de5f76b468335b00c78099f4055121efd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:25-jre-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:0c6e28549b1d523b824b289e621916990472389eab34694e4791645e729f38bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75218193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b237dc9ea4f0204bf171b642770d867df4957433467ca7dab872b00e465ad4de`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
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
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a03e407880c55620f0e43b85c60664561804c9453ae5ccb1d180bc6c103b79`  
		Last Modified: Thu, 05 Feb 2026 22:21:22 GMT  
		Size: 9.4 MB (9421241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0354a4d23da118b93a3e90484a517c8ff1d8c922997debaa273e0c4588dd39be`  
		Last Modified: Thu, 05 Feb 2026 22:21:23 GMT  
		Size: 62.0 MB (61989671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b7e16ede81088fa81d7e19a173979c0de76f02e5362629f4386dd207d41216`  
		Last Modified: Thu, 05 Feb 2026 22:21:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a4af20b6b2b1f286534df8cabc3306d7a8e4e76a2e8696ab41cab9c2d9ef86`  
		Last Modified: Thu, 05 Feb 2026 22:21:21 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4b266c744db762054a153e648c5df60f2d58ecffe6310827e904edfbdd88f004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **819.0 KB (818950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532b5447faaeb5ebf4b743511c60aab40ffec6667e66bdeac8fd3e10cac56164`

```dockerfile
```

-	Layers:
	-	`sha256:45fbbbddab7540a9388c8db2dc7b5a38a40d920c28f755401afa2ac5f56076d3`  
		Last Modified: Thu, 05 Feb 2026 22:21:21 GMT  
		Size: 799.8 KB (799814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f4435dc9b62cfd0325f6b262404d27725b2415708469d22d9ef480547acbd4b`  
		Last Modified: Thu, 05 Feb 2026 22:21:21 GMT  
		Size: 19.1 KB (19136 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-alpine-3.22` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:d728993c7c5bf1761c573f50b34d405ba0118d0d2a9f6682d2a19d36f160d260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74489227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c759c8fc9f3a3ffc0c74f9a8c348a9d893985bd6364e9fe6e07a9f4c8e9263f4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:20:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:20:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:20:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:20:03 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:20:03 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:20:08 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='159099235c536b152f86111a694a8a03392948924736f354c79e95532dcfc1f8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='2cbb356c6923f89814b892561e6f0377ecf035ab0577e3162d2cf4e202d38ee7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apk del --no-network .fetch-deps; # buildkit
# Thu, 05 Feb 2026 22:20:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:20:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:20:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678729a4f0bf452b5843eefcb09acd09aa14cc227b44a285399172c07d4d2c18`  
		Last Modified: Thu, 05 Feb 2026 22:20:23 GMT  
		Size: 9.4 MB (9434991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b6092f7ba995f6ddb52611d129e6e3149fe1a08b74852c31381a4fbf83c792`  
		Last Modified: Thu, 05 Feb 2026 22:20:23 GMT  
		Size: 60.9 MB (60912309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ec1928d0d1894164f26fc5ce6b8c1c6515d1d0ddde1065ae2b43caa2a2be38`  
		Last Modified: Thu, 05 Feb 2026 22:20:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133000b9b16a608f2b2b5d66dd19e9808f32cb9c1c864c026fe7385700265a2`  
		Last Modified: Thu, 05 Feb 2026 22:20:21 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8a2a3cb313c13e7ef9ac8a396144ebaa1563b180f75270967d0e22d1ac070d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **818.5 KB (818470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f1b4bcaf9056070f5615601cd19b81446ad407a131c919230199717a0178c0`

```dockerfile
```

-	Layers:
	-	`sha256:43c60f62a8327d6c8c7a4cd71fea1684283d98992a6e8ea4eacb9bd671caaea8`  
		Last Modified: Thu, 05 Feb 2026 22:20:21 GMT  
		Size: 799.2 KB (799225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f094b544cd32c8e0cfb60dd8b3431ed1eb862e05a2d565314f2ef063e342849`  
		Last Modified: Thu, 05 Feb 2026 22:20:21 GMT  
		Size: 19.2 KB (19245 bytes)  
		MIME: application/vnd.in-toto+json
