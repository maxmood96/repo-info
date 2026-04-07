## `maven:3-eclipse-temurin-25`

```console
$ docker pull maven@sha256:f0fe4f014a44e1cf8502950aa2867ae8fabba13d4ffac085642279a8b3ceb32d
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

### `maven:3-eclipse-temurin-25` - linux; amd64

```console
$ docker pull maven@sha256:38cbb091863e012149cc96a8656bfc62ff0d972ec4af484e46ddf7bc5a77bac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173421546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cfb9625636d97e4cda88b124314abee7f162e101ee8c2790fe460a1f74e1dc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:52:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:52:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:52:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:52:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:52:16 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 07 Apr 2026 01:52:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 01:52:37 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:52:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:52:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 01:52:37 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 05:06:31 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:06:31 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:06:31 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:06:31 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:06:31 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:06:31 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:06:31 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:06:31 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:06:31 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:06:31 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:06:31 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:06:31 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:06:31 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:06:31 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:06:31 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d7a89f363d00fbdb4eeb3725625f77439f3317bf972e4c8d4e74325647ecb6`  
		Last Modified: Tue, 07 Apr 2026 01:52:54 GMT  
		Size: 17.5 MB (17462707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58dcb4ab26520b9c733623bef23b51e9fbf6845834f6d3fad23e922d5c316b4`  
		Last Modified: Tue, 07 Apr 2026 01:52:57 GMT  
		Size: 92.4 MB (92388861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc49b9bffc8e184c7b52408c24aa9b27a669c1699ff5339445f20666c11d334`  
		Last Modified: Tue, 07 Apr 2026 01:52:54 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131bd6f641c5c84f25f7f1dee86f581fa79177936defdaf64dc7d2687b1db4ec`  
		Last Modified: Tue, 07 Apr 2026 05:06:44 GMT  
		Size: 24.5 MB (24521973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bce937481633affee40577461c341381b4284d727f2dd0f3cd94216d542676`  
		Last Modified: Tue, 07 Apr 2026 05:06:44 GMT  
		Size: 9.3 MB (9311196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19daefeb9d56b214f3dd61e0d52a5f2030562dc694be8d4ba9e7bce2c913f31`  
		Last Modified: Tue, 07 Apr 2026 05:06:44 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e4261355ba507c76af6a9ed79e778552a0114dd1b669b7e6084d0c807707cc`  
		Last Modified: Tue, 07 Apr 2026 05:06:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-25` - unknown; unknown

```console
$ docker pull maven@sha256:2f81bb84be1a32156644d30629a1e37556233e534521f31549d420e1360117f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4904816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d76665d5991e34d1ae5d8edbd1ac472d60d9b5cddd8cf549506048e1f26e37b`

```dockerfile
```

-	Layers:
	-	`sha256:d592220fa04156744ad2987ec3539500555e6765911e81b4a5afad3753b88936`  
		Last Modified: Tue, 07 Apr 2026 05:06:43 GMT  
		Size: 4.9 MB (4881690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6586184c78a9107abdeaf8133d33b1af934f37d6190f23a4a5d5ea5512cc8474`  
		Last Modified: Tue, 07 Apr 2026 05:06:43 GMT  
		Size: 23.1 KB (23126 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-25` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1ebf67f8c992a28828317a618039a0e552aa24d28ecc61fe35d94a014d0c05d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172879515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d202498062d725c4ed9d5bcb0f04f09f2bd63e183fed22abb12a44d90968ff`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:55:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:55:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:55:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:55:30 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 07 Apr 2026 01:55:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 01:55:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:55:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:55:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 01:55:54 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 05:12:17 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:12:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:12:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:12:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:12:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:12:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:12:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:12:17 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:12:17 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:12:17 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:12:17 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:12:17 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:12:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:12:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:12:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3015356b23ea1b0133580e617372417cc6db3dabdf6e97b8ce4e0c591947552`  
		Last Modified: Tue, 07 Apr 2026 01:56:10 GMT  
		Size: 18.7 MB (18654733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e4754d54bd61e52c7042dc67b848766f81f8e0b5fcc71ae9885823b64baca6`  
		Last Modified: Tue, 07 Apr 2026 01:56:12 GMT  
		Size: 91.4 MB (91424717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f199c35f5162fea3c8f07eef1e388cab02e2e3f619c9b2842b8bcd77a768e1e`  
		Last Modified: Tue, 07 Apr 2026 01:55:39 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a254b0a98a33b4d573c267528837916b78158990b8f9b68aed74ee0e14369dc`  
		Last Modified: Tue, 07 Apr 2026 05:12:31 GMT  
		Size: 24.6 MB (24611457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6392e5a79611f42bc872831cebe3376c4e658a57f0c7b8cf9323049c04847a2d`  
		Last Modified: Tue, 07 Apr 2026 05:12:31 GMT  
		Size: 9.3 MB (9311184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa07c7f27ac50667770bcdc393a7e8f611c6041c34b61baa01e0a5b9bc72b4b5`  
		Last Modified: Tue, 07 Apr 2026 05:12:30 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bc3e605cb27053d29c1a8c80fb5bc65cf199be6d37ca4c5f229eb3fe41654e`  
		Last Modified: Tue, 07 Apr 2026 05:12:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-25` - unknown; unknown

```console
$ docker pull maven@sha256:f5b7d567fcd6d14f19271e4c2fdbbc83f35471bacb6bea292257cc8d2e4f3eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5042767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f1d1b8275bf47f0f825ad6bcb3f64c0a1cf5c0e09d36289d4ee9376da37375`

```dockerfile
```

-	Layers:
	-	`sha256:47f655d757384bccea8929603382cea5ea26e533a5d69facfb8de26c80589d21`  
		Last Modified: Tue, 07 Apr 2026 05:12:30 GMT  
		Size: 5.0 MB (5019376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3313a33bb5fe939f191cb046eec3e375dcebd53d52a2dc4ff79dbbedaa90b42e`  
		Last Modified: Tue, 07 Apr 2026 05:12:30 GMT  
		Size: 23.4 KB (23391 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-25` - linux; ppc64le

```console
$ docker pull maven@sha256:815fca72234e435d75fa5d9a6322ab1124be71167e7d854d7060f3ee0625c918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181756637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4288fb2c541c4c32b92dfee15307263a7a398877bd98048479f60420b84a594`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 08:38:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 08:38:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 08:38:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 08:38:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 08:38:03 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Mar 2026 08:38:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 08:38:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 08:38:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 08:38:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 08:38:53 GMT
CMD ["jshell"]
# Tue, 17 Mar 2026 22:04:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 22:04:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 22:04:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 22:04:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 22:04:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 22:04:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 22:04:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 22:04:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 22:04:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 22:04:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 22:04:08 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 22:04:08 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 22:04:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 22:04:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 22:04:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719799e3fd3fced1bf5442d22aed7fb7582f8aef125453efff5308862d936136`  
		Last Modified: Tue, 17 Mar 2026 08:39:28 GMT  
		Size: 17.3 MB (17328483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fd462ea1b064dfa4c0f2866d0b9c265dbb70fc5dc940ba5349e7e89dca9544`  
		Last Modified: Tue, 17 Mar 2026 08:39:30 GMT  
		Size: 91.8 MB (91756951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7f07a919432b86262243e8578a37d80592647d53ec1896888579931c683559`  
		Last Modified: Tue, 17 Mar 2026 08:39:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fef80c36e9cbb75c3b2c6ba2b75765cbc0db3023b6ed9a68f7b9320a72b3f9`  
		Last Modified: Tue, 17 Mar 2026 22:04:36 GMT  
		Size: 29.0 MB (29046617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0693730ba340f3107c17c829dbd5535a389697d7ab1501ce71ee61bcdaee3d8e`  
		Last Modified: Tue, 17 Mar 2026 22:04:36 GMT  
		Size: 9.3 MB (9311182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25c69f97cea47b97b723c78e60ff85046a76859b6bb86dfe0ffe6a1d175559f`  
		Last Modified: Tue, 17 Mar 2026 22:04:35 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b7cdc791714060548a343c91c429db1e9370d4aef80a58f9024784d9fcfc9`  
		Last Modified: Tue, 17 Mar 2026 22:04:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-25` - unknown; unknown

```console
$ docker pull maven@sha256:b9a55afa17d823f542e475c5f4ffdea1456f0716ab68efb770082036aef11abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefac40338e75ac9bee86701ec7ae94ff98f705207e3000bac88ac980c8ab086`

```dockerfile
```

-	Layers:
	-	`sha256:2c17092fce5c2a3323d6474b6fab18a636e40fcb1f44dbfa546c9da59df41ed4`  
		Last Modified: Tue, 17 Mar 2026 22:04:36 GMT  
		Size: 4.9 MB (4915577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:089b76d2b6371364e9ad68bb8607b9fa13ae014c4ba0741b5562c91e1c4fd1c0`  
		Last Modified: Tue, 17 Mar 2026 22:04:35 GMT  
		Size: 23.2 KB (23242 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-25` - linux; riscv64

```console
$ docker pull maven@sha256:b5436a7f0e3d5cd714079dd1fb5f570942617f3ec109662973a53b04fc2a0198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.2 MB (178163547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70856a8bb1b727d50c2f20b4002a607c332992ec38b1626fae8d0f722f8bdfbb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Feb 2026 17:42:34 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:42:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:42:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:42:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:43:25 GMT
ADD file:1243b7db425cac690d91f87ad37c1beec0d95da6b3942dc8084039fe1cc2baf4 in / 
# Mon, 23 Feb 2026 17:43:30 GMT
CMD ["/bin/bash"]
# Sat, 21 Mar 2026 04:40:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 21 Mar 2026 04:40:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Mar 2026 04:40:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 21 Mar 2026 04:40:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Mar 2026 04:40:25 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Sat, 21 Mar 2026 04:42:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 21 Mar 2026 04:43:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 21 Mar 2026 04:43:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 21 Mar 2026 04:43:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 21 Mar 2026 04:43:08 GMT
CMD ["jshell"]
# Sun, 22 Mar 2026 21:12:53 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 22 Mar 2026 21:12:54 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Mar 2026 21:12:54 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Mar 2026 21:12:54 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Mar 2026 21:12:54 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Mar 2026 21:12:54 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Mar 2026 21:12:54 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Mar 2026 21:12:54 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Mar 2026 21:12:54 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Mar 2026 21:12:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Mar 2026 21:12:55 GMT
ARG MAVEN_VERSION=3.9.14
# Sun, 22 Mar 2026 21:12:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Mar 2026 21:12:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Mar 2026 21:12:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Mar 2026 21:12:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:866473980fd7aa6ac5a8a995315a35248ab945008a1938bd15f65082df53b2d3`  
		Last Modified: Mon, 23 Feb 2026 17:51:46 GMT  
		Size: 31.0 MB (30960145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a39ea40737df0869a665cb1cd59261c3e337da5cacd4b5bf17fab5765e174b`  
		Last Modified: Sat, 21 Mar 2026 04:46:34 GMT  
		Size: 13.8 MB (13849902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61a4c41ee7ac84fc9d708e3b438f588cbe9de5cbf14f708499a9366509dbf6`  
		Last Modified: Sat, 21 Mar 2026 04:46:45 GMT  
		Size: 90.9 MB (90910647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595de38fa3ddd618163afb8e9f42eb19f6a4c7a8ce9d4f89f4b6109fbd005c85`  
		Last Modified: Sat, 21 Mar 2026 04:46:30 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdeb13c552a7f8c993f04088707f50f77973673e209844abda3b01ff3eb90d3`  
		Last Modified: Sun, 22 Mar 2026 21:15:51 GMT  
		Size: 33.1 MB (33128299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132240d227c85a6d946014eddf321ea3f660571b7c0c664e23d07ff7fb397afa`  
		Last Modified: Sun, 22 Mar 2026 21:15:48 GMT  
		Size: 9.3 MB (9311195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce09ac09bdbd97177cb62db5ac2b3394bd417dd8a87572c2f1891c610d654c8`  
		Last Modified: Sun, 22 Mar 2026 21:15:45 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdd23537833d8f80c0ed2c9d9d8c3020a90589e38a08d9e903460416e400f3b`  
		Last Modified: Sun, 22 Mar 2026 21:15:45 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-25` - unknown; unknown

```console
$ docker pull maven@sha256:f23ad5e80f41b24d95da7c69db6143664aa13218d772c18139ab4dac2c1a4b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4990612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71abc378ccbc1b080376f11bf7281e87fd5d761a20d2ed10ae00c0a44a0320cb`

```dockerfile
```

-	Layers:
	-	`sha256:6ea5327da72ce5d847f01c918910f932d15d108d5a608d50f6987f0e497a0e99`  
		Last Modified: Sun, 22 Mar 2026 21:15:46 GMT  
		Size: 5.0 MB (4967371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c99ccb7624f2feb4c51acd225192acbdc2b6ebe5e5d0faddc4c82f9b969532d1`  
		Last Modified: Sun, 22 Mar 2026 21:15:45 GMT  
		Size: 23.2 KB (23241 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-25` - linux; s390x

```console
$ docker pull maven@sha256:b959786a7c4b6706319cd8d2187546eba6ba2acb6112854d2b865cd2aded6810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169643315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43068607c7727e2079e3d51f75cf5bddb741c1dd925eb6bb8c323973c0abe103`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 03 Apr 2026 15:12:46 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:12:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:12:46 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:12:48 GMT
ADD file:31d45a66208318e1066130bac8975f44dea6e7e93cbfb2d29b0888e686bb10d5 in / 
# Fri, 03 Apr 2026 15:12:48 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 03:10:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:10:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:10:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 03:10:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:10:25 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 07 Apr 2026 03:10:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 03:10:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 03:10:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:10:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:10:39 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 09:45:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:45:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 09:45:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 09:45:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 09:45:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 09:45:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 09:45:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 09:45:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 09:45:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 09:45:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 09:45:07 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 09:45:07 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 09:45:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 09:45:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 09:45:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:248eeda3355e38b5891b7f407370b5faea53785cd947438684bf34a757d0f83c`  
		Last Modified: Fri, 03 Apr 2026 15:57:06 GMT  
		Size: 29.9 MB (29911843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4faede105445d3bd795bc7d8f0df624f6136d385a408c8b711fa2f889d29b74`  
		Last Modified: Tue, 07 Apr 2026 03:11:03 GMT  
		Size: 16.3 MB (16310110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420605b37028e8129b0298a6b1ecc9d87364f35bd713709d378c9535aa90ee7`  
		Last Modified: Tue, 07 Apr 2026 03:11:06 GMT  
		Size: 88.4 MB (88369843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fbaf8d78a65877be7baa1bc40c97993c92212d890166ebb6fd149416207a53`  
		Last Modified: Tue, 07 Apr 2026 03:11:03 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9323e71f92e39028bc33c0763cb8b48adfea0ed40ed5c07caeff6182357bd5`  
		Last Modified: Tue, 07 Apr 2026 09:45:28 GMT  
		Size: 25.7 MB (25736980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156642b2115321c763d3c8eb98a4018867a247e57bdc1d8ee5e18c2596fd5279`  
		Last Modified: Tue, 07 Apr 2026 09:45:28 GMT  
		Size: 9.3 MB (9311188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f6e86b307fb850331b157520af112083f15a5245d14440a113fcf3d5d05c04`  
		Last Modified: Tue, 07 Apr 2026 09:45:27 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24318c74228ba4a71cf89b2be41cded7267420e9f442e424527d9332d55603da`  
		Last Modified: Tue, 07 Apr 2026 09:45:27 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-25` - unknown; unknown

```console
$ docker pull maven@sha256:c88edb45ff0c63e011e353cb468f3864d6a93d1ec95eda2680dc2eaae1c3fc40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4834782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcdcc678b6128dd19067f451cb1bd86d16e108fc66c0aae68733251782fc418`

```dockerfile
```

-	Layers:
	-	`sha256:d4d88b4570e6884b721bcc16796aae097b2abf89da97700fbcb1148c22d8cd32`  
		Last Modified: Tue, 07 Apr 2026 09:45:28 GMT  
		Size: 4.8 MB (4811656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7459fb2791d6565b0762278245f5fbc7e8f63e5982c1211e3f8d83af46804cbb`  
		Last Modified: Tue, 07 Apr 2026 09:45:28 GMT  
		Size: 23.1 KB (23126 bytes)  
		MIME: application/vnd.in-toto+json
