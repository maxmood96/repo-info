## `eclipse-temurin:17-noble`

```console
$ docker pull eclipse-temurin@sha256:e9ee71797d93f329981ab014d072f44bffc71987cad80242a72bdd63cbeca79a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-temurin:17-noble` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:ad223c9472420ad844f26a770c043ee3d2ff64023e63763239def59c9e02318d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 MB (197322506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4f66180e0b2f9ba50668a6a2ec0bbed0268cd67a8640894bc3ea68e13f30fb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='1a9a532a6c3e591c5eb72ef875d0f5825961bf8cb0eeea876d7f1e198575ed49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf331549f652756582afefc2ee7c09a64ab25e34d1ed06cced226ce3d8077a7`  
		Last Modified: Wed, 02 Jul 2025 03:10:26 GMT  
		Size: 23.0 MB (22954979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7116e2803008c88f3e0a01f8794d3f2d2cb4ced6873e1cbb1508f0ca3dbfa720`  
		Last Modified: Wed, 02 Jul 2025 04:11:17 GMT  
		Size: 144.6 MB (144646724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40062f2f076600e1a5ca4f053337dde667071b23dd75d99803999e13a422bfef`  
		Last Modified: Wed, 02 Jul 2025 03:10:24 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a023b21e1d611c552afa7c4c7b7112fca2b91d703f849cf0388c5f572c201088`  
		Last Modified: Wed, 02 Jul 2025 03:10:24 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:eeecb263c8ef5af3cc81bcf82fa4c738704d7123fd1d114bd72685e690952e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3548132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b666af7f2e6943c07ab639fa3ecb3e2c7466dff8a1e9addbbcd799a541c05b`

```dockerfile
```

-	Layers:
	-	`sha256:32f16f38ba01ab00d8696214c55d5991065ce8a80013b8fdb115e0bede9a2199`  
		Last Modified: Wed, 02 Jul 2025 06:13:54 GMT  
		Size: 3.5 MB (3522443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c531fef594dd5924079f6533b06f58262f19b4f9f336faad96a6807d116e92c`  
		Last Modified: Wed, 02 Jul 2025 06:13:55 GMT  
		Size: 25.7 KB (25689 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-noble` - linux; arm variant v7

```console
$ docker pull eclipse-temurin@sha256:5190c4288cafbf0d63946c11fbf998a673bae0cd0bb071bc1247c2d94274bba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190346936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c05b9db65895c85211cfb1d6089adecbb568ee86d2588f11f80ae5f80eb9784`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:f5b71e3353c1f92a265c88e163d98b6fc00235db4d001763328933c4838f3576 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='1a9a532a6c3e591c5eb72ef875d0f5825961bf8cb0eeea876d7f1e198575ed49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76393e3f1626a318c4984c6e6d91f17fe6888451b277b6cc175eab3a1032ebf5`  
		Last Modified: Tue, 03 Jun 2025 13:33:19 GMT  
		Size: 26.8 MB (26842221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46b8a210bad6a7297677b3b1916898e8d3b789dd0e85f107defb0e8ae077c0b`  
		Last Modified: Tue, 03 Jun 2025 13:54:46 GMT  
		Size: 21.4 MB (21380557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01b16212ccd08fdc0565bf8c0fec89c7f33db9f8529375d00a8b1b4f50e3d39`  
		Last Modified: Tue, 03 Jun 2025 13:54:54 GMT  
		Size: 142.1 MB (142121715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874423c92aa295c19ffe9cc7974725510c968cc666adee01a09b4c9e1e438ac0`  
		Last Modified: Tue, 03 Jun 2025 13:54:56 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7574df2f3d5fe875b6eea652f368a2237c7fc07dce9f6659b9d34d97e40989dd`  
		Last Modified: Tue, 03 Jun 2025 13:37:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f6226fc2a6e4241d07d75a1286936a584e2013ec37cad13486c8df03542ce465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3346699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8864386828174ea94fe67c049878c4235c88eb17442310b6528616f2806d277`

```dockerfile
```

-	Layers:
	-	`sha256:03c1a30da0646ddebda43169cac832034702c358ba6db78191bce6a97745a8cb`  
		Last Modified: Tue, 03 Jun 2025 14:29:12 GMT  
		Size: 3.3 MB (3320892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ee11b3282f9eebad2410ddc8de5aed77c78296cade73f3333f5c442be496075`  
		Last Modified: Tue, 03 Jun 2025 14:29:11 GMT  
		Size: 25.8 KB (25807 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-noble` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:7d940427b9e94b9463e35d07711176f32460cb9d10efe01f863a9110b39a0165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196535177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0947daeb10e29941ff63023dbe45d4d9a48889348ada9c23d96f1a177865db`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='1a9a532a6c3e591c5eb72ef875d0f5825961bf8cb0eeea876d7f1e198575ed49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15da95af15ab8199c89940e881555220a502607539d57e8a5a55302166d61a0`  
		Last Modified: Wed, 02 Jul 2025 05:11:24 GMT  
		Size: 24.2 MB (24163966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef89d4c96cf01b9b6aab425ef361f1fa1172e69ac949d67a2b9968bcfe85f69`  
		Last Modified: Wed, 02 Jul 2025 06:20:06 GMT  
		Size: 143.5 MB (143512752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9211fc1159d21d93a2a0cc7306282f6887d1e0e1fa85ad5390295fa499b5e93`  
		Last Modified: Wed, 02 Jul 2025 05:11:22 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3c11db89d4cd78cebdca1fab6dc3882604c7ec8bc989cc24133bd01e1dda12`  
		Last Modified: Wed, 02 Jul 2025 05:11:22 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:381c6cdcd8a8d6daace458d773762ed2faef89819ec1f7831fbaac200d5976b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3679835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347f1a7144a3831b93c9d556cf52e348c779c85d2bd80c3e934b9478f52423e6`

```dockerfile
```

-	Layers:
	-	`sha256:d2242a7937045fde30b5d804124ee4c1950e77058d8de9963903f8e8957de78d`  
		Last Modified: Wed, 02 Jul 2025 06:15:14 GMT  
		Size: 3.7 MB (3653988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69662670580a16b9997925d73afe5375e686f4b81967bb677e5db1a77f60b3e2`  
		Last Modified: Wed, 02 Jul 2025 06:15:15 GMT  
		Size: 25.8 KB (25847 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-noble` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:b4364421ff3179e9917f2822b826959379e03c968b52e7311d21f5d10809deb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202716551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a948c6567b4dc546761420818a1aa43b69819f78eb223bddf45e876a69c8c0af`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='1a9a532a6c3e591c5eb72ef875d0f5825961bf8cb0eeea876d7f1e198575ed49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1990ab693782ebb597ca9a3a678caa61fcbede21b4aaefc55dc64456936769`  
		Last Modified: Wed, 02 Jul 2025 03:23:39 GMT  
		Size: 24.1 MB (24103453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8199cb24903c2aaa9b6cb5ce65dd1369f792192ce2d2940c36b75367133e77a8`  
		Last Modified: Wed, 02 Jul 2025 06:16:15 GMT  
		Size: 144.3 MB (144289155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871d89e68eb2e5c6245cdc2e1aba3e827444c73f4cdea0122baa417c3b6e6a17`  
		Last Modified: Wed, 02 Jul 2025 03:23:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140030445c4bbe89f0898baf4765c19cadd6b435f20b83468654f0b922861754`  
		Last Modified: Wed, 02 Jul 2025 03:23:37 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:267458cf3d4f3a5a07b6aa3e7b81d797ed0d74133380c604d62bd154836178bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3595977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdce135b0568ed5b56b1dc989806334eafaca587aa41000c034122fa18644be`

```dockerfile
```

-	Layers:
	-	`sha256:26919f33d8cdae198cb2aad8215d7575cbdd06a2ac980e487047d963101e545e`  
		Last Modified: Wed, 02 Jul 2025 06:14:04 GMT  
		Size: 3.6 MB (3570229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac3c592131da48ff3f21cbfff025cf4b64316ef4bb88358c6f700ac2235bc665`  
		Last Modified: Wed, 02 Jul 2025 06:14:05 GMT  
		Size: 25.7 KB (25748 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-noble` - linux; riscv64

```console
$ docker pull eclipse-temurin@sha256:9c134151b3a53d34bb1c9ce32995417e68e77dec88fa88c35c859ce9c6de3fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189589925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39274f3597c84678df70ded483cdc0b97707bded89f80f7c883259ad5758a2ef`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:202c5a7a84e813495c089800398f2ba18952221717db2c10e042ce4179ee6fc0 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='1a9a532a6c3e591c5eb72ef875d0f5825961bf8cb0eeea876d7f1e198575ed49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ccdff8fdb11e14b8e0dab6804aeebce5855635c68b20f199dcf0efcd9b4c462`  
		Last Modified: Wed, 02 Jul 2025 01:17:14 GMT  
		Size: 31.0 MB (30951024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f307aa91f43f6bbfb083211438fde83a6415758b82a4c332bd7dd89aec8e99f0`  
		Last Modified: Wed, 02 Jul 2025 03:30:36 GMT  
		Size: 20.1 MB (20140446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e155206757d593b51cc828aae413b3134d21a605888f369c6558e96b4c989e1`  
		Last Modified: Wed, 02 Jul 2025 06:16:55 GMT  
		Size: 138.5 MB (138496014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda3360286ad8073fe54aa6a8dbaa77a5fdecb6625bd6acede9bb97beb4632e4`  
		Last Modified: Wed, 02 Jul 2025 03:30:34 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32dc6966f7c3bd05314e8db30a9ff60d4c908f89aebef592a52956764636704`  
		Last Modified: Wed, 02 Jul 2025 03:30:33 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:074c35ba7f293f537ca3b428dc04da4d15e1723e5e6cd9c060d7f71535acdcc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3653534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd274a61d619834c29012c14f1fba9089becb8b4aa80f1bd9cf99e1be40d668`

```dockerfile
```

-	Layers:
	-	`sha256:03f4a9c42f0d9290d2a66e3c0714e168ca3ae38e27424f332bf96e7e932be9a2`  
		Last Modified: Wed, 02 Jul 2025 06:14:09 GMT  
		Size: 3.6 MB (3627785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2ebb6a4f9c570730a8c98f053ef8e932818d77256e4407042220a234b3c356f`  
		Last Modified: Wed, 02 Jul 2025 06:14:10 GMT  
		Size: 25.7 KB (25749 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-noble` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:bef47266e9811094645b50e2717b7e91a6e2ab2b43f30d05dfcdde6b8c2a608b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186741656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6aae118acdf28b4f707f0a7fffa624d9dd43939f4b41a7c6abc279b13386df3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:80b0b0c2a08a762cf6a520d8428a5c769c29e72f4a51630adb2231f2816c50c4 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9616877c733c9249328ea9bd83a5c8c30e0f9a7af180cac8ffda9034161c2df2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='0db0d6cbe33238f33aa52837b1dc8fc6067b34d206b3e0f9243c7f8c9b9539a5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='8a3c859355f898c119d154e4caf867263e0e4c8065a91d63ae10666c19bc1108';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='0823d92d9537fcdd56952abc450d1f9585b4d329f8f884dcb230a2e08db6bf5d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        riscv64)          ESUM='1a9a532a6c3e591c5eb72ef875d0f5825961bf8cb0eeea876d7f1e198575ed49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='0033ef81d9c1d30782c5638c20bd7ce3681ebf4b8a68cbc750bb15d613e76e67';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30d64ca13d9d94eb48bf3fece3e38a4e60931d72f1a8c633dec981e43a0515a4`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 29.9 MB (29925630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f20e5bf93e1bfddd9097b0ff58228842e801f91f2b972d3a3308109367dee4`  
		Last Modified: Wed, 02 Jul 2025 04:19:29 GMT  
		Size: 22.1 MB (22132438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3636a63d95f0ce5b400df98681c871188b9de0e5574d717f0d6bab59240fdbce`  
		Last Modified: Wed, 02 Jul 2025 06:17:30 GMT  
		Size: 134.7 MB (134681147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69430f396324a2f30f2312f97ed07a2e793797e90d5e9dfb19f276a6f0af49bb`  
		Last Modified: Wed, 02 Jul 2025 04:19:27 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96cd9efedc0dc65cf9345899c568fdb0660526ce1337bc8dcf2ffe55465fc68`  
		Last Modified: Wed, 02 Jul 2025 04:19:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-noble` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5bc471ba09c3e23a132979dd8e909b9bb059c5c68224a0992bcea49bfbfe8176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3493944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa81b977cb110bec4d23cb4736a0e1940325219d7843bdae1f76bfd7b090d4a`

```dockerfile
```

-	Layers:
	-	`sha256:9e8d3593417ecfb97c639a90cb00c49f1576bc2bf4746a898c87bc25753a60e9`  
		Last Modified: Wed, 02 Jul 2025 06:14:15 GMT  
		Size: 3.5 MB (3468256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d687687faf10b2a185a781cb4fab2a6c07c37058b8a238bc6e160fdbd572df2`  
		Last Modified: Wed, 02 Jul 2025 06:14:15 GMT  
		Size: 25.7 KB (25688 bytes)  
		MIME: application/vnd.in-toto+json
