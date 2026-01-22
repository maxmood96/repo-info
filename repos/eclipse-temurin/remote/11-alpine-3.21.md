## `eclipse-temurin:11-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:e46f408750ff2de6bbf4001e3ae901c86c4b89524919eb7fa808a41f0b82abcf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:dd5143cf2acc30ac91f4be723af5bde7a730b524a7c29b6b627115af2c322817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159921746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b0da602575484bddfb6487d553a6bed753955f8ffb51a7f0f2109f4af291c8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:52:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:52:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:52:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:52:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:52:34 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Sat, 08 Nov 2025 17:57:02 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='c7b58655ffde7b5e6fce4a32fdcd21be5745b3bb64ee2bc723fcf55eae720ebe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:57:03 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:57:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:57:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:57:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c7058b15b74dfb201889d176cc8eebf0e009d1264ef4645766c89a8432aa07`  
		Last Modified: Sat, 08 Nov 2025 17:52:48 GMT  
		Size: 16.2 MB (16174518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2120d463506ae4d709c06efaf8ec0f2fdcd8421ad7823c3832310345338f62ad`  
		Last Modified: Sat, 08 Nov 2025 17:57:19 GMT  
		Size: 140.1 MB (140102249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11051f8ac27986c365fd02c4ea6d8c32410b2cea1ab26d04a335c40780f8a108`  
		Last Modified: Wed, 07 Jan 2026 20:03:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d771625b613e3026bd0ffe9748ac1cbbdb5419e98006990fa45bba3c5b4efd`  
		Last Modified: Sat, 08 Nov 2025 17:57:15 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:85134c7dd244559c03210a4ba5e5a602df7140fedf61fb81221e22001c8267ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1018655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241f63dc1f62953e565977d15b2f4676d0b2005a0aca3118a2059fc665e38de7`

```dockerfile
```

-	Layers:
	-	`sha256:3a728eb3ee859c32e6a9adf5e026bc05404f6e4eebd84d56a6a509b63a84abe9`  
		Last Modified: Sat, 08 Nov 2025 17:57:15 GMT  
		Size: 999.5 KB (999485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:690cff54d98f2a0bf5ece532d8a89b9b4460ec2e75222defaf19b713252778ec`  
		Last Modified: Sat, 08 Nov 2025 17:57:15 GMT  
		Size: 19.2 KB (19170 bytes)  
		MIME: application/vnd.in-toto+json
