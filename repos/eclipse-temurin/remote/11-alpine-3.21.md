## `eclipse-temurin:11-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:8631bdced20560ea97c24dc5ed6551a5c663155ef3d6d9e0458f52250c2d4d77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:614d9c88a9cf94e49d0268607a35c6f7c2751e3fc7123bc496522c9e582caa85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160549071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11040d8ddc7015765a4c6fb3bc6cf1bf50ebe734e2f50c90be10c16f7fd5d542`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='2e1f667395cdb1e872bd7320e3eda96c0f0978e29e574e75f9cdf61160e8974a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e0aa54164b6843d552c2435c045a0c5a2a2cd27283708e6fa2180148173693`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 16.1 MB (16135248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c720f84e28bacdb3393ed6b2a6030be896b26260a582ec9b98eaee9309811459`  
		Last Modified: Fri, 31 Jan 2025 01:29:56 GMT  
		Size: 140.8 MB (140769699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bcb92c2573d219bf42db4d1fee29137d4475aa507f8fa3b9562b018fee64bc`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70629d9a9ac9d595010d8b726a594730976dcb5a79615ac00b7d828903ecb498`  
		Last Modified: Fri, 31 Jan 2025 01:29:38 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:84541715d98bde49ed2e3a2489eb3c641bebe29acb7477718f252d9fcf1aecd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1015442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3dd7ff57454008d3a95e15349bbf07f66e3946794d65811497f91a08343244`

```dockerfile
```

-	Layers:
	-	`sha256:560bb1d5095c41eb26fd1e25404e9bfc37f178c325c689731fdbce0e0842b999`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 995.2 KB (995233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1469646bb84a6d68227062f9eadc2cda39f388b4ab344567806799f854831b52`  
		Last Modified: Fri, 31 Jan 2025 01:29:52 GMT  
		Size: 20.2 KB (20209 bytes)  
		MIME: application/vnd.in-toto+json
