## `eclipse-temurin:23-jdk`

```console
$ docker pull eclipse-temurin@sha256:0a9e7c45bb01e32c6ba72b6324af8a650462ebbbee509349140c36a5390e675f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:23-jdk` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:64e9d5fd87e4a282436e81524e39dc6d0989f0964e586fff1e81ff13fc0819ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216390137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae6d0c7e84c83b1deda99688877570da3955d9049c5b0173ff402ffee380cda`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='870ac8c05c6fe563e7a3878a47d0234b83c050e83651d2c47e8b822ec74512dd';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        arm64)          ESUM='fb43ae1202402842559cb6223886ec1663b90ffbec48479abbcb92c92c9012eb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64el)          ESUM='548fd82af4eb0802fe20b0b61a4664a69c7f03cd963540908f30dbf73636dafe';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        riscv64)          ESUM='1e102e1e6653f8810ef6c275b0d38ea7036abd4a8709f0f916b339f65e76bb56';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_riscv64_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='591ccf4d27016315700cc9cc979f7cf343900b6bee1b0b45c93f2c5f946e5aac';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3223b7cfaccdcdb72e1c082d52f6c0b253f980d3f3ab5ff51040ba6ece80737`  
		Last Modified: Fri, 31 Jan 2025 01:31:29 GMT  
		Size: 21.3 MB (21318051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402d821993cf0004785a8c958030a47c72f46c610eddfe97e69bb9a9f50a5a3a`  
		Last Modified: Fri, 31 Jan 2025 01:31:33 GMT  
		Size: 165.3 MB (165317803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1b05cc1428174c85976faa7b269d4951e294e1a760fa55dfe044b5c39fe2ec`  
		Last Modified: Fri, 31 Jan 2025 01:31:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jdk` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f3caefbe7f8323081972aedab2e45ea51b5c67564fb7f0e87cef9f15d368dc00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3317429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf035f58e76965fe8c66393f91b4b640ac5690468216db0ae023f1fe7b93e401`

```dockerfile
```

-	Layers:
	-	`sha256:2f79dc2d6f3957982c2612ce4eb7295f1bb6af61f2bd0af54bd7dca9535dfcca`  
		Last Modified: Fri, 31 Jan 2025 01:31:29 GMT  
		Size: 3.3 MB (3292818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e1b1c37876a7a083b0c400705f3ebd8d3021808b16bb11d56dc4e67328198d6`  
		Last Modified: Fri, 31 Jan 2025 01:31:28 GMT  
		Size: 24.6 KB (24611 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jdk` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:6b4ce026ddf1019076ee2a39f16fee26ae8c22f7deec543c1f7565510f770a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 MB (214744194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05e254c4da16bcbb3af6ffa30ba093149bc9c2ec6b1936ed4dbd892506ebc06`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='870ac8c05c6fe563e7a3878a47d0234b83c050e83651d2c47e8b822ec74512dd';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        arm64)          ESUM='fb43ae1202402842559cb6223886ec1663b90ffbec48479abbcb92c92c9012eb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64el)          ESUM='548fd82af4eb0802fe20b0b61a4664a69c7f03cd963540908f30dbf73636dafe';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        riscv64)          ESUM='1e102e1e6653f8810ef6c275b0d38ea7036abd4a8709f0f916b339f65e76bb56';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_riscv64_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='591ccf4d27016315700cc9cc979f7cf343900b6bee1b0b45c93f2c5f946e5aac';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a72f0d30453352f5b6347bc552f2cea40279f6d56d642896aecbfa222d9d23`  
		Last Modified: Wed, 22 Jan 2025 23:35:55 GMT  
		Size: 22.5 MB (22503039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cd5cfc79c3d2566c774440570ef6a378041903fc50d3ced422bdd278e18090`  
		Last Modified: Fri, 31 Jan 2025 01:51:55 GMT  
		Size: 163.3 MB (163346169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48ea1c3e6dcdbd7a31ca55b1306dfdf8c63bee32f771ff0469d5386a2f0cd93`  
		Last Modified: Fri, 31 Jan 2025 01:51:51 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jdk` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4aae80e2efee8ec4df7d52cde64ec4478172a4df82b0b22ae655611fe866ccfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3449105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774c51218ca6e14452fff45013101407fb32a5f098a4e9d1c1aa6078e19ad30f`

```dockerfile
```

-	Layers:
	-	`sha256:f60c024bddb2266ae4e0ccc051da02064674d51132ad77c15748ff5d381f363e`  
		Last Modified: Fri, 31 Jan 2025 01:51:51 GMT  
		Size: 3.4 MB (3424335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2693980bb5e3edaa7892f2c7b2aed88e1cf8432ce9b071c4d24a05717515ae`  
		Last Modified: Fri, 31 Jan 2025 01:51:51 GMT  
		Size: 24.8 KB (24770 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jdk` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:f061d96fef23f37af25887e8119a0a16455f9f84d7dce491a381f20e22789c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221661054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb864556005c78d154d31c0743ce193880ceaa311d55a28197944855d4493707`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Jan 2025 01:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 01:19:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2400267e4e9c0f6ae880a4d763af6caf18c673714bdee5debf8388b0b5d52886';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        arm64)          ESUM='808e3843293e50515bf02ad2f956e543da65e32dac82ae7a266a147b3485c61a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64el)          ESUM='1885ab141fe7b8ed6beb77b814b1c1c99fd54713399bf917edb6a4020545adde';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        riscv64)          ESUM='80d7bab9f9614bdf934c6bc441031bd1fead3aea85f16770123bd8a6bcdc52b6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_riscv64_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='39419d72082faea6d2501223f1cbf6a9128bc23000adfb7b7ee7acfce422509c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Jan 2025 01:19:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Jan 2025 01:19:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c83b801599783718711affc6464e5a69d718269b9c699909ec883790471b46`  
		Last Modified: Wed, 22 Jan 2025 18:58:26 GMT  
		Size: 22.1 MB (22081533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dfb3514162f60e109afcb558319b12c898e40ca1fb37c265c22b559640ae84`  
		Last Modified: Wed, 22 Jan 2025 18:58:31 GMT  
		Size: 165.2 MB (165188387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7d12edd98b7a200fefeced16d72a4f2237adbea0a2071eec67043895099ab`  
		Last Modified: Wed, 22 Jan 2025 18:58:25 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jdk` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:91c15d87a4e19476fe6223da2160519a1e51ff5f8a67a3fef80b7e4e21e73316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3365487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379f53f071c6afff8ec2af79f722cf6311fd62f010e187cc9225f80e681254c0`

```dockerfile
```

-	Layers:
	-	`sha256:1a5bac5d08740f2cb3ee285caeb6905b741e48a03dee7997d4c630772a448cb9`  
		Last Modified: Wed, 22 Jan 2025 18:58:26 GMT  
		Size: 3.3 MB (3340783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3727cb0c58b05023b5caecfef0aff68328e3604bdc14726731ec8d77ff85baf1`  
		Last Modified: Wed, 22 Jan 2025 18:58:25 GMT  
		Size: 24.7 KB (24704 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jdk` - linux; riscv64

```console
$ docker pull eclipse-temurin@sha256:2b6c7848397c50c0706e7828a587ed2321993c89e4fc5e50b05edd43fd984e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210367665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b628ff9705c6b5a30bd122b91b72742a378338bfb0ba3d888529a8bfe5078fb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:33:48 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:33:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:33:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:33:49 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:34:25 GMT
ADD file:23c2e341d6cf3572f2762ef1304c406cf6d4f5ee8ee8719ef289a3b75a8323aa in / 
# Tue, 19 Nov 2024 16:34:27 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='870ac8c05c6fe563e7a3878a47d0234b83c050e83651d2c47e8b822ec74512dd';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        arm64)          ESUM='fb43ae1202402842559cb6223886ec1663b90ffbec48479abbcb92c92c9012eb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64el)          ESUM='548fd82af4eb0802fe20b0b61a4664a69c7f03cd963540908f30dbf73636dafe';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        riscv64)          ESUM='1e102e1e6653f8810ef6c275b0d38ea7036abd4a8709f0f916b339f65e76bb56';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_riscv64_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='591ccf4d27016315700cc9cc979f7cf343900b6bee1b0b45c93f2c5f946e5aac';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:0dcc8c973ba119a0fb5275114fd0456179bba1132bdc69f2afa4e1c4a235c540`  
		Last Modified: Tue, 19 Nov 2024 17:38:52 GMT  
		Size: 31.0 MB (30980838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4461d53dc0eced0e40fa80251442976c0789866683647b09c3844dffb1587c9e`  
		Last Modified: Tue, 03 Dec 2024 07:17:15 GMT  
		Size: 18.4 MB (18380501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f74d16e4960f507a928a868e4b004e975163f10a7c6b2a97402aabf70c1313`  
		Last Modified: Fri, 31 Jan 2025 02:14:33 GMT  
		Size: 161.0 MB (161004011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1b92e5c9ed8cd444fd398ac4ba5f4e1047ee8520d0d315f3f5a054c84d4504`  
		Last Modified: Fri, 31 Jan 2025 02:14:09 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jdk` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:dddaa80330b71afd66d37d8723707b48789a2cca31188be17d7959e6048eea2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3425247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663abbb3ff5c849b519859252bda7c6e3c89597c7ae113963bd1be5a66c5fc5b`

```dockerfile
```

-	Layers:
	-	`sha256:e42032d5844d04fccffc6e4d24e5a455bde94656ac34a2bba0d269a7078cc6a5`  
		Last Modified: Fri, 31 Jan 2025 02:14:09 GMT  
		Size: 3.4 MB (3400576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3379169dd2a0bc4fe1a973c6f40cb227606102ba3d73e634141acf9b325ec4a`  
		Last Modified: Fri, 31 Jan 2025 02:14:08 GMT  
		Size: 24.7 KB (24671 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jdk` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:d714cea4e33a6206e7331c8bd220891abad28f145433117720159a1797439544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204906282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb184e7e703480897b3ae01021f5c661b8a121a4f4b8478442a31af3c880c78`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:14 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:14 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:16 GMT
ADD file:1c391e128b3c5e552a1401f9520290446bf94ba089c2d74a5d661001d3d8b60c in / 
# Tue, 19 Nov 2024 16:18:16 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='870ac8c05c6fe563e7a3878a47d0234b83c050e83651d2c47e8b822ec74512dd';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        arm64)          ESUM='fb43ae1202402842559cb6223886ec1663b90ffbec48479abbcb92c92c9012eb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64el)          ESUM='548fd82af4eb0802fe20b0b61a4664a69c7f03cd963540908f30dbf73636dafe';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        riscv64)          ESUM='1e102e1e6653f8810ef6c275b0d38ea7036abd4a8709f0f916b339f65e76bb56';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_riscv64_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='591ccf4d27016315700cc9cc979f7cf343900b6bee1b0b45c93f2c5f946e5aac';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:755503a8fb36d6a0d08275c3792ab81b69fdff95054dff0aa932d6dc30107609`  
		Last Modified: Tue, 19 Nov 2024 17:38:58 GMT  
		Size: 30.0 MB (30020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c54e188845646d46573f94780d9adce04a792e00faae8cf2b4791e5f157e1e8`  
		Last Modified: Wed, 22 Jan 2025 22:11:28 GMT  
		Size: 20.4 MB (20443159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdd4602e5b3d1a1fb4e8915505ccd0b462781a5d868c95d3a5a1bc82116eb95`  
		Last Modified: Fri, 31 Jan 2025 01:52:46 GMT  
		Size: 154.4 MB (154439983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9b0085f5aaae27d7562d9e212abe20e831b35a56fdf19192aa79ce5cd9b3a2`  
		Last Modified: Fri, 31 Jan 2025 01:52:44 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jdk` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1cbe85360bd31da9484f3c4f44b795305e68ee261621d2498b41be6b328e15f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31f7fa34ba8ae6788411a17746ac4ba4ec0d9e4e2095df77362ce2e2ebaed4f`

```dockerfile
```

-	Layers:
	-	`sha256:3ea7b51d9080e3854a5bd8c6948bc6f12b6d6dfaa3244cb7ba9dc4e06a5bb41b`  
		Last Modified: Fri, 31 Jan 2025 01:52:44 GMT  
		Size: 3.2 MB (3239042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b4cddc089d3a567aa4da2d47b85b1814e1fc81db883e446f6a4df44e9cca49e`  
		Last Modified: Fri, 31 Jan 2025 01:52:43 GMT  
		Size: 24.6 KB (24612 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jdk` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:b1e5888845c567c79c11c6675cb2a595c28734a7e0261192bdea667b3ea3f153
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2897548995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830a7575f07fb15f5007aea5b805a3add448f01fb6d2f5e56f0a651994445621`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Fri, 31 Jan 2025 01:35:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:35:25 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 01:35:51 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:36:00 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 31 Jan 2025 01:36:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904315b835de2fef53078d13a5e428ef8d0e64c60f898cad5809720320d83460`  
		Last Modified: Fri, 31 Jan 2025 01:36:04 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525e636202b5f5dc61c0277f5ca2a58f9e233c3607f138a2750953e5db5188b8`  
		Last Modified: Fri, 31 Jan 2025 01:36:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b757498d0d3c5f45cc87d9ed4ffff9d1cddf7a339b8ca14360979251d634ad08`  
		Last Modified: Fri, 31 Jan 2025 01:36:27 GMT  
		Size: 396.9 MB (396873598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4f56b7d0f503b6c1aefa3a6d7462c8ef52293107dcbfbddf2e5607a39de68f`  
		Last Modified: Fri, 31 Jan 2025 01:36:04 GMT  
		Size: 393.8 KB (393837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6594bc5fdc4b5e6f778ea923758cf0becd5e5a8df40a74ebfc1ff36dfa5e5eeb`  
		Last Modified: Fri, 31 Jan 2025 01:36:04 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jdk` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:90f642c409323221e27c26dbb16095a5d4aac41445f07c20bef63140d909861a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2659546478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744bee0bce3076b2018c347b8d2b32c116ee0b067542416946bd76d611ab3e70`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 31 Jan 2025 01:30:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:30:41 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 01:32:02 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:32:09 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 31 Jan 2025 01:32:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ba044f8e1d2e73b7ddeb6cc219df761f829fe28a7259cba1b24705c1b5584a`  
		Last Modified: Fri, 31 Jan 2025 01:32:13 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e326bf19a52a12609fe39b0b50156b386b5da5980e8ed6e368692f6da964ad5d`  
		Last Modified: Fri, 31 Jan 2025 01:32:13 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eea627498f4165359553c4150ab92b87514975eeddad9fa4217dba09cb1f7d0`  
		Last Modified: Fri, 31 Jan 2025 01:32:28 GMT  
		Size: 396.8 MB (396830506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5432de68e55d4d574316bf07ce0914426edca56fdcd71a191251dc3afa67f8`  
		Last Modified: Fri, 31 Jan 2025 01:32:14 GMT  
		Size: 326.8 KB (326838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641a711ce284af47ac320c31e6bf7457574970aafcdb59773821c672b01b1d7b`  
		Last Modified: Fri, 31 Jan 2025 01:32:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-jdk` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:95d9f550c35c9e36b9590d322d563736b56360d989d30d8791e4fdc58a3d0f66
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2523395974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32ac21995f8ea2dded83d19d30dbe037f5fcb7c1e120aa4914b0aefc1650d25`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 31 Jan 2025 01:30:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:30:40 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 01:32:49 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_windows_hotspot_23.0.2_7.msi ;     Write-Host ('Verifying sha256 (e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'e4ef33439c2dc725387fce4d57ed63794785c0d3ab55726bdc9861c0387dc3a0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:33:00 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 31 Jan 2025 01:33:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1a883cb00c69d0bdb519d430ade95100a427618db0faba1aa3f4f3db345fff`  
		Last Modified: Fri, 31 Jan 2025 01:33:03 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195248e9049375b50543b3e7aab0eab614002615ae8dcaf2a2f550a91e680b6b`  
		Last Modified: Fri, 31 Jan 2025 01:33:03 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6da4a065c4484ac514c389dc25b97cfc8d4935d97349030ed7d5fc2e9df79c`  
		Last Modified: Fri, 31 Jan 2025 01:33:20 GMT  
		Size: 396.9 MB (396850270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce263a9a4faf3e0a138a0b2f42290f6fd488a5f51c3d99e433908652e0dcffef`  
		Last Modified: Fri, 31 Jan 2025 01:33:04 GMT  
		Size: 4.3 MB (4329578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81bb601002c74f8a1064097ac53c0bd778b8fb45643fb74b11c8514ea1e2d942`  
		Last Modified: Fri, 31 Jan 2025 01:33:03 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
