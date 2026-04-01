## `eclipse-temurin:8u482-b08-jre-jammy`

```console
$ docker pull eclipse-temurin@sha256:7c083797a6db6f30cbab68e84cf522c9a387938e3c72ffa76906de9f081707c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u482-b08-jre-jammy` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:09b990655ec5ab412beca4a8eafb7af3feca61bb525d5324a7cd6583d641e6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88219936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775af7f7e595ffe76029e4c2efefd187e8bbda30d64a56930c9b3c08dbf39ec4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:09:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:09:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:09:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:09:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:09:57 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 01 Apr 2026 20:09:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='29c93e29421b9f77bc95305834f3239313466fd988111b5cf409fd9a2f727cff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 01 Apr 2026 20:09:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:09:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:09:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411d94d78660651982f8ea9396c29f168b475309253aa58800d66bf5d35b43c3`  
		Last Modified: Wed, 01 Apr 2026 20:10:11 GMT  
		Size: 16.1 MB (16149386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903ded3f2e7787a196c167b95e9350307d7ae11c304cb25e811211af6d122e61`  
		Last Modified: Wed, 01 Apr 2026 20:10:12 GMT  
		Size: 42.3 MB (42331727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94107fcdb07671418b9a112d2e3ef304d514331bfabb2b879ae3b0d259b3413c`  
		Last Modified: Wed, 01 Apr 2026 20:10:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60911814702725156de46c13c1365f5e1310e172a3ee3d5294c22a56e9eb50df`  
		Last Modified: Wed, 01 Apr 2026 20:10:10 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:101a72f96c18a9a95a822ad2276ffe4d635e32368bdd18051c49dea791c88355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24249aa049daa2f6de72807b543e23e91937a39fffb445faf8a3e70834e0f1e6`

```dockerfile
```

-	Layers:
	-	`sha256:da41177bd9299c7c603009f243c699cd951704f8614368e034dab71e3b614d68`  
		Last Modified: Wed, 01 Apr 2026 20:10:11 GMT  
		Size: 3.9 MB (3910108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e26f4fe499118c32f4efe3ef67ee1d342da7bbf6f4050e50fbd178f0fa21e25`  
		Last Modified: Wed, 01 Apr 2026 20:10:10 GMT  
		Size: 21.9 KB (21916 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u482-b08-jre-jammy` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:7c370f18c94249d1db1ed6b4a69ac5a9253b46d58d14ab5b05e037c4da908f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82503303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c013301939ea71a649bd030f5d41e4b7ff46bcda666e2856a712383ec93687`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:eaa1e345a925acc7b826effa9fb4c3dfb4aebe47807533938898d49afe7561cb in / 
# Sun, 22 Mar 2026 18:14:12 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:08:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:08:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:08:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:08:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:08:29 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 01 Apr 2026 20:08:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='29c93e29421b9f77bc95305834f3239313466fd988111b5cf409fd9a2f727cff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 01 Apr 2026 20:08:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:08:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:08:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e7c88f36edd2a67246005d083413bd656459d3b63bab8e6a05a1018c7658daae`  
		Last Modified: Sun, 22 Mar 2026 18:43:39 GMT  
		Size: 26.8 MB (26842286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88633c2d7cc2d76a9d37cfd237103b2a3adfab73bfcf26bc834697fb03606a2c`  
		Last Modified: Wed, 01 Apr 2026 20:08:52 GMT  
		Size: 15.9 MB (15890056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d046a13da3ebce1756213113acdc7d17dc6b78a2b9868b52c0adf5f4f843535b`  
		Last Modified: Wed, 01 Apr 2026 20:08:52 GMT  
		Size: 39.8 MB (39768551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003b56c550a2199fc0871f67f0dc9e6a81b6ac6bb727f7bc3742e1d9f7a53a13`  
		Last Modified: Wed, 01 Apr 2026 20:08:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abaf50509bd5bd543f12f674a14758f9c3b3f6aece558256d07ecb0e4ad1e9e`  
		Last Modified: Wed, 01 Apr 2026 20:08:51 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:bfd25c28fa66974c130c5fd8a86ff2286ee250657e1f0c3f5dfa69809a9623d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c477a2a271cd96c9aa5eef3ed2f123fd0bd067068efae76d0219cebeb31ab295`

```dockerfile
```

-	Layers:
	-	`sha256:d7f6059c41eba0fc1c12a48bcc41471c018fb6dd7b5a2141611085a4cc8de152`  
		Last Modified: Wed, 01 Apr 2026 20:08:51 GMT  
		Size: 3.9 MB (3916115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06f9943ffdf6f1ea7791e1e19f51f8b2971fffd13c0dd34ee42ce4155691d46b`  
		Last Modified: Wed, 01 Apr 2026 20:08:51 GMT  
		Size: 22.0 KB (22007 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u482-b08-jre-jammy` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:cfed1d00d76920c24240055a25833bfc85329c5bfeeee4aea70fec62bc454d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (84972367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1965620dec5a98f99edd13f448a78899529b43c29434df4281f682a2e1309910`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:10:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:10:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:10:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:10:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:10:15 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 01 Apr 2026 20:10:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='29c93e29421b9f77bc95305834f3239313466fd988111b5cf409fd9a2f727cff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 01 Apr 2026 20:10:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:10:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:10:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e9014f5eb87367d3448681e52c7e826b56cc01711c064f54350ab40885507d`  
		Last Modified: Wed, 01 Apr 2026 20:10:31 GMT  
		Size: 16.1 MB (16073495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840913b96d7ce295d1bd76661ce2b7ad31103d72df68fef5f9e359062dbe423b`  
		Last Modified: Wed, 01 Apr 2026 20:10:31 GMT  
		Size: 41.3 MB (41289519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64a78bc2c872bea616c1ee331e63a747bc4bacc5b6fcc58a6671489f3e61eed`  
		Last Modified: Wed, 01 Apr 2026 20:10:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507fa1c7ebbfaf51a003a36e8bf76f07909e5dcb4eb69c2f8b8036e7b63d13aa`  
		Last Modified: Wed, 01 Apr 2026 20:10:29 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:23acb6446cd5b5f1234291a8430b13d1aed6785f3df9c2086698fb484943fdd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6d07a2eeaf46fe2cb16dc4050d316208bf218ec3e097ec9c683cdf1fbe1211`

```dockerfile
```

-	Layers:
	-	`sha256:7ced46737babb40e8c11e7402d255d577bae137f379c834381d61f2dce924830`  
		Last Modified: Wed, 01 Apr 2026 20:10:30 GMT  
		Size: 3.9 MB (3910456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8175a3677036ac5745cb318c9bf227a1802686e3cfdd08b12ea2f6ea27cc5121`  
		Last Modified: Wed, 01 Apr 2026 20:10:30 GMT  
		Size: 22.0 KB (22027 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u482-b08-jre-jammy` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:b4f35275b84cc956ed646be8abdb21522c3e8035da3d53f0d7b798811bc9144f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (93998175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503d806bc3ffdebc41d36791cc62d65fbc1859dfd7c4d267ca5fdfa3ada01774`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:20:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:20:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:20:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:20:51 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:20:51 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 01 Apr 2026 20:20:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='29c93e29421b9f77bc95305834f3239313466fd988111b5cf409fd9a2f727cff';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 01 Apr 2026 20:20:58 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:21:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:21:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e568bb13a59c072b3af8c406e7b451459d28a2bdf653f96393ea9610f7d09959`  
		Last Modified: Wed, 01 Apr 2026 20:21:27 GMT  
		Size: 17.6 MB (17622524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d5afe00e5afbff2327f1e5ddfe70480d6bdb9f90ad6f92e1a98cf210440d36`  
		Last Modified: Wed, 01 Apr 2026 20:21:27 GMT  
		Size: 41.7 MB (41723583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85ac7af2e315c52c0d13aa1fb591e1afeb6936b7f5ce9f71452bf9a9499e439`  
		Last Modified: Wed, 01 Apr 2026 20:21:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab1587e146eac7857d6b4db8ad86055e9020258b1e33f51f83af77d31866425`  
		Last Modified: Wed, 01 Apr 2026 20:21:25 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jre-jammy` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9a3d6b05bad656bec441ede1d1ee38278a78d2859822d012fc9e67564f61292d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3936826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c19df8951d3a1e08e9bae9cbdba6b3288231f96fb9ba8d0f450528f7bc330f7`

```dockerfile
```

-	Layers:
	-	`sha256:ca6e05d7995bac0dca9fadf235d79a5c9ecaf1564bed495c7597da6ba72fc8ec`  
		Last Modified: Wed, 01 Apr 2026 20:21:26 GMT  
		Size: 3.9 MB (3914873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1f946f17f2318b5a2436d0b7fd9521c4e8a11c0cb3e91b676fa2a37e79a085`  
		Last Modified: Wed, 01 Apr 2026 20:21:25 GMT  
		Size: 22.0 KB (21953 bytes)  
		MIME: application/vnd.in-toto+json
