## `eclipse-temurin:21-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:8026860a632d4ebb4e2c88d32ebe2b6a33f3e0d55af5c4e36115d281b4340e85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:21-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:4b496db8d79c6264fa46a25e44280c002eefc89f6344b23b36ae03ae8260841a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182074100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33aff5552178c1f062a09a6c6e69a0989106748f3a1a8385bdd3b8a603f67cf7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Jan 2025 01:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 01:19:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f22e32b869dd0e5e3f248646f62bffaa307b360299488ac8764e622923d7e747';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='8da7da49101d45f646272616f20e8b10d57472bbf5961d64ffb07d7ba93c6909';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Jan 2025 01:19:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4157188cf25a43f289b2be22e99f247112f317855100006dc8556463fe736b7f`  
		Last Modified: Wed, 22 Jan 2025 18:27:57 GMT  
		Size: 20.7 MB (20665935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa228cd6761e4035fad401c9f20acf8bf991d6a9dbdb4bcff3e041095457a35`  
		Last Modified: Wed, 22 Jan 2025 18:27:59 GMT  
		Size: 157.8 MB (157779493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46732d7b5e2c50958fd20897caeb7d830ab5ccd1fcc233d7f15254879bfbd728`  
		Last Modified: Wed, 22 Jan 2025 18:27:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c682d4908eda90cca5440178e33645693ee2ee0bcec95cbeba9158620d10d3`  
		Last Modified: Wed, 22 Jan 2025 18:27:57 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:26ef96a2800455fd1394cf61faaad2cd9eaf5e5b4d14578261898f68f50c7787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1087693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308a23aa533556b06901e503b203110892813bce78d789c197d03aa170f091b7`

```dockerfile
```

-	Layers:
	-	`sha256:f40e096a006213079b95e06465467feb9ed44cfe1c739d9df243f5a5936adc4a`  
		Last Modified: Wed, 22 Jan 2025 18:27:57 GMT  
		Size: 1.1 MB (1067228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:241e9be6d95f00fb6b9a2ef22ea6e3be3d8c673b15b926b6ca622bb02bf60cec`  
		Last Modified: Wed, 22 Jan 2025 18:27:56 GMT  
		Size: 20.5 KB (20465 bytes)  
		MIME: application/vnd.in-toto+json
