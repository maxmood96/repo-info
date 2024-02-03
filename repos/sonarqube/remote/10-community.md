## `sonarqube:10-community`

```console
$ docker pull sonarqube@sha256:60f86482c5413c0f00ddc4daf14593dab1ae4fc708328bf1e9537b23faf0cfe0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:9513d8ce59a6033419cb3dc9319c5f3f3927809b3e50d3aa11aaa441bc4606d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.0 MB (483995353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43f336f6527641c135fbec55d54198ce7c4043eb174313df1ec9f7a5dd89001`
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
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
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
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26611c45681a8966387aee7b2e1494405e20bc5a46dc5da0af9228c45f8e8ec4`  
		Last Modified: Fri, 02 Feb 2024 07:50:10 GMT  
		Size: 17.5 MB (17458288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7657bba016afbc9b5b668492429479081862469157560f39c722fca733c6a4e7`  
		Last Modified: Fri, 02 Feb 2024 07:50:54 GMT  
		Size: 47.2 MB (47163193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c532b683186e5e796b6523fee32e214bd7eeda453b630d2322010697be91e8`  
		Last Modified: Fri, 02 Feb 2024 07:50:48 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e11da758202f5d3e080b1205b5f37c11a0ca72e8d428ba219b7d9d99befe18`  
		Last Modified: Fri, 02 Feb 2024 07:50:48 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f728301e94ee1700a18fdeb6205c806ae4f477b1ab31ad409ccf13ef1cafab3`  
		Last Modified: Fri, 02 Feb 2024 08:56:07 GMT  
		Size: 388.9 MB (388924616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff564f2dfed81bfb62006227fe91ed6e57af3b573e93b554716f72ebd886a4c`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10-community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:bbccc46bd5770c033694bf2f07a41d3f7285c018a2f90dd09253bbc00e15b52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3857694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df50975163113ba77bb45e99d0c3ef68441733579a67cda13392b40b841d59fc`

```dockerfile
```

-	Layers:
	-	`sha256:7e36a5ec1d69ff4c9df20fb90b6d7c85277f7d22c83cdba05015ea56369d793c`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 3.8 MB (3838778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0494f6ed9955136de2bc9c63a01d94c5a936b89c250ddb304bf3b08fc20c676`  
		Last Modified: Fri, 02 Feb 2024 08:55:57 GMT  
		Size: 18.9 KB (18916 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:10-community` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:ea3cfc7dac9ac342ce8a9ace96c96ec096692806c7aa01d4b5ee4358a04ef44b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.8 MB (482799943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a2dfee26062dc6a099e2b1f752cfae2652de72ff2a4a099f5d075a1a888a7d`
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
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
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
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d031894e4c0411af099ca88f2f4707adffb7144d8d3dc5d40457cededf240b5`  
		Last Modified: Fri, 02 Feb 2024 02:16:39 GMT  
		Size: 18.9 MB (18860666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0007a9ef9bab7b317a14a0d8594647e9c47755fcb79f9fa388e560fab31690`  
		Last Modified: Fri, 02 Feb 2024 02:17:22 GMT  
		Size: 46.6 MB (46639311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917c6cc534cfc01e73da456384906c210ffa86f1df265b8ee7255561e2a7c5fa`  
		Last Modified: Fri, 02 Feb 2024 02:17:17 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7a0f038262842ffcfdab428e9f3a7a1d0dc2e49da53bdde76335cbc0c02b48`  
		Last Modified: Fri, 02 Feb 2024 02:17:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e21f4c74fac3b206e91340dabff70fcc8c2a5d75d4d7fe5032f1710ac1304d9`  
		Last Modified: Sat, 03 Feb 2024 10:35:50 GMT  
		Size: 388.9 MB (388898486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994b43cba7ca743172b8055e0a552b82110bf73e7cf290f719e8321936c6e2b7`  
		Last Modified: Sat, 03 Feb 2024 10:35:42 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10-community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c2135673a8c1e93e982e787f313e40293ed6ce29b73363551a1867cbb440eb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202f47ef349e0a89f8d26d87726c0f6d4e1d601f115c1436c6961cb8a6241c10`

```dockerfile
```

-	Layers:
	-	`sha256:ba1bd39dc445db20bd9c6e14aefe7a6d51ea3e610026eb743fd49d35cb232a9d`  
		Last Modified: Sat, 03 Feb 2024 10:35:42 GMT  
		Size: 3.9 MB (3930821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6272a16af039ae4de6255f5ccfbe9aee1364fd7b14e45d265b5e11c4936819ad`  
		Last Modified: Sat, 03 Feb 2024 10:35:42 GMT  
		Size: 18.1 KB (18110 bytes)  
		MIME: application/vnd.in-toto+json
