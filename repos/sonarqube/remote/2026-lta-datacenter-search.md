## `sonarqube:2026-lta-datacenter-search`

```console
$ docker pull sonarqube@sha256:9a281f758cd199a3e595b654c577b1c9fae2530849ebf8ccd7cf4ef8eda466a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:2026-lta-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:f7ee8e6a76e97d5376e9d45655e58d4ed55c34b84428af7f083818073f2ca356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1648659889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878af6420a2e54abc40e3ab26e5e4b55a6a1c0e69aa05ef7912511af2f832611`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
# Tue, 02 Jun 2026 08:14:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:55 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 08:15:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='40c6862e6aff63fe9a03856ba0506531b516a17bdb5018464e9006ea7f0f5fe4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:15:03 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:15:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:15:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:15:03 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 09:16:28 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Tue, 02 Jun 2026 09:16:28 GMT
LABEL io.openshift.min-cpu=400m
# Tue, 02 Jun 2026 09:16:28 GMT
LABEL io.openshift.min-memory=2048M
# Tue, 02 Jun 2026 09:16:28 GMT
LABEL io.openshift.non-scalable=false
# Tue, 02 Jun 2026 09:16:28 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Tue, 02 Jun 2026 09:16:28 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Tue, 02 Jun 2026 09:16:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 09:16:28 GMT
ARG SONARQUBE_VERSION=2026.1.3.123084
# Tue, 02 Jun 2026 09:16:28 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2026.1.3.123084.zip
# Tue, 02 Jun 2026 09:16:28 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2026.1.3.123084 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Tue, 02 Jun 2026 09:16:28 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Tue, 02 Jun 2026 09:16:28 GMT
# ARGS: SONARQUBE_VERSION=2026.1.3.123084 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2026.1.3.123084.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --proto "=https" --fail --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --proto "=https" --fail --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chown -R sonarqube:root ${SONARQUBE_HOME};     chown -R sonarqube:root "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 02 Jun 2026 09:16:28 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Tue, 02 Jun 2026 09:16:28 GMT
COPY --chown=root:root --chmod=555 run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Tue, 02 Jun 2026 09:16:28 GMT
WORKDIR /opt/sonarqube
# Tue, 02 Jun 2026 09:16:28 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 02 Jun 2026 09:16:28 GMT
USER sonarqube
# Tue, 02 Jun 2026 09:16:28 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jun 2026 09:16:28 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Tue, 02 Jun 2026 09:16:28 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c01f3db1a2719e1e808c136c592a0317da2de26436d88427de04087774eba8`  
		Last Modified: Tue, 02 Jun 2026 08:15:21 GMT  
		Size: 23.0 MB (22967088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb223f00d1684b6ee21fe982b5801387d1b3ec9f7d64c33554284c601b317f6f`  
		Last Modified: Tue, 02 Jun 2026 08:15:25 GMT  
		Size: 158.2 MB (158171619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b4cb00b79d971cc3d3329a372aeae086cab6860dba5ba781ef348d277b9f1a`  
		Last Modified: Tue, 02 Jun 2026 08:15:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11ec3c5f9ee6853717e932b3c91430d0d29bbd47ea5eed1c864199628ef2297`  
		Last Modified: Tue, 02 Jun 2026 08:15:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a36e550eba0d7c3b5bdcce3ea8ede9e1fb8ecb06cb769b1612a1a2352bf2de`  
		Last Modified: Tue, 02 Jun 2026 09:18:05 GMT  
		Size: 1.4 GB (1437785074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e356de8e6eaca33b32d58ace11440d8d72255a3aea36e42b4d5ee9b3f0a99102`  
		Last Modified: Tue, 02 Jun 2026 09:17:35 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2026-lta-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:6d5cd5a2991dd4758c7e4eef30b28660114c369a8717e6a0feaf145297a49c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5126043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a371b4730a64ca8bb46ad38aa778d98374b65dd3271be31563a6032c29e5e5`

```dockerfile
```

-	Layers:
	-	`sha256:67392c320162f3109554c2096aa72363db779c9cd0db355bab35d1fa3f2b0546`  
		Last Modified: Tue, 02 Jun 2026 09:17:35 GMT  
		Size: 5.1 MB (5106232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a9681c1632770b1460187667e5e2a62c5687b71455e7a4aa079bc006c926704`  
		Last Modified: Tue, 02 Jun 2026 09:17:35 GMT  
		Size: 19.8 KB (19811 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:2026-lta-datacenter-search` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:a65e21f9653e15c2802245685dacce7984035bb50926b3069d6f5b3a79678b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1647345757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f424d6787f3cfcb0f7fdf99f638731665b57f9d35ef77113cba34da307bc2b7`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
# Tue, 02 Jun 2026 08:16:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:16:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:16:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:16:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:16:03 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 08:16:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='40c6862e6aff63fe9a03856ba0506531b516a17bdb5018464e9006ea7f0f5fe4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:16:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:16:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:16:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Jun 2026 08:16:10 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 09:25:55 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Tue, 02 Jun 2026 09:25:55 GMT
LABEL io.openshift.min-cpu=400m
# Tue, 02 Jun 2026 09:25:55 GMT
LABEL io.openshift.min-memory=2048M
# Tue, 02 Jun 2026 09:25:55 GMT
LABEL io.openshift.non-scalable=false
# Tue, 02 Jun 2026 09:25:55 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Tue, 02 Jun 2026 09:25:55 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Tue, 02 Jun 2026 09:25:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 09:25:55 GMT
ARG SONARQUBE_VERSION=2026.1.3.123084
# Tue, 02 Jun 2026 09:25:55 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2026.1.3.123084.zip
# Tue, 02 Jun 2026 09:25:55 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2026.1.3.123084 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Tue, 02 Jun 2026 09:25:55 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Tue, 02 Jun 2026 09:25:55 GMT
# ARGS: SONARQUBE_VERSION=2026.1.3.123084 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2026.1.3.123084.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --proto "=https" --fail --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --proto "=https" --fail --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chown -R sonarqube:root ${SONARQUBE_HOME};     chown -R sonarqube:root "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 02 Jun 2026 09:25:55 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Tue, 02 Jun 2026 09:25:55 GMT
COPY --chown=root:root --chmod=555 run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Tue, 02 Jun 2026 09:25:55 GMT
WORKDIR /opt/sonarqube
# Tue, 02 Jun 2026 09:25:55 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 02 Jun 2026 09:25:55 GMT
USER sonarqube
# Tue, 02 Jun 2026 09:25:55 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jun 2026 09:25:55 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Tue, 02 Jun 2026 09:25:55 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7ab84c2d67441fd3bba3abc37b68773f34e23d567cafb4fc02200349dd96c9`  
		Last Modified: Tue, 02 Jun 2026 08:16:29 GMT  
		Size: 24.2 MB (24172747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564f721386e7e6dd884c7e86149b2eccf2a7567f39b392cac9b7daaec0d44dbd`  
		Last Modified: Tue, 02 Jun 2026 08:16:32 GMT  
		Size: 156.5 MB (156473432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11127b4e771266a8d44b39627af51fefdb6fa421c879eb7d140a973db20c5ea4`  
		Last Modified: Tue, 02 Jun 2026 08:16:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3581c265283ead4745033bea80232c9672330e64126c9d520cf092afdd33e24f`  
		Last Modified: Tue, 02 Jun 2026 08:16:28 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8454bb72805aa33dd154cef007fc4bb1cc2859c4ae5b5f9a1ec9d39c9ea4418b`  
		Last Modified: Tue, 02 Jun 2026 09:27:35 GMT  
		Size: 1.4 GB (1437819866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eb59f807d98b94d01a97f8d55d7847461ae4f3f9d99630873868834691d758`  
		Last Modified: Tue, 02 Jun 2026 09:27:06 GMT  
		Size: 831.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2026-lta-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:f6e5cd236ad0839fd86b5a81053827a81909fcea39a613027656a23e3dce9a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17618764525f9e76a41533fec6c011be04e9262307a7584954d1c2be2514f35e`

```dockerfile
```

-	Layers:
	-	`sha256:a68bef64150a80e22b888e84843e1a35ce81fbfa5547a6d2f34f9104db8171f6`  
		Last Modified: Tue, 02 Jun 2026 09:27:07 GMT  
		Size: 5.2 MB (5237751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73eae2756ffb3f2244e7d638d776aeb3aea54b15dfffa14a5ae314b0815a76f5`  
		Last Modified: Tue, 02 Jun 2026 09:27:06 GMT  
		Size: 19.9 KB (19902 bytes)  
		MIME: application/vnd.in-toto+json
