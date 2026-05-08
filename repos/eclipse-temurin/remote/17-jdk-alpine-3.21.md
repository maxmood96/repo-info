## `eclipse-temurin:17-jdk-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:601bee717525b478c15e53c9b75d8efcb215cd7e13ccb2835839345451267dba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:cdbd9b0bf103836f115bf5227fc147f981b398e03320976c571d9ccce4b5ebdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169696405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90142df4ac86979e48c5c76aaadbeada2b913c519a0a381a7d57cebda08c69c8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 23:58:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:58:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:58:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:58:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 07 May 2026 23:58:38 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Thu, 07 May 2026 23:58:44 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='960b4090b75a887bb21a915a294bee3a97cd11876967c95e5bd29d9ec4812e17';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 07 May 2026 23:58:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:58:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:58:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 07 May 2026 23:58:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d9760dc5aeed55df14e1eade64e39ec4929612d30270bd8c03a6b25bfc9058`  
		Last Modified: Thu, 07 May 2026 23:59:01 GMT  
		Size: 21.0 MB (20995405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f09c58b70655da00cb96d9678b9b978627887daee44d1fec9db81f190e2ea69`  
		Last Modified: Thu, 07 May 2026 23:59:03 GMT  
		Size: 145.1 MB (145051715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f7445ea6d71346e276c14610d3b74da5ac9eb3e0ea63603b2faf9997bb4ad1`  
		Last Modified: Thu, 07 May 2026 23:59:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e026a90f17b88ab606e539aad837f7ad6d5683576552b8d012c9f2a58d5d254`  
		Last Modified: Thu, 07 May 2026 23:59:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ae7bd0f31dcbf240f8b80bf04fc3499e66dd9696a65c193188b77812f9268d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1122047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfef1034d647e90fa6c23d0a993878cb839977b40118ce74705efdcc33e0aed`

```dockerfile
```

-	Layers:
	-	`sha256:b030d504b27052276f6226bec302e1f7ca187fb99110e887736c5fa6e0201a85`  
		Last Modified: Thu, 07 May 2026 23:59:00 GMT  
		Size: 1.1 MB (1102426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:563415e10ee8ae5cbb8bac3d11055c424d48ec267fd2dbc359aa8eb77aa1d0ef`  
		Last Modified: Thu, 07 May 2026 23:59:00 GMT  
		Size: 19.6 KB (19621 bytes)  
		MIME: application/vnd.in-toto+json
