## `maven:3-eclipse-temurin-17`

```console
$ docker pull maven@sha256:2a2deba22e48200c86238d3db4228d7664578ded9790e2d4a9e2d91961f74b19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `maven:3-eclipse-temurin-17` - linux; amd64

```console
$ docker pull maven@sha256:2fe085bff607792ba5e8c51482db189f9fd478002375b97b9cae01c6cd677b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229685601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43763e59a856fdd58405d31d2bd0db334d4884acb38c18f6c781915a852e09d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='d024c100eba4709970716ddcac757ba5e3122a8ff9c6f539ff8bac5b47f51f3a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:32b824d45c6101d459f5d3c13ab8658b6f79713f3bd64e363d3f6bc98faf5d6d`  
		Last Modified: Tue, 27 Aug 2024 21:43:22 GMT  
		Size: 30.6 MB (30611547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe18bb7e114fb54a6ec75041e560d3ffcf2c4af97d06ad9e563c23182f1ff1ca`  
		Last Modified: Tue, 17 Sep 2024 01:09:58 GMT  
		Size: 22.2 MB (22162716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2688dd92e8c9cf8998d81f94b05b41b3677ba45bad9887b5408d2f236ab103`  
		Last Modified: Tue, 17 Sep 2024 01:10:07 GMT  
		Size: 145.2 MB (145177475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c472fdd4039772d12c422fd54607081ae8b58ea90fb97b2d26953be80c6bbdde`  
		Last Modified: Tue, 17 Sep 2024 01:09:55 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579ad2df89fa965efee91e5274d0a42d4b04ac279bd5ea4ff19586a0915e46dc`  
		Last Modified: Tue, 17 Sep 2024 01:09:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a616f74f00b1db2d6b2f8317bf92336bc4b2f967cab22b25071d9ae98fc2541c`  
		Last Modified: Fri, 27 Sep 2024 19:02:58 GMT  
		Size: 22.6 MB (22560012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0689f22ba7686fcc64636c81081a1e930d72deae908899aff0bddd11383887`  
		Last Modified: Fri, 27 Sep 2024 19:02:57 GMT  
		Size: 9.2 MB (9170209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd79ea2001acc18d5adc07392eab96ac7a653083dfdc9ddc7d9b9d74790fbd6b`  
		Last Modified: Fri, 27 Sep 2024 19:02:57 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03286df050970282e7144a1d26a3be901bbe837024caff22be292b4f1dc568e4`  
		Last Modified: Fri, 27 Sep 2024 19:02:57 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8260a1b8a087f5bd7db4d5d8a485a2931245fe30378eb62249a74a9c01a51fb4`  
		Last Modified: Fri, 27 Sep 2024 19:02:58 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:7f01512c84d8b40978a4c11cf0ae5e5eead34ea34ad838646c0916d099b42aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4754686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73cb8f688095ac5aa2da4a1f88ca9f109c533e843ecc5c81b044513c9208dfcb`

```dockerfile
```

-	Layers:
	-	`sha256:0986b29b2368e970b19079e27c888f277c0f6d2a3696e82faef5cefef72ba3f4`  
		Last Modified: Fri, 27 Sep 2024 19:02:57 GMT  
		Size: 4.7 MB (4730263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30940ab7c12b22331f70f09c01702e2ce4599ac630735f20f8937a2ba81532e`  
		Last Modified: Fri, 27 Sep 2024 19:02:57 GMT  
		Size: 24.4 KB (24423 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; arm variant v7

```console
$ docker pull maven@sha256:7844bc840912d6e8e33b8972f29e64fe34d63273ffe53a3d8b6c69de0fdedd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226837093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7310b6a8f87666d024c4c21a75a3af2bf49ec6b08761e9c7f367049387677287`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:0efc83f80e5e3a9125a702063e487f836d2e0ff9a88f4d0330897d15e445d415 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='d024c100eba4709970716ddcac757ba5e3122a8ff9c6f539ff8bac5b47f51f3a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3662f20bd36fe3ab5035e3d6d75d4a5a27e32e29abe306052959223600a1522c`  
		Last Modified: Tue, 17 Sep 2024 01:24:15 GMT  
		Size: 27.7 MB (27731977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b112d5cbaef10444c05c1d1de96b1ecedc18878c4707539ddaab77fd0d653bb`  
		Last Modified: Tue, 17 Sep 2024 01:26:34 GMT  
		Size: 20.0 MB (19993500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f8ff75c685a91bc9d4307938f1e3906d3bdf47da9c30c443c5f303bc057be`  
		Last Modified: Tue, 17 Sep 2024 01:26:44 GMT  
		Size: 142.6 MB (142644251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1f6cd58fec194a2fb4ba45dc5127213914e1f1d6908b96f6b2089c3b2b84ea`  
		Last Modified: Tue, 17 Sep 2024 01:26:31 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e87a847c272f46dafbc231ac4ba5b2c069ccc701e02a55a7a4afcd47ee322e`  
		Last Modified: Tue, 17 Sep 2024 01:26:31 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a4c440a934ca82854df44cc3298d45f1832ea11a43d5b4d2b882cbec423747`  
		Last Modified: Tue, 17 Sep 2024 03:03:56 GMT  
		Size: 27.3 MB (27293509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0504113da469bac019713c410a92434095a06e6b66841ba4712dbec302806c39`  
		Last Modified: Sat, 28 Sep 2024 06:41:47 GMT  
		Size: 9.2 MB (9170207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06afebf840a2b16fa12065ce879ffca6f7db5e11de42b5dbde1be2f23f1371b`  
		Last Modified: Sat, 28 Sep 2024 06:41:46 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb898f30f6ee2a8ea38b4b590fffe5c8118d50daa8b86030f99f5d1be7c08825`  
		Last Modified: Sat, 28 Sep 2024 06:41:46 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ce9afd222468e1fad69d0bb0efacd459abc3c435989f2c7b4384ccd2c46a56`  
		Last Modified: Sat, 28 Sep 2024 06:41:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:44120a363a076a112f3c573e2a09ca38aff7f69fc2ad3416000c3e692a97d9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4693533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d8fc62a16129dea0e06d5aa425dca82f8c6290142c5b651ebc3440e3b31456`

```dockerfile
```

-	Layers:
	-	`sha256:4702a51ce51a4a5b4065e8eea6db2144dc9c38a9cbb8e143dbe6c57d590993b9`  
		Last Modified: Sat, 28 Sep 2024 06:41:47 GMT  
		Size: 4.7 MB (4668983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:841283cddc1c9d648c7f4552265db1a77f1b5e7f3971adc134986d493c41fffd`  
		Last Modified: Sat, 28 Sep 2024 06:41:46 GMT  
		Size: 24.6 KB (24550 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:65cd75375b2d59e672447199940d14f7fb517b189f2091ff46e31c6c8bb8e34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228908651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d9242d08663c01c653d63fdd948e30c4846460b2ba32b17cb76bce8754a692`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='d024c100eba4709970716ddcac757ba5e3122a8ff9c6f539ff8bac5b47f51f3a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8a9c853c85e5a53a79f6bc6965cf01799f75bd947d761fc492da5738058f87a2`  
		Last Modified: Sat, 31 Aug 2024 18:28:27 GMT  
		Size: 30.0 MB (29953205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3c94b28576805baa094e0b9e9de3f1e9965bd25111a8c5d9f608066dc48ed6`  
		Last Modified: Tue, 17 Sep 2024 01:39:44 GMT  
		Size: 23.2 MB (23180459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a135d797bc5cfc05c0685a21c8c9da1c67471caed8887e4fe7ecc0de2b48d2`  
		Last Modified: Tue, 17 Sep 2024 01:39:50 GMT  
		Size: 144.0 MB (143967365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c45acbfb024d0258c966d8e6ed0c0f500dd95e5d2ee5964b25ad9f1bd72787`  
		Last Modified: Tue, 17 Sep 2024 01:39:41 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5932aa1ab1d213c23aa48a1e2fd3ca604829f1a93d035d52ba6e9507295d2a9d`  
		Last Modified: Tue, 17 Sep 2024 01:39:41 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3caea1edfe7ba46d3812b26d1a1b8f2d81eda6ff89a6b8b9c58adca07027ee2e`  
		Last Modified: Tue, 17 Sep 2024 09:32:23 GMT  
		Size: 22.6 MB (22633760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495c2601868e33592ace76a19cb4ba482627bd1e9025e9aa6a6cb749be75c623`  
		Last Modified: Sat, 28 Sep 2024 02:17:06 GMT  
		Size: 9.2 MB (9170215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d5a398c9186a8c24d2f9af132a0aaefec9105fbe6271033a9d2ae9ea6a9662`  
		Last Modified: Sat, 28 Sep 2024 02:17:06 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73414c8bee34d716ad2ce3e8adf7df0365101fa6e2d20cebc511dc8a06ae8566`  
		Last Modified: Sat, 28 Sep 2024 02:17:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49cce17ca5f9264c5221b9559cb967336a6e059d0127f666825eb70505b324f`  
		Last Modified: Sat, 28 Sep 2024 02:17:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:2c2f48e0a8b104abfc95a9d53476d80a8171680bf684fed791ff094cd56aea47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4892709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc72a175c9d46210d39c27231a8124f20baebfd32c5ea374f69773f81b713fc`

```dockerfile
```

-	Layers:
	-	`sha256:4fa29220fa6e373fc227ebb59232d633791d5784a3a3c17e5971e61685099b13`  
		Last Modified: Sat, 28 Sep 2024 02:17:06 GMT  
		Size: 4.9 MB (4867987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51911d774e204b50d2734a89bdef5d311bd6bac114f5b374faa196b1dbaa6dd`  
		Last Modified: Sat, 28 Sep 2024 02:17:05 GMT  
		Size: 24.7 KB (24722 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; ppc64le

```console
$ docker pull maven@sha256:cef5d041ea9d0a2ab6db183845d48b59f2f65a23b307cb4e042e0f6d2273a831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.1 MB (239116957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4e2f1a6c14af605c42f0fb561cf4803bff93c5af5ac12f619797104f201142`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='d024c100eba4709970716ddcac757ba5e3122a8ff9c6f539ff8bac5b47f51f3a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5d340ed979f83f097fa56590781e2ea4e2d63a50fc75b5e5bc616f845d2e2f80`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 35.5 MB (35518179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b70fc22b4a6f26473f15d50e289fb9531e2a65be723c3c20b99750368667d6`  
		Last Modified: Tue, 17 Sep 2024 01:08:42 GMT  
		Size: 22.8 MB (22827512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cc693d7a30441928617ed624ec4437ce2bea558ed84dc579a477f0c8c5cb52`  
		Last Modified: Tue, 17 Sep 2024 01:08:51 GMT  
		Size: 144.9 MB (144864119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e98dd24fc97331ede558393ab45e6514e52ed9323ab0e3c01eea9a8b81ee37b`  
		Last Modified: Tue, 17 Sep 2024 01:08:37 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4d3c5f25203e45afb2cfd6466f9ba616dc09d94e3c876ac13bcb6205315495`  
		Last Modified: Tue, 17 Sep 2024 01:08:37 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649798c37559ac1b78999473d1c03019730f05ac6e98cb3e4fcbf6d1f67f7e21`  
		Last Modified: Tue, 17 Sep 2024 09:22:04 GMT  
		Size: 26.7 MB (26733277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a4fe61b1762e2d3e9ec9fd4090425309eb72c8d8f6ec71d515cfc7909b240d`  
		Last Modified: Sat, 28 Sep 2024 05:43:25 GMT  
		Size: 9.2 MB (9170223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9995f13478f704ba79613d28d0984500a253329694c61899e892ea9d585208de`  
		Last Modified: Sat, 28 Sep 2024 05:43:25 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74faf9a3e882ac9cdcb0283f9f4619fdd92d166486bbd6e90778db1973b550b9`  
		Last Modified: Sat, 28 Sep 2024 05:43:25 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb26d56ce9ba033f5cd5b1358359ae56259a07d8e0444735369a7ed0bb409a26`  
		Last Modified: Sat, 28 Sep 2024 05:43:25 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:79defa0158682ff177ce7196ed4feab7761012f775fcbe6c39b463c3d0e3204e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4805729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f13beaf1d4b1031ffef6c5ffbf74e0397646f61c89a7ddadb9bbd0ec73cf5b5`

```dockerfile
```

-	Layers:
	-	`sha256:83564b54ae9b7693ec52ec323e4c33ffa2412fa7aefa011c552e89ed78c09297`  
		Last Modified: Sat, 28 Sep 2024 05:43:25 GMT  
		Size: 4.8 MB (4781264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9f164bb4d1f50f0df358959af6faf9e7e2af36b38ee3ae734e0592ba83084cf`  
		Last Modified: Sat, 28 Sep 2024 05:43:24 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17` - linux; s390x

```console
$ docker pull maven@sha256:1c522d108a5b99fde74cba83b819db801cb02ec85d5fd760395429f5a9b81e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 MB (216804390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae2bfd8fa873c2fc97e87b6db4703ad86649095e66e547972ea1ed61d21fd66`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:b59d96a664939a669058854c36d39c65ef534cfde0cbeb2b692f1dc285372fe9 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='d024c100eba4709970716ddcac757ba5e3122a8ff9c6f539ff8bac5b47f51f3a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2bcb95ea29b5590c02dc2f6a3ee8fd99cf5f250bb336838f772d9cd56bb242f4`  
		Last Modified: Wed, 02 Oct 2024 01:22:04 GMT  
		Size: 30.7 MB (30665442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575b12bbffba44e740fb24bba00627fe5d3d3fc325027f0b24213ebaad46298f`  
		Last Modified: Wed, 02 Oct 2024 01:23:09 GMT  
		Size: 18.7 MB (18731100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc92bbc83d39b17d316d0f23c720294847dc6a1fd2ee730fedf91862f9812e64`  
		Last Modified: Wed, 02 Oct 2024 01:23:17 GMT  
		Size: 134.4 MB (134408496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8157ccb960fa4987a338866c6245c655c058dd1a8cfc0fc3eacdf111f712c211`  
		Last Modified: Wed, 02 Oct 2024 01:23:06 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30b404c3e9830e97abe1fdf8a5e62f5d3a5fd5fd95ed30788bf1f773ffca70b`  
		Last Modified: Wed, 02 Oct 2024 01:23:06 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97e6c7425e68a0bba7a637241b0292aedf9a69d79d5f1fdda46cfcf4860cb3c`  
		Last Modified: Wed, 02 Oct 2024 02:40:17 GMT  
		Size: 23.8 MB (23825492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a149c56ec72bd8e6c5a5bada9d4318ad538a1b48c4c10c5359334af8870b40d`  
		Last Modified: Wed, 02 Oct 2024 02:40:17 GMT  
		Size: 9.2 MB (9170209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45f271b6e3c6ac742e85fe5c12f9aef2df6acf84f032a7116c478521c9eaf0b`  
		Last Modified: Wed, 02 Oct 2024 02:40:17 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b33e33d073c9793dc8164981eee10dd433aa61ac66be7e7dd8a37f8fced9433`  
		Last Modified: Wed, 02 Oct 2024 02:40:18 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3c03148fcf45a8cdef70957f2b603c7343ff041cab5a282f7e0fbf66482904`  
		Last Modified: Wed, 02 Oct 2024 02:40:18 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17` - unknown; unknown

```console
$ docker pull maven@sha256:755373e7e5b01bd70865cb58fac6a90dd3c1e0e667f05ac60796e728b0b439f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4700622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa330963dd2dea0dc4f87a595f11f19b570872f5aee1e872ae9a1b4054d3fbd2`

```dockerfile
```

-	Layers:
	-	`sha256:1a234e371411cc1bec19559e2b52ebd542ab7ad58fdb2c4f669f64a238ea46cd`  
		Last Modified: Wed, 02 Oct 2024 02:40:15 GMT  
		Size: 4.7 MB (4676196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cd56b75e4b2fe74b43b04e1e451c2e080ac68edc1012088072914d952eb10fa`  
		Last Modified: Wed, 02 Oct 2024 02:40:15 GMT  
		Size: 24.4 KB (24426 bytes)  
		MIME: application/vnd.in-toto+json
