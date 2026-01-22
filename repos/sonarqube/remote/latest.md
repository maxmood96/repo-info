## `sonarqube:latest`

```console
$ docker pull sonarqube@sha256:a9d843208d5690ed595a5ce9c7bb356a93a92bb95501558f71515dfdfb37a7bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:latest` - linux; amd64

```console
$ docker pull sonarqube@sha256:74081134c3e5e84e964dd4a57e42c2de51ba23cde56083bc37ab09c500195c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1123850918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba5fe1d78ce977599d69ba4f61bf0ff3b9eb505085a1911c5e950c566d16657`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:20:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:20:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:20:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:20:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:20:07 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 15 Jan 2026 22:20:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='ac411d52862fe8a4a48a6c3546bebced8f4879cd728746fc4ee4b06151aa9f8b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:20:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:20:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:20:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:20:14 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:08:06 GMT
LABEL io.k8s.description=SonarQube Community Build is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Fri, 16 Jan 2026 01:08:06 GMT
LABEL io.openshift.min-cpu=400m
# Fri, 16 Jan 2026 01:08:06 GMT
LABEL io.openshift.min-memory=2048M
# Fri, 16 Jan 2026 01:08:06 GMT
LABEL io.openshift.non-scalable=true
# Fri, 16 Jan 2026 01:08:06 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Fri, 16 Jan 2026 01:08:06 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Fri, 16 Jan 2026 01:08:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jan 2026 01:08:06 GMT
ARG SONARQUBE_VERSION=26.1.0.118079
# Fri, 16 Jan 2026 01:08:06 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-26.1.0.118079.zip
# Fri, 16 Jan 2026 01:08:06 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=26.1.0.118079 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Fri, 16 Jan 2026 01:08:06 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Fri, 16 Jan 2026 01:08:06 GMT
# ARGS: SONARQUBE_VERSION=26.1.0.118079 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-26.1.0.118079.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chown -R sonarqube:root ${SONARQUBE_HOME};     chown -R sonarqube:root "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 16 Jan 2026 01:08:06 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Fri, 16 Jan 2026 01:08:06 GMT
COPY --chown=root:root --chmod=555 entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Fri, 16 Jan 2026 01:08:06 GMT
WORKDIR /opt/sonarqube
# Fri, 16 Jan 2026 01:08:06 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 01:08:06 GMT
USER sonarqube
# Fri, 16 Jan 2026 01:08:06 GMT
STOPSIGNAL SIGINT
# Fri, 16 Jan 2026 01:08:06 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220e5f46c2556ad3d4e13b9f9820a6a493d998f1bc423515840a27d7a4f41ffe`  
		Last Modified: Thu, 15 Jan 2026 22:20:30 GMT  
		Size: 23.0 MB (22961225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3307ab29355ce71f400857b35cca7442414151b6d8d767171d67282f986ad07`  
		Last Modified: Thu, 15 Jan 2026 22:20:33 GMT  
		Size: 157.8 MB (157839172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ebe7eabaf26192ec8e30edade0a6df98ef2590420dfb0ef843456388a54147`  
		Last Modified: Thu, 15 Jan 2026 22:20:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8fd45c97cdc03c294a3813fd5dbdfccd2e3609de14ffa984b6f160afbb7edf`  
		Last Modified: Thu, 15 Jan 2026 22:20:29 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b520efd1dd5cc0f5825253392fbf46ae9a423bc682856e6512724043efed85e2`  
		Last Modified: Fri, 16 Jan 2026 01:09:05 GMT  
		Size: 913.3 MB (913321579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c170ed65eaf99d9d1815c833d9ba7d9c3d74a3a354a5750a9e7fab41a070d3`  
		Last Modified: Fri, 16 Jan 2026 01:08:50 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:latest` - unknown; unknown

```console
$ docker pull sonarqube@sha256:49d77cffdf1bc259d33ef34e90c96b100c0103e78d0117888d71a2767de61291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4609340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebc3edef16f6cc493fc6a7587a84bb197afe2c5dde60009b62ddb34e7c5a6e9`

```dockerfile
```

-	Layers:
	-	`sha256:905793a6494dc11b475d4dc2f842ea9b1ea6a9d41af2d370c6587baf7ef01444`  
		Last Modified: Fri, 16 Jan 2026 01:08:50 GMT  
		Size: 4.6 MB (4590371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fbda4327e38f22c91c2a44113dac889b74b57d9309761cf54456fa8c6f4845`  
		Last Modified: Fri, 16 Jan 2026 01:08:49 GMT  
		Size: 19.0 KB (18969 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:latest` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:4b18cec429db75b072a5d6cb5696e2d564e33c76f5cc126128c1e09328a6ffa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1122462778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0543291ca24ffb5490f88a062d7e641240b6b222e337e987ef50bdb7c3dce159`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:20:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:20:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:20:39 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:20:39 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 15 Jan 2026 22:20:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='ac411d52862fe8a4a48a6c3546bebced8f4879cd728746fc4ee4b06151aa9f8b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:20:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:20:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:20:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Jan 2026 22:20:47 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 01:11:32 GMT
LABEL io.k8s.description=SonarQube Community Build is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Fri, 16 Jan 2026 01:11:32 GMT
LABEL io.openshift.min-cpu=400m
# Fri, 16 Jan 2026 01:11:32 GMT
LABEL io.openshift.min-memory=2048M
# Fri, 16 Jan 2026 01:11:32 GMT
LABEL io.openshift.non-scalable=true
# Fri, 16 Jan 2026 01:11:32 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Fri, 16 Jan 2026 01:11:32 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Fri, 16 Jan 2026 01:11:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jan 2026 01:11:32 GMT
ARG SONARQUBE_VERSION=26.1.0.118079
# Fri, 16 Jan 2026 01:11:32 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-26.1.0.118079.zip
# Fri, 16 Jan 2026 01:11:32 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=26.1.0.118079 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Fri, 16 Jan 2026 01:11:32 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Fri, 16 Jan 2026 01:11:32 GMT
# ARGS: SONARQUBE_VERSION=26.1.0.118079 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-26.1.0.118079.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chown -R sonarqube:root ${SONARQUBE_HOME};     chown -R sonarqube:root "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 16 Jan 2026 01:11:32 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Fri, 16 Jan 2026 01:11:33 GMT
COPY --chown=root:root --chmod=555 entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Fri, 16 Jan 2026 01:11:33 GMT
WORKDIR /opt/sonarqube
# Fri, 16 Jan 2026 01:11:33 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 01:11:33 GMT
USER sonarqube
# Fri, 16 Jan 2026 01:11:33 GMT
STOPSIGNAL SIGINT
# Fri, 16 Jan 2026 01:11:33 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733d8aa488b55ac09113fb6923a025dd6c789770c55b738387a34a5cad1bf82e`  
		Last Modified: Thu, 15 Jan 2026 22:21:04 GMT  
		Size: 24.2 MB (24166529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2014bd5938928d55149f3bd12aafc9edd2b2564be58b1b8f4741a761c254d773`  
		Last Modified: Thu, 15 Jan 2026 22:21:07 GMT  
		Size: 156.1 MB (156108045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1205e43b16a07ab88cb31484712b906ca3fe032a61a21b18c69765799353c4b3`  
		Last Modified: Thu, 15 Jan 2026 22:21:03 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313b0162d5f630b291fc13a699023e777b0b5a20343c7c6b72c776d70a0b9ee9`  
		Last Modified: Thu, 15 Jan 2026 22:21:03 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73d13f5ebdf5c28d31083e6995da78fd2f113e28e6bb3c73d51ab29737eedd1`  
		Last Modified: Fri, 16 Jan 2026 01:12:40 GMT  
		Size: 913.3 MB (913321448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264560874a58faea912e447162240ab087fcc06610f9e24b9393b90e5b5d484e`  
		Last Modified: Fri, 16 Jan 2026 01:12:23 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:latest` - unknown; unknown

```console
$ docker pull sonarqube@sha256:73775a960f6368e69d8c2a3a8a486020d5972c82955ef7ebe740ef2541a9e0d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4740940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722cb613a18dc4129c051e7e6952abb4fe4be12764bcdc9ed3dde37432c5c672`

```dockerfile
```

-	Layers:
	-	`sha256:903e614a7ad79cd6d4273e5884657dc655102b704bd1594ac8a28b1f7701e49d`  
		Last Modified: Fri, 16 Jan 2026 01:12:23 GMT  
		Size: 4.7 MB (4721880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89588926d737d018a76b9fdc1f34da44fadb3a8bcdc459485a3c884c3f683309`  
		Last Modified: Fri, 16 Jan 2026 01:12:23 GMT  
		Size: 19.1 KB (19060 bytes)  
		MIME: application/vnd.in-toto+json
