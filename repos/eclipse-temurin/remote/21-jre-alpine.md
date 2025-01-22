## `eclipse-temurin:21-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:dce9a9b7de574c317962ff255d43f624cbd97ecc99e218353b5db169cbe4f13d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eclipse-temurin:21-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:01dce286c246fa0f905f9130aae1c2ec685d59052f36b13ee30cb8e962468139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72818856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119fc760ce6284d05a3a8e48409e2e8b73755955763a842df08c366a27a8585f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Jan 2025 01:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 01:19:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='12b988a3d934e3eb89c6a981a93f8e2adf0a62cc9030487dee76c0c29b93714d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='2dfa33fb8e9474e6967c6cf17964abb5ddce9c17fa6a9f8d7aa221a0ae295df9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5659b39bd49de33bcee35552f304c295a740369c1ab0ca99a218050524788829`  
		Last Modified: Wed, 22 Jan 2025 18:28:43 GMT  
		Size: 16.1 MB (16135294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b993f9652cd49ac9dceb387d9aca70fc8acff6c04d043e00e8d686b84e1266e9`  
		Last Modified: Wed, 22 Jan 2025 18:28:44 GMT  
		Size: 53.0 MB (53039438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde96ae108e0ea7f93f0e8e6113c630f022c5308f7aa3434561ab2cb0a2cf080`  
		Last Modified: Wed, 22 Jan 2025 18:28:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60b2ad13be19694daf1a89afdcee310320a8b59ba77f6893e78f5de5ffd6f2f`  
		Last Modified: Wed, 22 Jan 2025 18:28:43 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b5db4e1fada938c1aa6d1abbd5d9d6c46cf3dc197e54db91a08c41d7c878cf90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **913.2 KB (913158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8298da77b11e6a9dac18b3464edc954ac9c3ac8842e7e67046e8afc3eac1ad47`

```dockerfile
```

-	Layers:
	-	`sha256:448c4136d2f4612da1ee8de0348e622d3d6b7d2460e182ce252e6e91a7337534`  
		Last Modified: Wed, 22 Jan 2025 18:28:43 GMT  
		Size: 893.4 KB (893416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b25286516868483ee60792800d41be1228a0ea7e6aff79b3a257c78a627e6f`  
		Last Modified: Wed, 22 Jan 2025 18:28:43 GMT  
		Size: 19.7 KB (19742 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:e206bcee917b41015fccdeca8a93440f60e5dd374e0a0c0ca0e7f2159aa2d24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72365719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9132dd7d084faaa268a3756c6bdb53c1bbe658981b9e47d2bcd682aaa20471cf`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='12b988a3d934e3eb89c6a981a93f8e2adf0a62cc9030487dee76c0c29b93714d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='2dfa33fb8e9474e6967c6cf17964abb5ddce9c17fa6a9f8d7aa221a0ae295df9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331b45a14f398c306e40c479b2349b2483f83614aa5856f51d0bde876e02bbd9`  
		Last Modified: Wed, 08 Jan 2025 22:23:35 GMT  
		Size: 16.2 MB (16187942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadad08fdf59b77fee1496642636c9d1e48b51c478362a6ec9c6ccfc057b2d3c`  
		Last Modified: Wed, 08 Jan 2025 22:23:36 GMT  
		Size: 52.1 MB (52084599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53333c38ca5251f99d41ac07e8a9b6b3d55fcfbc8db4a3c124a7c47aa852939e`  
		Last Modified: Wed, 08 Jan 2025 22:23:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29caa31193cf72c3cdde29ff495b92727c0c52f574bc801476f7382d19615cf1`  
		Last Modified: Wed, 08 Jan 2025 22:23:34 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-alpine` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:66e6a400c42a7ae5048e0f51a059801813f3e6c0a75ac743ae89a94be0be87e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **904.4 KB (904444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b327e56c798799283d34ccfba000b63b492390ea66aba208a1462c6be1e9a51e`

```dockerfile
```

-	Layers:
	-	`sha256:fdaf89ab18c35fbf40650547251283fa687182f14f7b7eb116a2c1ca6cab3173`  
		Last Modified: Wed, 08 Jan 2025 22:23:34 GMT  
		Size: 885.2 KB (885245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b1c4d2dbd409848afa3c698f8a3beb7924228167bf6978c8189c7c0efaf094`  
		Last Modified: Wed, 08 Jan 2025 22:23:34 GMT  
		Size: 19.2 KB (19199 bytes)  
		MIME: application/vnd.in-toto+json
