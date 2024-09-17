## `sonarqube:10-community`

```console
$ docker pull sonarqube@sha256:72e9feec71242af83faf65f95a40d5e3bb2822a6c3b2cda8568790f3d31aecde
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:f289dacdf7b33a88468a93c11d125c6a102b29a394c0aaf445406ea4b5ce1fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **829.0 MB (829030795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2433ac783140f6153874adca40e138aee5292aff56e776ac26197bbe0e7c8cff`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Wed, 24 Jul 2024 09:49:45 GMT
ARG RELEASE
# Wed, 24 Jul 2024 09:49:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 24 Jul 2024 09:49:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 24 Jul 2024 09:49:45 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 24 Jul 2024 09:49:45 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 24 Jul 2024 09:49:45 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 09:49:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 09:49:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 09:49:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 09:49:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 09:49:45 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 24 Jul 2024 09:49:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 09:49:45 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 09:49:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 09:49:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jul 2024 09:49:45 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Wed, 24 Jul 2024 09:49:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 09:49:45 GMT
ARG SONARQUBE_VERSION=10.6.0.92116
# Wed, 24 Jul 2024 09:49:45 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.6.0.92116.zip
# Wed, 24 Jul 2024 09:49:45 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.6.0.92116 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Wed, 24 Jul 2024 09:49:45 GMT
# ARGS: SONARQUBE_VERSION=10.6.0.92116 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.6.0.92116.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install gnupg unzip curl bash fonts-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jul 2024 09:49:45 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Wed, 24 Jul 2024 09:49:45 GMT
WORKDIR /opt/sonarqube
# Wed, 24 Jul 2024 09:49:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 24 Jul 2024 09:49:45 GMT
USER sonarqube
# Wed, 24 Jul 2024 09:49:45 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jul 2024 09:49:45 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a34308537d0e24a7f0071494a76905295ed7c0b75d214d6ea286d8baa07f0`  
		Last Modified: Tue, 17 Sep 2024 01:10:27 GMT  
		Size: 47.3 MB (47280134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80338217a4aba4f8c6f0db147f66124a7d20f3bcd346bf35e5a8f2771864e538`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5fd5c7e18487a3562654981bd4650210fbcffd763f2e4ef507da0ac514c4bb`  
		Last Modified: Tue, 17 Sep 2024 01:10:20 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b87d6fa783da9310eb18656cf208ff4706651c152ef5fde77728571e5976dd0`  
		Last Modified: Tue, 17 Sep 2024 02:01:17 GMT  
		Size: 738.4 MB (738437045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd819c9b5eadd1ff8225da204193668b09f27999a991ffb791e28a68cf567b02`  
		Last Modified: Tue, 17 Sep 2024 02:00:57 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10-community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:04bbceef887d753f355f4987347f7b76cd6ac3161f19f380bcf422cf1873fdfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4047d4044e6cfb1e8dd919d181c2ff9b0673092f4e87ce9c364e822d72df08b`

```dockerfile
```

-	Layers:
	-	`sha256:b95d56e99448f63eec568919b9b66e0a3af06706480662c29ac2930f184040a5`  
		Last Modified: Tue, 17 Sep 2024 02:00:58 GMT  
		Size: 4.3 MB (4295787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c427e2b5fcc14657c35c83e5d584f66f7ef09eaa965e0d599eaba8c1405864`  
		Last Modified: Tue, 17 Sep 2024 02:00:57 GMT  
		Size: 18.1 KB (18072 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:10-community` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:2b40d255d97517b7c80d10ec5a77d0d3ba868224ee8b2e137070a0b256206b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **826.4 MB (826374964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d204475987ac8b60bc3fb94cac681bfce8255a5c2e77084de96da3f57ec34f1`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Wed, 24 Jul 2024 09:49:45 GMT
ARG RELEASE
# Wed, 24 Jul 2024 09:49:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 24 Jul 2024 09:49:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 24 Jul 2024 09:49:45 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 24 Jul 2024 09:49:45 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 24 Jul 2024 09:49:45 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 09:49:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 09:49:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 09:49:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 09:49:45 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 09:49:45 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 24 Jul 2024 09:49:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 09:49:45 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 09:49:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 09:49:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jul 2024 09:49:45 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Wed, 24 Jul 2024 09:49:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 09:49:45 GMT
ARG SONARQUBE_VERSION=10.6.0.92116
# Wed, 24 Jul 2024 09:49:45 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.6.0.92116.zip
# Wed, 24 Jul 2024 09:49:45 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.6.0.92116 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Wed, 24 Jul 2024 09:49:45 GMT
# ARGS: SONARQUBE_VERSION=10.6.0.92116 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.6.0.92116.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install gnupg unzip curl bash fonts-dejavu;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jul 2024 09:49:45 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Wed, 24 Jul 2024 09:49:45 GMT
WORKDIR /opt/sonarqube
# Wed, 24 Jul 2024 09:49:45 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 24 Jul 2024 09:49:45 GMT
USER sonarqube
# Wed, 24 Jul 2024 09:49:45 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jul 2024 09:49:45 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc429601029ecb71c941cbfdd32b85983522d0f4ef294d6f2de0ba93bb2f778`  
		Last Modified: Tue, 17 Sep 2024 01:37:28 GMT  
		Size: 12.8 MB (12813215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f704211ab9e8088b7780d5a6d78ef5f3e5555252dfa4bf1a76be2c292b1333`  
		Last Modified: Tue, 17 Sep 2024 01:40:06 GMT  
		Size: 46.7 MB (46746290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee39a89b4fd61e0dcd39c2dcdd56f0671b5fbd54e89103bc936b41a23d45f6`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25eb3700d3254446e455c594267b68dab7f244d9e679ae3b4c44abe8c7969f`  
		Last Modified: Tue, 17 Sep 2024 01:40:00 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3098d7b8f6ca242a333696fe6584ea4059b3389200125659725df1f698778fc9`  
		Last Modified: Tue, 17 Sep 2024 06:33:29 GMT  
		Size: 738.4 MB (738415600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ea2a39b0fb8c2f5c28e66e70a2cbcf60e0d55d04839ccc1ed69cb54bf0767e`  
		Last Modified: Tue, 17 Sep 2024 06:33:13 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10-community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:69afd9c6de2a5fb7224b5254eda093ce719a1c1e7c68d6946dd35bd8f5552e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5668177a2e82218ac91fc0238a2a25f062eea749b67bbcb035b920a3ff8ef36`

```dockerfile
```

-	Layers:
	-	`sha256:c4a8d77d588b1815cadb82b752dae78df9ba9f71103c73d33f89afd7608ef9b6`  
		Last Modified: Tue, 17 Sep 2024 06:33:13 GMT  
		Size: 4.3 MB (4296096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a63195ee11b6fdc299f0e8cee7fc6b129c0218e8f9f6a9ade968d839d5a15c4`  
		Last Modified: Tue, 17 Sep 2024 06:33:13 GMT  
		Size: 18.4 KB (18401 bytes)  
		MIME: application/vnd.in-toto+json
