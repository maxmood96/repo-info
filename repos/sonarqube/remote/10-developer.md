## `sonarqube:10-developer`

```console
$ docker pull sonarqube@sha256:75c019d3b18fc6e1f55e67e7518e6f1b53231b5bee7016b9119217c48d55dc4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:ce04e8511286301b5c8dcecfa4f812b8882e639adafb1aaca3e964b9b7f5ac9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.9 MB (649892075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43d52773a584ea9184b29ac7d6b8ef495ffd8fc40e956432ca52aede082c628`
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
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Feb 2024 14:22:19 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Mon, 26 Feb 2024 14:22:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 26 Feb 2024 14:22:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 26 Feb 2024 14:22:19 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 26 Feb 2024 14:22:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 26 Feb 2024 14:22:19 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 26 Feb 2024 14:22:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Feb 2024 14:22:19 GMT
ARG SONARQUBE_VERSION=10.4.1.88267
# Mon, 26 Feb 2024 14:22:19 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.4.1.88267.zip
# Mon, 26 Feb 2024 14:22:19 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.4.1.88267 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 26 Feb 2024 14:22:19 GMT
# ARGS: SONARQUBE_VERSION=10.4.1.88267 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.4.1.88267.zip
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
	-	`sha256:cfcf356fa6e6902e661a53c29cf3b351f284090cb2c0de2ad6c5c238a6fdb9a8`  
		Last Modified: Thu, 28 Mar 2024 02:03:28 GMT  
		Size: 12.9 MB (12904693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b345ba1396e8406df1a417529c91dac4e4802e6b18921719b9022f3dfb3734cf`  
		Last Modified: Thu, 28 Mar 2024 02:10:46 GMT  
		Size: 47.2 MB (47163261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e0a682e40f83e4da859eee85bc3b44b9444d2949261d3f2a475b030d190ecb`  
		Last Modified: Thu, 28 Mar 2024 02:10:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa5752204b57ae4cecf034a16e07738b48b46bfdb2f5aa6981b074fb11f5626`  
		Last Modified: Thu, 28 Mar 2024 02:10:39 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cabe2169a6bf5cd5e603233e6b2ceefd6d9a8d657e012e800614951336946de`  
		Last Modified: Thu, 28 Mar 2024 02:50:39 GMT  
		Size: 559.4 MB (559371444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241c287a92f09c3caca3528714fbdc527fe8fbd1d4f0727836d7777c9089a27d`  
		Last Modified: Thu, 28 Mar 2024 02:50:31 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:0295ddd13005014cd1fc01847c7160987c01d913dadfa47e34b8d0cf47fa8a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4276674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebdf67b5277b7e420e85e0612d45a745b02191761c1959c2dc88ec7ca9256ee`

```dockerfile
```

-	Layers:
	-	`sha256:a181b68549b5becd1a6af905b77928881314da69fc1180bc7e0b4c0b34897be0`  
		Last Modified: Thu, 28 Mar 2024 02:50:31 GMT  
		Size: 4.3 MB (4258111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da7a743bc7ef85eb8bb04b8da12eb177f17e5a67d7eff6227b5e0333c5a4b2d3`  
		Last Modified: Thu, 28 Mar 2024 02:50:30 GMT  
		Size: 18.6 KB (18563 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:10-developer` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:48b5762cadc58d1f6ca8654e1a53a61fef4a7b7ad5df0e540a10edbc09ed2038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **652.6 MB (652556428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfe8f362e3071e99f837178a0180085195e1b211089db672f30a482371769bb`
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
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.4.1.88267.zip
# Mon, 26 Feb 2024 14:22:19 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.4.1.88267 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 26 Feb 2024 14:22:19 GMT
# ARGS: SONARQUBE_VERSION=10.4.1.88267 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.4.1.88267.zip
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
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799297b6f9210d0b08ff588516d8ab6fe2169cdda6b76a0b5f854b6e76aec0ce`  
		Last Modified: Wed, 06 Mar 2024 04:08:04 GMT  
		Size: 18.9 MB (18857483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0f6cd036a6aa4998c7a9c375b0e7fb43615f3d03dfcb794b88cff90027fff7`  
		Last Modified: Wed, 06 Mar 2024 04:08:44 GMT  
		Size: 46.6 MB (46639407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30140b6dcdeba2a64a4d96bfde851abee456c368a15a215e1b86e3c0484bce`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13614e023aad4adadb99824ffb722959861646971b8c272a4eaf5b1fe098077e`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953b05fe9c826b6c67a29b180897449db45d09135e735706fd144a1ed09de7cb`  
		Last Modified: Wed, 06 Mar 2024 18:58:17 GMT  
		Size: 558.7 MB (558657521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6950d0754a4c0a6a6c5187b5d428348d2a5eab36c3b6bc35ebbd526fb27d1c5c`  
		Last Modified: Wed, 06 Mar 2024 18:58:06 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c81672d83e66b543a8cbaef4cbe4bdcf3b3601fff632b869e9e5a3d3a73253d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4527606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc0e494029fa69220989f4e42c53e48ca769289f92835b50149bfada927f461`

```dockerfile
```

-	Layers:
	-	`sha256:6b8bac606d82eae2cf37dedd58daa5eb338eea6f9a37a07d754727bcc2302b75`  
		Last Modified: Wed, 06 Mar 2024 18:58:06 GMT  
		Size: 4.5 MB (4509848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcbef2c8b29a71241523bee59a802896a1b6de311222b37cc365903c289f086`  
		Last Modified: Wed, 06 Mar 2024 18:58:06 GMT  
		Size: 17.8 KB (17758 bytes)  
		MIME: application/vnd.in-toto+json
