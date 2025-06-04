## `maven:3-eclipse-temurin-24-noble`

```console
$ docker pull maven@sha256:3d8e7908046b5c12453d88fd9cb4e50758d5606efcd4ab87434614d561375dba
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

### `maven:3-eclipse-temurin-24-noble` - linux; amd64

```console
$ docker pull maven@sha256:958c887454740022b46bb206c842de48b45f7d647c7995307e27d528fe9f420a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174361260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ce6a19da82849ecaceb6e94421f12227fc2a0f677de00001011733ed581774`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Mar 2025 16:03:48 GMT
ARG RELEASE
# Thu, 27 Mar 2025 16:03:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Mar 2025 16:03:48 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Mar 2025 16:03:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 16:03:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='78832cb5ea4074f2215cde0d01d6192d09c87636fc24b36647aea61fb23b8272';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        arm64)          ESUM='a598260e340028d9b2383c23df16aa286769a661bd3bf28a52e8c1a5774b1110';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64el)          ESUM='770e7e506d5ea3baf6c4c9004a82648e29508a1c731d8425acded34906e91b09';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        riscv64)          ESUM='4e953ec63e141b667e02f7179304c6553cbd13ba94b60dcadd8e45c7f309c89d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_riscv64_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='6ff3126ae0a7cff3a25b7590adc441550666750515fd7d6e2d2706b5fc9a1f6f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["jshell"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2b1733fa885870b63602a5156659e0a63685dfba408260006d988830abed85`  
		Last Modified: Tue, 03 Jun 2025 13:31:09 GMT  
		Size: 21.3 MB (21327277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60b1732f5c19a877f88783e2a1a995e463eb5f22bff6ee00564e5042d2a4aa5`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 90.0 MB (89960833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9815e77b54f33dbcd213d596eeaad209e5255afa9c22666ba991c8c1daf1211`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd9fd82cacd5a55de983cdadc44093b9891d72a9f67bdc3d4c29ed2513fab9a`  
		Last Modified: Tue, 03 Jun 2025 13:43:14 GMT  
		Size: 24.2 MB (24184021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870b0b2113ddad6785601d5d514dd4435c26f5af196b3a7124668ecae36d74d7`  
		Last Modified: Tue, 03 Jun 2025 13:43:14 GMT  
		Size: 9.2 MB (9170439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f883242224a75ec0a98a487e830206063d431454a6d5dc443f1e1fca011227a3`  
		Last Modified: Tue, 03 Jun 2025 13:43:13 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e226f2ab55218af7215578eb4cc23f8bf25db177f8b3985a4cfe16a6033a57`  
		Last Modified: Tue, 03 Jun 2025 13:43:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-24-noble` - unknown; unknown

```console
$ docker pull maven@sha256:5ac4435a98a667470c69f350becf8676f9b7d4e09419bc52aec759b177bb830c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4854748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d214c851624bee463abd403767953ed91b606f432673c264b84c768ec5be689`

```dockerfile
```

-	Layers:
	-	`sha256:685def8f552e23aedea45602ba548b465c3c7ac5592808386469b7324f8a39e8`  
		Last Modified: Tue, 03 Jun 2025 14:28:27 GMT  
		Size: 4.8 MB (4835088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22d1cd103fcdc784b8ebacfe3a459329e24e2a9da441a83700c69546b1ab790d`  
		Last Modified: Tue, 03 Jun 2025 14:28:28 GMT  
		Size: 19.7 KB (19660 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-24-noble` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:19a59816c739a076c739a873836d8f98e07f383abced84f56508fabad6c09944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173890720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cea006707337f9df32490803c56a4cd8e5f2ed8ac98033dcf907d6763b171a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Mar 2025 16:03:48 GMT
ARG RELEASE
# Thu, 27 Mar 2025 16:03:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Mar 2025 16:03:48 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Mar 2025 16:03:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 16:03:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='78832cb5ea4074f2215cde0d01d6192d09c87636fc24b36647aea61fb23b8272';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        arm64)          ESUM='a598260e340028d9b2383c23df16aa286769a661bd3bf28a52e8c1a5774b1110';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64el)          ESUM='770e7e506d5ea3baf6c4c9004a82648e29508a1c731d8425acded34906e91b09';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        riscv64)          ESUM='4e953ec63e141b667e02f7179304c6553cbd13ba94b60dcadd8e45c7f309c89d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_riscv64_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='6ff3126ae0a7cff3a25b7590adc441550666750515fd7d6e2d2706b5fc9a1f6f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["jshell"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d1b0680b194d67e948b3a639e1329e14be5d88ad5fec4214701acbd0c18048`  
		Last Modified: Tue, 03 Jun 2025 13:32:47 GMT  
		Size: 22.5 MB (22506244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c49d160d962b83161700ce87315037ce22326680395bca1604741b2c713d76`  
		Last Modified: Tue, 03 Jun 2025 13:32:52 GMT  
		Size: 89.1 MB (89091802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b4a167a42b283ab9ec70157a0915bd4a9ab079c1939b9096a4b3b3feb77a91`  
		Last Modified: Tue, 03 Jun 2025 13:32:46 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c011c4fcf8c465eb8e526965f7f350db51bd62edf2314c3e73fc1350aef3d8e2`  
		Last Modified: Tue, 03 Jun 2025 14:10:36 GMT  
		Size: 24.3 MB (24266984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d03f22d33e622c0873d04b3c55d28a72a27852493574bc0e2e324aac6b2a088`  
		Last Modified: Tue, 03 Jun 2025 14:10:35 GMT  
		Size: 9.2 MB (9170441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f879c244457c37f30dae12185a0fa5f8f959b99b6b11cd3a98513acc8e71efbb`  
		Last Modified: Tue, 03 Jun 2025 14:10:35 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1eb7d6f5cefe83095a8175f566c6318414998eb2c88e7276a0ca5e41c750d3`  
		Last Modified: Tue, 03 Jun 2025 14:10:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-24-noble` - unknown; unknown

```console
$ docker pull maven@sha256:c10e1d3141b0118792ea013039a68ed369d5fe05f31fd321610441a768d84799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4992437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a85f02f69c7b99e1a769370f0b67839845c7cd09de9533899a529009224edb`

```dockerfile
```

-	Layers:
	-	`sha256:055598f657255a6ce00ec15392288f4307b6f061033b9b0bddc2d51eab22ee66`  
		Last Modified: Tue, 03 Jun 2025 17:29:46 GMT  
		Size: 5.0 MB (4972645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa42ff97610abfe7c965a4fbdad64c3379bf52a8e73c64453eb01dd58d27ca90`  
		Last Modified: Tue, 03 Jun 2025 17:29:47 GMT  
		Size: 19.8 KB (19792 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-24-noble` - linux; ppc64le

```console
$ docker pull maven@sha256:1296094f789e45ca78fa0de760763a24d3c5df1d44041b891d36e768796fb365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.1 MB (184105437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07aac8af4758b3567aa605b2523365bfc768c3d1ecb68e0a85dfb5b38ae4e642`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Mar 2025 16:03:48 GMT
ARG RELEASE
# Thu, 27 Mar 2025 16:03:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Mar 2025 16:03:48 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Mar 2025 16:03:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 16:03:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='78832cb5ea4074f2215cde0d01d6192d09c87636fc24b36647aea61fb23b8272';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        arm64)          ESUM='a598260e340028d9b2383c23df16aa286769a661bd3bf28a52e8c1a5774b1110';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64el)          ESUM='770e7e506d5ea3baf6c4c9004a82648e29508a1c731d8425acded34906e91b09';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        riscv64)          ESUM='4e953ec63e141b667e02f7179304c6553cbd13ba94b60dcadd8e45c7f309c89d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_riscv64_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='6ff3126ae0a7cff3a25b7590adc441550666750515fd7d6e2d2706b5fc9a1f6f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["jshell"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d96a62a04cac1b60dc9c80e9fd395e0b7bde4bfd3c5c41463b42c3e4d96ffef`  
		Last Modified: Tue, 03 Jun 2025 15:06:33 GMT  
		Size: 22.0 MB (22049321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef8bb743d558d8b530ad7bc244aebe2edc2e4e269ce09da1ae43790cd1fa9d1`  
		Last Modified: Tue, 03 Jun 2025 15:06:38 GMT  
		Size: 89.9 MB (89927462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f75d3ded3222971624e3463873a2cd1ecf7af77c5d1ffab4653807cb0d5a82b`  
		Last Modified: Tue, 03 Jun 2025 15:06:34 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad6853a452a75f471c2b21c73091119874a251f9a9705773e1af3c107361bcf`  
		Last Modified: Wed, 04 Jun 2025 02:07:38 GMT  
		Size: 28.6 MB (28629661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1241d6637cb94241671e345d2586626ebec948e370a162100c793e3afc23c83e`  
		Last Modified: Wed, 04 Jun 2025 02:07:31 GMT  
		Size: 9.2 MB (9170428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5dd01f2e7f86daa9de6af6c040303ee649ebfa80167a43fbea88fc98a3e3eb0`  
		Last Modified: Wed, 04 Jun 2025 02:07:29 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20602f656971f9d116fc8a9a5e21270e438dd8a1f2905cead50a453cc1d2a81`  
		Last Modified: Wed, 04 Jun 2025 02:07:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-24-noble` - unknown; unknown

```console
$ docker pull maven@sha256:931ca815fae573da65bb76ce2af7b0b5bd126c73b4837c074fc7f87a115d8c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b88c5b323b5f7f87fe2faeed1528fceb83e725acc6480c3c8320a28879c17bb`

```dockerfile
```

-	Layers:
	-	`sha256:787682fd9c9b652d555ed6ed33dc7542fe6a190da39afb6f277099b4e1932d53`  
		Last Modified: Tue, 03 Jun 2025 14:28:40 GMT  
		Size: 4.9 MB (4886938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e07e4cb3c17569485e06de65e97161945c323d8e364161bcd68ebe1a97079a1`  
		Last Modified: Tue, 03 Jun 2025 14:28:40 GMT  
		Size: 19.7 KB (19710 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-24-noble` - linux; riscv64

```console
$ docker pull maven@sha256:93e6a6139aae03adb391fb7254d012e198c2e5bb5989631c5500df00c252cac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178880606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac44887612535f81e1d38c366a255a3acc728372b05900d4e56de86c3cafd04`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Mar 2025 16:03:48 GMT
ARG RELEASE
# Thu, 27 Mar 2025 16:03:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Mar 2025 16:03:48 GMT
ADD file:f68263cf915d0f5d61ab9caa83da511fc9ef55d936429cb8fb542906fc38a8fa in / 
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Mar 2025 16:03:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 16:03:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='78832cb5ea4074f2215cde0d01d6192d09c87636fc24b36647aea61fb23b8272';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        arm64)          ESUM='a598260e340028d9b2383c23df16aa286769a661bd3bf28a52e8c1a5774b1110';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64el)          ESUM='770e7e506d5ea3baf6c4c9004a82648e29508a1c731d8425acded34906e91b09';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        riscv64)          ESUM='4e953ec63e141b667e02f7179304c6553cbd13ba94b60dcadd8e45c7f309c89d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_riscv64_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='6ff3126ae0a7cff3a25b7590adc441550666750515fd7d6e2d2706b5fc9a1f6f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["jshell"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4ac2db62b9f8401057b5c4ebae4764d70573ec599f6a1f0b5dc2c4491ed8e39a`  
		Last Modified: Tue, 03 Jun 2025 13:37:40 GMT  
		Size: 30.9 MB (30947484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550d3961a726eda63da83020f4999748bd1de470291c9b291145222a5ea3b68f`  
		Last Modified: Tue, 03 Jun 2025 15:10:00 GMT  
		Size: 18.4 MB (18378719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5895bbe34cacddce2ce3645d6eda857a90dcf0847b5b8818281c09e70298063d`  
		Last Modified: Tue, 03 Jun 2025 15:10:04 GMT  
		Size: 87.6 MB (87627398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d998af04ec9a46346bdd5349dfa3d63a2d669dea6e6ee41f1ff8256d2a089779`  
		Last Modified: Tue, 03 Jun 2025 15:10:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35750cbdadcb97b9cd07293a00c623955a28c15bcbfdcd5e99a51ce506fc0342`  
		Last Modified: Tue, 03 Jun 2025 14:08:12 GMT  
		Size: 32.8 MB (32753234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329a375fc276a3082d34e03ae554920f37d999c33beaa2432a92127051fec4e9`  
		Last Modified: Tue, 03 Jun 2025 14:08:08 GMT  
		Size: 9.2 MB (9170420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bba41fa82a1e4a1a95270bc0fd73b67149a4ddc0dffb4636d300e4f14c76f8`  
		Last Modified: Tue, 03 Jun 2025 14:08:08 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0481ad206aff2be3f024d00fb0b240b822c35b13ec7c45cbd907c1abe29844`  
		Last Modified: Tue, 03 Jun 2025 14:08:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-24-noble` - unknown; unknown

```console
$ docker pull maven@sha256:72443fe9e80e6ef3c03fa10b48ae3542c18708d8c17343634ca7e4fd1ff4c0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4958415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8be0d726c4def28d5b9662aa923c8fa128caf407c835fcd29d50d046ac3c5ec`

```dockerfile
```

-	Layers:
	-	`sha256:518ac2f7181aa8b6ee118d96fd93f63473be70432a19c8d88684cdedb068a017`  
		Last Modified: Tue, 03 Jun 2025 17:29:54 GMT  
		Size: 4.9 MB (4938706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2fee5a67e0bb2d024e7a159626dba129e3b9538d4846f4d7a4caf4c96f64c75`  
		Last Modified: Tue, 03 Jun 2025 17:29:55 GMT  
		Size: 19.7 KB (19709 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-24-noble` - linux; s390x

```console
$ docker pull maven@sha256:0e11865e5962f13737a2c3c4d76d0bbd117545a41f04b43203a6efc0c41b9e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170108703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a83588f960ce22e19046bc9d55581e53dc2a707c35cdb835d14f8a206e671c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Mar 2025 16:03:48 GMT
ARG RELEASE
# Thu, 27 Mar 2025 16:03:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Mar 2025 16:03:48 GMT
ADD file:b6b8557b3fef6c06eb943ce735f649cf7033ab3925e70e6b43901f1f29b4d5e9 in / 
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Mar 2025 16:03:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 16:03:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='78832cb5ea4074f2215cde0d01d6192d09c87636fc24b36647aea61fb23b8272';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_linux_hotspot_24.0.1_9.tar.gz';          ;;        arm64)          ESUM='a598260e340028d9b2383c23df16aa286769a661bd3bf28a52e8c1a5774b1110';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.1_9.tar.gz';          ;;        ppc64el)          ESUM='770e7e506d5ea3baf6c4c9004a82648e29508a1c731d8425acded34906e91b09';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.1_9.tar.gz';          ;;        riscv64)          ESUM='4e953ec63e141b667e02f7179304c6553cbd13ba94b60dcadd8e45c7f309c89d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_riscv64_linux_hotspot_24.0.1_9.tar.gz';          ;;        s390x)          ESUM='6ff3126ae0a7cff3a25b7590adc441550666750515fd7d6e2d2706b5fc9a1f6f';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["jshell"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7fa55ab2f467363da0197dee4a8e5af9e7ba7ef5686c6f0951bc509c387b765c`  
		Last Modified: Tue, 03 Jun 2025 13:31:43 GMT  
		Size: 29.9 MB (29930056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93092b77a210c93915aff9678274b8fbed303b75811f0cfb2b717e46a5f5d7e9`  
		Last Modified: Tue, 03 Jun 2025 15:15:37 GMT  
		Size: 20.4 MB (20415241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a192f5a64353f106fc6d19dd6247d14757b2e84cd9105a8c561f14236d80631`  
		Last Modified: Tue, 03 Jun 2025 15:15:41 GMT  
		Size: 85.2 MB (85217762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934af4e8efed76e8283a6b1f7a42bd01302bc39650712371de999ae3834b9e4c`  
		Last Modified: Tue, 03 Jun 2025 15:15:36 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea31e9997d8838b613bfdf607559beed9f9b3e7f2c2e9a199dc1774934930f1`  
		Last Modified: Wed, 04 Jun 2025 02:07:17 GMT  
		Size: 25.4 MB (25371865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9fd1de124e6bee509632b4e50b644cf76450b0179b814cde32a9758caa45c7`  
		Last Modified: Wed, 04 Jun 2025 02:07:15 GMT  
		Size: 9.2 MB (9170430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542212a6cce4b9ac9aee99be129ca17ef90fab3bc4ce73552d1e403559042cd`  
		Last Modified: Wed, 04 Jun 2025 02:07:13 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dd93e5500cf9e7bc674b3989fec5b62251022e5005be69feaa5ca26edd0fd2`  
		Last Modified: Wed, 04 Jun 2025 02:07:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-24-noble` - unknown; unknown

```console
$ docker pull maven@sha256:31e481444cab39fe937b87b300164714cd13bdc440dc07233d6eece843ef90d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4802699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301d8059c18d946c8f1af82de0d0dedeff8db09065066f5666e3f547675fb7cc`

```dockerfile
```

-	Layers:
	-	`sha256:b55253721a95f720d373e3d0076e3fa4e527142e0391fbf6bbae89442beb821f`  
		Last Modified: Tue, 03 Jun 2025 14:28:51 GMT  
		Size: 4.8 MB (4783039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d5b459322cc898ecb37b74612ca4dd73f138dbc1d51c926fbe0b595ba141b8c`  
		Last Modified: Tue, 03 Jun 2025 14:28:52 GMT  
		Size: 19.7 KB (19660 bytes)  
		MIME: application/vnd.in-toto+json
