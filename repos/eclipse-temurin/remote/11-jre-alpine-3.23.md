## `eclipse-temurin:11-jre-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:20e81b53fda37ea2916d2db8d408d959e3ce3e84d71b1236b24b0b9f69537166
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jre-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:c8babf8b14fb132bdf4bc29cb69a33bad7111de1c3b6c90ff6ccb785a3129871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64334105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c5bed0416137759d0fa056ed626c7346d420cccb0a03b7f7650a347299680f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:13:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:13:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:13:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:13:12 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:13:12 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:16:27 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b30f7db6fd41047c60978bd2c88b6b9bea108803482db4e163dd7fd2b1aec1f7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:16:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:16:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:16:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba30a9b9fbd57b01a8081d96f19cccf9befdb10d3a054b012d5419c813f251a`  
		Last Modified: Thu, 05 Feb 2026 22:13:27 GMT  
		Size: 16.8 MB (16839871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbf5374ff29bf98fbfeccee86b45a4396939136a1c9b23faca892e2fe536710`  
		Last Modified: Thu, 05 Feb 2026 22:16:37 GMT  
		Size: 43.6 MB (43630007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b249cf2081bb5adec97fffe0d8755a8ec538ec6385e279dd2cd9d2d66aca23f`  
		Last Modified: Thu, 05 Feb 2026 22:16:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be9c3a64154ffe2219e6b5b6bef90b671481c6b31c5da9dee01069c080296a9`  
		Last Modified: Thu, 05 Feb 2026 22:16:35 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:04119a72c48a027cffdf2fcfd51476f1505cfe8eca3bf3439691cae2d22ccc3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **936.0 KB (935964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45acbd11434f7e78147a3446dac0a66c6c350a7b7d5377cff3224283ac6a278e`

```dockerfile
```

-	Layers:
	-	`sha256:63d42afecea616bd6c2ec158c1851860dfb8ace94fd188c6d772dec2b5c55589`  
		Last Modified: Thu, 05 Feb 2026 22:16:36 GMT  
		Size: 917.1 KB (917077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10fa96ef1a79e25f0c774969bcab5a23b936dbdfc724604c808c2c9f12e03164`  
		Last Modified: Thu, 05 Feb 2026 22:16:36 GMT  
		Size: 18.9 KB (18887 bytes)  
		MIME: application/vnd.in-toto+json
