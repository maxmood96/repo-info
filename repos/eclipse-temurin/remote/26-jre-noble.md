## `eclipse-temurin:26-jre-noble`

```console
$ docker pull eclipse-temurin@sha256:4dacce711fe478944dca9e943916b3e04c22a1e6f70d4f0e5ad3da4001fe9f3d
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

### `eclipse-temurin:26-jre-noble` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:28256ae9ee6c1609e084b6ff25a4348e4a647596e55a940a18edf0086f91d67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105769455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca567d9d32e073ef46391f6e5930aa7e515f813a1e5497f611d6be68e8450de3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:15:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:15:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:15:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:15:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:15:15 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Tue, 02 Jun 2026 08:15:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2e90cf68d31b28553fb2c8202d5a4c3a5e99a60285e125dc28c94ba5fb2ac1ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        arm64)          ESUM='bf5f733066599065de5e720edda550b39d85876f5bf23a94fee2cb6a8379cb36';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='d8f66903603c3661c0d8c03de41b76459260ed2e295ba874bb7b3f37a012c026';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        riscv64)          ESUM='277d00ea87cf0ec0ede6736007b2fb44432fac754613df4649e61f385beb55f0';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_riscv64_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='3c68d7df7d64a7738a6bd97b12fb2167774666d87bf9a309094bb2180073eb38';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:15:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd804d85875ce9c6c5b1f8d8f5d2f149f888776a8dee8faff99e8fa911e3634`  
		Last Modified: Tue, 02 Jun 2026 08:15:43 GMT  
		Size: 11.5 MB (11481117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b584248e1add90c9e94dbe142698191306ae261b83c307599d06fb0fd4fd0257`  
		Last Modified: Tue, 02 Jun 2026 08:15:45 GMT  
		Size: 64.6 MB (64553038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0678488eac7fa3b57691da468b1fa40da5e62a4b8888e27e697f48b5a0e749`  
		Last Modified: Tue, 02 Jun 2026 08:15:42 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ddff79ce7347a28dfed349292698b899e38e110cead255c83d1b82f5ea3ea1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3087026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99e92c1285daf2aa10ec22cf1e5a377bfa977bb6be00caacebba34a06a15982`

```dockerfile
```

-	Layers:
	-	`sha256:6e29f27a3695642132cb93f61007bacdbbbfff3624c0d0d07df3c1ebad94f080`  
		Last Modified: Tue, 02 Jun 2026 08:15:43 GMT  
		Size: 3.1 MB (3063991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:718649655d1e04aebaa231ccd312d8a68c18762a157bdcfe36a10e9195e537b4`  
		Last Modified: Tue, 02 Jun 2026 08:15:42 GMT  
		Size: 23.0 KB (23035 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26-jre-noble` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:8a0ed083ed6d3f84037e2ee7bd4d9763b48638a19295437453fa50e3764ecde1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103826014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c36a8b53c53a191a090e2fbba7ebac8f51b0c4b9fe01373a42d82bcba2ba57f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:16:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:16:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:16:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:16:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:16:28 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Tue, 02 Jun 2026 08:16:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2e90cf68d31b28553fb2c8202d5a4c3a5e99a60285e125dc28c94ba5fb2ac1ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        arm64)          ESUM='bf5f733066599065de5e720edda550b39d85876f5bf23a94fee2cb6a8379cb36';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='d8f66903603c3661c0d8c03de41b76459260ed2e295ba874bb7b3f37a012c026';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        riscv64)          ESUM='277d00ea87cf0ec0ede6736007b2fb44432fac754613df4649e61f385beb55f0';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_riscv64_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='3c68d7df7d64a7738a6bd97b12fb2167774666d87bf9a309094bb2180073eb38';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:16:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:16:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:16:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27125ce8edc76f8dd3695edd9a68ff30e6e4e147bcaedef4cb39cd89eeabf83e`  
		Last Modified: Tue, 02 Jun 2026 08:17:00 GMT  
		Size: 11.5 MB (11476684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9632ce95e05b029d51557701e87649b6984220d877277732649361ed4171c682`  
		Last Modified: Tue, 02 Jun 2026 08:17:02 GMT  
		Size: 63.5 MB (63470430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312ae223642b95394030e6ecf97d5519ce42c2ac5d630ef675be22a7e2ceb29f`  
		Last Modified: Tue, 02 Jun 2026 08:16:59 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6a8ff97febd5d7e98c077d3850de25361c64b11ef89a789b9e8e09765de07b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3087560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d5d02085ab0cf111bf22414803fb381bb17ea81a9692dec46bdf09bcae2bb6`

```dockerfile
```

-	Layers:
	-	`sha256:961a261655d02f89de8871cc1bdeeeb30bde8a40deb9dd0f352291271fd59ced`  
		Last Modified: Tue, 02 Jun 2026 08:16:59 GMT  
		Size: 3.1 MB (3064416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:010998ab17e60a5033e3f115ea3463c1ecbc1a55b0af2fe7a0015646f3c80893`  
		Last Modified: Tue, 02 Jun 2026 08:16:59 GMT  
		Size: 23.1 KB (23144 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26-jre-noble` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:e2a86072ea69efe6a884fb1ca75218222ce1cb8623a026eaa5d7ccbcbdea5ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110338959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0695ea0152730ed7c6306887da68d5f95b144930f516f32159a3daae261f0b0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:33 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Tue, 02 Jun 2026 08:16:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2e90cf68d31b28553fb2c8202d5a4c3a5e99a60285e125dc28c94ba5fb2ac1ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        arm64)          ESUM='bf5f733066599065de5e720edda550b39d85876f5bf23a94fee2cb6a8379cb36';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='d8f66903603c3661c0d8c03de41b76459260ed2e295ba874bb7b3f37a012c026';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        riscv64)          ESUM='277d00ea87cf0ec0ede6736007b2fb44432fac754613df4649e61f385beb55f0';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_riscv64_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='3c68d7df7d64a7738a6bd97b12fb2167774666d87bf9a309094bb2180073eb38';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:16:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:16:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:16:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14555f1475b5161df9db41ed4a7e500e82373184731715cb4aa463c046a5eb8d`  
		Last Modified: Tue, 02 Jun 2026 08:15:28 GMT  
		Size: 12.0 MB (12047670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016999c73bab7f30df6f7b7431faba7e78ab1aa1b9b6c650fefbd7f583c48a1f`  
		Last Modified: Tue, 02 Jun 2026 08:16:42 GMT  
		Size: 64.0 MB (63974697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f2b795ff2e89feaad38da960b253b6903cb867438ca5a2101f40adb7bbf89a`  
		Last Modified: Tue, 02 Jun 2026 08:16:40 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:55ee66d6fb1a4cd9ba2eff61b2d0001447a346dd8e30e345c3e422c70a7ea7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3090336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c40ec715b5f6b37c1558e6ab87797b01deda3964698a63108cc9ba6d4e93369`

```dockerfile
```

-	Layers:
	-	`sha256:d1fc69ff757edb867079e1e19a841fbf7825af9b504d6895623905defc011a84`  
		Last Modified: Tue, 02 Jun 2026 08:16:40 GMT  
		Size: 3.1 MB (3067267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d69a28376d10838765d30194116cc10e57bb8ce8714ae3929e31d1228ebe7519`  
		Last Modified: Tue, 02 Jun 2026 08:16:40 GMT  
		Size: 23.1 KB (23069 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26-jre-noble` - linux; riscv64

```console
$ docker pull eclipse-temurin@sha256:5272d840806937b129b9fc50a5354609aa9205c15f234a5ac61a424b2ddd7964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105848289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17c17f400b336dafaf875c5c04be5f5272b93756913aec80ba2541398bcc01f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:24:05 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:24:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:24:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 09:24:43 GMT
ADD file:a9a4679e3df2846468311b83a8f6ab86f5a205bab966d3f236c9f30151010c5b in / 
# Fri, 10 Apr 2026 09:24:47 GMT
CMD ["/bin/bash"]
# Thu, 16 Apr 2026 17:16:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 17:16:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 17:16:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Apr 2026 17:16:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 17:16:29 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Sat, 16 May 2026 19:26:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2e90cf68d31b28553fb2c8202d5a4c3a5e99a60285e125dc28c94ba5fb2ac1ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        arm64)          ESUM='bf5f733066599065de5e720edda550b39d85876f5bf23a94fee2cb6a8379cb36';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='d8f66903603c3661c0d8c03de41b76459260ed2e295ba874bb7b3f37a012c026';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        riscv64)          ESUM='277d00ea87cf0ec0ede6736007b2fb44432fac754613df4649e61f385beb55f0';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_riscv64_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='3c68d7df7d64a7738a6bd97b12fb2167774666d87bf9a309094bb2180073eb38';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 16 May 2026 19:26:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 16 May 2026 19:26:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 16 May 2026 19:26:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:a7f0c74374451005259fe6b1b7ef3185055f2b6c419b5ba0ae8e4f55b1e1c31d`  
		Last Modified: Fri, 10 Apr 2026 09:34:45 GMT  
		Size: 31.0 MB (30965327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb1da3a1b0530db8bac4f80d6d7cf1cab174ba1fdb49b966e841ec211df17d0`  
		Last Modified: Thu, 16 Apr 2026 17:21:23 GMT  
		Size: 11.6 MB (11570962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60efb421c699c82f1573270b4e9bf0673eb548ac8b9dc0cdf4ed5b453d1d1c0`  
		Last Modified: Sat, 16 May 2026 19:29:32 GMT  
		Size: 63.3 MB (63309507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fbb96c0aea1724b125beb65236b27996e74c84476f268bedaebbc957617f44`  
		Last Modified: Sat, 16 May 2026 19:29:22 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:22e7b4de80954e676759b14911aa00f9ccd6469151908318dec64c1cffdeb902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3079020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf7528fb038a6c8a75e3653448864eae635a30de3360eee8b69ca81626aaf41`

```dockerfile
```

-	Layers:
	-	`sha256:f549bc1b9aefd4fec455e5cb350dd8dd261ef2809d0281088a05bdd41176f3ca`  
		Last Modified: Sat, 16 May 2026 19:29:22 GMT  
		Size: 3.1 MB (3055949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:664fe1f6d22bb6da136fed638ca0212fb79aaec5659af1140ec0a495a1f6a4f1`  
		Last Modified: Sat, 16 May 2026 19:29:22 GMT  
		Size: 23.1 KB (23071 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26-jre-noble` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:38677d6b1b76540c49b7c64221600c0ed655c9dcd755c26830633478273e3e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103855909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e9daa2adb9bc46e79d1d2b9e8cea4e5c8ed33b6819134becc2807aa785db6f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 20 May 2026 01:37:09 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:11 GMT
ADD file:b574b1e436c2db4e4d66f69c75e47a9aebf0da1ad375147eb2c0b7ff76c6ab7e in / 
# Wed, 20 May 2026 01:37:11 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:12:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:12:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:12:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:12:09 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:12:09 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Tue, 02 Jun 2026 08:12:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='2e90cf68d31b28553fb2c8202d5a4c3a5e99a60285e125dc28c94ba5fb2ac1ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        arm64)          ESUM='bf5f733066599065de5e720edda550b39d85876f5bf23a94fee2cb6a8379cb36';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64el)          ESUM='d8f66903603c3661c0d8c03de41b76459260ed2e295ba874bb7b3f37a012c026';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        riscv64)          ESUM='277d00ea87cf0ec0ede6736007b2fb44432fac754613df4649e61f385beb55f0';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_riscv64_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='3c68d7df7d64a7738a6bd97b12fb2167774666d87bf9a309094bb2180073eb38';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jre_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:12:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:12:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:12:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c8ebd0a624851e8502e41ee64db2b6a45537554969784d82ebbc91c905cbc2ef`  
		Last Modified: Wed, 20 May 2026 02:16:00 GMT  
		Size: 29.9 MB (29912835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad609903bf3ca8d96c3a230dffbf8f5070376b7d17334dc2a8b0b7bef1cb57e`  
		Last Modified: Tue, 02 Jun 2026 08:12:41 GMT  
		Size: 11.8 MB (11758226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d838f5b272494729234e788a3de8a4a2641c9981e4cad4fa81dd0e45728cb329`  
		Last Modified: Tue, 02 Jun 2026 08:12:42 GMT  
		Size: 62.2 MB (62182353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8965dd88d1062c50da42715c2d0a506b253de0be205fd87268b924e647215ce`  
		Last Modified: Tue, 02 Jun 2026 08:12:41 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1058576c05d33d7856bce36123e764dc4406e407aaa7a7c6128e6ffb9cdd4e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3088624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed4cece07907b85abfa30f8f5a1b8a63aaf4349f268d12f7cc5a505dcca57f1`

```dockerfile
```

-	Layers:
	-	`sha256:19f1ce65344b82407932a161c968f76ac5038b9eeb03e8ecc6ed2d5e65eae876`  
		Last Modified: Tue, 02 Jun 2026 08:12:41 GMT  
		Size: 3.1 MB (3065589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ad0954cb338d7e086bdb1e1fd33187244c3667c5b6ecb3bf4c3c8d542a03e2`  
		Last Modified: Tue, 02 Jun 2026 08:12:41 GMT  
		Size: 23.0 KB (23035 bytes)  
		MIME: application/vnd.in-toto+json
