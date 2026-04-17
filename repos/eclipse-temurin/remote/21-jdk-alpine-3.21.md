## `eclipse-temurin:21-jdk-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:6dd49e971e444ea226f821f5e94de59a314f7c27411004cddc5c44289a52276a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f6bf9cfd62d7f1fca386ca22cafbf4dc907ebe93b73f06ff561ebbd4eee26424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182742604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d3ca5480a888f1d0344a1c6d0aaf40c63672ee879f52fea858006030bfda73`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:24:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Apr 2026 00:24:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:24:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Apr 2026 00:24:18 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 17 Apr 2026 00:24:18 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Fri, 17 Apr 2026 00:24:24 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 17 Apr 2026 00:24:25 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 17 Apr 2026 00:24:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:24:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 17 Apr 2026 00:24:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414d19b83c89e07b8bf7da8c832b559a4c6891a0f8166b42efa6d27e068fa635`  
		Last Modified: Fri, 17 Apr 2026 00:24:43 GMT  
		Size: 21.0 MB (20974409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb2e37b0fb9116cd2892c211160755315a7bcc0b3e1e383fe5403b70cc096b8`  
		Last Modified: Fri, 17 Apr 2026 00:24:46 GMT  
		Size: 158.1 MB (158118911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05b83a6bfcb7380ed7ed5ef3d401fe82722216211d00eed0a1349d5ca2323da`  
		Last Modified: Fri, 17 Apr 2026 00:24:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1117ae44a490bee4c72fa1665d887128c5c7c556b9317264e7e87278291b690`  
		Last Modified: Fri, 17 Apr 2026 00:24:41 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:620aec835cf9cd75adca609c651153590232b70acf49bce58514845464f21a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1124071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6d05e9725a847b56d01d6ec6fc226fce60cee33ce2bea8224bd9c78fb8f522`

```dockerfile
```

-	Layers:
	-	`sha256:40506009ecd25b91534c5e604de3dbdac6bd1971aa20e4e5436027509656f3fe`  
		Last Modified: Fri, 17 Apr 2026 00:24:41 GMT  
		Size: 1.1 MB (1103649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6c63d50f1fb099ddcd8baee8359c3f5390397bfdb2dadbd5e32dfe1ce62331`  
		Last Modified: Fri, 17 Apr 2026 00:24:41 GMT  
		Size: 20.4 KB (20422 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-alpine-3.21` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:e3cea3dc83c4749b8aac8ad98fd5731d87bae0a1fa2c190cfcd7e179b6d37b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.2 MB (181151379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6261336813090bf3c45de7e0886d54ef04475061b6e7ed27db270aa73a9dde3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:25:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Apr 2026 00:25:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:25:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 17 Apr 2026 00:25:46 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 17 Apr 2026 00:25:46 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Fri, 17 Apr 2026 00:25:53 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 17 Apr 2026 00:25:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 17 Apr 2026 00:25:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:25:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 17 Apr 2026 00:25:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442998c9d04ca0a3e1a44320dfca57f0bc583976bb738a3ca3c51b136aa2816a`  
		Last Modified: Fri, 17 Apr 2026 00:26:12 GMT  
		Size: 21.0 MB (21024516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40ed4e578b339b06637071306ca88067ad5550baf7e91b3b3ddc262d059eba2`  
		Last Modified: Fri, 17 Apr 2026 00:26:17 GMT  
		Size: 156.1 MB (156129991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e10c138cca9e900d319318f296b0368bc614511093d2cef529a32dd7bfcddd`  
		Last Modified: Fri, 17 Apr 2026 00:26:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd86575a8a949ead6d3d97343fd1864e61ed0db4e7dbc0cfcae6fe85a1f07bd`  
		Last Modified: Fri, 17 Apr 2026 00:26:00 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4b2b6680343fb24469dca7a3c6ce0976464c5c234cce3105e588b9380fe38d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1274195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8ec8afdbcb9bfe3ffa6a818a1ac060d1d4e9a386fbb5f6afe20be87bc6b218`

```dockerfile
```

-	Layers:
	-	`sha256:6cdd03fa1722ead56413bce932fb92e9de7d81785c2d8fc1a072108545c7723e`  
		Last Modified: Fri, 17 Apr 2026 00:26:11 GMT  
		Size: 1.3 MB (1253651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:478fb497e0355af7e4e83cac2ffd73ee5e954b3869c119e24e96ed72cface38a`  
		Last Modified: Fri, 17 Apr 2026 00:26:11 GMT  
		Size: 20.5 KB (20544 bytes)  
		MIME: application/vnd.in-toto+json
