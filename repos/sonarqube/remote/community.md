## `sonarqube:community`

```console
$ docker pull sonarqube@sha256:0842dcd4c8f851ce44f8edaf45ac93f7c9079017d60d99f614663e60cef5efe9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:community` - linux; amd64

```console
$ docker pull sonarqube@sha256:ceee7008d2aeae082866c4261ea48692ef3b83d28fd382f1add5f71a04cc4921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.3 MB (856251179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3295fe6246ac5cd70112cd5633cd3bf18cdb418db23970f31c7352cd8129275`
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
LABEL io.k8s.description=SonarQube is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.non-scalable=true
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=10.7.0.96327
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.7.0.96327.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
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
	-	`sha256:524c194d4b54cced9285ea373fdffada17527ff65e10ccae25eb33bac44af469`  
		Last Modified: Thu, 24 Oct 2024 02:01:14 GMT  
		Size: 763.6 MB (763627870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0039a7530a90b0d3ea21c28a0151e8aebde68f6219e243c972ca3fd35b09c2`  
		Last Modified: Thu, 24 Oct 2024 02:00:57 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c9779b11519f4909383d00bcb24f1b1e158a31ea1fda50009e81c3525fa3f5c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0883694a54a103683fc457e919c5ddf715150d2b4d5bca7e913a235d8012b21d`

```dockerfile
```

-	Layers:
	-	`sha256:f5943ddb27158ac32a26dc1383bc562e51ce972b546aa8ae8003fa569eac87b7`  
		Last Modified: Thu, 24 Oct 2024 02:00:58 GMT  
		Size: 4.5 MB (4473196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:012231f7080d1f33c2ab24b8ac382006d6b8f4d9bdfcf9b0cc285fa7152a66ac`  
		Last Modified: Thu, 24 Oct 2024 02:00:57 GMT  
		Size: 19.1 KB (19135 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:community` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:83d0ed8914fe21a54f6461dff0b5c6523d3a79950869e02dc65387a7e6f9fb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.5 MB (853482627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52abef9d26ecaa15de0b931b194d812621b2220d042449eb75f855a84975937`
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
LABEL io.k8s.description=SonarQube is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.non-scalable=true
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=10.7.0.96327
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.7.0.96327.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
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
	-	`sha256:4bec9b5f92ec1be6be8dca07b52a44fb78a8ad168476c206f4953e44c2fc688f`  
		Last Modified: Thu, 24 Oct 2024 04:18:13 GMT  
		Size: 763.6 MB (763628392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666db0722bb851173192edfb280933092bdf614a05bf26aaff210ffd3284b43a`  
		Last Modified: Thu, 24 Oct 2024 04:17:53 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:079e4761f5588cea3da3ba178fc7f4f8a26f743a175aedb246474e7408416dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a653bcacb127a873b414c60ac7c69babdaf5ef0f34439693fc23512708d13cd`

```dockerfile
```

-	Layers:
	-	`sha256:53f060bb168a483aa02ff93eeb444c8b77e2a5136b2860f863e9a347db908e23`  
		Last Modified: Thu, 24 Oct 2024 04:17:53 GMT  
		Size: 4.5 MB (4472886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2889feb18802f75e172e66a9683bab9582657f6ffba5495f4e804b6158f92157`  
		Last Modified: Thu, 24 Oct 2024 04:17:53 GMT  
		Size: 19.3 KB (19251 bytes)  
		MIME: application/vnd.in-toto+json
