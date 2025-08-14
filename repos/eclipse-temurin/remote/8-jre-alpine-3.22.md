## `eclipse-temurin:8-jre-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:c663227daba419d0b87262c2419a5fe18e9cd83134dab7e568ce53c6d28b71c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8-jre-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:7f5d0f85b15047ad88c8c8ec796674634d7473824c56818a4305f60d28a2bcbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61908659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9391a0570a90eecb4daa2fe5a7cb47cea6d30245761cf6898cf01e67aa16bf`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='fb10b6185c76cb48bdcbb76e466adc319b37ffc0b1cf89708a1f13e94adcc12c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f5dbd1404cc6b53790db982c77c79af58c8d3085329ef1ad7688ea4214e97b`  
		Last Modified: Mon, 04 Aug 2025 19:10:48 GMT  
		Size: 16.3 MB (16280181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326fa3556c639dacd9889c2caff8a7683d6012d1e2a86192042520f4767b9383`  
		Last Modified: Mon, 04 Aug 2025 19:10:51 GMT  
		Size: 41.8 MB (41826382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7c990858a2873d7c8a2fc90073c06c685ce8ee645702e09f902f5eea7cc49a`  
		Last Modified: Mon, 04 Aug 2025 19:10:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e79dd60cb28ebd69591d94da6e150d940dd65644a03f40773c4e0ba0f15c2d`  
		Last Modified: Mon, 04 Aug 2025 19:10:46 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8fc365ba73d301ddaa3bdc026cae96d6c4c495f99e3a182e5135adda57065c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.4 KB (945365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d83a7c32f615ddfd5e313539d98446b0e0a951b032b75900f60da467cfedf0`

```dockerfile
```

-	Layers:
	-	`sha256:d971551e153a533dc6e22930fb625ab33ea58c585661eec34c380b063e26a33c`  
		Last Modified: Mon, 04 Aug 2025 21:29:06 GMT  
		Size: 926.5 KB (926463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e7e55d0f7a9a9841d6be169ab8c0c6d9b7968cdfcb715902d0a1dd24de3caf9`  
		Last Modified: Mon, 04 Aug 2025 21:29:06 GMT  
		Size: 18.9 KB (18902 bytes)  
		MIME: application/vnd.in-toto+json
