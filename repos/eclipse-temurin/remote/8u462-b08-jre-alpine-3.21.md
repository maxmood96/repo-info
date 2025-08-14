## `eclipse-temurin:8u462-b08-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:9dc74c75a1bc693a739dcf20103dd37445f0edde3fe59c205b7e61ac2ea4e62e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u462-b08-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:c928122ce365f09e5cb9594ef66e0e999c6532f7d9cba12fb7e07d71797c1c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61629125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b14d073c3a8adae87e4e0880998436038e6dfa5b18a7f2cb5c8a9228da6e148`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
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
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1862b63145bcd843c2f221658463496ab133e2c29eb1dcfd0689495cbbb22980`  
		Last Modified: Mon, 04 Aug 2025 19:10:52 GMT  
		Size: 16.2 MB (16162746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8eaee53d08c408ed3e1b5be2991752c05fb7fe93f62eb0879adef9f10da981`  
		Last Modified: Mon, 04 Aug 2025 19:11:00 GMT  
		Size: 41.8 MB (41826400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3168a54c4a83c5534c5c4a492900c98cefb61aae470591d8b3b0e3100288b310`  
		Last Modified: Mon, 04 Aug 2025 19:10:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68eeff3dca3a0b4d27b5cea0f1b8ec3d022f6ec614b470f2c9641db31ea75b5a`  
		Last Modified: Mon, 04 Aug 2025 19:10:45 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u462-b08-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4f385e676aeb1d00713cb5ac7fb68092f4401995fe17d74710b5fcde7c81c01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **942.5 KB (942464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42eb8ad8c815f7eaa62bc99017864349891270b7ff4f26e7202d8c48c493fa9e`

```dockerfile
```

-	Layers:
	-	`sha256:4abd9a7f45498225c0382e0cea922747df8b03dfe9f796a53ba3149f5bc28740`  
		Last Modified: Mon, 04 Aug 2025 21:29:13 GMT  
		Size: 924.2 KB (924234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03d73d8fbe3dca0f1ffe1b42eef935df56311245b3c569e65e26cbde57e637cd`  
		Last Modified: Mon, 04 Aug 2025 21:29:14 GMT  
		Size: 18.2 KB (18230 bytes)  
		MIME: application/vnd.in-toto+json
