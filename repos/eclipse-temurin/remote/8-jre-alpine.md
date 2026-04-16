## `eclipse-temurin:8-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:d848882b90b586b9567e2e7e27eab5524f62ea27227e9d5b53426ed901fcde58
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2a7ea718f14981a4afb35196f256d810944c8b480254184918a27eb81f689fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62960932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a05d18cd37364902251ec8518017e0b82bc8de89190f10e89bb780e4f11fb7f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:31:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:31:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:31:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:31:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:31:59 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 15 Apr 2026 20:32:25 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c1b64ab1d2c96ac0fd89c60377396cc4457f954ee7ce931f3a0e547f701e6595';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 15 Apr 2026 20:32:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:32:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:32:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775c53a23a895a8fdcb2534de50a64b420d676e982f81a1e72e88f6b283280fe`  
		Last Modified: Wed, 15 Apr 2026 20:32:15 GMT  
		Size: 16.8 MB (16837772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d9e7676138e041099b072e72d939e6c6fe8cd2ab789ff07bfa4a264f2828f9`  
		Last Modified: Wed, 15 Apr 2026 20:32:35 GMT  
		Size: 42.3 MB (42256564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d393a668fd7abdb353104b0fce5968b214d5ac3ff3cbb65251bdfe6116b21b`  
		Last Modified: Wed, 15 Apr 2026 20:32:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4919f6d520994e2167a9836b4fefe39c400fc01a5d27f7f8f48f0e3f32a65ce`  
		Last Modified: Wed, 15 Apr 2026 20:32:34 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:fac8e445473b70604867f2917247c0c2cc09af77e8c4ea710f128d1619bee19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **952.2 KB (952220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bbd2f23a746b9cc9b47ae221f59a56f9dd5770b44a47f298619516e9264bca0`

```dockerfile
```

-	Layers:
	-	`sha256:3f924a7c37036cdf2a68cf411bf52f02be66b1ef8ebe96a3563bc332db79643f`  
		Last Modified: Wed, 15 Apr 2026 20:32:33 GMT  
		Size: 933.4 KB (933361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95125b5fda19fe664ca4566d999289669f592b5e271536ab68911c8858fac311`  
		Last Modified: Wed, 15 Apr 2026 20:32:33 GMT  
		Size: 18.9 KB (18859 bytes)  
		MIME: application/vnd.in-toto+json
