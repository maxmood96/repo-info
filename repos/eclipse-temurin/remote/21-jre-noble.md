## `eclipse-temurin:21-jre-noble`

```console
$ docker pull eclipse-temurin@sha256:77f4fd3f4fa16a9d2ee3f8bf3dbb377bd0d8da0436779ee2aab6144031fba3d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:21-jre-noble` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:92ba088c3641ebdab9e6c4f412629f53169b2bdbb9b36946b919a986762b46e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97900601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4e732abb81bdd83d0d72200c09e83f8f046c811c2698e457c3233bdb218a63`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 10 Oct 2024 07:41:37 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:41:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:41:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:41:37 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:41:40 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 10 Oct 2024 07:41:40 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        riscv64)          ESUM='bf814344429f53d11f8aace14d326e2580ea6e66dd81b109c79160bd41735237';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:aed300f9456f1ba3649e409619ab8495b52eea254997f9293d3fa2f1a213be79`  
		Last Modified: Thu, 10 Oct 2024 03:03:25 GMT  
		Size: 30.6 MB (30613278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1beb5331d363596b1827b1acf45f54c2c7746f8406636b8d72b09022b11fb7b3`  
		Last Modified: Fri, 11 Oct 2024 23:56:25 GMT  
		Size: 13.8 MB (13771214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b3180beb254d32bf230df5e23ac5ae54a526f8bebf3644eb7cbd60e3263792`  
		Last Modified: Fri, 11 Oct 2024 23:58:37 GMT  
		Size: 53.5 MB (53513842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4520b2b9ca82298855650dee01ae2c6dadf0af8e52b51e128b86333d750fcc0`  
		Last Modified: Fri, 11 Oct 2024 23:58:30 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d539a57ab5554882525d5eb9464a8035d5e65879520b197fec9093d7a4dd29d4`  
		Last Modified: Fri, 11 Oct 2024 23:58:30 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-noble` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:793bcd4080ceb307d1d6edb3736ce742229a5d7803bfb97f6db2c649e6a2803b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96395946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b70ce42e10c0b2a7b2d67faa87001c269cea4d3ec290ee8cc8f94b4b9e29429`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 10 Oct 2024 07:44:36 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:44:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:44:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:44:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:44:39 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Thu, 10 Oct 2024 07:44:40 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        riscv64)          ESUM='bf814344429f53d11f8aace14d326e2580ea6e66dd81b109c79160bd41735237';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:bbc050e99a562418305b0d9003042b38fc24f8c8c94687cf4c69ed6cd001161e`  
		Last Modified: Sat, 12 Oct 2024 00:07:49 GMT  
		Size: 30.0 MB (29953586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056e93bad04245da5d01c9d3de3081a8ad7d5bcd80abdd0ada262fae4f313b5c`  
		Last Modified: Sat, 12 Oct 2024 00:13:29 GMT  
		Size: 13.8 MB (13798544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a208f268d8f65cc6f03a2546a1ae6aa4a8a3657338d2b415e75a106d01dfc34`  
		Last Modified: Sat, 12 Oct 2024 00:15:30 GMT  
		Size: 52.6 MB (52641548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95a70a60d00f5231a8fee49e7ac2ce35e774b4b4dbce9eb4dedbf33c669da83`  
		Last Modified: Sat, 12 Oct 2024 00:15:24 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9552fe33b94eaf328ff01464256cff97bec7a19cfce835428923d48e28b75a3`  
		Last Modified: Sat, 12 Oct 2024 00:15:24 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-noble` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:09148d3d5fdc8ea662c7bbe726fe4e433cd7051c44408fd070c12bcca765bc6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104003630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1368100267bee6fff2bc390b7d070936ab9984b79071b4a5853251ccd4a2261d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 10 Oct 2024 07:43:56 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:43:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:43:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:43:56 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:44:00 GMT
ADD file:6ec0ebf9a019b7c00b0121b97e89fcad881460415f8dcb9bb94b1cc7f5d0a5bc in / 
# Thu, 10 Oct 2024 07:44:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        riscv64)          ESUM='bf814344429f53d11f8aace14d326e2580ea6e66dd81b109c79160bd41735237';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:870d99e54f9cdff4b5ba4448d967491786519e8cbf54f10bd271e5dd32285ceb`  
		Last Modified: Fri, 11 Oct 2024 23:47:07 GMT  
		Size: 35.5 MB (35513269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15086c23dcc309fa9386aa3f0907d6689b8bc489e8f1311ca8248bffcaf162db`  
		Last Modified: Fri, 11 Oct 2024 23:55:29 GMT  
		Size: 14.9 MB (14914320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6358763e71183673fa37ebd8c4d1189cf8ae4eb217432a0b7093143f489afd46`  
		Last Modified: Fri, 11 Oct 2024 23:57:52 GMT  
		Size: 53.6 MB (53573773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10224c3e3ba8cab403550ec92702d0c85abf1cb795967e50a82eb4b6f1c4c818`  
		Last Modified: Fri, 11 Oct 2024 23:57:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abd521aba0dbc367da3ba9fa016c19c7eb20ffb01f4a921b9534a939fe5a60f`  
		Last Modified: Fri, 11 Oct 2024 23:57:43 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-noble` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:f0d42272d0417bf9e529c12b24d87e728c7cef62b80f4aea35e55776a0f52f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94530275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d90f6fa666055d6d443419a35d2a45d1f57d8e588ab7b8c9c89fce27b8e20d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 10 Oct 2024 07:43:54 GMT
ARG RELEASE
# Thu, 10 Oct 2024 07:43:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 10 Oct 2024 07:43:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 10 Oct 2024 07:43:54 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 10 Oct 2024 07:43:56 GMT
ADD file:ed84c120e781b2f48856752e1e38d21db0bed5e09a2a64f961f004a4906abcb6 in / 
# Thu, 10 Oct 2024 07:43:56 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='d3affbb011ca6c722948f6345d15eba09bded33f9947d4d67e09723e2518c12a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='58845ce4275f3ec74fba075597c8216bb201773da036c4703be8b7b7b457355d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='46cf93653e2b553fb1c91760cfe2ff20999ba358d648d2df69e5948784768440';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        riscv64)          ESUM='bf814344429f53d11f8aace14d326e2580ea6e66dd81b109c79160bd41735237';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='7fb5b09987cb41de5118fecb5a81771b3a38a245cff411b39af33dbfbca3e760';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:220da50193dc0598aa4f0418f3c1f89ed396983e85b2032ceeac1e4e044e443a`  
		Last Modified: Sat, 12 Oct 2024 00:18:34 GMT  
		Size: 30.7 MB (30663130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f4b3060da0149631cc385d58c57350144169b82f0600be0bfca3031687fa1`  
		Last Modified: Sat, 12 Oct 2024 00:25:46 GMT  
		Size: 14.2 MB (14195098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36aeab76b9ff698f3997fb05fc8f31379589aa340479d762207002e07d0ff79`  
		Last Modified: Sat, 12 Oct 2024 00:27:10 GMT  
		Size: 49.7 MB (49669779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbeb70e4bfe5a208366a7c24148e8c3f6cac41bcc44b2a2fcaa4bde7869e7cd`  
		Last Modified: Sat, 12 Oct 2024 00:27:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545b2cb39216b8b6497a9c7627b36c32c1f4fe6545052706b340b69a5bea2485`  
		Last Modified: Sat, 12 Oct 2024 00:27:03 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
