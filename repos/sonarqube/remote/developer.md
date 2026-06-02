## `sonarqube:developer`

```console
$ docker pull sonarqube@sha256:c0e4bda85c9bf6e4235e614274da52dcf9224ac7ff635320d27c2272eadb034b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:c4d3e3035dec135b8ba1bd0596348c5115eb53b010f1d487e0fbec670fbb77de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1489465611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bd73141dbe57ea33c38ab4fc7eb6322f31441207a71fe911edb5ee34b62050`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:56 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 02 Jun 2026 08:15:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='3b23af7f7dfe82e1dc66509cb825d82d08372f2e7f66ae85a7fdb42a4c84bfcc';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:15:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:15:13 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 09:15:25 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Tue, 02 Jun 2026 09:15:25 GMT
LABEL io.openshift.min-cpu=400m
# Tue, 02 Jun 2026 09:15:25 GMT
LABEL io.openshift.min-memory=2048M
# Tue, 02 Jun 2026 09:15:25 GMT
LABEL io.openshift.non-scalable=true
# Tue, 02 Jun 2026 09:15:25 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Tue, 02 Jun 2026 09:15:25 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Tue, 02 Jun 2026 09:15:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 09:15:25 GMT
ARG SONARQUBE_VERSION=2026.3.1.123439
# Tue, 02 Jun 2026 09:15:25 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2026.3.1.123439.zip
# Tue, 02 Jun 2026 09:15:25 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2026.3.1.123439 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Tue, 02 Jun 2026 09:15:25 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Tue, 02 Jun 2026 09:15:25 GMT
# ARGS: SONARQUBE_VERSION=2026.3.1.123439 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2026.3.1.123439.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     cd /opt;     curl --proto "=https" --fail --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --proto "=https" --fail --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chown -R sonarqube:root ${SONARQUBE_HOME};     chown -R sonarqube:root "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 02 Jun 2026 09:15:25 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Tue, 02 Jun 2026 09:15:25 GMT
COPY --chown=root:root --chmod=555 entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Tue, 02 Jun 2026 09:15:25 GMT
WORKDIR /opt/sonarqube
# Tue, 02 Jun 2026 09:15:25 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 02 Jun 2026 09:15:25 GMT
USER sonarqube
# Tue, 02 Jun 2026 09:15:25 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jun 2026 09:15:25 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d264b91a55d8b0cadc2f4b2893df6a4b8b25b289ec395a4591ace4370b6bb6eb`  
		Last Modified: Tue, 02 Jun 2026 08:15:29 GMT  
		Size: 17.5 MB (17463879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e0126b19f17e58497cdde5558af28517d651d2b039e4383cef6abd6826ca82`  
		Last Modified: Tue, 02 Jun 2026 08:15:32 GMT  
		Size: 92.7 MB (92708876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c6a52a9f2d0a2c17c05bbf39b1d11933cf0c821cc38a4d29de0b85597dd6c0`  
		Last Modified: Tue, 02 Jun 2026 08:15:21 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0f4e13bf35bd198389b445b37e5dbbc9c33e125c0109345ab53b3e02783273`  
		Last Modified: Tue, 02 Jun 2026 09:17:00 GMT  
		Size: 1.3 GB (1349557246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9de29de7f2915e69bed9924d88111150bb44bb7d68016c01519a62937c90ff`  
		Last Modified: Tue, 02 Jun 2026 09:16:31 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:1f10f87c5bb289cf092acde5879556173cba8e8ff8ffc4fcdd4a15809224fd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4960756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1a7ad1998f25b3a60ccff76a225a2a3f4403e136fe145da1ccf125305f52a5`

```dockerfile
```

-	Layers:
	-	`sha256:f1b1c5794b61becf1dd3abfd4f6ed9201a3c170be1c3ca68e17a26c6e938370c`  
		Last Modified: Tue, 02 Jun 2026 09:16:31 GMT  
		Size: 4.9 MB (4941747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03738c531da95f8a47fb2cc3584fb2822484ac7a06a738c01482f995b34a8de7`  
		Last Modified: Tue, 02 Jun 2026 09:16:31 GMT  
		Size: 19.0 KB (19009 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:developer` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:dd971946162136595b61dd6b8b1c0199953b7569504426cf3ee5544cae0b7837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1488787857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ce397759f0fc1ef794d56ea29771a1beea7e6487c93dd1a8448acc6e50647e`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:16:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:16:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:16:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:16:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:16:12 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 02 Jun 2026 08:16:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        arm64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64el)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        riscv64)          ESUM='3b23af7f7dfe82e1dc66509cb825d82d08372f2e7f66ae85a7fdb42a4c84bfcc';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:16:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:16:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:16:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:16:33 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 09:24:35 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Tue, 02 Jun 2026 09:24:35 GMT
