## `eclipse-temurin:21-jdk-noble`

```console
$ docker pull eclipse-temurin@sha256:baecd2f19f72ae13dd8cc425372782cbc5f2a8f9efa3c5cc79e0024fd49b472f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `eclipse-temurin:21-jdk-noble` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:660583b2b7574445ca2c16ee42138900b90b63881333f6ee31cbf45aedb9ece0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210288345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11365818466b7119a1bfcd8a71edbd07ca3cdf752f88aa358f16223895d6e0ac`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='203796e4ba2689aa921b5e0cdc9e02984d88622f80fcb9acb05a118b05007be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:dde9ea9bd15bae201459397dbef16f5dee1c9859d6b87cc34f5fac132db0f261`  
		Last Modified: Fri, 31 Jan 2025 01:31:26 GMT  
		Size: 22.9 MB (22942545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e785af5c591ed1d7cc051903ef1156403dc3f974e799e6dde0f067a114ba921`  
		Last Modified: Fri, 31 Jan 2025 01:31:30 GMT  
		Size: 157.6 MB (157591392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a612cb0b0ff4994e480654c965a9ae3efa3ae7967db3c23f6e2febebdcc3e67e`  
		Last Modified: Fri, 31 Jan 2025 01:31:25 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1e83616f3eb5f368bf2fe7b93419bb89e8d302924d45234111be1ac90de074`  
		Last Modified: Fri, 31 Jan 2025 01:31:25 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e48bdfcc366d9c73928b1d88b0f5c65ff7d8d857fe45e7967cddcba67ae23e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3379284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d262ee8058d58aeb18e028e421b6bda687909932b5ce7fae320cb4949387741c`

```dockerfile
```

-	Layers:
	-	`sha256:6177dfdd0d06b536228e858e4e8616dd487b12aef0b6d46989bb4c7224ad001b`  
		Last Modified: Fri, 31 Jan 2025 01:31:26 GMT  
		Size: 3.4 MB (3354101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2527335b1729c474d930a2d7184c75cceba34b30cfaccd6ff66c84807c10efcb`  
		Last Modified: Fri, 31 Jan 2025 01:31:25 GMT  
		Size: 25.2 KB (25183 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-noble` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:53c80d877136443a0a488a8c20220d28b84ae922fa4201147ec0328c1dac77d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208923117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5537fc9b9053846d54061c72322d8daa24cbf3657ed3f65ceadf1fac850c9b8`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='203796e4ba2689aa921b5e0cdc9e02984d88622f80fcb9acb05a118b05007be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:8112b468d97fc1b8e58f23cc45c7b4449288dfc6348767e8522c42643be9f62f`  
		Last Modified: Wed, 22 Jan 2025 21:03:59 GMT  
		Size: 24.2 MB (24159896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4c340be4bc8c988e87db3430d1aac7cdb8d542b551f6c08a47c6f3a4657b3a`  
		Last Modified: Fri, 31 Jan 2025 01:46:33 GMT  
		Size: 155.9 MB (155868108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45163bf92b97e067f5621a74418afc1e99f2056a356fe6b9489a4e72d49ab7cf`  
		Last Modified: Fri, 31 Jan 2025 01:46:29 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cb46593f627267f8b734209a6f18b08573a6f4dbd89288b528091bd5d8bb36`  
		Last Modified: Fri, 31 Jan 2025 01:46:29 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9403b29096674866e7d0b4ef5c42cdda7697ea3d79644a60f829bed671ffa5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3511614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a1d219357d99c9b2d31b4946708c6f3be76888a07dfe1ac9b3b0e4e844c66f`

```dockerfile
```

-	Layers:
	-	`sha256:6911ead05fcdc3d7c8a0e515bf3ece26f17818c798308cd4adbaced14b2e2d09`  
		Last Modified: Fri, 31 Jan 2025 01:46:30 GMT  
		Size: 3.5 MB (3486261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:757950ace7755cd57cb21c759a4bfb89680d63272af5b5d6c2eaf6720a11e8a2`  
		Last Modified: Fri, 31 Jan 2025 01:46:29 GMT  
		Size: 25.4 KB (25353 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-noble` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:a66fb67912e69de6e951ce9144c0ddb8c3418c28c4b07076c9dcd93f14ce5650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216272290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff4f14f7fb4b87287794e47f6bc9ba0f8e6daf8cdd7e0672dc2dfd8d9bcbf5c`
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
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='203796e4ba2689aa921b5e0cdc9e02984d88622f80fcb9acb05a118b05007be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed2227906a2678e61430dc4db9096a1b9e484821f414e02fa2a74916d0b6940`  
		Last Modified: Tue, 03 Dec 2024 04:49:04 GMT  
		Size: 24.1 MB (24123967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0755f94a9c3936ee30b10a8c60df572a27586ced98c818d79fa1c76a2189f43f`  
		Last Modified: Fri, 31 Jan 2025 04:56:04 GMT  
		Size: 157.8 MB (157757060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc965e1bcb33aa607a16fec22c8ac1e6ad1efe44b68d958172eead7d7046cfd6`  
		Last Modified: Fri, 31 Jan 2025 04:56:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ea3e013e3c8830afd0e8be32632404a2a8d599b277a58a0495430c81ee25a4`  
		Last Modified: Fri, 31 Jan 2025 04:56:00 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9061f8ca8de032689abf0c7758a152b7fa433fd1cb282810d8d2a05d8328b2cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3427992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd49f0ed5809205c8a4fbc0caec634c9f0e97cb7745c0bbd9bb80219348ec231`

```dockerfile
```

-	Layers:
	-	`sha256:d6f954cd029840efb45e2719f9262cf3da32ec03ce66bf36ae57f0c6f1f0409f`  
		Last Modified: Fri, 31 Jan 2025 04:56:01 GMT  
		Size: 3.4 MB (3402743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:805162d643028f76d2b1ab477a01356a73b7104573328b79db68b497b1daa3dd`  
		Last Modified: Fri, 31 Jan 2025 04:56:00 GMT  
		Size: 25.2 KB (25249 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-noble` - linux; riscv64

```console
$ docker pull eclipse-temurin@sha256:d818a8f94e055bee462c57fde29ef146a44d53dd368c084fed036e90fe9eaf85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204511558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2aba652ef7908702ccc0e6152a74674928f80096351af37b88f2626bd930171`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='203796e4ba2689aa921b5e0cdc9e02984d88622f80fcb9acb05a118b05007be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:710f1e2747c592d43b9f75ecb2109573d56e6391ff9deb3c6d6f740458842b09`  
		Last Modified: Tue, 03 Dec 2024 06:55:01 GMT  
		Size: 20.1 MB (20137091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd773ba9601dc9076ba59b5c6905a497d2606f475ab26341bb681965b1c8a22`  
		Last Modified: Fri, 31 Jan 2025 02:03:49 GMT  
		Size: 153.4 MB (153391186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3d9d77f8e4b4a1c6b132053472508d2b338af895fccbf249550250bea12037`  
		Last Modified: Fri, 31 Jan 2025 02:03:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b062e56e1c1a9808446d5c98c2ffb9461897d585910c96467ba7755513efc883`  
		Last Modified: Fri, 31 Jan 2025 02:03:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a752467d96e6d3dee1876944d4a42a87be1d5ddc91ae649d2032cbfb1bd9092c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3487762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb9d18f879c3126c3d91370d3d72ee875b91e317e012d9e842e8a415815c38d`

```dockerfile
```

-	Layers:
	-	`sha256:4892d13a8e5ad74540e5bc6dfafcbafe1e3ce9756019367a1584e455ed5cee20`  
		Last Modified: Fri, 31 Jan 2025 02:03:28 GMT  
		Size: 3.5 MB (3462514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dabf408aa7892f15f2f2d34abaaba1b191ba22f8359f535682a6c44566321bdb`  
		Last Modified: Fri, 31 Jan 2025 02:03:28 GMT  
		Size: 25.2 KB (25248 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-noble` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:91f6c58458f764f4dcd06bd27731e388c7ddd75350b71be5ad4cd3402918d77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.0 MB (199046884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c841a4371cd9c0a8f4d6fac44e64e290b7a3afd754ca661ccd54dc7b725756bb`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='203796e4ba2689aa921b5e0cdc9e02984d88622f80fcb9acb05a118b05007be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:1715201283ca83d429bf0d3ba7a2ffbc88880932d15da4bf2c6a3b2e2e7f7f32`  
		Last Modified: Wed, 22 Jan 2025 21:55:45 GMT  
		Size: 22.2 MB (22151990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaea2ca495f362807fac06cd1226c505c7194612b53e3d5406aeb9b80ea3dd6`  
		Last Modified: Fri, 31 Jan 2025 01:47:54 GMT  
		Size: 146.9 MB (146871625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3d42ed62d97b00aea027d79fb7939d3fbe7419879d2cbf5da925894fa00e92`  
		Last Modified: Fri, 31 Jan 2025 01:47:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6186ae2adccbe2f0939f2d8f41b3cfc13264210e4f6d6f0962f40b0bb97a8afc`  
		Last Modified: Fri, 31 Jan 2025 01:47:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b5fe03cf18319d86da13432b00139995ff69eda896daf0bc620471a10f64962d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3326107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c578c144e4697da2415e57b273cd42315c9c9da03977a0071fda1d543bf04f5`

```dockerfile
```

-	Layers:
	-	`sha256:b4f517536b3b0c7f831c48f2e1d1b8dff31fb3bfb865aa02876230cd51c626ee`  
		Last Modified: Fri, 31 Jan 2025 01:47:52 GMT  
		Size: 3.3 MB (3300924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1130dfc9efbe5414beb215a4ea824e55f4566d25e94255c6a60240082ec1e2f1`  
		Last Modified: Fri, 31 Jan 2025 01:47:52 GMT  
		Size: 25.2 KB (25183 bytes)  
		MIME: application/vnd.in-toto+json
