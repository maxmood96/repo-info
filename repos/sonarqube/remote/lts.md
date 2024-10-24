## `sonarqube:lts`

```console
$ docker pull sonarqube@sha256:aac4b3bdd2ae29c95e1a4c07bc50f0cc81d1914019bc609e92dee25e72ff2e6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:lts` - linux; amd64

```console
$ docker pull sonarqube@sha256:2bdc6320f1e507b3571dc529aebc256e12dbc3b6f20776ea8fffcd0fac8a480d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.0 MB (393026783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac691a09c8d92c2733734f09467c66249fa1422399cc1a40e51dd59e1ef626a6`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 30 Sep 2024 13:17:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 30 Sep 2024 13:17:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=9.9.7.96285
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.7.96285.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da8ec43a12ff631d1579ab778a0883e59bca58adc86136e1c447ef261a2b6e`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 16.1 MB (16142555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12988e90d6107a2cb56e2156831a2f5e31ac9d7d05cd4abc8fc28b53788d282`  
		Last Modified: Thu, 24 Oct 2024 00:57:17 GMT  
		Size: 46.9 MB (46942141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d133ca2b7f0fb899d954a051126f4c33bfa55975b531ad37c45821e2a63416`  
		Last Modified: Thu, 24 Oct 2024 00:57:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143733ae87a42f42df943534de9fa97f96f238e35ca89d480a4d1acc707d99e0`  
		Last Modified: Thu, 24 Oct 2024 00:57:16 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d021fe0fda1e287bceb40fccea1b9438e255dc791b1cadc3c0a97296020db9d1`  
		Last Modified: Thu, 24 Oct 2024 01:59:32 GMT  
		Size: 300.4 MB (300403475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc52ff982b3da71ef8ed028fd73ffbb59e4eaedf9d59bcfc4d8696270d6664a1`  
		Last Modified: Thu, 24 Oct 2024 01:59:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts` - unknown; unknown

```console
$ docker pull sonarqube@sha256:0e537d940540791723ffad9e2ea897b47bdc92a82362a5be1c0fed41f04d7088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4161059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8542c8c9c1a0edf8363b5763c90d308c19aff45b99bdc5fbab448100d7b48406`

```dockerfile
```

-	Layers:
	-	`sha256:a91b8d1ac75f85303026b72788434f041cbd414af7680ce7763e3e7872fecb78`  
		Last Modified: Thu, 24 Oct 2024 01:59:29 GMT  
		Size: 4.1 MB (4142479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3c8ab69c91377afe413196ec80286da4ef54daba8507a719ffc9091ff49d5cc`  
		Last Modified: Thu, 24 Oct 2024 01:59:29 GMT  
		Size: 18.6 KB (18580 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:lts` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:53fb976a9f4a45fa7984624027801d60fbeb9c3148faec0b2a9bdccc1bf195b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 MB (390257964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1ccbf4bcbbd324987a2b533d6f02ce44b61f70b661ba64b19f2db0306a6b2e`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 30 Sep 2024 13:17:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 30 Sep 2024 13:17:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=9.9.7.96285
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.7.96285.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4821edbf1831262baf113efdfde0f697240ca3efc1fbebee80c4279708d73f92`  
		Last Modified: Thu, 24 Oct 2024 00:58:15 GMT  
		Size: 16.1 MB (16062123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c88cd8dd8835e47c7a890ad7abd2ca59cf691145582518cf5843edbd6d6bfa0`  
		Last Modified: Thu, 24 Oct 2024 01:12:30 GMT  
		Size: 46.4 MB (46430856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c3c08b455337af9ba6b5fe522389a1d0a2b621fe437f3832a54289cac03397`  
		Last Modified: Thu, 24 Oct 2024 01:12:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26811a6e12de121df2970871f9027eb19d2c672b0045944972cf63a39c74aa15`  
		Last Modified: Thu, 24 Oct 2024 01:12:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfab34b189c7b7ae876af75232bb72051c97d31770524a9e9951bff2c1bef803`  
		Last Modified: Thu, 24 Oct 2024 04:02:59 GMT  
		Size: 300.4 MB (300403734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40769a467d877bfe23609c0ce58ea4f006831e4a986c52ac4f1871e99f671e8`  
		Last Modified: Thu, 24 Oct 2024 04:02:52 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts` - unknown; unknown

```console
$ docker pull sonarqube@sha256:0369ebb0adca4c664b1dfb783f75e9fc4ee008ec96e4936f22eb239be5aa6b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4160865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b07434545adadc3c756f81fe8d0a1c04b24d371f6bf9166c31ec27cf9af8bdd`

```dockerfile
```

-	Layers:
	-	`sha256:c85f92422571a192268b3d0f9c64793ad5a535e2a22b536fc4e9ee897d2bfd8c`  
		Last Modified: Thu, 24 Oct 2024 04:02:53 GMT  
		Size: 4.1 MB (4142169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:233e20c21aed5e62cfafe728e66c1d641f584d488c28c605345abfef05c8e967`  
		Last Modified: Thu, 24 Oct 2024 04:02:53 GMT  
		Size: 18.7 KB (18696 bytes)  
		MIME: application/vnd.in-toto+json
