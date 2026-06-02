## `sonarqube:latest`

```console
$ docker pull sonarqube@sha256:223d0090322edce6211a5328298b6f646920f1535025ef8dd880cab6647bb1fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:latest` - linux; amd64

```console
$ docker pull sonarqube@sha256:71e085938c7da0ed909101401189e5a748cc93e280100403919982d46b20f8b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1072766188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee1ff5e4280c8f6ebf518bd536f9e32f5e19919c6d0a045596beef06a8e987b`
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
# Tue, 02 Jun 2026 09:18:39 GMT
LABEL io.k8s.description=SonarQube Community Build is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Tue, 02 Jun 2026 09:18:39 GMT
LABEL io.openshift.min-cpu=400m
# Tue, 02 Jun 2026 09:18:39 GMT
LABEL io.openshift.min-memory=2048M
# Tue, 02 Jun 2026 09:18:39 GMT
LABEL io.openshift.non-scalable=true
# Tue, 02 Jun 2026 09:18:39 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Tue, 02 Jun 2026 09:18:39 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Tue, 02 Jun 2026 09:18:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 09:18:39 GMT
ARG SONARQUBE_VERSION=26.5.0.122743
# Tue, 02 Jun 2026 09:18:39 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-26.5.0.122743.zip
# Tue, 02 Jun 2026 09:18:39 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=26.5.0.122743 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Tue, 02 Jun 2026 09:18:39 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Tue, 02 Jun 2026 09:18:39 GMT
# ARGS: SONARQUBE_VERSION=26.5.0.122743 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-26.5.0.122743.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     cd /opt;     curl --proto "=https" --fail --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --proto "=https" --fail --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chown -R sonarqube:root ${SONARQUBE_HOME};     chown -R sonarqube:root "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 02 Jun 2026 09:18:39 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Tue, 02 Jun 2026 09:18:39 GMT
COPY --chown=root:root --chmod=555 entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Tue, 02 Jun 2026 09:18:39 GMT
WORKDIR /opt/sonarqube
# Tue, 02 Jun 2026 09:18:39 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 02 Jun 2026 09:18:39 GMT
USER sonarqube
# Tue, 02 Jun 2026 09:18:39 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jun 2026 09:18:39 GMT
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
	-	`sha256:b742aea8e8a2ec69e16ce93ed25ae8782b2b469b3e83e8df8542dc866792eeed`  
		Last Modified: Tue, 02 Jun 2026 09:19:40 GMT  
		Size: 932.9 MB (932857823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70086c140ea37fc6d9b142c292269a905d4669498e4679114a63b4f88b426b8`  
		Last Modified: Tue, 02 Jun 2026 09:19:23 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:latest` - unknown; unknown

```console
$ docker pull sonarqube@sha256:88e5d5b944f4cd31fae69df2f10335fa1e91c20b88da498f4104e51a196e175e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebcc7cbc5362e7d67e15bfaaaba3c1a8a5fc76f3c9149bf2c9e44652b2e8937`

```dockerfile
```

-	Layers:
	-	`sha256:7ac7ecf744f61d60da132867ed42313ebcd31e4a4c5deb6b80360c4049a83001`  
		Last Modified: Tue, 02 Jun 2026 09:19:23 GMT  
		Size: 4.6 MB (4572115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c59abc56f3962dcaf402d80d5c0e4875c9442f162fae8f74d323d68bd69ac4a`  
		Last Modified: Tue, 02 Jun 2026 09:19:22 GMT  
		Size: 18.9 KB (18886 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:latest` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:e685c7b15b42d10caa5947a15a6625c4bd123a20632baaef8d3e900069d7621b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1072083870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148d5b1c8f16979a27ebf2b4735a2605840daf16eade4d1f9bf9ac56f4a5c457`
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
# Tue, 02 Jun 2026 09:28:07 GMT
LABEL io.k8s.description=SonarQube Community Build is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Tue, 02 Jun 2026 09:28:07 GMT
LABEL io.openshift.min-cpu=400m
# Tue, 02 Jun 2026 09:28:07 GMT
LABEL io.openshift.min-memory=2048M
# Tue, 02 Jun 2026 09:28:07 GMT
LABEL io.openshift.non-scalable=true
# Tue, 02 Jun 2026 09:28:07 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Tue, 02 Jun 2026 09:28:07 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Tue, 02 Jun 2026 09:28:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 09:28:07 GMT
ARG SONARQUBE_VERSION=26.5.0.122743
# Tue, 02 Jun 2026 09:28:07 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-26.5.0.122743.zip
# Tue, 02 Jun 2026 09:28:07 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=26.5.0.122743 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Tue, 02 Jun 2026 09:28:07 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Tue, 02 Jun 2026 09:28:07 GMT
# ARGS: SONARQUBE_VERSION=26.5.0.122743 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-26.5.0.122743.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     cd /opt;     curl --proto "=https" --fail --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --proto "=https" --fail --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chown -R sonarqube:root ${SONARQUBE_HOME};     chown -R sonarqube:root "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 02 Jun 2026 09:28:07 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Tue, 02 Jun 2026 09:28:07 GMT
COPY --chown=root:root --chmod=555 entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Tue, 02 Jun 2026 09:28:07 GMT
WORKDIR /opt/sonarqube
# Tue, 02 Jun 2026 09:28:07 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 02 Jun 2026 09:28:07 GMT
USER sonarqube
# Tue, 02 Jun 2026 09:28:07 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jun 2026 09:28:07 GMT
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
	-	`sha256:d987a84c548fb6dd5b0378723826bbcb0ac700ad788da31153cd8199e99714a5`  
		Last Modified: Tue, 02 Jun 2026 09:29:15 GMT  
		Size: 932.9 MB (932870807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cba5de0a8201533cf114266a59d2a7785da09390e3a094b6abf98a1bf3c1b8a`  
		Last Modified: Tue, 02 Jun 2026 09:28:58 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:latest` - unknown; unknown

```console
$ docker pull sonarqube@sha256:5dfb8437842b882f5acf047eeac7450272f5c495926696e4f2d6fc1791011320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4722599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eed5d602168e26f7d98b10ab02771c85fe02b0801191a43b73e6aff2a44cb1c`

```dockerfile
```

-	Layers:
	-	`sha256:a8bcb90a1d33adaf30a5342f90f5f4cda3676e3869854051044199c76bccd72a`  
		Last Modified: Tue, 02 Jun 2026 09:28:59 GMT  
		Size: 4.7 MB (4703621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b23160381a16b736eab9491c15eff090289261908a69fbb3a8188b10b3526178`  
		Last Modified: Tue, 02 Jun 2026 09:28:58 GMT  
		Size: 19.0 KB (18978 bytes)  
		MIME: application/vnd.in-toto+json
