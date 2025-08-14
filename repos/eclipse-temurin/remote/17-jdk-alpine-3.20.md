## `eclipse-temurin:17-jdk-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:7d913e8acd115edbb3cee9c423dd45a18b338aa2b976c86fa06e75a862aebd49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jdk-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:41f5a9ee7585f2f921c27336891803cc58e28787cf341e96e1fca218fdea28a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168133057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e44f071b037f5668f108b5caf7f0a99c54741e5aa98d074c6ca54163926a5b7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2e83ac152fb315db0d667761f2120b64504800f641a513044e834a1a41f29bc0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf348030b7cbe632ea0da207b2e9859a7b81dd889ede3233803d94281400fdd`  
		Last Modified: Mon, 04 Aug 2025 19:11:43 GMT  
		Size: 20.7 MB (20660865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a347d1fecbb092a7a3535a3854d7a2996f1c6b653579d1f2de471d6fa07854`  
		Last Modified: Mon, 04 Aug 2025 21:25:56 GMT  
		Size: 143.8 MB (143849307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6ac35fc925b794cc55865d33ec17fa3fb39f19ade35d529e1495f862ce33ef`  
		Last Modified: Mon, 04 Aug 2025 19:11:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39d0d538f1b375421aa8d60e4d847b4b5e4c9b8a54ea19c83224d24853469a5`  
		Last Modified: Mon, 04 Aug 2025 19:11:33 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:02bb900b1a8d51c1448921455b7389da0ceb06eeca9b95750ca37b2c9e92b765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1086584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9384557ca2dafa69234ffc96a3c679007b1aafb3f637e0cb9e2b79861a3ee8e`

```dockerfile
```

-	Layers:
	-	`sha256:8a5236de2f2e932e2e2c97cb4e187f7b093ca33d3b9f9d1af8d92c9622d4d01a`  
		Last Modified: Mon, 04 Aug 2025 21:16:31 GMT  
		Size: 1.1 MB (1066930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:503bc30beae6fc2365d7ef7faad556c6ba203ff6974fe2c737e20e534dadb424`  
		Last Modified: Mon, 04 Aug 2025 21:16:32 GMT  
		Size: 19.7 KB (19654 bytes)  
		MIME: application/vnd.in-toto+json
