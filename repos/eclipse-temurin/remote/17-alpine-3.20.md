## `eclipse-temurin:17-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:d9f423ac4806aecef24eebdcd2568933f4dcf721ad0067404abb008f8a3b588d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:71f14394db58ddf71a571d6f5899132ceccd6321ead01060d53d979d80f13c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (168010973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76346672858a48d957545b372363509fb0f02808461f9ddefbb256785feda54`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='259c85e16f7bbfdfb3e0a2ec1c5d6e2063300d413422286583265a9d8a882358';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dde9eee1a0511e0db98c09724413751d34b370f9423220b25b5dd10a0a275e`  
		Last Modified: Fri, 31 Jan 2025 01:29:49 GMT  
		Size: 20.7 MB (20665861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046a63ae8fc64900767e023c85a44b788b54ba40850770d4b463b553e8680836`  
		Last Modified: Fri, 31 Jan 2025 01:29:51 GMT  
		Size: 143.7 MB (143716441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f675c62ff78cc4225a36aaafd44f1c4b73575ae4faa03b7dc8acbbd70a183222`  
		Last Modified: Fri, 31 Jan 2025 01:29:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70629d9a9ac9d595010d8b726a594730976dcb5a79615ac00b7d828903ecb498`  
		Last Modified: Fri, 31 Jan 2025 01:29:38 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:002e66f6b8907f23cae24b4e4fe2c3606c5529a5cd66e00815c17ebd4953b467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1083778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf7ad96b76d85c9f060c78e2d1211f608a7e835a40e86eabe70ef4606cf8e89`

```dockerfile
```

-	Layers:
	-	`sha256:cb4d8dbf3e57ce14978fe3edfe97199184918df6c5b5290f44ece4bf68b56c83`  
		Last Modified: Fri, 31 Jan 2025 01:29:49 GMT  
		Size: 1.1 MB (1064124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecac81c7a1da214c05652bc788801267a88f89d97eaafd45fe465aca335d2527`  
		Last Modified: Fri, 31 Jan 2025 01:29:49 GMT  
		Size: 19.7 KB (19654 bytes)  
		MIME: application/vnd.in-toto+json
