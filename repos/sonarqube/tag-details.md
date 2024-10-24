<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sonarqube`

-	[`sonarqube:10-community`](#sonarqube10-community)
-	[`sonarqube:10-datacenter-app`](#sonarqube10-datacenter-app)
-	[`sonarqube:10-datacenter-search`](#sonarqube10-datacenter-search)
-	[`sonarqube:10-developer`](#sonarqube10-developer)
-	[`sonarqube:10-enterprise`](#sonarqube10-enterprise)
-	[`sonarqube:10.7-community`](#sonarqube107-community)
-	[`sonarqube:10.7-datacenter-app`](#sonarqube107-datacenter-app)
-	[`sonarqube:10.7-datacenter-search`](#sonarqube107-datacenter-search)
-	[`sonarqube:10.7-developer`](#sonarqube107-developer)
-	[`sonarqube:10.7-enterprise`](#sonarqube107-enterprise)
-	[`sonarqube:10.7.0-community`](#sonarqube1070-community)
-	[`sonarqube:10.7.0-datacenter-app`](#sonarqube1070-datacenter-app)
-	[`sonarqube:10.7.0-datacenter-search`](#sonarqube1070-datacenter-search)
-	[`sonarqube:10.7.0-developer`](#sonarqube1070-developer)
-	[`sonarqube:10.7.0-enterprise`](#sonarqube1070-enterprise)
-	[`sonarqube:9-community`](#sonarqube9-community)
-	[`sonarqube:9-datacenter-app`](#sonarqube9-datacenter-app)
-	[`sonarqube:9-datacenter-search`](#sonarqube9-datacenter-search)
-	[`sonarqube:9-developer`](#sonarqube9-developer)
-	[`sonarqube:9-enterprise`](#sonarqube9-enterprise)
-	[`sonarqube:9.9-community`](#sonarqube99-community)
-	[`sonarqube:9.9-datacenter-app`](#sonarqube99-datacenter-app)
-	[`sonarqube:9.9-datacenter-search`](#sonarqube99-datacenter-search)
-	[`sonarqube:9.9-developer`](#sonarqube99-developer)
-	[`sonarqube:9.9-enterprise`](#sonarqube99-enterprise)
-	[`sonarqube:9.9.7-community`](#sonarqube997-community)
-	[`sonarqube:9.9.7-datacenter-app`](#sonarqube997-datacenter-app)
-	[`sonarqube:9.9.7-datacenter-search`](#sonarqube997-datacenter-search)
-	[`sonarqube:9.9.7-developer`](#sonarqube997-developer)
-	[`sonarqube:9.9.7-enterprise`](#sonarqube997-enterprise)
-	[`sonarqube:community`](#sonarqubecommunity)
-	[`sonarqube:datacenter-app`](#sonarqubedatacenter-app)
-	[`sonarqube:datacenter-search`](#sonarqubedatacenter-search)
-	[`sonarqube:developer`](#sonarqubedeveloper)
-	[`sonarqube:enterprise`](#sonarqubeenterprise)
-	[`sonarqube:latest`](#sonarqubelatest)
-	[`sonarqube:lts`](#sonarqubelts)
-	[`sonarqube:lts-community`](#sonarqubelts-community)
-	[`sonarqube:lts-datacenter-app`](#sonarqubelts-datacenter-app)
-	[`sonarqube:lts-datacenter-search`](#sonarqubelts-datacenter-search)
-	[`sonarqube:lts-developer`](#sonarqubelts-developer)
-	[`sonarqube:lts-enterprise`](#sonarqubelts-enterprise)

## `sonarqube:10-community`

```console
$ docker pull sonarqube@sha256:0842dcd4c8f851ce44f8edaf45ac93f7c9079017d60d99f614663e60cef5efe9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10-community` - linux; amd64

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

### `sonarqube:10-community` - unknown; unknown

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

### `sonarqube:10-community` - linux; arm64 variant v8

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

### `sonarqube:10-community` - unknown; unknown

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

## `sonarqube:10-datacenter-app`

```console
$ docker pull sonarqube@sha256:ef1930ca425edb7405ef007e8604f719a9436ee213be63ee0dc6b476837f716b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:95962c53d5a8a2a581b752cffb5c0b0e75453cb7f303212ffa7fe3cc3d2dfc92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1092521785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ff27e729f54d54aea899ef845a9c16050fcb95e413583f5e709e58cac956cb`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
LABEL io.openshift.non-scalable=false
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=10.7.0.96327
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:54892ae41fabff8f7e10921196cdc7297e534454fc84863d5625427244a2846a`  
		Last Modified: Thu, 24 Oct 2024 02:01:49 GMT  
		Size: 999.9 MB (999897912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e277ee5d3785c23d91581a57494c3106115efdce13d87288ac4fa956c74be0`  
		Last Modified: Thu, 24 Oct 2024 02:01:34 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:b8922f56107e59c040cf3704f208f5a4d663bdef16f34b80be26f6b9155628a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6770a3064de3f64a317165df23f5fe64b39e0f97676ac27c7bf497cb509f66`

```dockerfile
```

-	Layers:
	-	`sha256:18c1f1d89f54b8d83663e5c75e9d96ede7afb7dd9e7b94fbbf384810e151dc5d`  
		Last Modified: Thu, 24 Oct 2024 02:01:34 GMT  
		Size: 4.7 MB (4720380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8b98769bc51a60851bc7f1cbc14dbce03f7175437292950981ec6c78916541`  
		Last Modified: Thu, 24 Oct 2024 02:01:34 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:10-datacenter-app` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:8254088b70af9ad7de2bd71f7dbaa2dee26e72934234645907e56f95aa3594fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1089757049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fb661cda7b3bd9e26cd597e01ee8749f7ff96021108c1698d0a9f364ddd716`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
LABEL io.openshift.non-scalable=false
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=10.7.0.96327
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:65fc7fe05bee7c8aacefac9e0bb798ad66de48168283e8e8f39faca69a0caa26`  
		Last Modified: Thu, 24 Oct 2024 04:32:32 GMT  
		Size: 999.9 MB (999902253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eac44f1defdbfcebd1fe73fffab37e5a885605c3539367f0e35bed458f1ecb`  
		Last Modified: Thu, 24 Oct 2024 04:32:12 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:8a66d05e4a36d072e68597998c2fc9d7245d4264e785f70294a3fa4769007dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ef3dd23d38100df94a9516034d87cd5faa5b5d9035dff8708da6b9623e6842`

```dockerfile
```

-	Layers:
	-	`sha256:ed47f36682c3fa013bd754c6146e9d5bb755acef814e96356300bfbab6aaaec3`  
		Last Modified: Thu, 24 Oct 2024 04:32:12 GMT  
		Size: 4.7 MB (4720064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12292ce537f772cdea93189d4060934b118eee2ae4aebdab8984f4934f995d2`  
		Last Modified: Thu, 24 Oct 2024 04:32:12 GMT  
		Size: 19.5 KB (19480 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:10-datacenter-search`

```console
$ docker pull sonarqube@sha256:79aa72ceb9c709b7c5e6622728fd6e30ba84c845d468517513cd14030b8fdf2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:71511bb366c1a0dc28a9baaebfbc2ced12ca5d0d6e41178e3e83eb95a9b8459d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1092521078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472fc3c8155a56dc8285e1e388b40f593a076f0865048b6a12afd99d71d48523`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
LABEL io.openshift.non-scalable=false
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=10.7.0.96327
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:cf4332291c90abac25a95c04a285e8115554b262a469cd932673961680d0011f`  
		Last Modified: Thu, 24 Oct 2024 02:02:01 GMT  
		Size: 999.9 MB (999897391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91e2666d7595c11789d058ab257035ef0199032edb9f4b2e75e780eae3e04f0`  
		Last Modified: Thu, 24 Oct 2024 02:01:47 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:bfadf30829c0434a13550cacbc2cfcbf17eed8ce3fcfcaa653f2b106722a85ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4737376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90474b2dc3213285fd9f68c915d48a3edc53ab7f18e16fe89042361ac32f7299`

```dockerfile
```

-	Layers:
	-	`sha256:23d3d184c8f2320f18c05af78753c60c9455fa7e428f968754aaf66d835e6530`  
		Last Modified: Thu, 24 Oct 2024 02:01:48 GMT  
		Size: 4.7 MB (4717837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87dfb045d6f68dad4feb6236dc4127d26d482856dd0c65e7690cd92783157b10`  
		Last Modified: Thu, 24 Oct 2024 02:01:47 GMT  
		Size: 19.5 KB (19539 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:10-datacenter-search` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:71e0feaf8c97c181b0ef68618f6c14dab3a32c051c6b983fc7b241b7f9687122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1089756136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:566bb84fd6c3dfc1b34bc2db6700b3b679c20013daa5ee4dfecccc8972c4661a`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
LABEL io.openshift.non-scalable=false
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=10.7.0.96327
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:044c80166f634a710e47324d2c91bdaf06690ef2582f83a6e08a924bc58f07a3`  
		Last Modified: Thu, 24 Oct 2024 04:37:08 GMT  
		Size: 999.9 MB (999901525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3d7c5503bbebafb6757b3139ef39d87d0e381238973889907913cbecbc9259`  
		Last Modified: Thu, 24 Oct 2024 04:36:48 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c197b4d81cd17cad58e1cf5faf7811669e3233903cd08c43fc2f27015b073cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4737164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f114eef7d6a4b9b5065f64df5a061157971dd0cc3bbd8897fec92c3bb166b5`

```dockerfile
```

-	Layers:
	-	`sha256:067c519dd9feceff6617a1b8b086070e2bb4d0bc6c60498298df41ae50771a08`  
		Last Modified: Thu, 24 Oct 2024 04:36:48 GMT  
		Size: 4.7 MB (4717521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b30ab60f1082327926a6b74972e7e2f818858c9972eba7502d80ce5c711727`  
		Last Modified: Thu, 24 Oct 2024 04:36:47 GMT  
		Size: 19.6 KB (19643 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:10-developer`

```console
$ docker pull sonarqube@sha256:7a5969f1f6dfc6652d95d9fcfe347fe671667afa6346d248a22a88c9706cb60b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:f15e7859cf41d05f733dd9f4cc2a9c5dc97855516332fc062b31ede148e058eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1061104119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc1feb369d7e690008703bd15512d6bbedb694cdd4758757e71e7faf915e884`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.7.0.96327.zip
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
	-	`sha256:fecdd26b0280f0316437679736231c7ead4f31d825c576ab0530cca5d113aef4`  
		Last Modified: Thu, 24 Oct 2024 02:02:15 GMT  
		Size: 968.5 MB (968480807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a1feba373d9fd1177f9e00002be1931749b13fa015c3e6be9962bc89a2a17`  
		Last Modified: Thu, 24 Oct 2024 02:01:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:1478fd9270cb3ba95d76e0ee61a09937d087e6da9a766f4e3e86b053102b26a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4607439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf6111f7019ad78cfb3d2b516b12ac5b14bd45d5a7022e62cfa7555a86f798a`

```dockerfile
```

-	Layers:
	-	`sha256:fe052cbc5cdbf918094f842f37b088322874fbd22550cca68dc2cddfe4f1c7df`  
		Last Modified: Thu, 24 Oct 2024 02:01:59 GMT  
		Size: 4.6 MB (4588539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc31480cd15349830b71cdc7220deb18a9a29703820cc15dfd72b639be575f6`  
		Last Modified: Thu, 24 Oct 2024 02:01:58 GMT  
		Size: 18.9 KB (18900 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:10-developer` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:21a787c8b748cd06ca47ffbc2c93eb2a7b8f5b8e01ea463845190663add1d2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1058335180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c52e6bf8af19f89ad9283d84d0bedd317615cc65c418a88022ac342aa90c10`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.7.0.96327.zip
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
	-	`sha256:ecf0b67713a8785a497d4da9a552ee07838d70dd12c8af9e042221e9892a0d67`  
		Last Modified: Thu, 24 Oct 2024 04:22:20 GMT  
		Size: 968.5 MB (968480945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd89bfb485033de0565747ec8c37a658558b4deaaa199375bc2c076d8f6529df`  
		Last Modified: Thu, 24 Oct 2024 04:22:01 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:af682ed22b57052041da13e9960484e4e214cd7ce5a18c84b2b80f50f3777e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4607222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24acefce8966ab5dd7872089a06dc99b2d3d36cae8cf568fe958650810446987`

```dockerfile
```

-	Layers:
	-	`sha256:e5539c9ec389bbb617686e349d34f80b8e803ff4cb3cf19dc5e58b0c10a3c014`  
		Last Modified: Thu, 24 Oct 2024 04:22:01 GMT  
		Size: 4.6 MB (4588217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0b5d1a6389d0c835d3e758e4888a9c44899d9540ef8618f6a01ee54373669a`  
		Last Modified: Thu, 24 Oct 2024 04:22:01 GMT  
		Size: 19.0 KB (19005 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:10-enterprise`

```console
$ docker pull sonarqube@sha256:74efc260974201a209ec102cf1c8fcddf21dbec0d3399ffd1dae98dab18e1aac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:f77325e6c9beaeeafe22ac6912714440a6a7e01bccf91433a9cbb4806c62e399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1090618072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc3838a079fecff6ab6225c6fd73fca2e244925ed169b11d9c9be5419949178`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-10.7.0.96327.zip
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
	-	`sha256:c2bef6a22930c9e75a6e8c4f5a8c7762c05d535da3a2172fe43800d6df781c12`  
		Last Modified: Thu, 24 Oct 2024 02:01:35 GMT  
		Size: 998.0 MB (997994761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e5ee9772edabff1d7918f81dc1e7e7b50294a9c13607a459b50d8d53780cf7`  
		Last Modified: Thu, 24 Oct 2024 02:01:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:e0013c9eb48ad44623788fe4da859606413efa89edb34dd027eafedc9b38d14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4663125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc62d21cf3049c09cb6c5b3439e1c78f8ca00188c67b4a08be2886f076b5b4b2`

```dockerfile
```

-	Layers:
	-	`sha256:7b60ccca8e67dfe3ca7343b13df4649fe20774856fd4a1aad2a1cb006d994d15`  
		Last Modified: Thu, 24 Oct 2024 02:01:20 GMT  
		Size: 4.6 MB (4644207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88a36430226a11211bd93fd6533f8ba2383fed4d64ebe18fb0a1c06e0f95cdea`  
		Last Modified: Thu, 24 Oct 2024 02:01:19 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:10-enterprise` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:8bddfdfcbd01b606913880ad92d16894047b1f543e89aaaeee8ce31b7e4fd7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1087849247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466b7455c1291198dd4732c92c25f776f014a0bec27cef63235d74fa04ecf5e7`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-10.7.0.96327.zip
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
	-	`sha256:6bba52a69c784fc1e8d5dfb3f08afab554d7e4f759debf36eab7c3c346a9ca44`  
		Last Modified: Thu, 24 Oct 2024 04:26:41 GMT  
		Size: 998.0 MB (997995012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b58fd8fe5d25d94fbefa8249364231858dca5e79682973bd066fb4570414c`  
		Last Modified: Thu, 24 Oct 2024 04:26:17 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:d2d769e03a67fcd8fd2dad43a5dc5296952d2eb91c740c9f8b679813de5c2b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4662907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a578769c4fbcf2f0651b940cc25efcc9d73fa32b853c7bc800f6af7dfdb8293`

```dockerfile
```

-	Layers:
	-	`sha256:4ce4970bddb06a66363b1c730319b7d13f7b45f54d10f3232766d3815a5c7399`  
		Last Modified: Thu, 24 Oct 2024 04:26:17 GMT  
		Size: 4.6 MB (4643885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51ecd76e9a030f6a4899b8a93a4f5f328a747ffa46bbef965d6968af84c186cb`  
		Last Modified: Thu, 24 Oct 2024 04:26:17 GMT  
		Size: 19.0 KB (19022 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:10.7-community`

```console
$ docker pull sonarqube@sha256:0842dcd4c8f851ce44f8edaf45ac93f7c9079017d60d99f614663e60cef5efe9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10.7-community` - linux; amd64

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

### `sonarqube:10.7-community` - unknown; unknown

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

### `sonarqube:10.7-community` - linux; arm64 variant v8

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

### `sonarqube:10.7-community` - unknown; unknown

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

## `sonarqube:10.7-datacenter-app`

```console
$ docker pull sonarqube@sha256:ef1930ca425edb7405ef007e8604f719a9436ee213be63ee0dc6b476837f716b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10.7-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:95962c53d5a8a2a581b752cffb5c0b0e75453cb7f303212ffa7fe3cc3d2dfc92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1092521785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ff27e729f54d54aea899ef845a9c16050fcb95e413583f5e709e58cac956cb`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
LABEL io.openshift.non-scalable=false
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=10.7.0.96327
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:54892ae41fabff8f7e10921196cdc7297e534454fc84863d5625427244a2846a`  
		Last Modified: Thu, 24 Oct 2024 02:01:49 GMT  
		Size: 999.9 MB (999897912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e277ee5d3785c23d91581a57494c3106115efdce13d87288ac4fa956c74be0`  
		Last Modified: Thu, 24 Oct 2024 02:01:34 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10.7-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:b8922f56107e59c040cf3704f208f5a4d663bdef16f34b80be26f6b9155628a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6770a3064de3f64a317165df23f5fe64b39e0f97676ac27c7bf497cb509f66`

```dockerfile
```

-	Layers:
	-	`sha256:18c1f1d89f54b8d83663e5c75e9d96ede7afb7dd9e7b94fbbf384810e151dc5d`  
		Last Modified: Thu, 24 Oct 2024 02:01:34 GMT  
		Size: 4.7 MB (4720380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8b98769bc51a60851bc7f1cbc14dbce03f7175437292950981ec6c78916541`  
		Last Modified: Thu, 24 Oct 2024 02:01:34 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:10.7-datacenter-app` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:8254088b70af9ad7de2bd71f7dbaa2dee26e72934234645907e56f95aa3594fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1089757049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fb661cda7b3bd9e26cd597e01ee8749f7ff96021108c1698d0a9f364ddd716`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
LABEL io.openshift.non-scalable=false
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=10.7.0.96327
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:65fc7fe05bee7c8aacefac9e0bb798ad66de48168283e8e8f39faca69a0caa26`  
		Last Modified: Thu, 24 Oct 2024 04:32:32 GMT  
		Size: 999.9 MB (999902253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eac44f1defdbfcebd1fe73fffab37e5a885605c3539367f0e35bed458f1ecb`  
		Last Modified: Thu, 24 Oct 2024 04:32:12 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10.7-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:8a66d05e4a36d072e68597998c2fc9d7245d4264e785f70294a3fa4769007dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ef3dd23d38100df94a9516034d87cd5faa5b5d9035dff8708da6b9623e6842`

```dockerfile
```

-	Layers:
	-	`sha256:ed47f36682c3fa013bd754c6146e9d5bb755acef814e96356300bfbab6aaaec3`  
		Last Modified: Thu, 24 Oct 2024 04:32:12 GMT  
		Size: 4.7 MB (4720064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12292ce537f772cdea93189d4060934b118eee2ae4aebdab8984f4934f995d2`  
		Last Modified: Thu, 24 Oct 2024 04:32:12 GMT  
		Size: 19.5 KB (19480 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:10.7-datacenter-search`

```console
$ docker pull sonarqube@sha256:79aa72ceb9c709b7c5e6622728fd6e30ba84c845d468517513cd14030b8fdf2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10.7-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:71511bb366c1a0dc28a9baaebfbc2ced12ca5d0d6e41178e3e83eb95a9b8459d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1092521078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472fc3c8155a56dc8285e1e388b40f593a076f0865048b6a12afd99d71d48523`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
LABEL io.openshift.non-scalable=false
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=10.7.0.96327
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:cf4332291c90abac25a95c04a285e8115554b262a469cd932673961680d0011f`  
		Last Modified: Thu, 24 Oct 2024 02:02:01 GMT  
		Size: 999.9 MB (999897391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91e2666d7595c11789d058ab257035ef0199032edb9f4b2e75e780eae3e04f0`  
		Last Modified: Thu, 24 Oct 2024 02:01:47 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10.7-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:bfadf30829c0434a13550cacbc2cfcbf17eed8ce3fcfcaa653f2b106722a85ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4737376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90474b2dc3213285fd9f68c915d48a3edc53ab7f18e16fe89042361ac32f7299`

```dockerfile
```

-	Layers:
	-	`sha256:23d3d184c8f2320f18c05af78753c60c9455fa7e428f968754aaf66d835e6530`  
		Last Modified: Thu, 24 Oct 2024 02:01:48 GMT  
		Size: 4.7 MB (4717837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87dfb045d6f68dad4feb6236dc4127d26d482856dd0c65e7690cd92783157b10`  
		Last Modified: Thu, 24 Oct 2024 02:01:47 GMT  
		Size: 19.5 KB (19539 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:10.7-datacenter-search` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:71e0feaf8c97c181b0ef68618f6c14dab3a32c051c6b983fc7b241b7f9687122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1089756136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:566bb84fd6c3dfc1b34bc2db6700b3b679c20013daa5ee4dfecccc8972c4661a`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
LABEL io.openshift.non-scalable=false
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=10.7.0.96327
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:044c80166f634a710e47324d2c91bdaf06690ef2582f83a6e08a924bc58f07a3`  
		Last Modified: Thu, 24 Oct 2024 04:37:08 GMT  
		Size: 999.9 MB (999901525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3d7c5503bbebafb6757b3139ef39d87d0e381238973889907913cbecbc9259`  
		Last Modified: Thu, 24 Oct 2024 04:36:48 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10.7-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c197b4d81cd17cad58e1cf5faf7811669e3233903cd08c43fc2f27015b073cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4737164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f114eef7d6a4b9b5065f64df5a061157971dd0cc3bbd8897fec92c3bb166b5`

```dockerfile
```

-	Layers:
	-	`sha256:067c519dd9feceff6617a1b8b086070e2bb4d0bc6c60498298df41ae50771a08`  
		Last Modified: Thu, 24 Oct 2024 04:36:48 GMT  
		Size: 4.7 MB (4717521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b30ab60f1082327926a6b74972e7e2f818858c9972eba7502d80ce5c711727`  
		Last Modified: Thu, 24 Oct 2024 04:36:47 GMT  
		Size: 19.6 KB (19643 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:10.7-developer`

```console
$ docker pull sonarqube@sha256:7a5969f1f6dfc6652d95d9fcfe347fe671667afa6346d248a22a88c9706cb60b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10.7-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:f15e7859cf41d05f733dd9f4cc2a9c5dc97855516332fc062b31ede148e058eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1061104119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc1feb369d7e690008703bd15512d6bbedb694cdd4758757e71e7faf915e884`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.7.0.96327.zip
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
	-	`sha256:fecdd26b0280f0316437679736231c7ead4f31d825c576ab0530cca5d113aef4`  
		Last Modified: Thu, 24 Oct 2024 02:02:15 GMT  
		Size: 968.5 MB (968480807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a1feba373d9fd1177f9e00002be1931749b13fa015c3e6be9962bc89a2a17`  
		Last Modified: Thu, 24 Oct 2024 02:01:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10.7-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:1478fd9270cb3ba95d76e0ee61a09937d087e6da9a766f4e3e86b053102b26a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4607439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf6111f7019ad78cfb3d2b516b12ac5b14bd45d5a7022e62cfa7555a86f798a`

```dockerfile
```

-	Layers:
	-	`sha256:fe052cbc5cdbf918094f842f37b088322874fbd22550cca68dc2cddfe4f1c7df`  
		Last Modified: Thu, 24 Oct 2024 02:01:59 GMT  
		Size: 4.6 MB (4588539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc31480cd15349830b71cdc7220deb18a9a29703820cc15dfd72b639be575f6`  
		Last Modified: Thu, 24 Oct 2024 02:01:58 GMT  
		Size: 18.9 KB (18900 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:10.7-developer` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:21a787c8b748cd06ca47ffbc2c93eb2a7b8f5b8e01ea463845190663add1d2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1058335180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c52e6bf8af19f89ad9283d84d0bedd317615cc65c418a88022ac342aa90c10`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.7.0.96327.zip
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
	-	`sha256:ecf0b67713a8785a497d4da9a552ee07838d70dd12c8af9e042221e9892a0d67`  
		Last Modified: Thu, 24 Oct 2024 04:22:20 GMT  
		Size: 968.5 MB (968480945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd89bfb485033de0565747ec8c37a658558b4deaaa199375bc2c076d8f6529df`  
		Last Modified: Thu, 24 Oct 2024 04:22:01 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10.7-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:af682ed22b57052041da13e9960484e4e214cd7ce5a18c84b2b80f50f3777e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4607222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24acefce8966ab5dd7872089a06dc99b2d3d36cae8cf568fe958650810446987`

```dockerfile
```

-	Layers:
	-	`sha256:e5539c9ec389bbb617686e349d34f80b8e803ff4cb3cf19dc5e58b0c10a3c014`  
		Last Modified: Thu, 24 Oct 2024 04:22:01 GMT  
		Size: 4.6 MB (4588217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0b5d1a6389d0c835d3e758e4888a9c44899d9540ef8618f6a01ee54373669a`  
		Last Modified: Thu, 24 Oct 2024 04:22:01 GMT  
		Size: 19.0 KB (19005 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:10.7-enterprise`

```console
$ docker pull sonarqube@sha256:74efc260974201a209ec102cf1c8fcddf21dbec0d3399ffd1dae98dab18e1aac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10.7-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:f77325e6c9beaeeafe22ac6912714440a6a7e01bccf91433a9cbb4806c62e399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1090618072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc3838a079fecff6ab6225c6fd73fca2e244925ed169b11d9c9be5419949178`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-10.7.0.96327.zip
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
	-	`sha256:c2bef6a22930c9e75a6e8c4f5a8c7762c05d535da3a2172fe43800d6df781c12`  
		Last Modified: Thu, 24 Oct 2024 02:01:35 GMT  
		Size: 998.0 MB (997994761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e5ee9772edabff1d7918f81dc1e7e7b50294a9c13607a459b50d8d53780cf7`  
		Last Modified: Thu, 24 Oct 2024 02:01:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10.7-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:e0013c9eb48ad44623788fe4da859606413efa89edb34dd027eafedc9b38d14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4663125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc62d21cf3049c09cb6c5b3439e1c78f8ca00188c67b4a08be2886f076b5b4b2`

```dockerfile
```

-	Layers:
	-	`sha256:7b60ccca8e67dfe3ca7343b13df4649fe20774856fd4a1aad2a1cb006d994d15`  
		Last Modified: Thu, 24 Oct 2024 02:01:20 GMT  
		Size: 4.6 MB (4644207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88a36430226a11211bd93fd6533f8ba2383fed4d64ebe18fb0a1c06e0f95cdea`  
		Last Modified: Thu, 24 Oct 2024 02:01:19 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:10.7-enterprise` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:8bddfdfcbd01b606913880ad92d16894047b1f543e89aaaeee8ce31b7e4fd7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1087849247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466b7455c1291198dd4732c92c25f776f014a0bec27cef63235d74fa04ecf5e7`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-10.7.0.96327.zip
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
	-	`sha256:6bba52a69c784fc1e8d5dfb3f08afab554d7e4f759debf36eab7c3c346a9ca44`  
		Last Modified: Thu, 24 Oct 2024 04:26:41 GMT  
		Size: 998.0 MB (997995012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b58fd8fe5d25d94fbefa8249364231858dca5e79682973bd066fb4570414c`  
		Last Modified: Thu, 24 Oct 2024 04:26:17 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10.7-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:d2d769e03a67fcd8fd2dad43a5dc5296952d2eb91c740c9f8b679813de5c2b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4662907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a578769c4fbcf2f0651b940cc25efcc9d73fa32b853c7bc800f6af7dfdb8293`

```dockerfile
```

-	Layers:
	-	`sha256:4ce4970bddb06a66363b1c730319b7d13f7b45f54d10f3232766d3815a5c7399`  
		Last Modified: Thu, 24 Oct 2024 04:26:17 GMT  
		Size: 4.6 MB (4643885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51ecd76e9a030f6a4899b8a93a4f5f328a747ffa46bbef965d6968af84c186cb`  
		Last Modified: Thu, 24 Oct 2024 04:26:17 GMT  
		Size: 19.0 KB (19022 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:10.7.0-community`

```console
$ docker pull sonarqube@sha256:0842dcd4c8f851ce44f8edaf45ac93f7c9079017d60d99f614663e60cef5efe9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10.7.0-community` - linux; amd64

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

### `sonarqube:10.7.0-community` - unknown; unknown

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

### `sonarqube:10.7.0-community` - linux; arm64 variant v8

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

### `sonarqube:10.7.0-community` - unknown; unknown

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

## `sonarqube:10.7.0-datacenter-app`

```console
$ docker pull sonarqube@sha256:ef1930ca425edb7405ef007e8604f719a9436ee213be63ee0dc6b476837f716b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10.7.0-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:95962c53d5a8a2a581b752cffb5c0b0e75453cb7f303212ffa7fe3cc3d2dfc92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1092521785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ff27e729f54d54aea899ef845a9c16050fcb95e413583f5e709e58cac956cb`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
LABEL io.openshift.non-scalable=false
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=10.7.0.96327
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:54892ae41fabff8f7e10921196cdc7297e534454fc84863d5625427244a2846a`  
		Last Modified: Thu, 24 Oct 2024 02:01:49 GMT  
		Size: 999.9 MB (999897912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e277ee5d3785c23d91581a57494c3106115efdce13d87288ac4fa956c74be0`  
		Last Modified: Thu, 24 Oct 2024 02:01:34 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10.7.0-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:b8922f56107e59c040cf3704f208f5a4d663bdef16f34b80be26f6b9155628a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6770a3064de3f64a317165df23f5fe64b39e0f97676ac27c7bf497cb509f66`

```dockerfile
```

-	Layers:
	-	`sha256:18c1f1d89f54b8d83663e5c75e9d96ede7afb7dd9e7b94fbbf384810e151dc5d`  
		Last Modified: Thu, 24 Oct 2024 02:01:34 GMT  
		Size: 4.7 MB (4720380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8b98769bc51a60851bc7f1cbc14dbce03f7175437292950981ec6c78916541`  
		Last Modified: Thu, 24 Oct 2024 02:01:34 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:10.7.0-datacenter-app` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:8254088b70af9ad7de2bd71f7dbaa2dee26e72934234645907e56f95aa3594fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1089757049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fb661cda7b3bd9e26cd597e01ee8749f7ff96021108c1698d0a9f364ddd716`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
LABEL io.openshift.non-scalable=false
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=10.7.0.96327
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:65fc7fe05bee7c8aacefac9e0bb798ad66de48168283e8e8f39faca69a0caa26`  
		Last Modified: Thu, 24 Oct 2024 04:32:32 GMT  
		Size: 999.9 MB (999902253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eac44f1defdbfcebd1fe73fffab37e5a885605c3539367f0e35bed458f1ecb`  
		Last Modified: Thu, 24 Oct 2024 04:32:12 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10.7.0-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:8a66d05e4a36d072e68597998c2fc9d7245d4264e785f70294a3fa4769007dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ef3dd23d38100df94a9516034d87cd5faa5b5d9035dff8708da6b9623e6842`

```dockerfile
```

-	Layers:
	-	`sha256:ed47f36682c3fa013bd754c6146e9d5bb755acef814e96356300bfbab6aaaec3`  
		Last Modified: Thu, 24 Oct 2024 04:32:12 GMT  
		Size: 4.7 MB (4720064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12292ce537f772cdea93189d4060934b118eee2ae4aebdab8984f4934f995d2`  
		Last Modified: Thu, 24 Oct 2024 04:32:12 GMT  
		Size: 19.5 KB (19480 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:10.7.0-datacenter-search`

```console
$ docker pull sonarqube@sha256:79aa72ceb9c709b7c5e6622728fd6e30ba84c845d468517513cd14030b8fdf2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10.7.0-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:71511bb366c1a0dc28a9baaebfbc2ced12ca5d0d6e41178e3e83eb95a9b8459d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1092521078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472fc3c8155a56dc8285e1e388b40f593a076f0865048b6a12afd99d71d48523`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
LABEL io.openshift.non-scalable=false
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=10.7.0.96327
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:cf4332291c90abac25a95c04a285e8115554b262a469cd932673961680d0011f`  
		Last Modified: Thu, 24 Oct 2024 02:02:01 GMT  
		Size: 999.9 MB (999897391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91e2666d7595c11789d058ab257035ef0199032edb9f4b2e75e780eae3e04f0`  
		Last Modified: Thu, 24 Oct 2024 02:01:47 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10.7.0-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:bfadf30829c0434a13550cacbc2cfcbf17eed8ce3fcfcaa653f2b106722a85ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4737376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90474b2dc3213285fd9f68c915d48a3edc53ab7f18e16fe89042361ac32f7299`

```dockerfile
```

-	Layers:
	-	`sha256:23d3d184c8f2320f18c05af78753c60c9455fa7e428f968754aaf66d835e6530`  
		Last Modified: Thu, 24 Oct 2024 02:01:48 GMT  
		Size: 4.7 MB (4717837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87dfb045d6f68dad4feb6236dc4127d26d482856dd0c65e7690cd92783157b10`  
		Last Modified: Thu, 24 Oct 2024 02:01:47 GMT  
		Size: 19.5 KB (19539 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:10.7.0-datacenter-search` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:71e0feaf8c97c181b0ef68618f6c14dab3a32c051c6b983fc7b241b7f9687122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1089756136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:566bb84fd6c3dfc1b34bc2db6700b3b679c20013daa5ee4dfecccc8972c4661a`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
LABEL io.openshift.non-scalable=false
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=10.7.0.96327
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:044c80166f634a710e47324d2c91bdaf06690ef2582f83a6e08a924bc58f07a3`  
		Last Modified: Thu, 24 Oct 2024 04:37:08 GMT  
		Size: 999.9 MB (999901525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3d7c5503bbebafb6757b3139ef39d87d0e381238973889907913cbecbc9259`  
		Last Modified: Thu, 24 Oct 2024 04:36:48 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10.7.0-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c197b4d81cd17cad58e1cf5faf7811669e3233903cd08c43fc2f27015b073cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4737164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f114eef7d6a4b9b5065f64df5a061157971dd0cc3bbd8897fec92c3bb166b5`

```dockerfile
```

-	Layers:
	-	`sha256:067c519dd9feceff6617a1b8b086070e2bb4d0bc6c60498298df41ae50771a08`  
		Last Modified: Thu, 24 Oct 2024 04:36:48 GMT  
		Size: 4.7 MB (4717521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b30ab60f1082327926a6b74972e7e2f818858c9972eba7502d80ce5c711727`  
		Last Modified: Thu, 24 Oct 2024 04:36:47 GMT  
		Size: 19.6 KB (19643 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:10.7.0-developer`

```console
$ docker pull sonarqube@sha256:7a5969f1f6dfc6652d95d9fcfe347fe671667afa6346d248a22a88c9706cb60b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10.7.0-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:f15e7859cf41d05f733dd9f4cc2a9c5dc97855516332fc062b31ede148e058eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1061104119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc1feb369d7e690008703bd15512d6bbedb694cdd4758757e71e7faf915e884`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.7.0.96327.zip
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
	-	`sha256:fecdd26b0280f0316437679736231c7ead4f31d825c576ab0530cca5d113aef4`  
		Last Modified: Thu, 24 Oct 2024 02:02:15 GMT  
		Size: 968.5 MB (968480807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a1feba373d9fd1177f9e00002be1931749b13fa015c3e6be9962bc89a2a17`  
		Last Modified: Thu, 24 Oct 2024 02:01:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10.7.0-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:1478fd9270cb3ba95d76e0ee61a09937d087e6da9a766f4e3e86b053102b26a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4607439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf6111f7019ad78cfb3d2b516b12ac5b14bd45d5a7022e62cfa7555a86f798a`

```dockerfile
```

-	Layers:
	-	`sha256:fe052cbc5cdbf918094f842f37b088322874fbd22550cca68dc2cddfe4f1c7df`  
		Last Modified: Thu, 24 Oct 2024 02:01:59 GMT  
		Size: 4.6 MB (4588539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc31480cd15349830b71cdc7220deb18a9a29703820cc15dfd72b639be575f6`  
		Last Modified: Thu, 24 Oct 2024 02:01:58 GMT  
		Size: 18.9 KB (18900 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:10.7.0-developer` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:21a787c8b748cd06ca47ffbc2c93eb2a7b8f5b8e01ea463845190663add1d2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1058335180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c52e6bf8af19f89ad9283d84d0bedd317615cc65c418a88022ac342aa90c10`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.7.0.96327.zip
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
	-	`sha256:ecf0b67713a8785a497d4da9a552ee07838d70dd12c8af9e042221e9892a0d67`  
		Last Modified: Thu, 24 Oct 2024 04:22:20 GMT  
		Size: 968.5 MB (968480945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd89bfb485033de0565747ec8c37a658558b4deaaa199375bc2c076d8f6529df`  
		Last Modified: Thu, 24 Oct 2024 04:22:01 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10.7.0-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:af682ed22b57052041da13e9960484e4e214cd7ce5a18c84b2b80f50f3777e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4607222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24acefce8966ab5dd7872089a06dc99b2d3d36cae8cf568fe958650810446987`

```dockerfile
```

-	Layers:
	-	`sha256:e5539c9ec389bbb617686e349d34f80b8e803ff4cb3cf19dc5e58b0c10a3c014`  
		Last Modified: Thu, 24 Oct 2024 04:22:01 GMT  
		Size: 4.6 MB (4588217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0b5d1a6389d0c835d3e758e4888a9c44899d9540ef8618f6a01ee54373669a`  
		Last Modified: Thu, 24 Oct 2024 04:22:01 GMT  
		Size: 19.0 KB (19005 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:10.7.0-enterprise`

```console
$ docker pull sonarqube@sha256:74efc260974201a209ec102cf1c8fcddf21dbec0d3399ffd1dae98dab18e1aac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:10.7.0-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:f77325e6c9beaeeafe22ac6912714440a6a7e01bccf91433a9cbb4806c62e399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1090618072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc3838a079fecff6ab6225c6fd73fca2e244925ed169b11d9c9be5419949178`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-10.7.0.96327.zip
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
	-	`sha256:c2bef6a22930c9e75a6e8c4f5a8c7762c05d535da3a2172fe43800d6df781c12`  
		Last Modified: Thu, 24 Oct 2024 02:01:35 GMT  
		Size: 998.0 MB (997994761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e5ee9772edabff1d7918f81dc1e7e7b50294a9c13607a459b50d8d53780cf7`  
		Last Modified: Thu, 24 Oct 2024 02:01:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10.7.0-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:e0013c9eb48ad44623788fe4da859606413efa89edb34dd027eafedc9b38d14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4663125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc62d21cf3049c09cb6c5b3439e1c78f8ca00188c67b4a08be2886f076b5b4b2`

```dockerfile
```

-	Layers:
	-	`sha256:7b60ccca8e67dfe3ca7343b13df4649fe20774856fd4a1aad2a1cb006d994d15`  
		Last Modified: Thu, 24 Oct 2024 02:01:20 GMT  
		Size: 4.6 MB (4644207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88a36430226a11211bd93fd6533f8ba2383fed4d64ebe18fb0a1c06e0f95cdea`  
		Last Modified: Thu, 24 Oct 2024 02:01:19 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:10.7.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:8bddfdfcbd01b606913880ad92d16894047b1f543e89aaaeee8ce31b7e4fd7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1087849247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466b7455c1291198dd4732c92c25f776f014a0bec27cef63235d74fa04ecf5e7`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-10.7.0.96327.zip
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
	-	`sha256:6bba52a69c784fc1e8d5dfb3f08afab554d7e4f759debf36eab7c3c346a9ca44`  
		Last Modified: Thu, 24 Oct 2024 04:26:41 GMT  
		Size: 998.0 MB (997995012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b58fd8fe5d25d94fbefa8249364231858dca5e79682973bd066fb4570414c`  
		Last Modified: Thu, 24 Oct 2024 04:26:17 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:10.7.0-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:d2d769e03a67fcd8fd2dad43a5dc5296952d2eb91c740c9f8b679813de5c2b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4662907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a578769c4fbcf2f0651b940cc25efcc9d73fa32b853c7bc800f6af7dfdb8293`

```dockerfile
```

-	Layers:
	-	`sha256:4ce4970bddb06a66363b1c730319b7d13f7b45f54d10f3232766d3815a5c7399`  
		Last Modified: Thu, 24 Oct 2024 04:26:17 GMT  
		Size: 4.6 MB (4643885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51ecd76e9a030f6a4899b8a93a4f5f328a747ffa46bbef965d6968af84c186cb`  
		Last Modified: Thu, 24 Oct 2024 04:26:17 GMT  
		Size: 19.0 KB (19022 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9-community`

```console
$ docker pull sonarqube@sha256:aac4b3bdd2ae29c95e1a4c07bc50f0cc81d1914019bc609e92dee25e72ff2e6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9-community` - linux; amd64

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

### `sonarqube:9-community` - unknown; unknown

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

### `sonarqube:9-community` - linux; arm64 variant v8

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

### `sonarqube:9-community` - unknown; unknown

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

## `sonarqube:9-datacenter-app`

```console
$ docker pull sonarqube@sha256:7d8becfd63badc3595509042806e247a8c038801992fee4be9163b31e43ae004
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:823a79a86f3ddce51330c9f78475e9f8456361c88abefa74fa885aecd7f29caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.5 MB (531507425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c094cbf5e17a638a8f4af7a4ad281dd626d96f345f8c404da0d431b1683446ae`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:2613306c89ad885ff61bbee43304cee6653d7270e06839b7c6f05445ae8992c2`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 438.9 MB (438883561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438d4defa76781348b781b64cb2c54dd09fdad44cb440bc973fe5f9477fe8321`  
		Last Modified: Thu, 24 Oct 2024 02:00:20 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:d33c6dafa9b5a4674fd8032ef17fab08dba61a02be9b3d12345ad66a3fdc6819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cb896e079a7aad5ca48183e9c0e336463f9267591a9374c770266c66e400e4`

```dockerfile
```

-	Layers:
	-	`sha256:f0e8b119ce66d55466575038abf4aa3f29a4bd89b51e10e156056857a5e47fe1`  
		Last Modified: Thu, 24 Oct 2024 02:00:19 GMT  
		Size: 4.4 MB (4447738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b043c8090ad8dd90bfc3c92e76e37a91f6e0c57acf7313e18262743357ac9d`  
		Last Modified: Thu, 24 Oct 2024 02:00:19 GMT  
		Size: 19.0 KB (18959 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9-datacenter-app` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:9175a5a95c447cccc9c73c7ecb4886d012a6d3d548afc97dc2aa1ea481a97107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528751109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec3aa4fbce04433b70f920bf51c4c3ab4571f4d92599d35e2cad775cec884b3`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:af01c6c6696ce891c43d463ad31a69c8bc8538c422baefd126848e554bc05367`  
		Last Modified: Thu, 24 Oct 2024 04:11:50 GMT  
		Size: 438.9 MB (438896318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96f764d9405d67e11000092e70d024be10f106adf5176097c7333696cf7a962`  
		Last Modified: Thu, 24 Oct 2024 04:11:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:11baba515404e338714733900af05b24b950146cc3a7a412dceeb4b9b6e49ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288f2776c897a531d3c6b11e46c7da7733ef1d466042f98dd99e8a55cca79d06`

```dockerfile
```

-	Layers:
	-	`sha256:8788dfbc83b3f64d3aa1a9f58a5a5f596aac62847adf755a0b8cc45989ede422`  
		Last Modified: Thu, 24 Oct 2024 04:11:37 GMT  
		Size: 4.4 MB (4447422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b57b8aad45ac3ac19d9246fcb44a9d10f68f8ee9af2c78319176cb0da735fa4d`  
		Last Modified: Thu, 24 Oct 2024 04:11:36 GMT  
		Size: 19.1 KB (19062 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9-datacenter-search`

```console
$ docker pull sonarqube@sha256:592541ad310dc6c22cd04e9dc3399c455ce0e21682d907d14b4380dd7db9d0d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:466b7213f87a1706fbb7a683aac68058adae3b4abd905ec828d65e846682435b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.5 MB (531507148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a594ef908cc1ebf1b970ac29e3daeb9969a54c17ecf8d874398ce6b0198cae`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:5afbdea98b0b5385aae5b7fff15ea78eb3daef029dd6cec1df14a051c04f559e`  
		Last Modified: Thu, 24 Oct 2024 02:00:25 GMT  
		Size: 438.9 MB (438883466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea47e3260b78d50e74adfbb9cc0360e2e4f72310ecec48eb226bba3db8dbeb3b`  
		Last Modified: Thu, 24 Oct 2024 02:00:17 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:333a532301764ce8c52b6a507ea5d27f5fc5c13ec425add792e849ab79e369c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d03138d7b20cfa8f37d9979ac105b5eb44390647a1def293523a4d1ea0b19f`

```dockerfile
```

-	Layers:
	-	`sha256:02ba3c41cb26478c27571401e8414343fa5f8e73b0b236ec0443a2a670ff65bf`  
		Last Modified: Thu, 24 Oct 2024 02:00:18 GMT  
		Size: 4.4 MB (4447762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4268506be65a644c6fd4c234a2fec4dd56a142faf19d08a40ee8c3dd7a9315b`  
		Last Modified: Thu, 24 Oct 2024 02:00:17 GMT  
		Size: 19.0 KB (18977 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9-datacenter-search` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:467f97abb0db146aec6788308348d2479d0dc5acd3d3a09b7d886e13451ea938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528750977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4990516c466d71d46bc3bd46919bab8b4bf280f2afc7fc1b65e33ba49a3192c2`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:95815674d1caddea6b23073271e56ed0c4046668a762ac42b9b18ae515a33f20`  
		Last Modified: Thu, 24 Oct 2024 04:14:34 GMT  
		Size: 438.9 MB (438896369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76d67b22b21217e97691c0e9771ee65f015bb9f0a651154efe94ad45786d369`  
		Last Modified: Thu, 24 Oct 2024 04:14:25 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:a22c61e93f1b5a24d2ac9d5e9408b3668a89d819271218625c596682b2977f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ed5cd3a22a2b81d43018d5af833e6c1e903afcb59c72fa1539f75bca92d05e`

```dockerfile
```

-	Layers:
	-	`sha256:873568fb19337ffac9253c26c4c107a7aba32e8736c8ad07e76180f6d2b759e8`  
		Last Modified: Thu, 24 Oct 2024 04:14:25 GMT  
		Size: 4.4 MB (4447446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb159655442cd35f6f080ffdf005605960c641b8662d754cec3d6d5c7cf4b98e`  
		Last Modified: Thu, 24 Oct 2024 04:14:25 GMT  
		Size: 19.1 KB (19081 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9-developer`

```console
$ docker pull sonarqube@sha256:d6441aaf3dcbe1c09b378f0a2fd0986204b71eaa33b666534991187fd792bd18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:7bd290744873c0815af823221227ba65af67ac13e30dedaac999636283a86654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.6 MB (487579508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e769c8db61a613236e2cb4679b17c75b5a25d1191d9a26da76f08f74bc235e86`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.7.96285.zip
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
	-	`sha256:102e4e58c7dee0f767acdbda4d2c400e42e8571b31ebeb1a230a4bae4ddef412`  
		Last Modified: Thu, 24 Oct 2024 01:59:53 GMT  
		Size: 395.0 MB (394956203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1036433ccfdd8890ca3b7e7a807c564b07d24ead1e22ebc50ecbd78a07f630`  
		Last Modified: Thu, 24 Oct 2024 01:59:48 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:0bc4f8bc041cc7050bd443e5a11e921fa75f2873efc595b409e0f998bbc7e61b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4277076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cac190262137392ce4eba452ec2191fe84b7f1c94d76a3ee24bac11af67e94`

```dockerfile
```

-	Layers:
	-	`sha256:c173f98c0a4093565aef96e15829618f407d33470e6acf6a4eeae9e1e4438cb6`  
		Last Modified: Thu, 24 Oct 2024 01:59:48 GMT  
		Size: 4.3 MB (4258724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62fe39f9c55024151dffdb09b34fc0dcc7054f45cef402aa940315f5d99f0623`  
		Last Modified: Thu, 24 Oct 2024 01:59:48 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9-developer` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:466a2c8f305a4a7be494517204f4a2b1fbcfc60f1d1f940acca35e2d75883382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.8 MB (484810676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e61646d22e3a0f0c61bc23c9a9a49cf93ebee1d529aa1521ea184800ce3b70f`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.7.96285.zip
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
	-	`sha256:3057c31c5260bcf91a54dd9f7ee64baffa40299d2b2334738fb47593bb343c1c`  
		Last Modified: Thu, 24 Oct 2024 04:05:39 GMT  
		Size: 395.0 MB (394956444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eacc4fd026868220515fd58421bad0eb4ba69991f29165239d0bb851459e07a`  
		Last Modified: Thu, 24 Oct 2024 04:05:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:f8175e977b7d7647fad4c5fef799b6535b0ae4b41f6c270cdeab9be3ffb70b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4276858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0662eaa8feb99bb325a94a43b02e5c5c6686be4dc6adc29c697b63074b15e0de`

```dockerfile
```

-	Layers:
	-	`sha256:ad15d5a6bb03842a89ea59285e361f33e84d64e80972441909d0998e53e81484`  
		Last Modified: Thu, 24 Oct 2024 04:05:30 GMT  
		Size: 4.3 MB (4258402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e65172d00228a5cc26afd6d8816c974611783cb858c0a2f972f10fc2991d7e2`  
		Last Modified: Thu, 24 Oct 2024 04:05:29 GMT  
		Size: 18.5 KB (18456 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9-enterprise`

```console
$ docker pull sonarqube@sha256:6f6755c54608fa0c616281389f82988a9988553bc1a080d30c5e5d4a4843143a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:16a03131fbfe25443284ce2f369245dff7cffb32816a59501a4fef954fe9b8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506646510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6945fdb8f22a9dc7469db82ae96bafa8b0cd45e2fc4765994b3d6dba59d935b`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.7.96285.zip
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
	-	`sha256:ea99c2678d94f31bc59d4ad1a951c6c54d8a3b29414c4e86cd9b22f00871183b`  
		Last Modified: Thu, 24 Oct 2024 02:55:41 GMT  
		Size: 414.0 MB (414023201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d30610814cdab4f8955d19032896556291b2fd60359c30c2e6d64619296f827`  
		Last Modified: Thu, 24 Oct 2024 02:55:35 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:f72a7d245e8f23ccb779e2182319c743506e9233d8ab12c3f4406a93adb9f310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735755c0b387637714887b5c19252b925fa1269b776598101a6893470b7abbc3`

```dockerfile
```

-	Layers:
	-	`sha256:cefc37d17ca1742efa5020ae75fedd4e38c7ab98bcef8c7035db221b4a1ea724`  
		Last Modified: Thu, 24 Oct 2024 02:55:35 GMT  
		Size: 4.3 MB (4305998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0457fe48ed0ef7aae0c0681fc35b171656a993fc296f87d7e6802e29c04b5b8e`  
		Last Modified: Thu, 24 Oct 2024 02:55:35 GMT  
		Size: 18.4 KB (18369 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9-enterprise` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:36519c865beb6656d30147358b8921617fea4f0490f3995fdf4117544c6d4614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.9 MB (503877676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d9edd34dd0f103ba3f652f040acfaa2681a65f063fa42247929d680b0988f1`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.7.96285.zip
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
	-	`sha256:65fb989741f1384e0e1e00f449f8c34cd4fef2fc7c5aac67159e5a23ebd645b6`  
		Last Modified: Thu, 24 Oct 2024 04:08:40 GMT  
		Size: 414.0 MB (414023442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5a1327b2fdd539376faf236daaa123c54be048f1e43f52e117fb55bb6680e4`  
		Last Modified: Thu, 24 Oct 2024 04:08:28 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:18f0b236ea743d4f4e544bc14cdab15f3eec0229cfaa453415bd8c873f3a6a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d0cb741dd085d2a13bb38335076f8cff8594ede3e758d56165dee163ad4b9a`

```dockerfile
```

-	Layers:
	-	`sha256:c1f27a4617b37148772039319568fbcc8a75b283d5ae74bd52af2a7c8b503359`  
		Last Modified: Thu, 24 Oct 2024 04:08:28 GMT  
		Size: 4.3 MB (4305676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb7443ab47eb3846e7782ea7ac18e105a369adc72652816de477f4d403e68042`  
		Last Modified: Thu, 24 Oct 2024 04:08:28 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9.9-community`

```console
$ docker pull sonarqube@sha256:aac4b3bdd2ae29c95e1a4c07bc50f0cc81d1914019bc609e92dee25e72ff2e6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9.9-community` - linux; amd64

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

### `sonarqube:9.9-community` - unknown; unknown

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

### `sonarqube:9.9-community` - linux; arm64 variant v8

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

### `sonarqube:9.9-community` - unknown; unknown

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

## `sonarqube:9.9-datacenter-app`

```console
$ docker pull sonarqube@sha256:7d8becfd63badc3595509042806e247a8c038801992fee4be9163b31e43ae004
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9.9-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:823a79a86f3ddce51330c9f78475e9f8456361c88abefa74fa885aecd7f29caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.5 MB (531507425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c094cbf5e17a638a8f4af7a4ad281dd626d96f345f8c404da0d431b1683446ae`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:2613306c89ad885ff61bbee43304cee6653d7270e06839b7c6f05445ae8992c2`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 438.9 MB (438883561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438d4defa76781348b781b64cb2c54dd09fdad44cb440bc973fe5f9477fe8321`  
		Last Modified: Thu, 24 Oct 2024 02:00:20 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:d33c6dafa9b5a4674fd8032ef17fab08dba61a02be9b3d12345ad66a3fdc6819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cb896e079a7aad5ca48183e9c0e336463f9267591a9374c770266c66e400e4`

```dockerfile
```

-	Layers:
	-	`sha256:f0e8b119ce66d55466575038abf4aa3f29a4bd89b51e10e156056857a5e47fe1`  
		Last Modified: Thu, 24 Oct 2024 02:00:19 GMT  
		Size: 4.4 MB (4447738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b043c8090ad8dd90bfc3c92e76e37a91f6e0c57acf7313e18262743357ac9d`  
		Last Modified: Thu, 24 Oct 2024 02:00:19 GMT  
		Size: 19.0 KB (18959 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9.9-datacenter-app` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:9175a5a95c447cccc9c73c7ecb4886d012a6d3d548afc97dc2aa1ea481a97107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528751109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec3aa4fbce04433b70f920bf51c4c3ab4571f4d92599d35e2cad775cec884b3`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:af01c6c6696ce891c43d463ad31a69c8bc8538c422baefd126848e554bc05367`  
		Last Modified: Thu, 24 Oct 2024 04:11:50 GMT  
		Size: 438.9 MB (438896318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96f764d9405d67e11000092e70d024be10f106adf5176097c7333696cf7a962`  
		Last Modified: Thu, 24 Oct 2024 04:11:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:11baba515404e338714733900af05b24b950146cc3a7a412dceeb4b9b6e49ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288f2776c897a531d3c6b11e46c7da7733ef1d466042f98dd99e8a55cca79d06`

```dockerfile
```

-	Layers:
	-	`sha256:8788dfbc83b3f64d3aa1a9f58a5a5f596aac62847adf755a0b8cc45989ede422`  
		Last Modified: Thu, 24 Oct 2024 04:11:37 GMT  
		Size: 4.4 MB (4447422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b57b8aad45ac3ac19d9246fcb44a9d10f68f8ee9af2c78319176cb0da735fa4d`  
		Last Modified: Thu, 24 Oct 2024 04:11:36 GMT  
		Size: 19.1 KB (19062 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9.9-datacenter-search`

```console
$ docker pull sonarqube@sha256:592541ad310dc6c22cd04e9dc3399c455ce0e21682d907d14b4380dd7db9d0d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9.9-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:466b7213f87a1706fbb7a683aac68058adae3b4abd905ec828d65e846682435b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.5 MB (531507148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a594ef908cc1ebf1b970ac29e3daeb9969a54c17ecf8d874398ce6b0198cae`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:5afbdea98b0b5385aae5b7fff15ea78eb3daef029dd6cec1df14a051c04f559e`  
		Last Modified: Thu, 24 Oct 2024 02:00:25 GMT  
		Size: 438.9 MB (438883466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea47e3260b78d50e74adfbb9cc0360e2e4f72310ecec48eb226bba3db8dbeb3b`  
		Last Modified: Thu, 24 Oct 2024 02:00:17 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:333a532301764ce8c52b6a507ea5d27f5fc5c13ec425add792e849ab79e369c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d03138d7b20cfa8f37d9979ac105b5eb44390647a1def293523a4d1ea0b19f`

```dockerfile
```

-	Layers:
	-	`sha256:02ba3c41cb26478c27571401e8414343fa5f8e73b0b236ec0443a2a670ff65bf`  
		Last Modified: Thu, 24 Oct 2024 02:00:18 GMT  
		Size: 4.4 MB (4447762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4268506be65a644c6fd4c234a2fec4dd56a142faf19d08a40ee8c3dd7a9315b`  
		Last Modified: Thu, 24 Oct 2024 02:00:17 GMT  
		Size: 19.0 KB (18977 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9.9-datacenter-search` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:467f97abb0db146aec6788308348d2479d0dc5acd3d3a09b7d886e13451ea938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528750977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4990516c466d71d46bc3bd46919bab8b4bf280f2afc7fc1b65e33ba49a3192c2`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:95815674d1caddea6b23073271e56ed0c4046668a762ac42b9b18ae515a33f20`  
		Last Modified: Thu, 24 Oct 2024 04:14:34 GMT  
		Size: 438.9 MB (438896369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76d67b22b21217e97691c0e9771ee65f015bb9f0a651154efe94ad45786d369`  
		Last Modified: Thu, 24 Oct 2024 04:14:25 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:a22c61e93f1b5a24d2ac9d5e9408b3668a89d819271218625c596682b2977f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ed5cd3a22a2b81d43018d5af833e6c1e903afcb59c72fa1539f75bca92d05e`

```dockerfile
```

-	Layers:
	-	`sha256:873568fb19337ffac9253c26c4c107a7aba32e8736c8ad07e76180f6d2b759e8`  
		Last Modified: Thu, 24 Oct 2024 04:14:25 GMT  
		Size: 4.4 MB (4447446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb159655442cd35f6f080ffdf005605960c641b8662d754cec3d6d5c7cf4b98e`  
		Last Modified: Thu, 24 Oct 2024 04:14:25 GMT  
		Size: 19.1 KB (19081 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9.9-developer`

```console
$ docker pull sonarqube@sha256:d6441aaf3dcbe1c09b378f0a2fd0986204b71eaa33b666534991187fd792bd18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9.9-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:7bd290744873c0815af823221227ba65af67ac13e30dedaac999636283a86654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.6 MB (487579508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e769c8db61a613236e2cb4679b17c75b5a25d1191d9a26da76f08f74bc235e86`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.7.96285.zip
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
	-	`sha256:102e4e58c7dee0f767acdbda4d2c400e42e8571b31ebeb1a230a4bae4ddef412`  
		Last Modified: Thu, 24 Oct 2024 01:59:53 GMT  
		Size: 395.0 MB (394956203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1036433ccfdd8890ca3b7e7a807c564b07d24ead1e22ebc50ecbd78a07f630`  
		Last Modified: Thu, 24 Oct 2024 01:59:48 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:0bc4f8bc041cc7050bd443e5a11e921fa75f2873efc595b409e0f998bbc7e61b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4277076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cac190262137392ce4eba452ec2191fe84b7f1c94d76a3ee24bac11af67e94`

```dockerfile
```

-	Layers:
	-	`sha256:c173f98c0a4093565aef96e15829618f407d33470e6acf6a4eeae9e1e4438cb6`  
		Last Modified: Thu, 24 Oct 2024 01:59:48 GMT  
		Size: 4.3 MB (4258724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62fe39f9c55024151dffdb09b34fc0dcc7054f45cef402aa940315f5d99f0623`  
		Last Modified: Thu, 24 Oct 2024 01:59:48 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9.9-developer` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:466a2c8f305a4a7be494517204f4a2b1fbcfc60f1d1f940acca35e2d75883382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.8 MB (484810676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e61646d22e3a0f0c61bc23c9a9a49cf93ebee1d529aa1521ea184800ce3b70f`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.7.96285.zip
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
	-	`sha256:3057c31c5260bcf91a54dd9f7ee64baffa40299d2b2334738fb47593bb343c1c`  
		Last Modified: Thu, 24 Oct 2024 04:05:39 GMT  
		Size: 395.0 MB (394956444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eacc4fd026868220515fd58421bad0eb4ba69991f29165239d0bb851459e07a`  
		Last Modified: Thu, 24 Oct 2024 04:05:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:f8175e977b7d7647fad4c5fef799b6535b0ae4b41f6c270cdeab9be3ffb70b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4276858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0662eaa8feb99bb325a94a43b02e5c5c6686be4dc6adc29c697b63074b15e0de`

```dockerfile
```

-	Layers:
	-	`sha256:ad15d5a6bb03842a89ea59285e361f33e84d64e80972441909d0998e53e81484`  
		Last Modified: Thu, 24 Oct 2024 04:05:30 GMT  
		Size: 4.3 MB (4258402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e65172d00228a5cc26afd6d8816c974611783cb858c0a2f972f10fc2991d7e2`  
		Last Modified: Thu, 24 Oct 2024 04:05:29 GMT  
		Size: 18.5 KB (18456 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9.9-enterprise`

```console
$ docker pull sonarqube@sha256:6f6755c54608fa0c616281389f82988a9988553bc1a080d30c5e5d4a4843143a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9.9-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:16a03131fbfe25443284ce2f369245dff7cffb32816a59501a4fef954fe9b8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506646510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6945fdb8f22a9dc7469db82ae96bafa8b0cd45e2fc4765994b3d6dba59d935b`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.7.96285.zip
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
	-	`sha256:ea99c2678d94f31bc59d4ad1a951c6c54d8a3b29414c4e86cd9b22f00871183b`  
		Last Modified: Thu, 24 Oct 2024 02:55:41 GMT  
		Size: 414.0 MB (414023201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d30610814cdab4f8955d19032896556291b2fd60359c30c2e6d64619296f827`  
		Last Modified: Thu, 24 Oct 2024 02:55:35 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:f72a7d245e8f23ccb779e2182319c743506e9233d8ab12c3f4406a93adb9f310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735755c0b387637714887b5c19252b925fa1269b776598101a6893470b7abbc3`

```dockerfile
```

-	Layers:
	-	`sha256:cefc37d17ca1742efa5020ae75fedd4e38c7ab98bcef8c7035db221b4a1ea724`  
		Last Modified: Thu, 24 Oct 2024 02:55:35 GMT  
		Size: 4.3 MB (4305998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0457fe48ed0ef7aae0c0681fc35b171656a993fc296f87d7e6802e29c04b5b8e`  
		Last Modified: Thu, 24 Oct 2024 02:55:35 GMT  
		Size: 18.4 KB (18369 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9.9-enterprise` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:36519c865beb6656d30147358b8921617fea4f0490f3995fdf4117544c6d4614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.9 MB (503877676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d9edd34dd0f103ba3f652f040acfaa2681a65f063fa42247929d680b0988f1`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.7.96285.zip
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
	-	`sha256:65fb989741f1384e0e1e00f449f8c34cd4fef2fc7c5aac67159e5a23ebd645b6`  
		Last Modified: Thu, 24 Oct 2024 04:08:40 GMT  
		Size: 414.0 MB (414023442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5a1327b2fdd539376faf236daaa123c54be048f1e43f52e117fb55bb6680e4`  
		Last Modified: Thu, 24 Oct 2024 04:08:28 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:18f0b236ea743d4f4e544bc14cdab15f3eec0229cfaa453415bd8c873f3a6a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d0cb741dd085d2a13bb38335076f8cff8594ede3e758d56165dee163ad4b9a`

```dockerfile
```

-	Layers:
	-	`sha256:c1f27a4617b37148772039319568fbcc8a75b283d5ae74bd52af2a7c8b503359`  
		Last Modified: Thu, 24 Oct 2024 04:08:28 GMT  
		Size: 4.3 MB (4305676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb7443ab47eb3846e7782ea7ac18e105a369adc72652816de477f4d403e68042`  
		Last Modified: Thu, 24 Oct 2024 04:08:28 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9.9.7-community`

```console
$ docker pull sonarqube@sha256:aac4b3bdd2ae29c95e1a4c07bc50f0cc81d1914019bc609e92dee25e72ff2e6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9.9.7-community` - linux; amd64

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

### `sonarqube:9.9.7-community` - unknown; unknown

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

### `sonarqube:9.9.7-community` - linux; arm64 variant v8

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

### `sonarqube:9.9.7-community` - unknown; unknown

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

## `sonarqube:9.9.7-datacenter-app`

```console
$ docker pull sonarqube@sha256:7d8becfd63badc3595509042806e247a8c038801992fee4be9163b31e43ae004
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9.9.7-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:823a79a86f3ddce51330c9f78475e9f8456361c88abefa74fa885aecd7f29caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.5 MB (531507425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c094cbf5e17a638a8f4af7a4ad281dd626d96f345f8c404da0d431b1683446ae`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:2613306c89ad885ff61bbee43304cee6653d7270e06839b7c6f05445ae8992c2`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 438.9 MB (438883561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438d4defa76781348b781b64cb2c54dd09fdad44cb440bc973fe5f9477fe8321`  
		Last Modified: Thu, 24 Oct 2024 02:00:20 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9.7-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:d33c6dafa9b5a4674fd8032ef17fab08dba61a02be9b3d12345ad66a3fdc6819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cb896e079a7aad5ca48183e9c0e336463f9267591a9374c770266c66e400e4`

```dockerfile
```

-	Layers:
	-	`sha256:f0e8b119ce66d55466575038abf4aa3f29a4bd89b51e10e156056857a5e47fe1`  
		Last Modified: Thu, 24 Oct 2024 02:00:19 GMT  
		Size: 4.4 MB (4447738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b043c8090ad8dd90bfc3c92e76e37a91f6e0c57acf7313e18262743357ac9d`  
		Last Modified: Thu, 24 Oct 2024 02:00:19 GMT  
		Size: 19.0 KB (18959 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9.9.7-datacenter-app` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:9175a5a95c447cccc9c73c7ecb4886d012a6d3d548afc97dc2aa1ea481a97107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528751109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec3aa4fbce04433b70f920bf51c4c3ab4571f4d92599d35e2cad775cec884b3`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:af01c6c6696ce891c43d463ad31a69c8bc8538c422baefd126848e554bc05367`  
		Last Modified: Thu, 24 Oct 2024 04:11:50 GMT  
		Size: 438.9 MB (438896318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96f764d9405d67e11000092e70d024be10f106adf5176097c7333696cf7a962`  
		Last Modified: Thu, 24 Oct 2024 04:11:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9.7-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:11baba515404e338714733900af05b24b950146cc3a7a412dceeb4b9b6e49ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288f2776c897a531d3c6b11e46c7da7733ef1d466042f98dd99e8a55cca79d06`

```dockerfile
```

-	Layers:
	-	`sha256:8788dfbc83b3f64d3aa1a9f58a5a5f596aac62847adf755a0b8cc45989ede422`  
		Last Modified: Thu, 24 Oct 2024 04:11:37 GMT  
		Size: 4.4 MB (4447422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b57b8aad45ac3ac19d9246fcb44a9d10f68f8ee9af2c78319176cb0da735fa4d`  
		Last Modified: Thu, 24 Oct 2024 04:11:36 GMT  
		Size: 19.1 KB (19062 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9.9.7-datacenter-search`

```console
$ docker pull sonarqube@sha256:592541ad310dc6c22cd04e9dc3399c455ce0e21682d907d14b4380dd7db9d0d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9.9.7-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:466b7213f87a1706fbb7a683aac68058adae3b4abd905ec828d65e846682435b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.5 MB (531507148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a594ef908cc1ebf1b970ac29e3daeb9969a54c17ecf8d874398ce6b0198cae`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:5afbdea98b0b5385aae5b7fff15ea78eb3daef029dd6cec1df14a051c04f559e`  
		Last Modified: Thu, 24 Oct 2024 02:00:25 GMT  
		Size: 438.9 MB (438883466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea47e3260b78d50e74adfbb9cc0360e2e4f72310ecec48eb226bba3db8dbeb3b`  
		Last Modified: Thu, 24 Oct 2024 02:00:17 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9.7-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:333a532301764ce8c52b6a507ea5d27f5fc5c13ec425add792e849ab79e369c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d03138d7b20cfa8f37d9979ac105b5eb44390647a1def293523a4d1ea0b19f`

```dockerfile
```

-	Layers:
	-	`sha256:02ba3c41cb26478c27571401e8414343fa5f8e73b0b236ec0443a2a670ff65bf`  
		Last Modified: Thu, 24 Oct 2024 02:00:18 GMT  
		Size: 4.4 MB (4447762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4268506be65a644c6fd4c234a2fec4dd56a142faf19d08a40ee8c3dd7a9315b`  
		Last Modified: Thu, 24 Oct 2024 02:00:17 GMT  
		Size: 19.0 KB (18977 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9.9.7-datacenter-search` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:467f97abb0db146aec6788308348d2479d0dc5acd3d3a09b7d886e13451ea938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528750977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4990516c466d71d46bc3bd46919bab8b4bf280f2afc7fc1b65e33ba49a3192c2`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:95815674d1caddea6b23073271e56ed0c4046668a762ac42b9b18ae515a33f20`  
		Last Modified: Thu, 24 Oct 2024 04:14:34 GMT  
		Size: 438.9 MB (438896369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76d67b22b21217e97691c0e9771ee65f015bb9f0a651154efe94ad45786d369`  
		Last Modified: Thu, 24 Oct 2024 04:14:25 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9.7-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:a22c61e93f1b5a24d2ac9d5e9408b3668a89d819271218625c596682b2977f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ed5cd3a22a2b81d43018d5af833e6c1e903afcb59c72fa1539f75bca92d05e`

```dockerfile
```

-	Layers:
	-	`sha256:873568fb19337ffac9253c26c4c107a7aba32e8736c8ad07e76180f6d2b759e8`  
		Last Modified: Thu, 24 Oct 2024 04:14:25 GMT  
		Size: 4.4 MB (4447446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb159655442cd35f6f080ffdf005605960c641b8662d754cec3d6d5c7cf4b98e`  
		Last Modified: Thu, 24 Oct 2024 04:14:25 GMT  
		Size: 19.1 KB (19081 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9.9.7-developer`

```console
$ docker pull sonarqube@sha256:d6441aaf3dcbe1c09b378f0a2fd0986204b71eaa33b666534991187fd792bd18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9.9.7-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:7bd290744873c0815af823221227ba65af67ac13e30dedaac999636283a86654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.6 MB (487579508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e769c8db61a613236e2cb4679b17c75b5a25d1191d9a26da76f08f74bc235e86`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.7.96285.zip
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
	-	`sha256:102e4e58c7dee0f767acdbda4d2c400e42e8571b31ebeb1a230a4bae4ddef412`  
		Last Modified: Thu, 24 Oct 2024 01:59:53 GMT  
		Size: 395.0 MB (394956203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1036433ccfdd8890ca3b7e7a807c564b07d24ead1e22ebc50ecbd78a07f630`  
		Last Modified: Thu, 24 Oct 2024 01:59:48 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9.7-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:0bc4f8bc041cc7050bd443e5a11e921fa75f2873efc595b409e0f998bbc7e61b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4277076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cac190262137392ce4eba452ec2191fe84b7f1c94d76a3ee24bac11af67e94`

```dockerfile
```

-	Layers:
	-	`sha256:c173f98c0a4093565aef96e15829618f407d33470e6acf6a4eeae9e1e4438cb6`  
		Last Modified: Thu, 24 Oct 2024 01:59:48 GMT  
		Size: 4.3 MB (4258724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62fe39f9c55024151dffdb09b34fc0dcc7054f45cef402aa940315f5d99f0623`  
		Last Modified: Thu, 24 Oct 2024 01:59:48 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9.9.7-developer` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:466a2c8f305a4a7be494517204f4a2b1fbcfc60f1d1f940acca35e2d75883382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.8 MB (484810676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e61646d22e3a0f0c61bc23c9a9a49cf93ebee1d529aa1521ea184800ce3b70f`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.7.96285.zip
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
	-	`sha256:3057c31c5260bcf91a54dd9f7ee64baffa40299d2b2334738fb47593bb343c1c`  
		Last Modified: Thu, 24 Oct 2024 04:05:39 GMT  
		Size: 395.0 MB (394956444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eacc4fd026868220515fd58421bad0eb4ba69991f29165239d0bb851459e07a`  
		Last Modified: Thu, 24 Oct 2024 04:05:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9.7-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:f8175e977b7d7647fad4c5fef799b6535b0ae4b41f6c270cdeab9be3ffb70b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4276858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0662eaa8feb99bb325a94a43b02e5c5c6686be4dc6adc29c697b63074b15e0de`

```dockerfile
```

-	Layers:
	-	`sha256:ad15d5a6bb03842a89ea59285e361f33e84d64e80972441909d0998e53e81484`  
		Last Modified: Thu, 24 Oct 2024 04:05:30 GMT  
		Size: 4.3 MB (4258402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e65172d00228a5cc26afd6d8816c974611783cb858c0a2f972f10fc2991d7e2`  
		Last Modified: Thu, 24 Oct 2024 04:05:29 GMT  
		Size: 18.5 KB (18456 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9.9.7-enterprise`

```console
$ docker pull sonarqube@sha256:6f6755c54608fa0c616281389f82988a9988553bc1a080d30c5e5d4a4843143a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9.9.7-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:16a03131fbfe25443284ce2f369245dff7cffb32816a59501a4fef954fe9b8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506646510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6945fdb8f22a9dc7469db82ae96bafa8b0cd45e2fc4765994b3d6dba59d935b`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.7.96285.zip
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
	-	`sha256:ea99c2678d94f31bc59d4ad1a951c6c54d8a3b29414c4e86cd9b22f00871183b`  
		Last Modified: Thu, 24 Oct 2024 02:55:41 GMT  
		Size: 414.0 MB (414023201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d30610814cdab4f8955d19032896556291b2fd60359c30c2e6d64619296f827`  
		Last Modified: Thu, 24 Oct 2024 02:55:35 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9.7-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:f72a7d245e8f23ccb779e2182319c743506e9233d8ab12c3f4406a93adb9f310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735755c0b387637714887b5c19252b925fa1269b776598101a6893470b7abbc3`

```dockerfile
```

-	Layers:
	-	`sha256:cefc37d17ca1742efa5020ae75fedd4e38c7ab98bcef8c7035db221b4a1ea724`  
		Last Modified: Thu, 24 Oct 2024 02:55:35 GMT  
		Size: 4.3 MB (4305998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0457fe48ed0ef7aae0c0681fc35b171656a993fc296f87d7e6802e29c04b5b8e`  
		Last Modified: Thu, 24 Oct 2024 02:55:35 GMT  
		Size: 18.4 KB (18369 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9.9.7-enterprise` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:36519c865beb6656d30147358b8921617fea4f0490f3995fdf4117544c6d4614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.9 MB (503877676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d9edd34dd0f103ba3f652f040acfaa2681a65f063fa42247929d680b0988f1`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.7.96285.zip
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
	-	`sha256:65fb989741f1384e0e1e00f449f8c34cd4fef2fc7c5aac67159e5a23ebd645b6`  
		Last Modified: Thu, 24 Oct 2024 04:08:40 GMT  
		Size: 414.0 MB (414023442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5a1327b2fdd539376faf236daaa123c54be048f1e43f52e117fb55bb6680e4`  
		Last Modified: Thu, 24 Oct 2024 04:08:28 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9.7-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:18f0b236ea743d4f4e544bc14cdab15f3eec0229cfaa453415bd8c873f3a6a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d0cb741dd085d2a13bb38335076f8cff8594ede3e758d56165dee163ad4b9a`

```dockerfile
```

-	Layers:
	-	`sha256:c1f27a4617b37148772039319568fbcc8a75b283d5ae74bd52af2a7c8b503359`  
		Last Modified: Thu, 24 Oct 2024 04:08:28 GMT  
		Size: 4.3 MB (4305676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb7443ab47eb3846e7782ea7ac18e105a369adc72652816de477f4d403e68042`  
		Last Modified: Thu, 24 Oct 2024 04:08:28 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

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

## `sonarqube:datacenter-app`

```console
$ docker pull sonarqube@sha256:ef1930ca425edb7405ef007e8604f719a9436ee213be63ee0dc6b476837f716b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:95962c53d5a8a2a581b752cffb5c0b0e75453cb7f303212ffa7fe3cc3d2dfc92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1092521785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ff27e729f54d54aea899ef845a9c16050fcb95e413583f5e709e58cac956cb`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
LABEL io.openshift.non-scalable=false
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=10.7.0.96327
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:54892ae41fabff8f7e10921196cdc7297e534454fc84863d5625427244a2846a`  
		Last Modified: Thu, 24 Oct 2024 02:01:49 GMT  
		Size: 999.9 MB (999897912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e277ee5d3785c23d91581a57494c3106115efdce13d87288ac4fa956c74be0`  
		Last Modified: Thu, 24 Oct 2024 02:01:34 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:b8922f56107e59c040cf3704f208f5a4d663bdef16f34b80be26f6b9155628a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6770a3064de3f64a317165df23f5fe64b39e0f97676ac27c7bf497cb509f66`

```dockerfile
```

-	Layers:
	-	`sha256:18c1f1d89f54b8d83663e5c75e9d96ede7afb7dd9e7b94fbbf384810e151dc5d`  
		Last Modified: Thu, 24 Oct 2024 02:01:34 GMT  
		Size: 4.7 MB (4720380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8b98769bc51a60851bc7f1cbc14dbce03f7175437292950981ec6c78916541`  
		Last Modified: Thu, 24 Oct 2024 02:01:34 GMT  
		Size: 19.4 KB (19376 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:datacenter-app` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:8254088b70af9ad7de2bd71f7dbaa2dee26e72934234645907e56f95aa3594fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1089757049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fb661cda7b3bd9e26cd597e01ee8749f7ff96021108c1698d0a9f364ddd716`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
LABEL io.openshift.non-scalable=false
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=10.7.0.96327
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:65fc7fe05bee7c8aacefac9e0bb798ad66de48168283e8e8f39faca69a0caa26`  
		Last Modified: Thu, 24 Oct 2024 04:32:32 GMT  
		Size: 999.9 MB (999902253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eac44f1defdbfcebd1fe73fffab37e5a885605c3539367f0e35bed458f1ecb`  
		Last Modified: Thu, 24 Oct 2024 04:32:12 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:8a66d05e4a36d072e68597998c2fc9d7245d4264e785f70294a3fa4769007dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ef3dd23d38100df94a9516034d87cd5faa5b5d9035dff8708da6b9623e6842`

```dockerfile
```

-	Layers:
	-	`sha256:ed47f36682c3fa013bd754c6146e9d5bb755acef814e96356300bfbab6aaaec3`  
		Last Modified: Thu, 24 Oct 2024 04:32:12 GMT  
		Size: 4.7 MB (4720064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a12292ce537f772cdea93189d4060934b118eee2ae4aebdab8984f4934f995d2`  
		Last Modified: Thu, 24 Oct 2024 04:32:12 GMT  
		Size: 19.5 KB (19480 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:datacenter-search`

```console
$ docker pull sonarqube@sha256:79aa72ceb9c709b7c5e6622728fd6e30ba84c845d468517513cd14030b8fdf2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:71511bb366c1a0dc28a9baaebfbc2ced12ca5d0d6e41178e3e83eb95a9b8459d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1092521078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472fc3c8155a56dc8285e1e388b40f593a076f0865048b6a12afd99d71d48523`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
LABEL io.openshift.non-scalable=false
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=10.7.0.96327
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:cf4332291c90abac25a95c04a285e8115554b262a469cd932673961680d0011f`  
		Last Modified: Thu, 24 Oct 2024 02:02:01 GMT  
		Size: 999.9 MB (999897391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91e2666d7595c11789d058ab257035ef0199032edb9f4b2e75e780eae3e04f0`  
		Last Modified: Thu, 24 Oct 2024 02:01:47 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:bfadf30829c0434a13550cacbc2cfcbf17eed8ce3fcfcaa653f2b106722a85ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4737376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90474b2dc3213285fd9f68c915d48a3edc53ab7f18e16fe89042361ac32f7299`

```dockerfile
```

-	Layers:
	-	`sha256:23d3d184c8f2320f18c05af78753c60c9455fa7e428f968754aaf66d835e6530`  
		Last Modified: Thu, 24 Oct 2024 02:01:48 GMT  
		Size: 4.7 MB (4717837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87dfb045d6f68dad4feb6236dc4127d26d482856dd0c65e7690cd92783157b10`  
		Last Modified: Thu, 24 Oct 2024 02:01:47 GMT  
		Size: 19.5 KB (19539 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:datacenter-search` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:71e0feaf8c97c181b0ef68618f6c14dab3a32c051c6b983fc7b241b7f9687122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1089756136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:566bb84fd6c3dfc1b34bc2db6700b3b679c20013daa5ee4dfecccc8972c4661a`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
LABEL io.openshift.non-scalable=false
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 30 Sep 2024 13:17:42 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_VERSION=10.7.0.96327
# Mon, 30 Sep 2024 13:17:42 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-10.7.0.96327.zip
RUN set -eux;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:044c80166f634a710e47324d2c91bdaf06690ef2582f83a6e08a924bc58f07a3`  
		Last Modified: Thu, 24 Oct 2024 04:37:08 GMT  
		Size: 999.9 MB (999901525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3d7c5503bbebafb6757b3139ef39d87d0e381238973889907913cbecbc9259`  
		Last Modified: Thu, 24 Oct 2024 04:36:48 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c197b4d81cd17cad58e1cf5faf7811669e3233903cd08c43fc2f27015b073cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4737164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f114eef7d6a4b9b5065f64df5a061157971dd0cc3bbd8897fec92c3bb166b5`

```dockerfile
```

-	Layers:
	-	`sha256:067c519dd9feceff6617a1b8b086070e2bb4d0bc6c60498298df41ae50771a08`  
		Last Modified: Thu, 24 Oct 2024 04:36:48 GMT  
		Size: 4.7 MB (4717521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b30ab60f1082327926a6b74972e7e2f818858c9972eba7502d80ce5c711727`  
		Last Modified: Thu, 24 Oct 2024 04:36:47 GMT  
		Size: 19.6 KB (19643 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:developer`

```console
$ docker pull sonarqube@sha256:7a5969f1f6dfc6652d95d9fcfe347fe671667afa6346d248a22a88c9706cb60b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:f15e7859cf41d05f733dd9f4cc2a9c5dc97855516332fc062b31ede148e058eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1061104119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc1feb369d7e690008703bd15512d6bbedb694cdd4758757e71e7faf915e884`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.7.0.96327.zip
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
	-	`sha256:fecdd26b0280f0316437679736231c7ead4f31d825c576ab0530cca5d113aef4`  
		Last Modified: Thu, 24 Oct 2024 02:02:15 GMT  
		Size: 968.5 MB (968480807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475a1feba373d9fd1177f9e00002be1931749b13fa015c3e6be9962bc89a2a17`  
		Last Modified: Thu, 24 Oct 2024 02:01:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:1478fd9270cb3ba95d76e0ee61a09937d087e6da9a766f4e3e86b053102b26a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4607439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf6111f7019ad78cfb3d2b516b12ac5b14bd45d5a7022e62cfa7555a86f798a`

```dockerfile
```

-	Layers:
	-	`sha256:fe052cbc5cdbf918094f842f37b088322874fbd22550cca68dc2cddfe4f1c7df`  
		Last Modified: Thu, 24 Oct 2024 02:01:59 GMT  
		Size: 4.6 MB (4588539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc31480cd15349830b71cdc7220deb18a9a29703820cc15dfd72b639be575f6`  
		Last Modified: Thu, 24 Oct 2024 02:01:58 GMT  
		Size: 18.9 KB (18900 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:developer` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:21a787c8b748cd06ca47ffbc2c93eb2a7b8f5b8e01ea463845190663add1d2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1058335180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c52e6bf8af19f89ad9283d84d0bedd317615cc65c418a88022ac342aa90c10`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-10.7.0.96327.zip
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
	-	`sha256:ecf0b67713a8785a497d4da9a552ee07838d70dd12c8af9e042221e9892a0d67`  
		Last Modified: Thu, 24 Oct 2024 04:22:20 GMT  
		Size: 968.5 MB (968480945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd89bfb485033de0565747ec8c37a658558b4deaaa199375bc2c076d8f6529df`  
		Last Modified: Thu, 24 Oct 2024 04:22:01 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:af682ed22b57052041da13e9960484e4e214cd7ce5a18c84b2b80f50f3777e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4607222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24acefce8966ab5dd7872089a06dc99b2d3d36cae8cf568fe958650810446987`

```dockerfile
```

-	Layers:
	-	`sha256:e5539c9ec389bbb617686e349d34f80b8e803ff4cb3cf19dc5e58b0c10a3c014`  
		Last Modified: Thu, 24 Oct 2024 04:22:01 GMT  
		Size: 4.6 MB (4588217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0b5d1a6389d0c835d3e758e4888a9c44899d9540ef8618f6a01ee54373669a`  
		Last Modified: Thu, 24 Oct 2024 04:22:01 GMT  
		Size: 19.0 KB (19005 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:enterprise`

```console
$ docker pull sonarqube@sha256:74efc260974201a209ec102cf1c8fcddf21dbec0d3399ffd1dae98dab18e1aac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:f77325e6c9beaeeafe22ac6912714440a6a7e01bccf91433a9cbb4806c62e399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1090618072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc3838a079fecff6ab6225c6fd73fca2e244925ed169b11d9c9be5419949178`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-10.7.0.96327.zip
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
	-	`sha256:c2bef6a22930c9e75a6e8c4f5a8c7762c05d535da3a2172fe43800d6df781c12`  
		Last Modified: Thu, 24 Oct 2024 02:01:35 GMT  
		Size: 998.0 MB (997994761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e5ee9772edabff1d7918f81dc1e7e7b50294a9c13607a459b50d8d53780cf7`  
		Last Modified: Thu, 24 Oct 2024 02:01:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:e0013c9eb48ad44623788fe4da859606413efa89edb34dd027eafedc9b38d14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4663125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc62d21cf3049c09cb6c5b3439e1c78f8ca00188c67b4a08be2886f076b5b4b2`

```dockerfile
```

-	Layers:
	-	`sha256:7b60ccca8e67dfe3ca7343b13df4649fe20774856fd4a1aad2a1cb006d994d15`  
		Last Modified: Thu, 24 Oct 2024 02:01:20 GMT  
		Size: 4.6 MB (4644207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88a36430226a11211bd93fd6533f8ba2383fed4d64ebe18fb0a1c06e0f95cdea`  
		Last Modified: Thu, 24 Oct 2024 02:01:19 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:enterprise` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:8bddfdfcbd01b606913880ad92d16894047b1f543e89aaaeee8ce31b7e4fd7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1087849247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466b7455c1291198dd4732c92c25f776f014a0bec27cef63235d74fa04ecf5e7`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-10.7.0.96327.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=10.7.0.96327 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=10.7.0.96327 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-10.7.0.96327.zip
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
	-	`sha256:6bba52a69c784fc1e8d5dfb3f08afab554d7e4f759debf36eab7c3c346a9ca44`  
		Last Modified: Thu, 24 Oct 2024 04:26:41 GMT  
		Size: 998.0 MB (997995012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b58fd8fe5d25d94fbefa8249364231858dca5e79682973bd066fb4570414c`  
		Last Modified: Thu, 24 Oct 2024 04:26:17 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:d2d769e03a67fcd8fd2dad43a5dc5296952d2eb91c740c9f8b679813de5c2b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4662907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a578769c4fbcf2f0651b940cc25efcc9d73fa32b853c7bc800f6af7dfdb8293`

```dockerfile
```

-	Layers:
	-	`sha256:4ce4970bddb06a66363b1c730319b7d13f7b45f54d10f3232766d3815a5c7399`  
		Last Modified: Thu, 24 Oct 2024 04:26:17 GMT  
		Size: 4.6 MB (4643885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51ecd76e9a030f6a4899b8a93a4f5f328a747ffa46bbef965d6968af84c186cb`  
		Last Modified: Thu, 24 Oct 2024 04:26:17 GMT  
		Size: 19.0 KB (19022 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:latest`

```console
$ docker pull sonarqube@sha256:0842dcd4c8f851ce44f8edaf45ac93f7c9079017d60d99f614663e60cef5efe9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:latest` - linux; amd64

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

### `sonarqube:latest` - unknown; unknown

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

### `sonarqube:latest` - linux; arm64 variant v8

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

### `sonarqube:latest` - unknown; unknown

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

## `sonarqube:lts-community`

```console
$ docker pull sonarqube@sha256:aac4b3bdd2ae29c95e1a4c07bc50f0cc81d1914019bc609e92dee25e72ff2e6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:lts-community` - linux; amd64

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

### `sonarqube:lts-community` - unknown; unknown

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

### `sonarqube:lts-community` - linux; arm64 variant v8

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

### `sonarqube:lts-community` - unknown; unknown

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

## `sonarqube:lts-datacenter-app`

```console
$ docker pull sonarqube@sha256:7d8becfd63badc3595509042806e247a8c038801992fee4be9163b31e43ae004
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:lts-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:823a79a86f3ddce51330c9f78475e9f8456361c88abefa74fa885aecd7f29caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.5 MB (531507425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c094cbf5e17a638a8f4af7a4ad281dd626d96f345f8c404da0d431b1683446ae`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:2613306c89ad885ff61bbee43304cee6653d7270e06839b7c6f05445ae8992c2`  
		Last Modified: Thu, 24 Oct 2024 02:00:27 GMT  
		Size: 438.9 MB (438883561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438d4defa76781348b781b64cb2c54dd09fdad44cb440bc973fe5f9477fe8321`  
		Last Modified: Thu, 24 Oct 2024 02:00:20 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:d33c6dafa9b5a4674fd8032ef17fab08dba61a02be9b3d12345ad66a3fdc6819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cb896e079a7aad5ca48183e9c0e336463f9267591a9374c770266c66e400e4`

```dockerfile
```

-	Layers:
	-	`sha256:f0e8b119ce66d55466575038abf4aa3f29a4bd89b51e10e156056857a5e47fe1`  
		Last Modified: Thu, 24 Oct 2024 02:00:19 GMT  
		Size: 4.4 MB (4447738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b043c8090ad8dd90bfc3c92e76e37a91f6e0c57acf7313e18262743357ac9d`  
		Last Modified: Thu, 24 Oct 2024 02:00:19 GMT  
		Size: 19.0 KB (18959 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:lts-datacenter-app` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:9175a5a95c447cccc9c73c7ecb4886d012a6d3d548afc97dc2aa1ea481a97107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528751109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec3aa4fbce04433b70f920bf51c4c3ab4571f4d92599d35e2cad775cec884b3`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:af01c6c6696ce891c43d463ad31a69c8bc8538c422baefd126848e554bc05367`  
		Last Modified: Thu, 24 Oct 2024 04:11:50 GMT  
		Size: 438.9 MB (438896318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96f764d9405d67e11000092e70d024be10f106adf5176097c7333696cf7a962`  
		Last Modified: Thu, 24 Oct 2024 04:11:36 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:11baba515404e338714733900af05b24b950146cc3a7a412dceeb4b9b6e49ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288f2776c897a531d3c6b11e46c7da7733ef1d466042f98dd99e8a55cca79d06`

```dockerfile
```

-	Layers:
	-	`sha256:8788dfbc83b3f64d3aa1a9f58a5a5f596aac62847adf755a0b8cc45989ede422`  
		Last Modified: Thu, 24 Oct 2024 04:11:37 GMT  
		Size: 4.4 MB (4447422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b57b8aad45ac3ac19d9246fcb44a9d10f68f8ee9af2c78319176cb0da735fa4d`  
		Last Modified: Thu, 24 Oct 2024 04:11:36 GMT  
		Size: 19.1 KB (19062 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:lts-datacenter-search`

```console
$ docker pull sonarqube@sha256:592541ad310dc6c22cd04e9dc3399c455ce0e21682d907d14b4380dd7db9d0d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:lts-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:466b7213f87a1706fbb7a683aac68058adae3b4abd905ec828d65e846682435b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.5 MB (531507148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a594ef908cc1ebf1b970ac29e3daeb9969a54c17ecf8d874398ce6b0198cae`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:5afbdea98b0b5385aae5b7fff15ea78eb3daef029dd6cec1df14a051c04f559e`  
		Last Modified: Thu, 24 Oct 2024 02:00:25 GMT  
		Size: 438.9 MB (438883466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea47e3260b78d50e74adfbb9cc0360e2e4f72310ecec48eb226bba3db8dbeb3b`  
		Last Modified: Thu, 24 Oct 2024 02:00:17 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:333a532301764ce8c52b6a507ea5d27f5fc5c13ec425add792e849ab79e369c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d03138d7b20cfa8f37d9979ac105b5eb44390647a1def293523a4d1ea0b19f`

```dockerfile
```

-	Layers:
	-	`sha256:02ba3c41cb26478c27571401e8414343fa5f8e73b0b236ec0443a2a670ff65bf`  
		Last Modified: Thu, 24 Oct 2024 02:00:18 GMT  
		Size: 4.4 MB (4447762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4268506be65a644c6fd4c234a2fec4dd56a142faf19d08a40ee8c3dd7a9315b`  
		Last Modified: Thu, 24 Oct 2024 02:00:17 GMT  
		Size: 19.0 KB (18977 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:lts-datacenter-search` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:467f97abb0db146aec6788308348d2479d0dc5acd3d3a09b7d886e13451ea938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528750977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4990516c466d71d46bc3bd46919bab8b4bf280f2afc7fc1b65e33ba49a3192c2`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.7.96285.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 30 Sep 2024 13:17:42 GMT
WORKDIR /opt/sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 30 Sep 2024 13:17:42 GMT
USER sonarqube
# Mon, 30 Sep 2024 13:17:42 GMT
STOPSIGNAL SIGINT
# Mon, 30 Sep 2024 13:17:42 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 30 Sep 2024 13:17:42 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
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
	-	`sha256:95815674d1caddea6b23073271e56ed0c4046668a762ac42b9b18ae515a33f20`  
		Last Modified: Thu, 24 Oct 2024 04:14:34 GMT  
		Size: 438.9 MB (438896369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76d67b22b21217e97691c0e9771ee65f015bb9f0a651154efe94ad45786d369`  
		Last Modified: Thu, 24 Oct 2024 04:14:25 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:a22c61e93f1b5a24d2ac9d5e9408b3668a89d819271218625c596682b2977f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ed5cd3a22a2b81d43018d5af833e6c1e903afcb59c72fa1539f75bca92d05e`

```dockerfile
```

-	Layers:
	-	`sha256:873568fb19337ffac9253c26c4c107a7aba32e8736c8ad07e76180f6d2b759e8`  
		Last Modified: Thu, 24 Oct 2024 04:14:25 GMT  
		Size: 4.4 MB (4447446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb159655442cd35f6f080ffdf005605960c641b8662d754cec3d6d5c7cf4b98e`  
		Last Modified: Thu, 24 Oct 2024 04:14:25 GMT  
		Size: 19.1 KB (19081 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:lts-developer`

```console
$ docker pull sonarqube@sha256:d6441aaf3dcbe1c09b378f0a2fd0986204b71eaa33b666534991187fd792bd18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:lts-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:7bd290744873c0815af823221227ba65af67ac13e30dedaac999636283a86654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.6 MB (487579508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e769c8db61a613236e2cb4679b17c75b5a25d1191d9a26da76f08f74bc235e86`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.7.96285.zip
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
	-	`sha256:102e4e58c7dee0f767acdbda4d2c400e42e8571b31ebeb1a230a4bae4ddef412`  
		Last Modified: Thu, 24 Oct 2024 01:59:53 GMT  
		Size: 395.0 MB (394956203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1036433ccfdd8890ca3b7e7a807c564b07d24ead1e22ebc50ecbd78a07f630`  
		Last Modified: Thu, 24 Oct 2024 01:59:48 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:0bc4f8bc041cc7050bd443e5a11e921fa75f2873efc595b409e0f998bbc7e61b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4277076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cac190262137392ce4eba452ec2191fe84b7f1c94d76a3ee24bac11af67e94`

```dockerfile
```

-	Layers:
	-	`sha256:c173f98c0a4093565aef96e15829618f407d33470e6acf6a4eeae9e1e4438cb6`  
		Last Modified: Thu, 24 Oct 2024 01:59:48 GMT  
		Size: 4.3 MB (4258724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62fe39f9c55024151dffdb09b34fc0dcc7054f45cef402aa940315f5d99f0623`  
		Last Modified: Thu, 24 Oct 2024 01:59:48 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:lts-developer` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:466a2c8f305a4a7be494517204f4a2b1fbcfc60f1d1f940acca35e2d75883382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.8 MB (484810676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e61646d22e3a0f0c61bc23c9a9a49cf93ebee1d529aa1521ea184800ce3b70f`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.7.96285.zip
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
	-	`sha256:3057c31c5260bcf91a54dd9f7ee64baffa40299d2b2334738fb47593bb343c1c`  
		Last Modified: Thu, 24 Oct 2024 04:05:39 GMT  
		Size: 395.0 MB (394956444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eacc4fd026868220515fd58421bad0eb4ba69991f29165239d0bb851459e07a`  
		Last Modified: Thu, 24 Oct 2024 04:05:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:f8175e977b7d7647fad4c5fef799b6535b0ae4b41f6c270cdeab9be3ffb70b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4276858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0662eaa8feb99bb325a94a43b02e5c5c6686be4dc6adc29c697b63074b15e0de`

```dockerfile
```

-	Layers:
	-	`sha256:ad15d5a6bb03842a89ea59285e361f33e84d64e80972441909d0998e53e81484`  
		Last Modified: Thu, 24 Oct 2024 04:05:30 GMT  
		Size: 4.3 MB (4258402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e65172d00228a5cc26afd6d8816c974611783cb858c0a2f972f10fc2991d7e2`  
		Last Modified: Thu, 24 Oct 2024 04:05:29 GMT  
		Size: 18.5 KB (18456 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:lts-enterprise`

```console
$ docker pull sonarqube@sha256:6f6755c54608fa0c616281389f82988a9988553bc1a080d30c5e5d4a4843143a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:lts-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:16a03131fbfe25443284ce2f369245dff7cffb32816a59501a4fef954fe9b8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.6 MB (506646510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6945fdb8f22a9dc7469db82ae96bafa8b0cd45e2fc4765994b3d6dba59d935b`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.7.96285.zip
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
	-	`sha256:ea99c2678d94f31bc59d4ad1a951c6c54d8a3b29414c4e86cd9b22f00871183b`  
		Last Modified: Thu, 24 Oct 2024 02:55:41 GMT  
		Size: 414.0 MB (414023201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d30610814cdab4f8955d19032896556291b2fd60359c30c2e6d64619296f827`  
		Last Modified: Thu, 24 Oct 2024 02:55:35 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:f72a7d245e8f23ccb779e2182319c743506e9233d8ab12c3f4406a93adb9f310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735755c0b387637714887b5c19252b925fa1269b776598101a6893470b7abbc3`

```dockerfile
```

-	Layers:
	-	`sha256:cefc37d17ca1742efa5020ae75fedd4e38c7ab98bcef8c7035db221b4a1ea724`  
		Last Modified: Thu, 24 Oct 2024 02:55:35 GMT  
		Size: 4.3 MB (4305998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0457fe48ed0ef7aae0c0681fc35b171656a993fc296f87d7e6802e29c04b5b8e`  
		Last Modified: Thu, 24 Oct 2024 02:55:35 GMT  
		Size: 18.4 KB (18369 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:lts-enterprise` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:36519c865beb6656d30147358b8921617fea4f0490f3995fdf4117544c6d4614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.9 MB (503877676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d9edd34dd0f103ba3f652f040acfaa2681a65f063fa42247929d680b0988f1`
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
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.7.96285.zip
# Mon, 30 Sep 2024 13:17:42 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.7.96285 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 30 Sep 2024 13:17:42 GMT
# ARGS: SONARQUBE_VERSION=9.9.7.96285 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.7.96285.zip
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
	-	`sha256:65fb989741f1384e0e1e00f449f8c34cd4fef2fc7c5aac67159e5a23ebd645b6`  
		Last Modified: Thu, 24 Oct 2024 04:08:40 GMT  
		Size: 414.0 MB (414023442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5a1327b2fdd539376faf236daaa123c54be048f1e43f52e117fb55bb6680e4`  
		Last Modified: Thu, 24 Oct 2024 04:08:28 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:18f0b236ea743d4f4e544bc14cdab15f3eec0229cfaa453415bd8c873f3a6a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4324149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d0cb741dd085d2a13bb38335076f8cff8594ede3e758d56165dee163ad4b9a`

```dockerfile
```

-	Layers:
	-	`sha256:c1f27a4617b37148772039319568fbcc8a75b283d5ae74bd52af2a7c8b503359`  
		Last Modified: Thu, 24 Oct 2024 04:08:28 GMT  
		Size: 4.3 MB (4305676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb7443ab47eb3846e7782ea7ac18e105a369adc72652816de477f4d403e68042`  
		Last Modified: Thu, 24 Oct 2024 04:08:28 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json
