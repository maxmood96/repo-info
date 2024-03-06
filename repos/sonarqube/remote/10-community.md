## `sonarqube:10-community`

```console
$ docker pull sonarqube@sha256:b71d04c76bbfd39728ca5f51bcaba466872d3c86172432fb581d69999e491ed3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:4b31ec5b230af3d354d6c13f7764b84b813999bc45b3d7fc69db7c04a9ca4b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557217775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba3b520d50eafebd1b4f013898d2eb8e1fbeae2c2f5448fdd98a0dc6541ffec0`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 26 Feb 2024 14:22:19 GMT
ARG RELEASE
# Mon, 26 Feb 2024 14:22:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 26 Feb 2024 14:22:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 26 Feb 2024 14:22:19 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 26 Feb 2024 14:22:19 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Mon, 26 Feb 2024 14:22:19 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 14:22:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 26 Feb 2024 14:22:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Feb 2024 14:22:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Feb 2024 14:22:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 26 Feb 2024 14:22:19 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Mon, 26 Feb 2024 14:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 26 Feb 2024 14:22:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 26 Feb 2024 14:22:19 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 26 Feb 2024 14:22:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 26 Feb 2024 14:22:19 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 26 Feb 2024 14:22:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Feb 2024 14:22:19 GMT
ARG SONARQUBE_VERSION=10.4.1.88267
# Mon, 26 Feb 2024 14:22:19 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.4.1.88267.zip
# Mon, 26 Feb 2024 14:22:19 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.4.1.88267 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 26 Feb 2024 14:22:19 GMT
# ARGS: SONARQUBE_VERSION=10.4.1.88267 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.4.1.88267.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install gnupg unzip curl bash fonts-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 26 Feb 2024 14:22:19 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 26 Feb 2024 14:22:19 GMT
WORKDIR /opt/sonarqube
# Mon, 26 Feb 2024 14:22:19 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 26 Feb 2024 14:22:19 GMT
USER sonarqube
# Mon, 26 Feb 2024 14:22:19 GMT
STOPSIGNAL SIGINT
# Mon, 26 Feb 2024 14:22:19 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2670537dcebc0b445ca47e68b31667f3572b8758b8388e24d8a6770e860ecc8`  
		Last Modified: Wed, 06 Mar 2024 06:09:59 GMT  
		Size: 17.5 MB (17456336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c059ccfa41820fb3f1472c4358304407b00e3eed15933f067b1d4957a40bfc3`  
		Last Modified: Wed, 06 Mar 2024 06:10:45 GMT  
		Size: 47.2 MB (47163248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23d33d59f2ab52fa44e6fbd4e629813614bb753bb3ccac98940e981a3b13c4e`  
		Last Modified: Wed, 06 Mar 2024 06:10:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a648f54390edf0b921f43c547b5d6d6b937e58728be46796f6aefcd4735fb`  
		Last Modified: Wed, 06 Mar 2024 06:10:39 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77836e5f0579f8583d48d42cfdc2aa33cb9fccede5b8f2ecbddb2c608abb0dd8`  
		Last Modified: Wed, 06 Mar 2024 06:49:58 GMT  
		Size: 462.1 MB (462145512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e25cb96243660e71962b688535982744bc85845c60d88115dbfd1822aa41d78`  
		Last Modified: Wed, 06 Mar 2024 06:49:49 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10-community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:5d2d4b83ddfc78733a4c5fa964fa0bfd6d9cf7b6a28bf1207ae3b970b974823b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4343093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a816a0a3c5ee6b177efeb7ed97290fcc6bbe382fd646c90d9ab37da66713981e`

```dockerfile
```

-	Layers:
	-	`sha256:262678efd07f8f9015ade17b81cb3ec6804d18f65b0dc02d267961699c74790b`  
		Last Modified: Wed, 06 Mar 2024 06:49:50 GMT  
		Size: 4.3 MB (4324293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aa82b2c37355ec6ab316efe3f9683b339d4b16863bd7eeca328df95a9851747`  
		Last Modified: Wed, 06 Mar 2024 06:49:49 GMT  
		Size: 18.8 KB (18800 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:10-community` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:3e61235b349025021c5ef5d12ccd89ef85c4f2c5e7a64d5915ac87b57880fb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (556027507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c29bce77d059d0c78f57a68bd4f7cbf64032577074b8046eaa7d3c386b9f78`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:51:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 04:51:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 04:51:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Feb 2024 04:52:49 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:52:49 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 16 Feb 2024 04:53:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Feb 2024 04:53:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 16 Feb 2024 04:53:10 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 16 Feb 2024 04:53:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 26 Feb 2024 14:22:19 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 26 Feb 2024 14:22:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Feb 2024 14:22:19 GMT
ARG SONARQUBE_VERSION=10.4.1.88267
# Mon, 26 Feb 2024 14:22:19 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.4.1.88267.zip
# Mon, 26 Feb 2024 14:22:19 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.4.1.88267 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 26 Feb 2024 14:22:19 GMT
# ARGS: SONARQUBE_VERSION=10.4.1.88267 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.4.1.88267.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install gnupg unzip curl bash fonts-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 26 Feb 2024 14:22:19 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 26 Feb 2024 14:22:19 GMT
WORKDIR /opt/sonarqube
# Mon, 26 Feb 2024 14:22:19 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 26 Feb 2024 14:22:19 GMT
USER sonarqube
# Mon, 26 Feb 2024 14:22:19 GMT
STOPSIGNAL SIGINT
# Mon, 26 Feb 2024 14:22:19 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bac6b544c281c39df6cde20776732e9b89dbfbbbb49870c60c9af5ef1df471`  
		Last Modified: Fri, 16 Feb 2024 04:55:46 GMT  
		Size: 18.9 MB (18860590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244992bb9e51f456f3e5c927182054789a275d47eba65099182705a8e1952dc2`  
		Last Modified: Fri, 16 Feb 2024 04:56:12 GMT  
		Size: 46.6 MB (46639325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e543faa97f71ea4edea5a6153e1b82e4e9143354356435ca0a085c427b9b07e`  
		Last Modified: Fri, 16 Feb 2024 04:56:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b734e973751dd4636bc278f0ef5ee31fc8e10cc65a07ebd5ef57aa728870187`  
		Last Modified: Fri, 16 Feb 2024 04:56:06 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958207477f2137944a88c1e649feb3733df714f3a27f11104bc73f07871cb571`  
		Last Modified: Mon, 26 Feb 2024 19:52:55 GMT  
		Size: 462.1 MB (462125893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46802117675901c4c4ec39b83869fa6766b1ef496040339634509376f6ae2f7b`  
		Last Modified: Mon, 26 Feb 2024 19:52:45 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10-community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:11096f65e04b30bf90031bbfbf5a96ca428da411a3cfa7dd66fcf0859ab77bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4438445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f321d54c0bc2fd5e0289fc3721607b2215c71e8585c529e8c47c951d58cced6e`

```dockerfile
```

-	Layers:
	-	`sha256:8de24b1a0bb87ec1ff2d0f300a81210d955acfe38be9e25daf2a14a4af709748`  
		Last Modified: Mon, 26 Feb 2024 19:52:45 GMT  
		Size: 4.4 MB (4420450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07d79e6180c9f4f26775a6161532269f6ada49abdd98d04a0eeece08cf81aee3`  
		Last Modified: Mon, 26 Feb 2024 19:52:45 GMT  
		Size: 18.0 KB (17995 bytes)  
		MIME: application/vnd.in-toto+json
