## `eclipse-temurin:8u442-b06-jre-focal`

```console
$ docker pull eclipse-temurin@sha256:578080ce57200d6a851dcd87eaf36d589ed0a6041199660944380dd2154284c6
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

### `eclipse-temurin:8u442-b06-jre-focal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:bc10caecbb2979e5b5790aeb78112b780a5f1ee4d8b2f8b83d298fdeddad5eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89652543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424f72935cba80fb4c6950d091779f58cde189c91ee5ac453a22ea40fec29149`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='055c47c5c1dfe8c9c135d87fed7a3745c17374618bc8d5acb9316d1b812c0e6d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0e7b9c8cee8097e1ae6b185ddf7a5b29d6c95c6633efd2c0f9a13813e04323`  
		Last Modified: Wed, 09 Apr 2025 01:15:15 GMT  
		Size: 20.3 MB (20260206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35260a664b4a8afc750745416ad5505a3fb8aaeded9524b08d333896490c6a77`  
		Last Modified: Wed, 09 Apr 2025 01:15:15 GMT  
		Size: 41.9 MB (41879536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfeb4939f4bc91a906cb09122139dd2113ed62b05ccebb280385b5efa773c0f3`  
		Last Modified: Wed, 09 Apr 2025 01:15:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a34aaea29b0eb3fecf3371aa10826ee9b6d20aba3d8e85802144185fb5636b`  
		Last Modified: Wed, 09 Apr 2025 01:15:15 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jre-focal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c11be2dde75cdef89088402fccaf39709b903f486c7c21fbe4e560f6350c932b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcfc196d78b792313153c375b02933819eeb203e9bffec4f328901b9895f93f`

```dockerfile
```

-	Layers:
	-	`sha256:805b762bc602451186454f302eb93ebac904b3390c543ac14961aacc439d947e`  
		Last Modified: Wed, 09 Apr 2025 01:15:15 GMT  
		Size: 3.7 MB (3738181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abca642b82ee002c1ad98e674ef719280fc142d211a75f8ba84bcfe53f2cb55a`  
		Last Modified: Wed, 09 Apr 2025 01:15:15 GMT  
		Size: 22.0 KB (21960 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u442-b06-jre-focal` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:14ff78bf48478081f6c27f51b2cfb91385f910966a6ccefed8260a2ff9910dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81461268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb08440df94585521d0b531d6d4e2bcf706395cfb74b045c8770b5d6b8275603`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:34 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:34 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:36 GMT
ADD file:f76c848564adfa0c782654cd9423feee0ffacccd95abfe3e4e696203d5e61fbf in / 
# Fri, 11 Oct 2024 03:38:37 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='055c47c5c1dfe8c9c135d87fed7a3745c17374618bc8d5acb9316d1b812c0e6d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:10b337d353b3ceaf6823ab2d8696989401feed741b22eb313c8a0cd378762d39`  
		Last Modified: Fri, 11 Oct 2024 04:41:36 GMT  
		Size: 23.6 MB (23620412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf7dfa91dfefd2d38b8ffd98f5296dec749e2c8b186d41439b07e2e8ade5eba`  
		Last Modified: Thu, 24 Oct 2024 00:57:44 GMT  
		Size: 18.5 MB (18475795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4ee80983cf684bdd386a5ceba41902aa0d1a2807229adba80116cd7838bffc`  
		Last Modified: Fri, 31 Jan 2025 01:32:46 GMT  
		Size: 39.4 MB (39362652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea62920c8f8b3f0ae2e89fbd0d7e796f4cd3c917395fb735056bb637d7b1af7`  
		Last Modified: Fri, 31 Jan 2025 01:32:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6883c2cf120839e8fdf9502ccf3d9acb4d324c3c005f52ecc85453a1c48d785f`  
		Last Modified: Fri, 31 Jan 2025 01:32:44 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jre-focal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6c0465a1d3aa55c1e1849748493763638abc14609159116dc2492969ce6577c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3765207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f90c2af4e6efde7c076f1255de9f09b7f59c1c3e1dac55ef10ed46f8f050ace`

```dockerfile
```

-	Layers:
	-	`sha256:4c95cbef6b85c0fa564bd33ba9954a0164ab8c95c6754209e91a562b7e688b9a`  
		Last Modified: Fri, 31 Jan 2025 01:32:45 GMT  
		Size: 3.7 MB (3743162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db45a53f5fdbe0111a23257c8510743b62fb9f4f40e85ad7c3dc66ab41a071ee`  
		Last Modified: Fri, 31 Jan 2025 01:32:44 GMT  
		Size: 22.0 KB (22045 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u442-b06-jre-focal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:729ba227bf8385afb20ab79e0e085627b243cdf62c812d09ab53198b01d71127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86950731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1088f8ff6d5223266e7e5e57b64b8e582448b95cd4f07d2bf9ad774239c9551`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='055c47c5c1dfe8c9c135d87fed7a3745c17374618bc8d5acb9316d1b812c0e6d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e623d12075ed7a05b064c5e3f3efe3b64669e0176900a7b195c750eec83f6f79`  
		Last Modified: Wed, 22 Jan 2025 20:50:38 GMT  
		Size: 20.1 MB (20094632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec110cdef34c6829c2f088dd32067784ed2dd806d4657a74f60a167560815080`  
		Last Modified: Fri, 31 Jan 2025 01:33:08 GMT  
		Size: 40.9 MB (40879861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f74fd78af2433d1304ba76f2dc5fe0aeaa7e26b77e8deeacc09b3729f3d709`  
		Last Modified: Fri, 31 Jan 2025 01:33:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d4a0076d0f6e9da1387fe0c1bde2ecd400d764f61a18f1f37618d6de067b88`  
		Last Modified: Fri, 31 Jan 2025 01:33:07 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jre-focal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:314d76d0dc1a865a2c6b28f8b2ad5bcdaab05fefa53b4375e3d445c61c7f9ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5cd6688fff62b7807648598a3d93abc4b99a5c73c2d4b092198f2f69c3f4f9`

```dockerfile
```

-	Layers:
	-	`sha256:95f9a744e69c113007b941a6663c09d64f0488ee94193ff142a4f6a488ee5d9b`  
		Last Modified: Fri, 31 Jan 2025 01:33:07 GMT  
		Size: 3.7 MB (3737827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80c9a9d14d4b40a74a4031a9599d9e54da371c9ed7c667d6e1d914aec5652d6a`  
		Last Modified: Fri, 31 Jan 2025 01:33:06 GMT  
		Size: 22.1 KB (22070 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u442-b06-jre-focal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:81458e3a00233b712ac8530e0368a79487e955bfc07fa63e95d7a8926268232a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95769786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995472001a7138b3b0cfe4da47e0a62e9ef8696081ce6546e42ad730b16df8de`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        arm64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        armhf)          ESUM='055c47c5c1dfe8c9c135d87fed7a3745c17374618bc8d5acb9316d1b812c0e6d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_arm_linux_hotspot_8u442b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5eddb83d3002695f58ef132a43fe0c41ba6a1338438d3698725700dfbf1177`  
		Last Modified: Wed, 09 Apr 2025 04:33:49 GMT  
		Size: 22.4 MB (22424673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015cbfca84a7a3d1c0e467f0e7d6fe371fe0c9127b7b4e299866c9e481799a93`  
		Last Modified: Wed, 09 Apr 2025 04:37:15 GMT  
		Size: 41.3 MB (41265757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0f3b63d6effabc87f7d0404edf4deb190dce9a602d8f6131ffedc8c757d60c`  
		Last Modified: Wed, 09 Apr 2025 04:37:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afb8f30902dec3edeedb28e30fb9adf84c1a7bc52e81510b330a08ab4d8fcbd`  
		Last Modified: Wed, 09 Apr 2025 04:37:14 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jre-focal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8d6f0effdfe6940e21e9b46e5d898ddef3cb019b7ec707fdb381b0958920c335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3764730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f8188fe1b4c60075cecc5ff301c6277b0acc656740484dcf9d15a03fdc269d`

```dockerfile
```

-	Layers:
	-	`sha256:b8d615c2f083d1d978f2bdfa0ca36a9908683dfac773691878eca68b878eaf93`  
		Last Modified: Wed, 09 Apr 2025 04:37:14 GMT  
		Size: 3.7 MB (3742734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc05dbd32e89dfb6435dd01a509303b7b59cb1457351e1ab6958ef9ee6a142dd`  
		Last Modified: Wed, 09 Apr 2025 04:37:13 GMT  
		Size: 22.0 KB (21996 bytes)  
		MIME: application/vnd.in-toto+json
