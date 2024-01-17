## `eclipse-temurin:21-jre-jammy`

```console
$ docker pull eclipse-temurin@sha256:6b234f2165f7836771a0377ac62efa94da4c6234f9fbda1980ebb5a5b7191f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:21-jre-jammy` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:dfa181420478f22b709ef9ea6cdc6d94d874f652bc19f9209ffeeb4b3b498576
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101409341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0320994be5e54810f0cf7f1668f69762bcff62a345c2d9cebb27d25951006d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:16:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:17:17 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Wed, 17 Jan 2024 07:17:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4582c4cc0c6d498ba7a23fdb0a5179c9d9c0d7a26f2ee8610468d5c2954fcf2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='277f4084bee875f127a978253cfbaad09c08df597feaf5ccc82d2206962279a3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_x64_linux_hotspot_21.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='05cc9b7bfbe246c27d307783b3d5095797be747184b168018ae3f7cc55608db2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 17 Jan 2024 07:17:45 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 17 Jan 2024 07:17:45 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 17 Jan 2024 07:17:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c506251a0ae0b836353578bafa8d6aeb266158d3291ba4abbc2f5f8ccda6f742`  
		Last Modified: Wed, 17 Jan 2024 07:20:28 GMT  
		Size: 17.5 MB (17458145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2aa73936704069027c98952b72189230438b10236fe58fc0ef4704c74bbe63`  
		Last Modified: Wed, 17 Jan 2024 07:21:43 GMT  
		Size: 53.5 MB (53503189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf13e0261e7105c66a7172e19c539d226b2276cb2ce6be758854747439133690`  
		Last Modified: Wed, 17 Jan 2024 07:21:35 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4538b67df0c2d8b2278ee769ef138043b419881ba62cb4791ed1e1c2aaa70fd8`  
		Last Modified: Wed, 17 Jan 2024 07:21:35 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-jammy` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:f93612b9ec59019438317d22fe7f54f4731327124bb0d9fb8c78b9c182770254
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99933489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f18e8d91f1bf73a975869796fae2120c02a0c5fc599847de0782c75802eba9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 06:57:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 06:57:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 06:57:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 06:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 06:59:40 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Wed, 17 Jan 2024 07:00:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4582c4cc0c6d498ba7a23fdb0a5179c9d9c0d7a26f2ee8610468d5c2954fcf2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='277f4084bee875f127a978253cfbaad09c08df597feaf5ccc82d2206962279a3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_x64_linux_hotspot_21.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='05cc9b7bfbe246c27d307783b3d5095797be747184b168018ae3f7cc55608db2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 17 Jan 2024 07:00:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 17 Jan 2024 07:00:04 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 17 Jan 2024 07:00:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6a2be6e4013cffcaae1614f67dca08e0c8d56b9d2da9051ae71c48b43a409a`  
		Last Modified: Wed, 17 Jan 2024 07:02:15 GMT  
		Size: 18.9 MB (18860096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a85118e7535f824a0bd5cbb5bf852d0b54750a2c1ab0645a45cf1aad35576a`  
		Last Modified: Wed, 17 Jan 2024 07:03:19 GMT  
		Size: 52.7 MB (52672883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a58a31070695de9980d9e219c26741702502d1275d61c8607c99e4a3721b8f7`  
		Last Modified: Wed, 17 Jan 2024 07:03:13 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a5df737a37871544f45d6629503a303ab31419923f05a158f9a6e23184877f`  
		Last Modified: Wed, 17 Jan 2024 07:03:13 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-jammy` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:2fb87570f9b44e025886f68e7d52eec300caf148c7b8c7cb208d2e187ca238a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107648219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee932c89097be211ea8faeb13e02599dd924116f833c531bdd057fec76edacc3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 11 Jan 2024 17:10:02 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:10:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:10:06 GMT
ADD file:4da6fb9ba29da03fa46ed73abfae01fa7c87f2c26044ee297c88359085392aef in / 
# Thu, 11 Jan 2024 17:10:06 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:29:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:29:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:29:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:33:26 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:34:44 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Wed, 17 Jan 2024 07:35:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4582c4cc0c6d498ba7a23fdb0a5179c9d9c0d7a26f2ee8610468d5c2954fcf2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='277f4084bee875f127a978253cfbaad09c08df597feaf5ccc82d2206962279a3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_x64_linux_hotspot_21.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='05cc9b7bfbe246c27d307783b3d5095797be747184b168018ae3f7cc55608db2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 17 Jan 2024 07:35:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 17 Jan 2024 07:35:36 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 17 Jan 2024 07:35:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:898e4a5fe680690395e7fd9d920dfa248b7508ec0573741c491bf250179ddbda`  
		Last Modified: Wed, 17 Jan 2024 05:26:53 GMT  
		Size: 35.7 MB (35657152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f95565053a2c917aa3ba2deb3ea392ef7c78d2f7d32e87be656a8d2139ae1d2`  
		Last Modified: Wed, 17 Jan 2024 07:38:06 GMT  
		Size: 18.7 MB (18725652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ac527cd7001b6f5c70dd9741a520fab368bd8cd5c481f25f53f5578df6e332`  
		Last Modified: Wed, 17 Jan 2024 07:39:23 GMT  
		Size: 53.3 MB (53264523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960840a90991a71053a54a909bc0ff9bc04f5c275ba5c023a59339d8830114fd`  
		Last Modified: Wed, 17 Jan 2024 07:39:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3157aee2ab3dec3a7b88935aec30c05e3e6283d00a310ddcd8646fa0f07f4a`  
		Last Modified: Wed, 17 Jan 2024 07:39:15 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
