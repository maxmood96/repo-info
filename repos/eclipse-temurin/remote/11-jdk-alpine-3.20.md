## `eclipse-temurin:11-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:2e850c4df17d8c0305d5f602c5b76ee643a9830601dc989e8ff61858b682cf8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:063185254c2f82d039b4c0338896be2a199ed425e8ba7f377a9c4812f2e7e7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160628552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576aded9a059aeff3451554ad97d2d4ec216e83c34ebe13c889559c183b2bf05`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:15:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:15:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:15:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:15:00 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:15:00 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:15:09 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b55a38b75ba99d86f4adb47552ee5306b9589e2026861a3b8f030993c42aedc7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:15:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:15:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:15:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:15:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13e5fd44bc73332069c9abf10ed11d99ce0fc5eedf0d6bd1e53aab1744a1277`  
		Last Modified: Thu, 05 Feb 2026 22:15:24 GMT  
		Size: 16.1 MB (16081579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d39ccd0917b2714252748e4d80a8e0f029605ea52aa362a282f6938c537287f`  
		Last Modified: Thu, 05 Feb 2026 22:15:27 GMT  
		Size: 140.9 MB (140916698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddf250eeb26ed320ea6277bbe3ede74c77d942b9c8b66049b6181f8216e40e2`  
		Last Modified: Thu, 05 Feb 2026 22:15:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf7e5782e588e56a7827e11705c4600662b2562dc7c539ce203222a0d6c1abc`  
		Last Modified: Thu, 05 Feb 2026 22:15:23 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cfcaa965edf16cc189cc0d23bdb109a8370ffb3dfc68744774145a9ea1980025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1013432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c352458a4c123fa874882ddbf808663121fdf200d815959c8476bfc9511f1d`

```dockerfile
```

-	Layers:
	-	`sha256:d7598198955f9f3b9dbeaf83a5032469cf2210b1ec29341fabb1f55a278a1ac0`  
		Last Modified: Thu, 05 Feb 2026 22:15:23 GMT  
		Size: 994.3 KB (994263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c2392abde813f86e0dccb385a531efdba1f2e69b9f183fa538f23ebde953d12`  
		Last Modified: Thu, 05 Feb 2026 22:15:23 GMT  
		Size: 19.2 KB (19169 bytes)  
		MIME: application/vnd.in-toto+json
