## `eclipse-temurin:17-jre-alpine-3.20`

```console
$ docker pull eclipse-temurin@sha256:1df3b3f0077cb0c8df449d8211fe1e076a73332b7e45be0085a705167a27e4e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jre-alpine-3.20` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:1f0d78aef0944ab6b63327dfa2ef21d4dc0c2c8eb4782a6e0943519c3b7967c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66371794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95b28719e0ff5336cca1c50fc3ab756064a75477a516cb2fcfd958cf7c574b2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:58:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:30 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:58:30 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='6c3047e8edd3878e8d2a1cee95c04606042c6a55954ad365d20b58f88cc9ecd5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sat, 08 Nov 2025 17:58:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e2a06b10391ace47765a057449ce09f2c43b48b3e4e4ad2d908bb0b6c44da4`  
		Last Modified: Thu, 08 Jan 2026 00:08:26 GMT  
		Size: 16.0 MB (16023387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bd5b47abf113b66566abf1291ea7c79e27f693bcc749036c6de2e6b01c9bf0`  
		Last Modified: Wed, 07 Jan 2026 23:58:47 GMT  
		Size: 46.7 MB (46718945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd8b29d0efaf2db0604c3ef5315727c96d0e0ef88c5a666d15e9794dda2a0ec`  
		Last Modified: Sat, 08 Nov 2025 17:58:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9d2d77875a4620f9951b6db5a3cb20f43b6a08202ca955cd292118bae2cad8`  
		Last Modified: Thu, 08 Jan 2026 00:08:27 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-alpine-3.20` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:81747f8b79bc23d97bcc6a691021e64eb73049ba6ad6a69d08b8cf4ff00f08e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.5 KB (906467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca190368d47c814e3b358095804483ed42cf351a23411e0b034618155e3b92cb`

```dockerfile
```

-	Layers:
	-	`sha256:18fae7e283513b4fe3bf6ac80f44beb5ad16f13df7ab4da1f6ca89f0cbe98730`  
		Last Modified: Sat, 08 Nov 2025 17:58:42 GMT  
		Size: 888.2 KB (888243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:743bb2354c5b03bf29f4a6785c0b0b6fd17426e3e2559ae74146c0566168c74a`  
		Last Modified: Sat, 08 Nov 2025 17:58:42 GMT  
		Size: 18.2 KB (18224 bytes)  
		MIME: application/vnd.in-toto+json
