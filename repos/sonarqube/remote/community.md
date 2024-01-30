## `sonarqube:community`

```console
$ docker pull sonarqube@sha256:548f3d4246cda60c311a035620c26ea8fb21b3abc870c5806626a32ef936982b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:community` - linux; amd64

```console
$ docker pull sonarqube@sha256:7bc951c82ebe2aeb2356764d035344f8f16de1af095a992d6cdc014a9b49c042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.0 MB (483994531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7172e97a26a3fdff5c6deea926362cfca6c692e171f4c987053d6f5f9d67d5`
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
ARG SONARQUBE_VERSION=10.3.0.82913
# Tue, 14 Nov 2023 10:44:06 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.3.0.82913.zip
# Tue, 14 Nov 2023 10:44:06 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.3.0.82913 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Tue, 14 Nov 2023 10:44:06 GMT
# ARGS: SONARQUBE_VERSION=10.3.0.82913 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.3.0.82913.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get install -y gnupg unzip curl bash fonts-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:5703a3cb4dd346b3b9a59b014fc7f955d831dfe20301884b8f9e8433983a980b`  
		Last Modified: Mon, 29 Jan 2024 22:52:39 GMT  
		Size: 388.9 MB (388924657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6165258be60e97d9d71a581a39af0f12769ec3d98b6eea7b7069c799e05ee5`  
		Last Modified: Mon, 29 Jan 2024 22:52:32 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:8dd882b7240ff7119e7a699953bd38121c761177c306b3a52b9bf1850abd69a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3857702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952b2fb0234fe98df1717378cfd9762c99d0fba9977dd66c16329ab280c65551`

```dockerfile
```

-	Layers:
	-	`sha256:93744deeabd7e8ec8b33d9465ee404034490c4dc61a0c5a63b655a571cdadb70`  
		Last Modified: Mon, 29 Jan 2024 22:52:32 GMT  
		Size: 3.8 MB (3838786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8add84634b176d886d1a9ddfc1449ea8fe2d7c87ce2377c24c16c42a71f65ad1`  
		Last Modified: Mon, 29 Jan 2024 22:52:32 GMT  
		Size: 18.9 KB (18916 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:community` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:438b86010b9b0a73fad1cb86120ccd6a7cc8311c6c4e4ec5d2eb78c668c7618b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.8 MB (482799015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed7d824f2fd63527b68c57bd1a506a303f68b2aaaa687973547a4613c3a387c`
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
ARG SONARQUBE_VERSION=10.3.0.82913
# Tue, 14 Nov 2023 10:44:06 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.3.0.82913.zip
# Tue, 14 Nov 2023 10:44:06 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.3.0.82913 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Tue, 14 Nov 2023 10:44:06 GMT
# ARGS: SONARQUBE_VERSION=10.3.0.82913 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.3.0.82913.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get install -y gnupg unzip curl bash fonts-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:be20c4f58aa8b38a73d6474557b245fba21e25c4a288c3f217f7549fc2d056d7`  
		Last Modified: Tue, 30 Jan 2024 01:40:29 GMT  
		Size: 388.9 MB (388898582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cb09b9de78b2bae5a42df7133f26fe28aadd4e03a63799e4ffb1a34d48f6b7`  
		Last Modified: Tue, 30 Jan 2024 01:40:21 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:f3ef68d898ccefccf910646e94fbbb279751ab0e508cba8e92e64c923674e999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9e1e4ac26958cd2a16b2751898a27bedfc8b7cd9e8b9162baf5b1b615a3061`

```dockerfile
```

-	Layers:
	-	`sha256:0cb363751465976848c6fb76a74ca5bcc5481d0b5e49b5ebeff3abfd2f2c5c9a`  
		Last Modified: Tue, 30 Jan 2024 01:40:21 GMT  
		Size: 3.9 MB (3922565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c3e9604bfff8faa738172e6e1bb4757d39ebb3be32edc9425afa8ccbfeb0a98`  
		Last Modified: Tue, 30 Jan 2024 01:40:21 GMT  
		Size: 18.1 KB (18110 bytes)  
		MIME: application/vnd.in-toto+json
