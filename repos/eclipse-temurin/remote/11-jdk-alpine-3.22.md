## `eclipse-temurin:11-jdk-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:7706f66121ea03730772099da03407b1a1b57f310278761148d6e50e5694fe73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d4c32aaeab45a0624f4d15829b627c8be93fcc40b3d938fc7c019f9aaf4a3fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161154102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7203ffea720e335ded4a99540891593965af8eac6e3e09b8765076465cbf6534`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:56:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:56:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:56:37 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:56:37 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Mon, 22 Jun 2026 19:56:43 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='ed06a4b8381786a6e8091c10539856675497d2b821cd2d0200cc5b65f453b982';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 22 Jun 2026 19:56:44 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:56:44 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:56:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:56:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91056ca0b8099151118f30bcc3ab7ad0b1271b8ef58a8df46a58ae9c6ecbea0f`  
		Last Modified: Mon, 22 Jun 2026 19:56:59 GMT  
		Size: 16.3 MB (16289496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b8a7f24ef14bde3833fffebedb1db9555a92dd7ee64ac79185483a6b5d30aa`  
		Last Modified: Mon, 22 Jun 2026 19:57:01 GMT  
		Size: 141.1 MB (141074602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1a111cfda011695e74fc96ba47465a01b4c8aaeadabb04632960f4fc853ffa`  
		Last Modified: Mon, 22 Jun 2026 19:56:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039bafe071a7d694a048eea276837c72fc3629f45db9dfb8705b8f490e54e5c3`  
		Last Modified: Mon, 22 Jun 2026 19:56:58 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5c39d78f24283b423f28e7c4f8a67d19f182d220d7be1958f2395192e4ad953f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1003908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b66e95e583f72dcf2b563c63fe91d319921dbf3b6e3851791daf0282b3671bb`

```dockerfile
```

-	Layers:
	-	`sha256:34fa9e0c741568bfb79ac27b7a86d19dacc28feec274b6c12b48ff2bb9f93b23`  
		Last Modified: Mon, 22 Jun 2026 19:56:58 GMT  
		Size: 984.7 KB (984728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:358107f42fbb86e84e3d5ac3bb213e8be344c80049c47c0c9ee72e257778f75d`  
		Last Modified: Mon, 22 Jun 2026 19:56:58 GMT  
		Size: 19.2 KB (19180 bytes)  
		MIME: application/vnd.in-toto+json
