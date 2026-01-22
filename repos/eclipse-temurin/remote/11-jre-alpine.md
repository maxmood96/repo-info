## `eclipse-temurin:11-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:91f4327861b432433ce40bb4006a8ed1141a2ae51f5492364e9e1422b3748918
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:6a8210675aff73d82f8be07e6be05e77c393d39745c36a1ba3c22ac4682e5c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63309283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f135099692b9063581e597d17b40f01d7fd1f9951f373c85b1ccb53a6be150be`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:57:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:57:59 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:58:01 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='a37e818c23e19a0f3f6a77827eac9c6dab572c22efafa6c0e888cce2555d39a2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sat, 08 Nov 2025 17:58:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da322013c3a3e15f50b875d45b515b19f6df7ee1a9bc2ecbc19bae96a2a4ced`  
		Last Modified: Wed, 07 Jan 2026 19:03:21 GMT  
		Size: 16.3 MB (16289781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d07fa442272c6b6b7d37eaad510b9abacfb13413bb01971120588a4ea75080`  
		Last Modified: Sat, 08 Nov 2025 17:58:12 GMT  
		Size: 43.2 MB (43214642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f5f62162419ffc91b31a781d9372bd81ae2c5a7b7794a7fb64943e88acf6ed`  
		Last Modified: Sat, 08 Nov 2025 17:58:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c474a9ef5e2665aac3c45c688976fca94a3d70d262d657c659cabae6fde8105`  
		Last Modified: Wed, 07 Jan 2026 19:03:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0d8df47e0530d76fde735371c6e8a2bdc5c36d4f71b533ed775fc4771f4fea69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **929.1 KB (929098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe2af36b5260c80f77a0f4313b0396382f3c020c998bd4fe98203a0688866cb`

```dockerfile
```

-	Layers:
	-	`sha256:9372a1c0105dd6a17632604372cd7128558b5903b8d9c1d11b4ef8f57de6e352`  
		Last Modified: Wed, 07 Jan 2026 22:48:47 GMT  
		Size: 910.2 KB (910210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a81197b6a7d77cdd2938884b1b521f437fcf09f4657ed7bc0de563ad1f32f77`  
		Last Modified: Sat, 08 Nov 2025 17:58:11 GMT  
		Size: 18.9 KB (18888 bytes)  
		MIME: application/vnd.in-toto+json
