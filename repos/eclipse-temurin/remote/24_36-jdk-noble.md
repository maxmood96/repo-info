## `eclipse-temurin:24_36-jdk-noble`

```console
$ docker pull eclipse-temurin@sha256:5c234fbadb2405374858d3fdc9e5742229b4e225d2ac01c2310c2643096080b4
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
$ docker pull eclipse-temurin@sha256:08b912766bfabaf12bfe4ecdb003509585220f408fc271d575607fc24bfbcff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149523932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bfabd082e1e32068836a0d60abb8281d0db373d779a571fda703d6913a5612`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d64a00472960835509d7aca644e6f1aa288b1da5b66276bdaaa89cfb795508`  
		Last Modified: Tue, 25 Mar 2025 21:57:57 GMT  
		Size: 29.8 MB (29810691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11cca89372c16627655655d29d212f2f05234515758cd5b9221a628de390a9d6`  
		Last Modified: Tue, 25 Mar 2025 21:57:58 GMT  
		Size: 90.0 MB (89956636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e10385d296e036f10239d1b2aa58020cdf5982d5dd6249b22b681df84efe17`  
		Last Modified: Tue, 25 Mar 2025 21:57:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24_36-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:23346acddc7d46e41965ee59493d05cca3ec149ee531eb4e61f1f4f353e3bc93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce77bd91af33201d01d4026cb9d130190aaff2832ba889075522eb5439cf6802`

```dockerfile
```

-	Layers:
	-	`sha256:5239632002f393d9ede4913948d4b3abf9a4b0319f69bec25337d2e67fe2a08a`  
		Last Modified: Tue, 25 Mar 2025 21:57:56 GMT  
		Size: 3.2 MB (3239232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c4eea9372d001973e96c46662458a91ec9f3b14b364d47a6cbf0f6e81ecca01`  
		Last Modified: Tue, 25 Mar 2025 21:57:56 GMT  
		Size: 24.5 KB (24517 bytes)  
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
$ docker pull eclipse-temurin@sha256:1d5644703acfe3160d7204f20050756270a95654433fb1a9cbda2d18264495f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155868579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2187e9e04b9b5481e65d3ade5242554588d35b464ec4055303f91067a9ad4527`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
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
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bc7c74b0a88589faef5673d61f5b9665fbaeb604582d1fb76cb818f3b6563d`  
		Last Modified: Tue, 25 Mar 2025 22:07:50 GMT  
		Size: 31.5 MB (31548686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f13241e743491379ede23f654a21dd0ab37097965794d96d77275137ebb7c9`  
		Last Modified: Tue, 25 Mar 2025 22:07:52 GMT  
		Size: 89.9 MB (89927755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40dfbc506a807b208fbeb6341d43de54af50c1727e97d91303cfda44cfef7ec`  
		Last Modified: Tue, 25 Mar 2025 22:07:49 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24_36-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d1dc1feeb1aac64e78238310af56144c87522ee28fec61ded9e73d0920acef6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3313068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8fd65c66626be8fa18c9fa390d03bb93e1dd42aeb020ccfb3cc8388c824713`

```dockerfile
```

-	Layers:
	-	`sha256:d24ed78a98cac57e90bfc8025345a7048bc657e6175602ae79aabde9b78676f5`  
		Last Modified: Tue, 25 Mar 2025 22:07:49 GMT  
		Size: 3.3 MB (3288494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fdaa1eaecdd0647d79c7db6c4a8bddc089825fe0e6c02695de68be33628362f`  
		Last Modified: Tue, 25 Mar 2025 22:07:49 GMT  
		Size: 24.6 KB (24574 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24_36-jdk-noble` - linux; riscv64

```console
$ docker pull eclipse-temurin@sha256:411ed36cf4db20dd40107fd9000a0cbad28f2a7e64d26782d11ef88020db1362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (136989317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a92da2835aaeedef9e66b8ae6ffb08d9c65db7486469a7fe0b63707c4ddea9d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:46:38 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:46:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:46:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:46:39 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:47:10 GMT
ADD file:69c46ae9666e78c27ca5b5f25cec1a5536ff16f17cb00104e5c77e722bd8d643 in / 
# Mon, 27 Jan 2025 04:47:12 GMT
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
	-	`sha256:6e1053d729cc1718daa9369927cf6ddfbf892a846041de0e610d1c77ade136c5`  
		Last Modified: Mon, 27 Jan 2025 05:10:15 GMT  
		Size: 31.0 MB (30983910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6532351b5a9abc55e43c6e4a89566b1d23ca956b4bf9523adfc86ef993f297c`  
		Last Modified: Tue, 04 Feb 2025 05:18:22 GMT  
		Size: 18.4 MB (18374638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c945418ac695b835334a44dd3f9c2a41820215fe8e13db4f7b2e02e99999c255`  
		Last Modified: Tue, 25 Mar 2025 22:02:31 GMT  
		Size: 87.6 MB (87628454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5174d87b62837594a8e69e0af520d13c37c2df6d7a2c1241868dee2f8a6ec6ad`  
		Last Modified: Tue, 25 Mar 2025 22:02:19 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24_36-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:49bb6589323f7dea9daee532008bf62caf09c6c185cd90db6d906b9c19c2b610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3374736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7d0c5db477e00fc10dfaa18e66e0c9dc43762b915eb66b03d83a3080f4aaac`

```dockerfile
```

-	Layers:
	-	`sha256:e825ecc1b44de754d488f0d59b96f3f146aac983a3ca92e8471e5fda7c4b5340`  
		Last Modified: Tue, 25 Mar 2025 22:02:19 GMT  
		Size: 3.4 MB (3350159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd7f406b4311defb325be70a9474ccedbb1067ab9406863ecb21b84616a4d3d`  
		Last Modified: Tue, 25 Mar 2025 22:02:18 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24_36-jdk-noble` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:9b041a823ce5a543fd885f5f2dca73215ddbd46cc252c11c492b6bce2a8f0cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143004668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71552768a9e32b44d0ac5da605757210b8cf2788cd02318f8e4e59b51579a5a4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:15:19 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:15:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:15:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:15:19 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:15:20 GMT
ADD file:1a65bb049384da7e51a2b1e9180f11d6ec22b1427da7ca5682814abd261ba57e in / 
# Mon, 27 Jan 2025 04:15:20 GMT
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
	-	`sha256:8e1d25585ef2d346b71072d258a697a9d190e3c5754512c7cb978dbbe80911e6`  
		Last Modified: Mon, 27 Jan 2025 05:10:30 GMT  
		Size: 30.0 MB (30027563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88477e6f6da4ec2c4722d9d9decee6ffb88f4f57f402646e5dcca26d1f8b8aa1`  
		Last Modified: Tue, 25 Mar 2025 22:03:36 GMT  
		Size: 27.7 MB (27748934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad465ad17cdeed14bbef33bb6fc3cbd1d1ed20d0f6785083ca71c877d5f19af5`  
		Last Modified: Tue, 25 Mar 2025 22:03:34 GMT  
		Size: 85.2 MB (85225857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3da3173e8dd4c7f1a7f8be242bc17309078d69c06194769d3563330e5952a98`  
		Last Modified: Tue, 25 Mar 2025 22:03:32 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24_36-jdk-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:83843f879c1fd985be50b35d467d5c86a1fd5eefe386a40c16c06cba545997f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3212526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737241b71e63da2708fdf587e2d6a8078b9a17692affad2c2f8fb11f956f501a`

```dockerfile
```

-	Layers:
	-	`sha256:69ca3b74ae951f2145d27e7d772232e46d57353e40b6883d13c1d5fcdb4a371e`  
		Last Modified: Tue, 25 Mar 2025 22:03:32 GMT  
		Size: 3.2 MB (3188009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f3131683640fef3597cbf7e9e931ab598b808c64bc077572bb67ff86bd088b1`  
		Last Modified: Tue, 25 Mar 2025 22:03:32 GMT  
		Size: 24.5 KB (24517 bytes)  
		MIME: application/vnd.in-toto+json
