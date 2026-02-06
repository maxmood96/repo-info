## `eclipse-temurin:17-jdk-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:5a4bac771ffbe4a092b97bd17a0136b0369bc5102a1dcdacf2538e7e27dce5c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:99a0f401fb2325938afa5b22adebebd8cae98bbf6f1c6b7be5dbe140d0b547b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169684976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca331e45662708ebc9d0b6111696d1f6a1fca01c27a5d384bc25b7efebbefe5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:17:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:17:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:17:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:17:06 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:17:06 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 05 Feb 2026 22:17:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='3246fb1834d21c22ed717db9f8ba3f07e0f562bbeeebdc44a7499d5eb6df47bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:17:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:17:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:17:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:17:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0128ac9f9a99d35c98e291a9dd00c10d2e3a97a0a0ffb6074ecdd44b27dc4e`  
		Last Modified: Thu, 05 Feb 2026 22:17:28 GMT  
		Size: 21.1 MB (21115444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd43103182b018ea3b423990f424eb1d9069ec8619db1e00608ad5d0b1ba1420`  
		Last Modified: Thu, 05 Feb 2026 22:17:31 GMT  
		Size: 144.8 MB (144762246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3640e9845387db2923c6b23397e35f93927fea181ad513c394008282c177df`  
		Last Modified: Thu, 05 Feb 2026 22:17:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9814d1b2085ef65a9f6d69e4efddd0d2d62c792e7438e60baba1f93c9e117697`  
		Last Modified: Thu, 05 Feb 2026 22:17:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:71f5de05b474bba099e9d9b28e337d0ecc9a5aaff5a179fd1b419f9a9281838b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1123636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a6fa8e2a557cad4990c420b90dbdae3a29a5ff2af1c0c32be9518ce4376753`

```dockerfile
```

-	Layers:
	-	`sha256:03ce387ebe5783b7039f128c4a43d35548a403adf927a9dd4e46af61aa5fb3b0`  
		Last Modified: Thu, 05 Feb 2026 22:17:28 GMT  
		Size: 1.1 MB (1104025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d6f1b49c09cf33a5089017d2e2b9571e6fecace8c458fa460fca61970b6135`  
		Last Modified: Thu, 05 Feb 2026 22:17:28 GMT  
		Size: 19.6 KB (19611 bytes)  
		MIME: application/vnd.in-toto+json
