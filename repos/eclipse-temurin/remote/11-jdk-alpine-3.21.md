## `eclipse-temurin:11-jdk-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:4cad7bc8e423b4ccf7b71a5d1d2094d8533501b07a6100ffbbeb1ff4c7edecff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9251e6bfb545a9835c74ac611a6e0054935b3cc7d07694a55015b4b2cf633089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160661141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e360ff51750f792a9390fe32d2428cb08f71c7e9d41eab5308b9046fe9f782`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
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
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7e9e5241d1378d75ae70e9b216d0d51d3aa2e61e187e92e09d117cb613e16ee4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e518bf4d2dc069c03c1ee405432433fa41ad1d693b65c8ae3505a0cbfb96fef1`  
		Last Modified: Wed, 08 Oct 2025 23:01:35 GMT  
		Size: 16.2 MB (16174554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e85591cc6df739bce5336c773f25423038dc84dc3ec455962adab1eafa561f4`  
		Last Modified: Thu, 09 Oct 2025 00:13:07 GMT  
		Size: 140.8 MB (140841609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe80d87e1e391e254ecece5c43911c68edfddd2bd6a7582367fda36de120a1f7`  
		Last Modified: Wed, 08 Oct 2025 23:02:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e292129e0fa0f3fd5d4c68c90a9ac89b092e4768cf7bdef779596a5f99c513`  
		Last Modified: Wed, 08 Oct 2025 23:02:06 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a539233a01b94ce7c29c695cfd1a98097ff778c6745a2682c75102bf3bc8ef5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1018698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47c0ce7031a2f1e9f06413247dd06f1c00d19e7969629b3fdf5385456252b2f`

```dockerfile
```

-	Layers:
	-	`sha256:2092a76410b0e37a55b49406dbcb9eb09958c35f07bc0976d4d810b492cd3e90`  
		Last Modified: Thu, 09 Oct 2025 00:12:29 GMT  
		Size: 999.5 KB (999485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab25f8718a4599bc9e46f23b8234d0bd32e32b06b8d9661a16a8073ce44b72c1`  
		Last Modified: Thu, 09 Oct 2025 00:12:30 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json
