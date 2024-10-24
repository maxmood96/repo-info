## `eclipse-temurin:17-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:148f1c965d9314fc1207b7719f0eec35a374ad2ccfb8200268b5ac17a25e05fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f7f8fc0641a1a01abaeb1a38da8e3fbfa31e1a3f3305583ac0a151f18a3fddaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68549342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc169694b39c38605f4282cf21403038b2880db997c3fffc729b869b61ecd4e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7a2df4e2f86eca649af1e17d990ab8e354cb6dee389606025b9d05f75623c388';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3c739cbbde371aeac64f64cb65446d94016de3ba6208cfe467175685ea83ad`  
		Last Modified: Thu, 24 Oct 2024 00:56:53 GMT  
		Size: 18.3 MB (18307266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf0b938dc10b6443ef1374a87033b27e34e71b4d202528de99b6ce99f49ff37`  
		Last Modified: Thu, 24 Oct 2024 00:56:54 GMT  
		Size: 46.6 MB (46615862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468b92b5146174980b6d04049e5495a7bdc111344f3ad50ffb5081703e5c37e7`  
		Last Modified: Thu, 24 Oct 2024 00:56:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115a3aaaef12b260cec261b2790f26b2d78108975e6a961f2b0dc9dd19684e55`  
		Last Modified: Thu, 24 Oct 2024 00:56:52 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:29c29c7e0640eedb545c189bf92c0a93ac87f16eb8a720dcbd37464fff5d65ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **901.5 KB (901545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae8eeffbb4e28612340ee9f6de7fc8400b9cf9551fede08400b5abcfd28b152`

```dockerfile
```

-	Layers:
	-	`sha256:2ac60a79c0bac6f7685157f0ed14de9dcafe7090b6a7f96d5dfc2bdf4c18b4b0`  
		Last Modified: Thu, 24 Oct 2024 00:56:53 GMT  
		Size: 883.5 KB (883450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1898b40469f31241094d4302139b660ee4c292068f0e4494d11fdb68f7ceebd1`  
		Last Modified: Thu, 24 Oct 2024 00:56:52 GMT  
		Size: 18.1 KB (18095 bytes)  
		MIME: application/vnd.in-toto+json
