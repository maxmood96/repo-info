## `sonarqube:lts`

```console
$ docker pull sonarqube@sha256:700d05b4758c53b18517469baa62abdf01ce1e16f5200794e9076456e5c91bd4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:lts` - linux; amd64

```console
$ docker pull sonarqube@sha256:579a7e9123e0cc39715be70d3ee570f23cc1ee21e3fae94602393ac834c9090b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.1 MB (393078559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b56b4a3c6d695a0f5a47ba2187e2e88844fc2bcdf569772102a97513162b5a2`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Tue, 25 Mar 2025 16:51:11 GMT
ARG RELEASE
# Tue, 25 Mar 2025 16:51:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 16:51:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 16:51:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Mar 2025 16:51:11 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Tue, 25 Mar 2025 16:51:11 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 16:51:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 16:51:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 16:51:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 16:51:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 16:51:11 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 25 Mar 2025 16:51:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 25 Mar 2025 16:51:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 16:51:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 16:51:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 16:51:11 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Tue, 25 Mar 2025 16:51:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 16:51:11 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Tue, 25 Mar 2025 16:51:11 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
# Tue, 25 Mar 2025 16:51:11 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Tue, 25 Mar 2025 16:51:11 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 25 Mar 2025 16:51:11 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Tue, 25 Mar 2025 16:51:11 GMT
WORKDIR /opt/sonarqube
# Tue, 25 Mar 2025 16:51:11 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 25 Mar 2025 16:51:11 GMT
USER sonarqube
# Tue, 25 Mar 2025 16:51:11 GMT
STOPSIGNAL SIGINT
# Tue, 25 Mar 2025 16:51:11 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094bfcb4db7a5f519259e3fe3770affd9596cef0a3ba491c6a061e6d14972bab`  
		Last Modified: Mon, 05 May 2025 16:35:16 GMT  
		Size: 16.1 MB (16146206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df791be4da659132dea4b5bb8435ffac9728463aab0b421013aefaf00253146`  
		Last Modified: Mon, 05 May 2025 16:35:17 GMT  
		Size: 47.0 MB (46958354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a8e80e60c29d06e337a6a5e0c546bde1b547f1b08cfbc00b38195b14da1d66`  
		Last Modified: Mon, 05 May 2025 16:35:16 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be47dbb02a776fb8eaae5a3127ca438e4982eae6edc2b8a0d2c7d00aa02e078`  
		Last Modified: Mon, 05 May 2025 16:35:16 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c8ff67f9489ea0d09f0aed1950f67f1c6b2939586e9d13be08c1e9dca2282e`  
		Last Modified: Mon, 05 May 2025 17:05:19 GMT  
		Size: 300.4 MB (300438468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2737e808f9c37302f57050a8dd1339c795ca7544cbfcadbe81ea73e2ad027fab`  
		Last Modified: Mon, 05 May 2025 17:05:14 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts` - unknown; unknown

```console
$ docker pull sonarqube@sha256:6018dd6bf0e67931b82ba88d3c37eb46dfe481c71f2ffb55c76fd2ae9eb3ac4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4155136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca0bc9f63d85e337c00adc6048186ba595699ea1d2620c63cedd559adf2e9d7`

```dockerfile
```

-	Layers:
	-	`sha256:6e91c9a53edf7368392ea4ee5474d0970cd49dc2b16077483197efc5c0818c46`  
		Last Modified: Mon, 05 May 2025 17:05:14 GMT  
		Size: 4.1 MB (4136554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbe1df07dc55583fba6b99644d64f0ca5f5b669d19a7d0dadf234c146f5eb933`  
		Last Modified: Mon, 05 May 2025 17:05:14 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:lts` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:4fb33bd4aa71440597a6761a8b5d64475773f7df174d927e1c4d7bd782be9826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 MB (390329474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdcfb2a4a6d8e0af510361004b4a134a6102dd6f7703bc7c1dd05a4d7b8c28db`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Tue, 25 Mar 2025 16:51:11 GMT
ARG RELEASE
# Tue, 25 Mar 2025 16:51:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Mar 2025 16:51:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Mar 2025 16:51:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Mar 2025 16:51:11 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Tue, 25 Mar 2025 16:51:11 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 16:51:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 16:51:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 16:51:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 16:51:11 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Mar 2025 16:51:11 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 25 Mar 2025 16:51:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 25 Mar 2025 16:51:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 16:51:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 16:51:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 16:51:11 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Tue, 25 Mar 2025 16:51:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 16:51:11 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Tue, 25 Mar 2025 16:51:11 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
# Tue, 25 Mar 2025 16:51:11 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Tue, 25 Mar 2025 16:51:11 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 25 Mar 2025 16:51:11 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Tue, 25 Mar 2025 16:51:11 GMT
WORKDIR /opt/sonarqube
# Tue, 25 Mar 2025 16:51:11 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 25 Mar 2025 16:51:11 GMT
USER sonarqube
# Tue, 25 Mar 2025 16:51:11 GMT
STOPSIGNAL SIGINT
# Tue, 25 Mar 2025 16:51:11 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d988c284109adb0ee08f6d6a95a152f6e364456e1a4853bb6c3ebc58c40f099`  
		Last Modified: Wed, 09 Apr 2025 06:58:01 GMT  
		Size: 16.1 MB (16059566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac488a8321ea959588c227573cf8a20259cc8fde212361febce0a1b0c814dbef`  
		Last Modified: Wed, 23 Apr 2025 16:38:17 GMT  
		Size: 46.5 MB (46474324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1af5cf872e078be1505c0565767eed13113730ec78326847e626469b0b8c663`  
		Last Modified: Wed, 23 Apr 2025 16:38:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af88f83d0cfd9bd69d840192dccb1b340da7121b21b5d2c5d41ad894714765f2`  
		Last Modified: Wed, 23 Apr 2025 16:38:15 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4529a1f30be6c73a7f3253dc12ce8ef9f5b9b88b4218dfd5464e9120790103b7`  
		Last Modified: Wed, 23 Apr 2025 18:44:16 GMT  
		Size: 300.4 MB (300438432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2606eba22a14fbd29c52c1a31de62b2b1c3c2ba9464c08bb81268c3209be38`  
		Last Modified: Wed, 23 Apr 2025 18:44:08 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts` - unknown; unknown

```console
$ docker pull sonarqube@sha256:fbc8be86124d20013b98aa12e6082be04e36499993b474b9cbc12497d36d7e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a5a82f4d10672c99f0e514287e43f00b292a4947777e7d694011b5b2a0b060`

```dockerfile
```

-	Layers:
	-	`sha256:f7ec488bbca507c5320d8903d3c4b1879fb1b1f77c2d01b63e6106c6688cd649`  
		Last Modified: Wed, 23 Apr 2025 18:44:09 GMT  
		Size: 4.1 MB (4136246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe125464a9f7cba1b0dce4dc07e10d4f4066b0387e1398b83d2e04fa3124c009`  
		Last Modified: Wed, 23 Apr 2025 18:44:08 GMT  
		Size: 18.7 KB (18698 bytes)  
		MIME: application/vnd.in-toto+json