LABEL io.openshift.min-cpu=400m
# Tue, 02 Jun 2026 09:24:35 GMT
LABEL io.openshift.min-memory=2048M
# Tue, 02 Jun 2026 09:24:35 GMT
LABEL io.openshift.non-scalable=true
# Tue, 02 Jun 2026 09:24:35 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Tue, 02 Jun 2026 09:24:35 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Tue, 02 Jun 2026 09:24:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 09:24:35 GMT
ARG SONARQUBE_VERSION=2026.3.1.123439
# Tue, 02 Jun 2026 09:24:35 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2026.3.1.123439.zip
# Tue, 02 Jun 2026 09:24:35 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2026.3.1.123439 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Tue, 02 Jun 2026 09:24:35 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Tue, 02 Jun 2026 09:24:35 GMT
# ARGS: SONARQUBE_VERSION=2026.3.1.123439 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2026.3.1.123439.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     cd /opt;     curl --proto "=https" --fail --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --proto "=https" --fail --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chown -R sonarqube:root ${SONARQUBE_HOME};     chown -R sonarqube:root "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 02 Jun 2026 09:24:35 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Tue, 02 Jun 2026 09:24:35 GMT
COPY --chown=root:root --chmod=555 entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Tue, 02 Jun 2026 09:24:35 GMT
WORKDIR /opt/sonarqube
# Tue, 02 Jun 2026 09:24:35 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 02 Jun 2026 09:24:35 GMT
USER sonarqube
# Tue, 02 Jun 2026 09:24:35 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jun 2026 09:24:35 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5929d83a8a3203db9ba6c54231915963cdf30741ed32624c1526437dfeb8f6a0`  
		Last Modified: Tue, 02 Jun 2026 08:16:50 GMT  
		Size: 18.7 MB (18656880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba65805d8cf21bf730f21c8e74c9bacf7bf507394903abb91abef9f4c51ce53c`  
		Last Modified: Tue, 02 Jun 2026 08:16:52 GMT  
		Size: 91.7 MB (91676973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7229c6fba250cd9ec9dea9d2580e679f6a3e697d45386c7d8e63d493bf8134fa`  
		Last Modified: Tue, 02 Jun 2026 08:16:31 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8425484b3757432690a9aaaf73d0def58d44db8c110c6e2d9c84909eab6b93b6`  
		Last Modified: Tue, 02 Jun 2026 09:26:13 GMT  
		Size: 1.3 GB (1349574793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28ad019171b2014f79c200c5180c03f033255abdb146dba8468ddaf1d5d76d8`  
		Last Modified: Tue, 02 Jun 2026 09:25:42 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:1b1a0b8819b8caa725b8d6880f5a379075fe2c5125779ae81703f7ce2601bdfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5092354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4767cca993a6756ec2dcf8ebbd79d8723891ea857c59b7b0a2602a29ef97516e`

```dockerfile
```

-	Layers:
	-	`sha256:722cbfd3b3b557f84cabaf746387d478554132ae241c00d49579aef8f0bb0a45`  
		Last Modified: Tue, 02 Jun 2026 09:25:42 GMT  
		Size: 5.1 MB (5073253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:332c148549d7240b8c8d2a5af1c5e8cb580c3b8acaf93cc491664e631e257905`  
		Last Modified: Tue, 02 Jun 2026 09:25:42 GMT  
		Size: 19.1 KB (19101 bytes)  
		MIME: application/vnd.in-toto+json
