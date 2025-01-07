## `eclipse-temurin:21-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:c4e39b956750b52fdf49c93d51a63546a5e91b22224fc462e58b00be91b17b62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:aecfde022afcd4fd1de5f0b1380ca0e6270656f456b8300302dbfbe7de965c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182042808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03403422d51928e45a3ab1a3f7f0f672a41f7836e37f3407720c69b5a6e100fa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f22e32b869dd0e5e3f248646f62bffaa307b360299488ac8764e622923d7e747';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='8da7da49101d45f646272616f20e8b10d57472bbf5961d64ffb07d7ba93c6909';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74124278afe2b18a31c86c5481b70f13610d72f9251456efb60077c008ba80d9`  
		Last Modified: Tue, 07 Jan 2025 03:31:25 GMT  
		Size: 20.6 MB (20646874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8fcf39531b5efa8fb9a8f692b5b7b7feca498796d140b94c6255523f4c7f6d`  
		Last Modified: Tue, 07 Jan 2025 03:31:27 GMT  
		Size: 157.8 MB (157779528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62fe376e35d90e3e99f049badca94e8fe7301d699d6a2539330a8994d9f8799`  
		Last Modified: Tue, 07 Jan 2025 03:31:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5d46d44a8796aecf2575f05400a60dd8d65d4f9f801590d09cd3b4f278318d`  
		Last Modified: Tue, 07 Jan 2025 03:31:25 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f1b5400a1c5d3101d43702d81d2f02657a825045f32b7d0527fa174d01c8d26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1081738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff84299e2075edd8032f86de46723ecd49d7692a18023b58e04b364df99eb1f3`

```dockerfile
```

-	Layers:
	-	`sha256:eca0e5ccaff5598f617689aab513cd09e4d7bc257d534e66e75e51bac7ef3534`  
		Size: 1.1 MB (1061320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:141386f791d43bd4632d647fa7f3e3cb385280ac462af193d40d1a3ffd568e50`  
		Last Modified: Tue, 07 Jan 2025 03:31:25 GMT  
		Size: 20.4 KB (20418 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:d63c09150bf8a83499e5c79787bb2338b4b20fd3df18dfb7a8960aafddacefb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180862608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460fbeba0800d5e6e410ac65b2188ebe0fa5f27517bd5a128bfa1e3750d4235d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f22e32b869dd0e5e3f248646f62bffaa307b360299488ac8764e622923d7e747';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='8da7da49101d45f646272616f20e8b10d57472bbf5961d64ffb07d7ba93c6909';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0debfbcf140de1b1e0c5b7204c63e292d79de69a68e3267957c67e04f0ba24af`  
		Size: 21.0 MB (21033362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7e26f108db4058af6f9154e47e87b732fbd6fb04792a0871d1074952992b75`  
		Last Modified: Tue, 07 Jan 2025 07:27:36 GMT  
		Size: 155.7 MB (155740151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3ed595529c90be877f0b53e3b866c077cd55bd6b85c36388f452338ba4c676`  
		Last Modified: Tue, 07 Jan 2025 07:27:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3a0beda2910401756d0ac146e871cdae993a2a999f118127df9ca88c508fc0`  
		Last Modified: Tue, 07 Jan 2025 07:27:32 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2053eb60701b38b396c206c513de27924bee5d395c851634a3d58da174fdcec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1186381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ff11b482d7fb4b348dd9513d79c0eaf64d54880e44d68b7c5976c75ee902f0`

```dockerfile
```

-	Layers:
	-	`sha256:7e78d55adb9fd5d7ddfa6c2acfd078be75fac089a35abddd22cb2c8e909daac7`  
		Last Modified: Tue, 07 Jan 2025 07:27:32 GMT  
		Size: 1.2 MB (1165840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1fd97dad6de79509b055958324ba21621e40169ceb607ab76bb8f9dbc21f30b`  
		Size: 20.5 KB (20541 bytes)  
		MIME: application/vnd.in-toto+json
