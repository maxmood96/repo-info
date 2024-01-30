## `sonarqube:9-community`

```console
$ docker pull sonarqube@sha256:54b7d3a2d755368d72c190996f0e5470c638100ad70e427a828b627c9101b555
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:6853e6d42a3e1722a336c737360f3bc2c96fbc3bcb91c7a5b8811f3306c37eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.4 MB (396354638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef5886c8c587cdfb8c4c82d6376916719e07cc2ee01cb6cae2ad91bb38cdf96`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Tue, 14 Nov 2023 10:44:06 GMT
ARG RELEASE
# Tue, 14 Nov 2023 10:44:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 10:44:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 10:44:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 10:44:06 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Tue, 14 Nov 2023 10:44:06 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 10:44:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Nov 2023 10:44:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Nov 2023 10:44:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Nov 2023 10:44:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 10:44:06 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 14 Nov 2023 10:44:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 14 Nov 2023 10:44:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 14 Nov 2023 10:44:06 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 14 Nov 2023 10:44:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Nov 2023 10:44:06 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Tue, 14 Nov 2023 10:44:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Nov 2023 10:44:06 GMT
ARG SONARQUBE_VERSION=9.9.3.79811
# Tue, 14 Nov 2023 10:44:06 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.3.79811.zip
# Tue, 14 Nov 2023 10:44:06 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.3.79811 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Tue, 14 Nov 2023 10:44:06 GMT
# ARGS: SONARQUBE_VERSION=9.9.3.79811 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.3.79811.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get install -y gnupg unzip curl bash fonts-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 14 Nov 2023 10:44:06 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Tue, 14 Nov 2023 10:44:06 GMT
WORKDIR /opt/sonarqube
# Tue, 14 Nov 2023 10:44:06 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 14 Nov 2023 10:44:06 GMT
USER sonarqube
# Tue, 14 Nov 2023 10:44:06 GMT
STOPSIGNAL SIGINT
# Tue, 14 Nov 2023 10:44:06 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c506251a0ae0b836353578bafa8d6aeb266158d3291ba4abbc2f5f8ccda6f742`  
		Last Modified: Wed, 17 Jan 2024 07:20:28 GMT  
		Size: 17.5 MB (17458145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8c673b95895c0efae2a8f0414597595f1d4f6b3e7973d0b99ee9b366580dd1`  
		Last Modified: Wed, 24 Jan 2024 20:48:16 GMT  
		Size: 47.2 MB (47163238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3fdfdbc1541d3276eaff7653137f8be176069196a72c68a0bf735dc617e7a2`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4080cbbe938d7cadb00eda7a89a93f5878d7e968b4e8b23640b11c37ad69ca7b`  
		Last Modified: Thu, 25 Jan 2024 19:36:00 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82ac5234dcaa7dd72d21956040135cb6e0d536aa0508b29ad7fe3a14a96f4a0`  
		Last Modified: Mon, 29 Jan 2024 22:52:43 GMT  
		Size: 301.3 MB (301284763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725f233730393878b6f930a639a39dbea5163c5e91272b1406971f3a8e02e41c`  
		Last Modified: Mon, 29 Jan 2024 22:52:34 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:52ecaf3eed428b89467e718fe011640d14332dc9aae545c32be4a5b422dcc9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7fdc629a3f95686aa2cf33cb573461536165b001ecd82ff23a50c06c8ac9981`

```dockerfile
```

-	Layers:
	-	`sha256:e5eb5198538dabe136e6d2503fe4fad64a1283e04a5437d19a76e62505e6abb2`  
		Last Modified: Mon, 29 Jan 2024 22:52:35 GMT  
		Size: 3.6 MB (3606632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0455917ffb7dac21a819acad887693a9b60e0cfb51673926a571f1bdcefc970`  
		Last Modified: Mon, 29 Jan 2024 22:52:34 GMT  
		Size: 18.9 KB (18857 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9-community` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:29b188599d46c22e83793b960c544297da9458dc0e6786f01e5e242218a0dbce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.2 MB (395154574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e35744049b2b148f2037fe7ca0edae24a28bf3422d14412d3249c7649fd7315`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Tue, 14 Nov 2023 10:44:06 GMT
ARG RELEASE
# Tue, 14 Nov 2023 10:44:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 10:44:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 10:44:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 10:44:06 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Tue, 14 Nov 2023 10:44:06 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 10:44:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Nov 2023 10:44:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Nov 2023 10:44:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Nov 2023 10:44:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 10:44:06 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 14 Nov 2023 10:44:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 14 Nov 2023 10:44:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 14 Nov 2023 10:44:06 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 14 Nov 2023 10:44:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Nov 2023 10:44:06 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Tue, 14 Nov 2023 10:44:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Nov 2023 10:44:06 GMT
ARG SONARQUBE_VERSION=9.9.3.79811
# Tue, 14 Nov 2023 10:44:06 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.3.79811.zip
# Tue, 14 Nov 2023 10:44:06 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.3.79811 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Tue, 14 Nov 2023 10:44:06 GMT
# ARGS: SONARQUBE_VERSION=9.9.3.79811 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.3.79811.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get install -y gnupg unzip curl bash fonts-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 14 Nov 2023 10:44:06 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Tue, 14 Nov 2023 10:44:06 GMT
WORKDIR /opt/sonarqube
# Tue, 14 Nov 2023 10:44:06 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 14 Nov 2023 10:44:06 GMT
USER sonarqube
# Tue, 14 Nov 2023 10:44:06 GMT
STOPSIGNAL SIGINT
# Tue, 14 Nov 2023 10:44:06 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6a2be6e4013cffcaae1614f67dca08e0c8d56b9d2da9051ae71c48b43a409a`  
		Last Modified: Wed, 17 Jan 2024 07:02:15 GMT  
		Size: 18.9 MB (18860096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c758562b2b3e61329aca1af5bb5fa0700d9b5f7cf4e68faa8e2235d15dccfd1a`  
		Last Modified: Wed, 24 Jan 2024 20:52:24 GMT  
		Size: 46.6 MB (46639344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12285b9bc0b75c36f5f58bb0cba487613706fb4718325baccbf6a0d2eb157be6`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c24226ebd43098c00c6e2715c22788dde6531777752b1ae35e81c95623edeae`  
		Last Modified: Thu, 25 Jan 2024 19:43:16 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d1c0eb1a74ea65495397d9f67154dd13f87a389971c9197e8a212801005ec0`  
		Last Modified: Tue, 30 Jan 2024 01:33:46 GMT  
		Size: 301.3 MB (301254146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17824f9f8d6d0b0b1d7cb608156c83193e60141f0c9baa1492e05c52e7944c7`  
		Last Modified: Tue, 30 Jan 2024 01:33:40 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:12a7ee72ab60031efd09a33b0c8c9ee0993425f86cb00837abfa0f6437c53819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3708455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424fc6879f84c06b2f5575473d17cde330848f86c62e4e379e5252fcf454f907`

```dockerfile
```

-	Layers:
	-	`sha256:126690d3bdd93bab0c71e1a6b851664391c4bf7de1f4171b220cf348b21edb20`  
		Last Modified: Tue, 30 Jan 2024 01:33:40 GMT  
		Size: 3.7 MB (3690403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8df199aff60103f92e9095ac1306c98a97027391a52f3865a5231d7dff60a440`  
		Last Modified: Tue, 30 Jan 2024 01:33:39 GMT  
		Size: 18.1 KB (18052 bytes)  
		MIME: application/vnd.in-toto+json
