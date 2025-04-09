## `eclipse-temurin:24_36-jdk-noble`

```console
$ docker pull eclipse-temurin@sha256:f202c3a01e184aae5ed33480b99a7f4897be6a76c9d2386f4a595553da5ec1cd
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

### `eclipse-temurin:24_36-jdk-noble` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:0433ea598644e3cee68e0fcea850d2dd578e8ab9a0d6a13f3caba5316450f9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (141003486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce266cb0c99b2ee9dd0506f154f2f678321563ebb2f9820de3cdcb6f592e8d6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Mar 2025 17:58:27 GMT
ARG RELEASE
# Tue, 25 Mar 2025 17:58:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 25 Mar 2025 17:58:27 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='c340dee97b6aa215d248bc196dcac5b56e7be9b5c5d45e691344d40d5d0b171d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_linux_hotspot_24_36.tar.gz';          ;;        arm64)          ESUM='18071047526ab4b53131f9bb323e8703485ae37fcb2f2c5ef0f1b7bab66d1b94';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64el)          ESUM='3a5641ab862a2bbae56886d4ec47f735052780bfe124df7aea2ca40e0f973b5a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        riscv64)          ESUM='a1d993ab0b4b80101ec2e2452bdd37735572b734c255576a47c5130eab55f09a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_riscv64_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='e3149dc2ab1db0bdf86ab8d27a5ad67e32e30c829cef8a02628d36e5781f44ff';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_s390x_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e424a5f4017c616dd70e460381d8638ca74da30bce4cc759914e06c782aa2b8`  
		Last Modified: Wed, 09 Apr 2025 01:16:38 GMT  
		Size: 21.3 MB (21326882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ff1ff9a059dfbbea99287fc827dcbaab5bbb5f34f047e9e13fd5435637e80f`  
		Last Modified: Wed, 09 Apr 2025 01:16:40 GMT  
		Size: 90.0 MB (89956637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21c27cceb184256ee474b28fbafebf0ea555626b31cdfc372746ab7e12839f0`  
		Last Modified: Wed, 09 Apr 2025 01:16:38 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24_36-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0d26aed54768eef2a8a82ece9304541a1e9ecc050b97b0c767b3a90697102e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a7ad3587390c9d4af3f5abd03bbcc0dfb136d110fe22adca5d7b8564fe53eb`

```dockerfile
```

-	Layers:
	-	`sha256:ceb31a203c3baf617b2a2ec6505f6c146611013824e83047d831bcf1d8cd18c9`  
		Last Modified: Wed, 09 Apr 2025 01:16:38 GMT  
		Size: 3.2 MB (3240026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48073be2867400f57972aa296a98f4ea13e24fef597b6b146d1b572f6c2b1995`  
		Last Modified: Wed, 09 Apr 2025 01:16:37 GMT  
		Size: 24.5 KB (24515 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24_36-jdk-noble` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:ed89b1de7cd6c498c48d77d18b2d33fb2c5bd8fe087231df1bc2ce85ab546726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148564674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b25c7d40751bdefb63cee379ce4ab70322148b1f65543fff5f59c640384ab7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='c340dee97b6aa215d248bc196dcac5b56e7be9b5c5d45e691344d40d5d0b171d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_linux_hotspot_24_36.tar.gz';          ;;        arm64)          ESUM='18071047526ab4b53131f9bb323e8703485ae37fcb2f2c5ef0f1b7bab66d1b94';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64el)          ESUM='3a5641ab862a2bbae56886d4ec47f735052780bfe124df7aea2ca40e0f973b5a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        riscv64)          ESUM='a1d993ab0b4b80101ec2e2452bdd37735572b734c255576a47c5130eab55f09a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_riscv64_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='e3149dc2ab1db0bdf86ab8d27a5ad67e32e30c829cef8a02628d36e5781f44ff';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_s390x_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe6ed91129b7d4def6fa771bdde6970a7982e7fad16ae145192b4e16dccf4f9`  
		Last Modified: Tue, 25 Mar 2025 22:03:57 GMT  
		Size: 30.6 MB (30575227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94b245a41dc050bf013c4e251e6f42adc662b63845f553dd0f36408eca39fb9`  
		Last Modified: Tue, 25 Mar 2025 22:03:59 GMT  
		Size: 89.1 MB (89093535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64135d99b56097d1ea171c9795be20eb16a29b08259b176721818b12d58a88bc`  
		Last Modified: Tue, 25 Mar 2025 22:03:56 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24_36-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:526f5e949d3813bce4cbfa97d5a3e6ae797b3c438d0e31e108e515e91b2c5040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3395438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e268812ce526104d47924b58d3ffe4aac3fcc2630d64c5ba5413bb0f2356189b`

```dockerfile
```

-	Layers:
	-	`sha256:b2e2f8c71b147711863cc7dc08e7b0f18e100c5d598149508d49ddd951bdff34`  
		Last Modified: Tue, 25 Mar 2025 22:03:56 GMT  
		Size: 3.4 MB (3370763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbaa666e1c23f8c49a9111ee9e5b519b0c77f1a277baf527a898131c678f3ebf`  
		Last Modified: Tue, 25 Mar 2025 22:03:56 GMT  
		Size: 24.7 KB (24675 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24_36-jdk-noble` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:98c08ab503ac7bbe0e7b2951d4c7271eb98066d24df3f303c376c3df1f9557d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146320309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdfef91dff833117076158d9fa3e6a01a7836ba9f055d96f23e92e39b011f2c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Mar 2025 17:58:27 GMT
ARG RELEASE
# Tue, 25 Mar 2025 17:58:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 25 Mar 2025 17:58:27 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='c340dee97b6aa215d248bc196dcac5b56e7be9b5c5d45e691344d40d5d0b171d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_linux_hotspot_24_36.tar.gz';          ;;        arm64)          ESUM='18071047526ab4b53131f9bb323e8703485ae37fcb2f2c5ef0f1b7bab66d1b94';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64el)          ESUM='3a5641ab862a2bbae56886d4ec47f735052780bfe124df7aea2ca40e0f973b5a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        riscv64)          ESUM='a1d993ab0b4b80101ec2e2452bdd37735572b734c255576a47c5130eab55f09a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_riscv64_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='e3149dc2ab1db0bdf86ab8d27a5ad67e32e30c829cef8a02628d36e5781f44ff';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_s390x_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b88d3678b4be019bd7eebdda85972ed222e4c9c19610d7636f7838113b3a47`  
		Last Modified: Wed, 09 Apr 2025 04:55:39 GMT  
		Size: 22.0 MB (22049405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1123fddae74cd78a8b49310ea859220526669dde725712b69e6f38a8ceb9c912`  
		Last Modified: Wed, 09 Apr 2025 04:55:41 GMT  
		Size: 89.9 MB (89927722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7403dadf933fbdbbaf6e9bcdc40979b2173a2a5a9528ab3774ada5733b4e6c8c`  
		Last Modified: Wed, 09 Apr 2025 04:55:38 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24_36-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:944b4e0d0af767729fc5cb52a0029e512c882d4c64025e6870e2ed125d6d7147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3313865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f137d7a1a6cb8f7451c3a7fb9d2c94e6f77d8d9f63600261655dc2838fa965d`

```dockerfile
```

-	Layers:
	-	`sha256:6e1484234744dbff88e4537f9479907b28a48640484ffdb04cad05422c2e73ef`  
		Last Modified: Wed, 09 Apr 2025 04:55:38 GMT  
		Size: 3.3 MB (3289288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73bb55beb5165ec298bb604ea9f42cd6987cabb3044ab1b27040cc81a99f5b28`  
		Last Modified: Wed, 09 Apr 2025 04:55:37 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24_36-jdk-noble` - linux; riscv64

```console
$ docker pull eclipse-temurin@sha256:cfc9e1af500dddeaa4c50f810d869c3999a261425b9a1e8a50e954f054b5ce9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (136952940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb438ee62fe2e9a961e681f8c3913cd009d2d029cef496a2fa64a4b29942012`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Mar 2025 17:58:27 GMT
ARG RELEASE
# Tue, 25 Mar 2025 17:58:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 25 Mar 2025 17:58:27 GMT
ADD file:ef7c97f5dd8d665aae899afe52c54f7acaf71fa51e9d7f26e13ed6073141c666 in / 
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='c340dee97b6aa215d248bc196dcac5b56e7be9b5c5d45e691344d40d5d0b171d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_linux_hotspot_24_36.tar.gz';          ;;        arm64)          ESUM='18071047526ab4b53131f9bb323e8703485ae37fcb2f2c5ef0f1b7bab66d1b94';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64el)          ESUM='3a5641ab862a2bbae56886d4ec47f735052780bfe124df7aea2ca40e0f973b5a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        riscv64)          ESUM='a1d993ab0b4b80101ec2e2452bdd37735572b734c255576a47c5130eab55f09a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_riscv64_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='e3149dc2ab1db0bdf86ab8d27a5ad67e32e30c829cef8a02628d36e5781f44ff';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_s390x_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ba2f284f7444fb0b78fa804d74c44dee4b397610267539e4a6e9c41ae41e06a1`  
		Last Modified: Tue, 08 Apr 2025 11:54:06 GMT  
		Size: 30.9 MB (30943202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c92c21d833c06c090f85c4bdc5ddb44f5709e8109a4cef55c8fbf37fd8c2bd`  
		Last Modified: Wed, 09 Apr 2025 05:54:13 GMT  
		Size: 18.4 MB (18379010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec2fd5270db78a25fdb19cef4432226d3960e4b55fe61cf2b5518d408a01d1f`  
		Last Modified: Wed, 09 Apr 2025 05:54:23 GMT  
		Size: 87.6 MB (87628414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176eebc30d946da65f1b02dc1b2e9bbe2225c94d0faf43c837a5d5c2489e5db8`  
		Last Modified: Wed, 09 Apr 2025 05:54:10 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24_36-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:099802f633ee2a3c2b60447b54de3a55bce718dfa0755af472600af01dc3f523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51590b9bebc4470cebc82349808221d30d6e24c90e511f337b0e14de4a55c7e0`

```dockerfile
```

-	Layers:
	-	`sha256:cd7e7722bfdf7100f91960e83f92472badb9fe725a8e4dbafc1570fb107eace8`  
		Last Modified: Wed, 09 Apr 2025 05:54:10 GMT  
		Size: 3.3 MB (3347798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3145bdb36edeafa4b860d69e49bdcdd7ca4cb3c6f8ad5d4712b0931138ff00f2`  
		Last Modified: Wed, 09 Apr 2025 05:54:10 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24_36-jdk-noble` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:158cc03b5d3bed0ea2b6ce2a2db7384a21773ea074087b64b0c50ebc3c6ab601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135599232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba69ac82ef9a99a7aa7e9cbb909fdc2082853919e293cc8c40920a900a030d35`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Mar 2025 17:58:27 GMT
ARG RELEASE
# Tue, 25 Mar 2025 17:58:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 17:58:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 25 Mar 2025 17:58:27 GMT
ADD file:8f287f40ca940c9bd87c8706751f5f1c5bbd0a83fd75f7d938832b226fdb936d in / 
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='c340dee97b6aa215d248bc196dcac5b56e7be9b5c5d45e691344d40d5d0b171d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_linux_hotspot_24_36.tar.gz';          ;;        arm64)          ESUM='18071047526ab4b53131f9bb323e8703485ae37fcb2f2c5ef0f1b7bab66d1b94';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64el)          ESUM='3a5641ab862a2bbae56886d4ec47f735052780bfe124df7aea2ca40e0f973b5a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        riscv64)          ESUM='a1d993ab0b4b80101ec2e2452bdd37735572b734c255576a47c5130eab55f09a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_riscv64_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='e3149dc2ab1db0bdf86ab8d27a5ad67e32e30c829cef8a02628d36e5781f44ff';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_s390x_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e5722f32c6281fa87f1e5f7ebe307864b50aa95a116496a205ce47478bc9b52c`  
		Last Modified: Tue, 08 Apr 2025 11:54:12 GMT  
		Size: 30.0 MB (29956206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eaafd8c5a3e092182032e97ceba6359b4366612c575b5582fcb49076467fa33`  
		Last Modified: Wed, 09 Apr 2025 04:27:34 GMT  
		Size: 20.4 MB (20414864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ba649f6592fffb698b4967e4cc7f5ac007aac2ae9d86e01ffbd464a7b30a3e`  
		Last Modified: Wed, 09 Apr 2025 04:27:35 GMT  
		Size: 85.2 MB (85225847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e87be84bf04c4a3952f0bc9460515f3a7b875ecfa1745e896b72aaed9f924dc`  
		Last Modified: Wed, 09 Apr 2025 04:27:33 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24_36-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2545fd16f2ee76735669068696a3f28848b2a3700f6f66768a4835fb4c914252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3213320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea5175ad654396afba7d79651314c8a00c66cac9dd3528c33f41116d199fe99`

```dockerfile
```

-	Layers:
	-	`sha256:7a6ec0f54361daa4f1b50b0ac250cb44c4971285aa2ff11fc3226738035c5a58`  
		Last Modified: Wed, 09 Apr 2025 04:27:33 GMT  
		Size: 3.2 MB (3188803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa771554705a5ae89ffa404c6d11fd30b346bc2af29176bd08b44868695fe21f`  
		Last Modified: Wed, 09 Apr 2025 04:27:33 GMT  
		Size: 24.5 KB (24517 bytes)  
		MIME: application/vnd.in-toto+json
