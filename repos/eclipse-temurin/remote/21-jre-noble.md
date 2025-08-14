## `eclipse-temurin:21-jre-noble`

```console
$ docker pull eclipse-temurin@sha256:b5ddc4afebe332e2214c39c216c80821ca90eb21692a3eb7f4e160019fc6dffc
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

### `eclipse-temurin:21-jre-noble` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9e91c02e5b2701efccb4b22bd5918b4cf1f01197848fd15e359ca74b1810db82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99666253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44121acc9d96841763cc90bb11e6fd71028d685633f60e783f817d29cc4cbe02`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1ceb63b80a861ae319235f3b1e3e392279a30c5cc9f0dec5c5582505b55f8`  
		Last Modified: Tue, 12 Aug 2025 17:24:47 GMT  
		Size: 17.0 MB (16971683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62b74addfec2b46a83d8e9d131c7c6563aa4399f142b91d977d506f6c137dcb`  
		Last Modified: Tue, 12 Aug 2025 17:25:01 GMT  
		Size: 53.0 MB (52968913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ac95b0cea99b9ed5ddc084d329fc5e139c2adde65e599e4f9803bd9aa474ef`  
		Last Modified: Tue, 12 Aug 2025 17:24:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cce32af8d45a5194c78928090c5748f048a001dcd13b737c7a2992892753871`  
		Last Modified: Tue, 12 Aug 2025 17:24:49 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:683844a5ce0dcefcaf20cc710075bfe503db35539c1a5990efc1c27e1712b068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3311001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b21f0452156adb5571b936d73a9131172d7af3642ea42a6a1b5a5a561e8b49d`

```dockerfile
```

-	Layers:
	-	`sha256:3df15f763bbd2868361a25fc79af9651c38723310851b820ed100e56b2c2be0a`  
		Last Modified: Tue, 12 Aug 2025 18:16:52 GMT  
		Size: 3.3 MB (3287833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a1cdd8291a39d60540c11833d66dc034555ad885e610b1bc4a7c5453f9a1735`  
		Last Modified: Tue, 12 Aug 2025 18:16:53 GMT  
		Size: 23.2 KB (23168 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-noble` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:43718d360ef2121737dd9bf23391b7cec9927f7bae4a667a496cf2b041a9bae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98000104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7476f48e07cfff121716eda18484c44a2faa97835dffa22b517a2329d2b6d3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3eefddfbcab06ca4f10ce56a232d4ec2d822b72ac91b8958abc9acd3c4223c`  
		Last Modified: Tue, 12 Aug 2025 18:31:54 GMT  
		Size: 17.0 MB (16988833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2683f57ecc3239b77668933adbcb066b796b3d8385694028dfa534473428efe9`  
		Last Modified: Tue, 12 Aug 2025 18:39:53 GMT  
		Size: 52.1 MB (52148453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1835951682aea5916d97b15850e70d45156732945ac0dbb2535d8c6306228f`  
		Last Modified: Tue, 12 Aug 2025 18:39:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766ee17d70f62cab7ff1f4f47b0567a37c24335c88c58b652cb5b22e4f7e92e0`  
		Last Modified: Tue, 12 Aug 2025 18:39:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:48fe9c12df1890d45051ad2f8b10192590077b19659ff38f08bbcf4d9c4a15c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3311606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db472a6c4de18d3453ded2afa2d177392296376520fc88d65d355a45b3f7367`

```dockerfile
```

-	Layers:
	-	`sha256:f85c8bc7e8472d80beb417122e0601b28c3f3add93ecd0391de3979f800f4f40`  
		Last Modified: Tue, 12 Aug 2025 21:16:35 GMT  
		Size: 3.3 MB (3288304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1edb256bdac5fb21dc29b5eb1388c01e50e73f63ea5af99f186dcadf5761bba8`  
		Last Modified: Tue, 12 Aug 2025 21:16:35 GMT  
		Size: 23.3 KB (23302 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-noble` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:540928a9878af4f857c97a05fd6937929dba23307c88db4ace764e3b17a733de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106141693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b938130fe7ff1cf4323b8394199543b55306d89dd20e5ce7cc8b912d376c8198`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 06:57:25 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:57:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:57:28 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Wed, 30 Jul 2025 06:57:29 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096eab1deeb8fde16ff57db7eaa184cd4e8ab0d206018acdb9ab5ac1843566c9`  
		Last Modified: Tue, 12 Aug 2025 17:31:12 GMT  
		Size: 18.8 MB (18814780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9fd634439ca1370072ba1a114ffac16012a693f82cdd9a285aa7d71bde5ba7`  
		Last Modified: Tue, 12 Aug 2025 17:46:17 GMT  
		Size: 53.0 MB (52994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0703252e00e50d5a6f62e33bc1a05da3c95b9db9f7e62dd25ba8a4cbec89693f`  
		Last Modified: Tue, 12 Aug 2025 17:46:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995d6fe317f031d8b5db1016d22ab1cfb66a718a5899cd588f150c37024450c6`  
		Last Modified: Tue, 12 Aug 2025 17:46:09 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b7c7b06845e6336f213a8c0ca3881729467ee1ce44b2b421d268ec8539d7ae58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3315117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5230905be3ee18b146e9b13cee567a53606ff37c68137fbd7ab5819d009086d0`

```dockerfile
```

-	Layers:
	-	`sha256:9e248bb79fec7ef576d6d3ad94db3610754ff6b7ae32e44a7763ef96f27751e5`  
		Last Modified: Tue, 12 Aug 2025 18:17:01 GMT  
		Size: 3.3 MB (3291901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b61567ba21483fdc592cc1a16d67265695ceb3e02302dfeb37ae4dfc068973f7`  
		Last Modified: Tue, 12 Aug 2025 18:17:02 GMT  
		Size: 23.2 KB (23216 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-noble` - linux; riscv64

```console
$ docker pull eclipse-temurin@sha256:e42ba6f9a314f8799f2178fac85002f2b5f57e4a83f629df6eee6a481cc12f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99538737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c958956f9634db473c7d22671c954c46ede932fa23aef7409c6b37e0ac5ec280`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 07:17:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:17:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:17:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:17:52 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:18:34 GMT
ADD file:07f3c32dd2b7f6af0f399701257442794654b72aa96759b98cb033a715461739 in / 
# Wed, 30 Jul 2025 07:18:38 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:b12e9b07091787c99b29dd2be63680c86c47e8be60a46566329007fb82cee41d`  
		Last Modified: Tue, 12 Aug 2025 17:05:53 GMT  
		Size: 31.0 MB (30951577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48af681b8ec6db282cced99124adaf7d258d933ef637b46da596f62b231927`  
		Last Modified: Tue, 12 Aug 2025 17:44:15 GMT  
		Size: 17.9 MB (17863907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dbfe3ed9efed71dae22a46950ae2fd53b19b93e95762cb725d312d5374e785`  
		Last Modified: Tue, 12 Aug 2025 18:53:08 GMT  
		Size: 50.7 MB (50720811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a050e62896ae3f6627690501b0c497dff6e81e84dfbbe6fdb2eafa0173eb496`  
		Last Modified: Tue, 12 Aug 2025 18:34:53 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb8360ba1c7447d291decf5adc5a48e97ae9b94614514edce23011d4f0df3c1`  
		Last Modified: Tue, 12 Aug 2025 18:35:03 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2d04378e325b38cd71a47de7c72850579117a52e9dd8a162d59385a2fd7823d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3303123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a49704061831d9ea90d7b9aac82c237c607102c27063cdabe262a0c1301574`

```dockerfile
```

-	Layers:
	-	`sha256:74ea918390193ed4a2623da6c4ab139089ee199918449d64b6acc72e8f3e0cf5`  
		Last Modified: Tue, 12 Aug 2025 18:17:08 GMT  
		Size: 3.3 MB (3279907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26ec92d800545b25ddd234bf0dbecf04929b3ee72572662b2104357891df9c0e`  
		Last Modified: Tue, 12 Aug 2025 18:17:08 GMT  
		Size: 23.2 KB (23216 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jre-noble` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:3eae38f5d7ae6d1fd66ff71e78fd1bdc311786976a9196a0e1ead669ea57e8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97022996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25cc07757ab3676d24eda5ceaa1d84ca0383c51add6f8bbfcd4221659d069a2e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 06:55:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:55:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:55:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:55:11 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:55:12 GMT
ADD file:f751959e6b8dae58a35017dc82c7271708f085c111710b59527373699b0784b5 in / 
# Wed, 30 Jul 2025 06:55:12 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1c5d0b18c745fadd2e177b54d4df793f25b01437577bc09c72ae52a0f3f9aeb3`  
		Last Modified: Wed, 30 Jul 2025 11:30:49 GMT  
		Size: 29.9 MB (29932680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be43c90819238ceb0f3b3a9810a063a7e4b16e3faac49694c12e7ffaf1bf1717`  
		Last Modified: Tue, 12 Aug 2025 18:15:47 GMT  
		Size: 17.6 MB (17580544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130a9dfd0e826b6595b61b81803dedef02201928ae3af96590de9ca8e173aa3c`  
		Last Modified: Tue, 12 Aug 2025 17:35:48 GMT  
		Size: 49.5 MB (49507332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96f1b238d749e60583c74dcc45e5bd15601ef144200f7b59d365c85ca19eb0e`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74843a49fad97c2fbf396399b995216f6f2c0989c10985e8f7b9d7d908a8a4f`  
		Last Modified: Tue, 12 Aug 2025 17:35:43 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jre-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:60e76da504bc20fd3db0cf5a03ff95e63de25bfd75288060c37d6a7a3cd389ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3313201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b5d5770cba88c9fdc5d37dd1da8ae96f7f99de806c13a6451d8d78090b1d20`

```dockerfile
```

-	Layers:
	-	`sha256:20567b957bae49752e345990ad28eecd4c8f7baf4f6c09fb1370d75e18169b8c`  
		Last Modified: Tue, 12 Aug 2025 18:17:13 GMT  
		Size: 3.3 MB (3290033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:435cc49a0369c8d13206ae8f1a99add75bfd2cbb2acc9203e5bf41fc67b740b6`  
		Last Modified: Tue, 12 Aug 2025 18:17:14 GMT  
		Size: 23.2 KB (23168 bytes)  
		MIME: application/vnd.in-toto+json
