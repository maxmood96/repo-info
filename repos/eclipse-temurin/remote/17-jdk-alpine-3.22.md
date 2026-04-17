## `eclipse-temurin:17-jdk-alpine-3.22`

```console
$ docker pull eclipse-temurin@sha256:cb75717ed0a1daf0e285a6ca656e3d92aff50d718c76b9a7489ed80d6a4a7dfa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:2c38758c613c2039ebc2a23ccc9b3f3495265c0b795602b62dbfb58ca0806138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169711560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbc04a30d7925bd53cfd4b3e0ffc48c1773b0ef2dc6546f95c3dfd9c8726dca`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:24:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Apr 2026 00:24:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:24:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Apr 2026 00:24:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 17 Apr 2026 00:24:05 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Fri, 17 Apr 2026 00:24:13 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='3246fb1834d21c22ed717db9f8ba3f07e0f562bbeeebdc44a7499d5eb6df47bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 17 Apr 2026 00:24:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 17 Apr 2026 00:24:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:24:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 17 Apr 2026 00:24:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a8d3d923bfb3335930fc2415e8ba786dafd1f83b1bc68c356c918c50b0125`  
		Last Modified: Fri, 17 Apr 2026 00:24:28 GMT  
		Size: 21.1 MB (21138606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d849453de0104feacec2ffa3e6b81d10bed040107797f739cc944d06ab3bb54c`  
		Last Modified: Fri, 17 Apr 2026 00:24:31 GMT  
		Size: 144.8 MB (144762354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249fc4fcff3484351ff3ca6dabc05082ade8db7e74339fcc5184778aa6c66da5`  
		Last Modified: Fri, 17 Apr 2026 00:24:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5047c160ce3435880d7d4f1d4b1cad35d8b3cf7436a71bca82fc09109e72b14`  
		Last Modified: Fri, 17 Apr 2026 00:24:16 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2e5fd430a025ad95cfd8ea4f572f4f4160fa789e7a4180c1fd82fc794b3a7c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1122951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288a6eaa5753d318a7bae6489b16ff3912c9ee5cfe586e09b142cf3110b8e8c2`

```dockerfile
```

-	Layers:
	-	`sha256:570d2b4875006a172793daca40d95703cc14a86c7acbdc532bdd8ea644d18eaa`  
		Last Modified: Fri, 17 Apr 2026 00:24:27 GMT  
		Size: 1.1 MB (1103340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca6e7b227c24266d6cece9a917a3b1c93bbd5a08f2483b14be658fc9d16d6f01`  
		Last Modified: Fri, 17 Apr 2026 00:24:27 GMT  
		Size: 19.6 KB (19611 bytes)  
		MIME: application/vnd.in-toto+json
