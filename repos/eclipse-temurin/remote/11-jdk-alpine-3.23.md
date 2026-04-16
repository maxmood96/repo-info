## `eclipse-temurin:11-jdk-alpine-3.23`

```console
$ docker pull eclipse-temurin@sha256:3febcdb4bf3bffd5205fb827fbc8360751760236b48454eb077c2a8f68b389e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jdk-alpine-3.23` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:1fdfdec861f63196d36a8f86b7ddb24b85653bda0862b0621507edaea99916a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161621102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e306b9d2b1ed442b42e8fe27a874ff3b822210349f614e5acb419e36ee2848e8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:32:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:32:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:32:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:32:47 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:32:47 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Wed, 15 Apr 2026 20:32:55 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='b55a38b75ba99d86f4adb47552ee5306b9589e2026861a3b8f030993c42aedc7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 15 Apr 2026 20:32:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:32:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:32:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:32:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec914d871e26d0465399fedbb12a944add78359e4bacb45111654e407011389`  
		Last Modified: Wed, 15 Apr 2026 20:33:10 GMT  
		Size: 16.8 MB (16837789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e0f2de0712b22eb820b820ec9d10381f0162a40034dd9db90063cf9bc5b7f9`  
		Last Modified: Wed, 15 Apr 2026 20:33:13 GMT  
		Size: 140.9 MB (140916718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97836bb5bbf19dc634eaea3ff5cfbc9b0ca22932b1bbb49c9a806a0bb040b842`  
		Last Modified: Wed, 15 Apr 2026 20:33:09 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c470514f36b76e7d4fbd25626009aade331446b35fde7acb2f42ae8b0b5c53a1`  
		Last Modified: Wed, 15 Apr 2026 20:33:09 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-alpine-3.23` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2472c8416ab6f069535b54d296facb8e30145145e54bd5345aa4e58e37f72661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1027115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1f6bfb3cfeeab950d6f00632fa54dc8a019fe00e8ab876cd1450c0198cbe20`

```dockerfile
```

-	Layers:
	-	`sha256:78d5dac24fbe5897eebd92c8b7c2b92b6a9db1dda25468e4d65ac8e6f0f833a7`  
		Last Modified: Wed, 15 Apr 2026 20:33:09 GMT  
		Size: 1.0 MB (1006950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62ab4de07526012ee7474aae8c7483278cc0dbc322e6d8ab8076043359850a08`  
		Last Modified: Wed, 15 Apr 2026 20:33:09 GMT  
		Size: 20.2 KB (20165 bytes)  
		MIME: application/vnd.in-toto+json
