## `eclipse-temurin:8u482-b08-jre-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:ee546521d00f1274e3e56bad6a845d6197d9ffdd4cd46f9dc68d1392a07a9136
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:8u482-b08-jre-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:655b25045ad54f780e18a4a513f6f7a6f00ec60919d293ded9043cc7241be5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62960821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49067c5096139d6c8f7f1250363f9831f3085bbe795a8b5ac381b88f36da8d9e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:14:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:14:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:14:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:14:24 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:14:24 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Thu, 05 Feb 2026 22:14:26 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c1b64ab1d2c96ac0fd89c60377396cc4457f954ee7ce931f3a0e547f701e6595';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:14:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:14:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:14:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8e32ef2a05e2b66409cd0d9bbaa2552c0a242a33424dc222546ebd7ee40f92`  
		Last Modified: Thu, 05 Feb 2026 22:14:37 GMT  
		Size: 16.8 MB (16840018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ce1a505392ec0f24d133e5f7fd5012a992e1a31b845ddf57e040f550500f86`  
		Last Modified: Thu, 05 Feb 2026 22:14:37 GMT  
		Size: 42.3 MB (42256574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7460e89a30572848ca4704efa57e6b4c7835072838063ba428664da89eacbe2`  
		Last Modified: Thu, 05 Feb 2026 22:14:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f89f7df6a5d2142897ebd5204302c9e1ea2cd88a4c782b02477c2200ea508`  
		Last Modified: Thu, 05 Feb 2026 22:14:36 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:fc39ec1f830639c48919d1d148982baecc42111975a8312314dbd5d4a817f28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **954.2 KB (954175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5584c6eb350017f9fbefd57247c6f64f7125ddc277a7e6cb0382106a8863cab0`

```dockerfile
```

-	Layers:
	-	`sha256:c74c791f00d82b808abd573a0656157e63caf08f25a05ee25cda8d89cc46991b`  
		Last Modified: Thu, 05 Feb 2026 22:14:36 GMT  
		Size: 935.3 KB (935316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:885552a1fd5f33880896a62827794764609fead8543daae8fb839301a832c6eb`  
		Last Modified: Thu, 05 Feb 2026 22:14:36 GMT  
		Size: 18.9 KB (18859 bytes)  
		MIME: application/vnd.in-toto+json
