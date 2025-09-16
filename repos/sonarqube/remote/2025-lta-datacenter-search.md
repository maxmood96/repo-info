## `sonarqube:2025-lta-datacenter-search`

```console
$ docker pull sonarqube@sha256:16fcf16816a40fe81d8c8f6037e1acab8e45ea99f74ec33b59a444e874c2c074
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:2025-lta-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:21af80abd29a222d8f0f9bf027272a99d856a26d368a76ffaadbf4aed35ea2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1202909147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf51e66a74c0741e137cc41fd7b8f808e51a3a9e31a0033db1bb0200a0d5649`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 07 Jul 2025 16:01:59 GMT
ARG RELEASE
# Mon, 07 Jul 2025 16:01:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Jul 2025 16:01:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Jul 2025 16:01:59 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Jul 2025 16:01:59 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Mon, 07 Jul 2025 16:01:59 GMT
CMD ["/bin/bash"]
# Mon, 07 Jul 2025 16:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Jul 2025 16:01:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 16:01:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 07 Jul 2025 16:01:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 16:01:59 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Mon, 07 Jul 2025 16:01:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 07 Jul 2025 16:01:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 07 Jul 2025 16:01:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 07 Jul 2025 16:01:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 07 Jul 2025 16:01:59 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 07 Jul 2025 16:01:59 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 07 Jul 2025 16:01:59 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 07 Jul 2025 16:01:59 GMT
LABEL io.openshift.non-scalable=false
# Mon, 07 Jul 2025 16:01:59 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 07 Jul 2025 16:01:59 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 07 Jul 2025 16:01:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 07 Jul 2025 16:01:59 GMT
ARG SONARQUBE_VERSION=2025.1.3.110580
# Mon, 07 Jul 2025 16:01:59 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.3.110580.zip
# Mon, 07 Jul 2025 16:01:59 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.3.110580 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 07 Jul 2025 16:01:59 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 07 Jul 2025 16:01:59 GMT
# ARGS: SONARQUBE_VERSION=2025.1.3.110580 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.3.110580.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 07 Jul 2025 16:01:59 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 07 Jul 2025 16:01:59 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 07 Jul 2025 16:01:59 GMT
WORKDIR /opt/sonarqube
# Mon, 07 Jul 2025 16:01:59 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 07 Jul 2025 16:01:59 GMT
USER sonarqube
# Mon, 07 Jul 2025 16:01:59 GMT
STOPSIGNAL SIGINT
# Mon, 07 Jul 2025 16:01:59 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 07 Jul 2025 16:01:59 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202b6d722eed4ab5d2bfa3ba17d989bd8d7dc4a291c1209e2eb7ef260604281f`  
		Last Modified: Mon, 15 Sep 2025 22:12:58 GMT  
		Size: 17.0 MB (16971594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5977a0d6dec28378d73bb46e5d3cd1b1a3955abeeedd73f72dedaf3526ca7c0`  
		Last Modified: Mon, 15 Sep 2025 22:14:08 GMT  
		Size: 53.0 MB (52968864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbb660f10559d931e97d7fbb23a041649054e126050a897fc20220af289e55c`  
		Last Modified: Mon, 15 Sep 2025 22:14:06 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c4a30a693e015ffb62f59cf7c534d403965cc95d439067ffd50685d46451cc`  
		Last Modified: Mon, 15 Sep 2025 22:14:07 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa695d6b5355380089f1dde8d1e29d4f62874206d21b8922feeafbac8225042`  
		Last Modified: Tue, 16 Sep 2025 01:09:03 GMT  
		Size: 1.1 GB (1103241938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7d61e50524862342436c7b88b1bc8e256ba24d59eb7cf2b85f5f3094234a73`  
		Last Modified: Mon, 15 Sep 2025 23:22:50 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025-lta-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:ddb93664aba14f1ad3d73c84f9d15cbb87e8a5f1630ec0f543a254ebfb77189e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4651718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79674b37e33c6a11f805e6e8a1f01596f2744fc4f84855bcabc881c36b87fb06`

```dockerfile
```

-	Layers:
	-	`sha256:b8a023a433a8165caff487dd8cccae8e93e487ea9121b2c0e31b890386e718e8`  
		Last Modified: Tue, 16 Sep 2025 01:10:28 GMT  
		Size: 4.6 MB (4632321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc2c54d198137e5359cffe6fe17659c767a9da24709e8b991aed48fdb7150c15`  
		Last Modified: Tue, 16 Sep 2025 01:10:26 GMT  
		Size: 19.4 KB (19397 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:2025-lta-datacenter-search` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:86a66fc54038bac0fc5b4c61c04c35590471039010392054e6731f47aa6242d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1201277937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39079994eb47ae1a1b6bd7c97f01abe408a98845a1c8ad6ea4208b3f46cdf182`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 07 Jul 2025 16:01:59 GMT
ARG RELEASE
# Mon, 07 Jul 2025 16:01:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Jul 2025 16:01:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Jul 2025 16:01:59 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Jul 2025 16:01:59 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Mon, 07 Jul 2025 16:01:59 GMT
CMD ["/bin/bash"]
# Mon, 07 Jul 2025 16:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Jul 2025 16:01:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 16:01:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 07 Jul 2025 16:01:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Jul 2025 16:01:59 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Mon, 07 Jul 2025 16:01:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 07 Jul 2025 16:01:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 07 Jul 2025 16:01:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 07 Jul 2025 16:01:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 07 Jul 2025 16:01:59 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 07 Jul 2025 16:01:59 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 07 Jul 2025 16:01:59 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 07 Jul 2025 16:01:59 GMT
LABEL io.openshift.non-scalable=false
# Mon, 07 Jul 2025 16:01:59 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 07 Jul 2025 16:01:59 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 07 Jul 2025 16:01:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 07 Jul 2025 16:01:59 GMT
ARG SONARQUBE_VERSION=2025.1.3.110580
# Mon, 07 Jul 2025 16:01:59 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.3.110580.zip
# Mon, 07 Jul 2025 16:01:59 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.3.110580 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 07 Jul 2025 16:01:59 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 07 Jul 2025 16:01:59 GMT
# ARGS: SONARQUBE_VERSION=2025.1.3.110580 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.3.110580.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 07 Jul 2025 16:01:59 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 07 Jul 2025 16:01:59 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 07 Jul 2025 16:01:59 GMT
WORKDIR /opt/sonarqube
# Mon, 07 Jul 2025 16:01:59 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 07 Jul 2025 16:01:59 GMT
USER sonarqube
# Mon, 07 Jul 2025 16:01:59 GMT
STOPSIGNAL SIGINT
# Mon, 07 Jul 2025 16:01:59 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 07 Jul 2025 16:01:59 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66c56a4918114509e97ed9ed9ebdaf856e55fe323215963d5991d3851790f19`  
		Last Modified: Mon, 15 Sep 2025 22:12:08 GMT  
		Size: 17.0 MB (16988895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9f61075a372571d9a633d7ace3cfc17ab09413770a1d34c782f08b4a4c1f4b`  
		Last Modified: Mon, 15 Sep 2025 22:13:02 GMT  
		Size: 52.1 MB (52148406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2909ffc811b49798b423b55cff1692c12db9415b52c8e27883ebce3a1704a1`  
		Last Modified: Mon, 15 Sep 2025 22:12:59 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91808dcf954f9bb6b1bcd3e849f01344139cc0d8d10d7a6a8f838dec4e1105b2`  
		Last Modified: Mon, 15 Sep 2025 22:12:59 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8187b7244043f6c3d3f3cff97eacec98e187fa03a1b6b447b7d5e27a4c1c105`  
		Last Modified: Mon, 15 Sep 2025 23:22:35 GMT  
		Size: 1.1 GB (1103276018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7260fc55ec3780869cc320a240a4fcf53d4620235213b342a14a06cef425ae75`  
		Last Modified: Mon, 15 Sep 2025 23:22:45 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025-lta-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:d430a026de7f82bb07f6e546537516f046e22f723b669019385bce2bf7dd4372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4652280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62c8a8be6add3c5b499121944a22ab429efb52e51c8e9caf53232c9c020d792`

```dockerfile
```

-	Layers:
	-	`sha256:65521d6b25148b8710ad2ca278fd492254fede3b1bef3085625c6b1686d3331f`  
		Last Modified: Tue, 16 Sep 2025 02:51:34 GMT  
		Size: 4.6 MB (4632790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39875d0b5a0583de4f393fa7efc6c4e8acd51b2ad660d40d15e76da5bfd4cd71`  
		Last Modified: Tue, 16 Sep 2025 02:51:35 GMT  
		Size: 19.5 KB (19490 bytes)  
		MIME: application/vnd.in-toto+json
