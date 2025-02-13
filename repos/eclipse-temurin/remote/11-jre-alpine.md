## `eclipse-temurin:11-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:760d8ca92f4231ecdfb287860a8888c14a06fb601918919f3b86e499b8ab0503
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:11-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:bc4be6fa50d7edd7c2412e179dc6895b0f7fb97ba7ff38621eb5b626c745c208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63355764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d09ac576629d98e55c3e31828190f95a8afaeb9156455a816475d7d4438bc9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='69031fc68d41189691dbeca73447ca543040d26995f61cef83fd7aed8fb4dbd2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5a42cf738281976d915dbd55f89c2fdd7ba7b8fde6ab2646b28d40e3b012d3`  
		Last Modified: Mon, 03 Feb 2025 20:15:19 GMT  
		Size: 16.1 MB (16135304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055b64b6daad64d7a5bf24a7726dc253f86e814dc09800053216da9986aa3098`  
		Last Modified: Mon, 03 Feb 2025 21:04:56 GMT  
		Size: 43.6 MB (43576339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e556e87b038d9eed0f6bd10546cfec1490acd3256ab2c008a9938c2f6af4ef91`  
		Last Modified: Mon, 03 Feb 2025 20:31:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70629d9a9ac9d595010d8b726a594730976dcb5a79615ac00b7d828903ecb498`  
		Last Modified: Mon, 03 Feb 2025 20:45:06 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ab901183c22208267c535d4444be7c751759dcddd6175bd82b831a0b6ba8c2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **922.3 KB (922336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c743ae4f0149e2453fda5284c7d80b1ccde498126f6b05328d72c881354d14`

```dockerfile
```

-	Layers:
	-	`sha256:1eaec6660533c2d689f5df41ecfb1766e3a393571fa6f4246d233478a1fa25dd`  
		Last Modified: Mon, 10 Feb 2025 03:03:53 GMT  
		Size: 903.4 KB (903405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b06c3b778e2d913212b1652abb1a35bfea18174ea329b5e2149c0a16c56bfac`  
		Last Modified: Thu, 13 Feb 2025 13:51:08 GMT  
		Size: 18.9 KB (18931 bytes)  
		MIME: application/vnd.in-toto+json
