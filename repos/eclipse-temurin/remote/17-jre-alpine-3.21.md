## `eclipse-temurin:17-jre-alpine-3.21`

```console
$ docker pull eclipse-temurin@sha256:865cca6d0b31f284a5fc4e8cbd8f9375f470fd07cf6e909cea62f2790d4187fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `eclipse-temurin:17-jre-alpine-3.21` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:7e1a7f5301d77be53b54bb2a82d18edc70dc6b88a7ec795253c90e9c4b608898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66439686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2aa7b0be9ced7b5cc272d241a61cdcc0ec44158aba72c02ac3595f7451ba36f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
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
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='9dcc53a30676692e604571a6e0bd13ac0c1b15f4bc2b78d19f88bd316075f84a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cc66ba0a96819420d8faf6f4c52e8d945d6b63a95860584022a8a19e6e7826`  
		Last Modified: Fri, 14 Feb 2025 20:34:33 GMT  
		Size: 16.2 MB (16175644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2830fdce3f8490cef419b2649bc04882f36bbb72656a0e08c4b4b851191b46f`  
		Last Modified: Fri, 14 Feb 2025 20:34:35 GMT  
		Size: 46.6 MB (46619385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d359e0dcce06e171a793aefe4843a8de78a18e661c1037ef36dfd3cce3e4852d`  
		Last Modified: Fri, 14 Feb 2025 20:34:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51631fe5dc907fa7751b1ea513749d84083935f3b79726f22e765131db943325`  
		Last Modified: Fri, 14 Feb 2025 20:34:32 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:95564d096b99301357dbe13bb38badd3ba87eef0dda7b651a0aa456738d71808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **909.9 KB (909852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed8bc54c886dd6d6c97c5176db2ed16fc626a9b37575cd9d940881e62c8d39f`

```dockerfile
```

-	Layers:
	-	`sha256:79989167fab2c1e3ecfc203286660d969dc8684c1c11b6015784f88084c1bf67`  
		Last Modified: Fri, 14 Feb 2025 22:13:38 GMT  
		Size: 890.9 KB (890922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9e9728a93821b44034d738a6245934d57ccb11e1480e14e672b54da00d0a36`  
		Last Modified: Fri, 14 Feb 2025 22:13:38 GMT  
		Size: 18.9 KB (18930 bytes)  
		MIME: application/vnd.in-toto+json
