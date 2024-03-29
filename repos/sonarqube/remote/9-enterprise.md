## `sonarqube:9-enterprise`

```console
$ docker pull sonarqube@sha256:a7a147a143fecfcd3c0a96e8e495c369e82ab277105530039a8b72d3c1d1138c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:9755639b2ba59e983bb2251b7f47b15e105fda4b1752ab5d38a3224296d860b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.5 MB (506517155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e20380ed3fb2229dc3a18a8588c410fa3320cad0df2da1b4ad0a23b954fe0f9e`
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
ARG SONARQUBE_VERSION=9.9.4.87374
# Mon, 26 Feb 2024 14:22:19 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.4.87374.zip
# Mon, 26 Feb 2024 14:22:19 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.4.87374 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 26 Feb 2024 14:22:19 GMT
# ARGS: SONARQUBE_VERSION=9.9.4.87374 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.4.87374.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install gnupg unzip curl bash fonts-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:06faaa0e6597e3e36a46bd6a7f9a639ccd8e25be62786beb9ba59cb43bc515c7`  
		Last Modified: Thu, 28 Mar 2024 02:50:17 GMT  
		Size: 416.0 MB (415996526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24884ea0cfb9014f643cd6ff9944ee773b7af5696b3f77b4707699ab5e0f4cb`  
		Last Modified: Thu, 28 Mar 2024 02:50:11 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:101c7ef79b6702fb48c07cc5bb4f3a87e5f75f12eb5a6c114c67d87ef7cb6de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6a8a48f417a95b84f27436ecf0bc07473fe86f096e6dead28563c615a81cef`

```dockerfile
```

-	Layers:
	-	`sha256:c194b5bc485e74e764f859b3d15c9d4eac353f5a80fbc1a7b11527b4f8461127`  
		Last Modified: Thu, 28 Mar 2024 02:50:11 GMT  
		Size: 4.1 MB (4079982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e818fd3b4621fc9c8e227877366d7efe4f812bc4be7598e1c86d61fcce20bc46`  
		Last Modified: Thu, 28 Mar 2024 02:50:11 GMT  
		Size: 18.7 KB (18701 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9-enterprise` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:1e93057f93f7953be4c32ddafaa68af83c4daa6ea35d89e0f48384be053499b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.9 MB (503855979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd53ec9630951deeba16a3f6250e05b58de579d8d37c216fedd893af7ccfda44`
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
ARG SONARQUBE_VERSION=9.9.4.87374
# Mon, 26 Feb 2024 14:22:19 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.4.87374.zip
# Mon, 26 Feb 2024 14:22:19 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.4.87374 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 26 Feb 2024 14:22:19 GMT
# ARGS: SONARQUBE_VERSION=9.9.4.87374 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.4.87374.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install gnupg unzip curl bash fonts-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:2168560270786452bc1288278f5b8a7831c90a490efa55dc798deec8e871311a`  
		Last Modified: Thu, 28 Mar 2024 00:48:42 GMT  
		Size: 12.8 MB (12846303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6274ee4a91612c77ed0ab2ea4b1df4f10d29a3c2881d2d8b564571694cd9f69`  
		Last Modified: Thu, 28 Mar 2024 00:54:00 GMT  
		Size: 46.6 MB (46639100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f6d824ccd2521a065aa5ce5d027e0f7b027066e53446b20eaa7793a0bce51b`  
		Last Modified: Thu, 28 Mar 2024 00:53:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754a82fa6b427b86617d873030d69cf741994674dcdcb02c137f9489c28e29c5`  
		Last Modified: Thu, 28 Mar 2024 00:53:55 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac4a33696cf912d2a60e266949190c2fa6c334e2286fac583c34d1d7e45c0dd`  
		Last Modified: Thu, 28 Mar 2024 19:55:09 GMT  
		Size: 416.0 MB (415968563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735f6a96ba51eb03af0c8735fc950ee471dd749485bd81285813b2d74dfb4a1c`  
		Last Modified: Thu, 28 Mar 2024 19:55:00 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:6343e93eca16c3c48a1b325bed7d28710c55302bc50af643fc5e0c019bd36ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4098129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0507dacae574b5116a0c6fd1717407eb61a2b1860e031240390039e167a5d3a`

```dockerfile
```

-	Layers:
	-	`sha256:9f1fa6165d10a7b0a505c21b784ec8d3a3e2858402f26a50ea4af28b0a585247`  
		Last Modified: Thu, 28 Mar 2024 19:55:01 GMT  
		Size: 4.1 MB (4080234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:652a0d0989fdaca444d113bab3697afb1e818458dd295dc1b40d51a4194a5780`  
		Last Modified: Thu, 28 Mar 2024 19:55:00 GMT  
		Size: 17.9 KB (17895 bytes)  
		MIME: application/vnd.in-toto+json
