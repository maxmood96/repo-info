## `sonarqube:enterprise`

```console
$ docker pull sonarqube@sha256:23c9218617367d84e9b9c5e4c1b9c236a0df9ad8e56b86fba835bbdee9ab38bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:4aa86a911c8add9552d9624c349a562b1c6e59942102cdde45479a73703f45d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1408131221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095af147f750fc7111631ea8a8a8596a1a70ec2b3f4a7d3cd941ef117eda1086`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 05 Nov 2025 19:27:35 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Wed, 05 Nov 2025 19:27:35 GMT
LABEL io.openshift.min-cpu=400m
# Wed, 05 Nov 2025 19:27:35 GMT
LABEL io.openshift.min-memory=2048M
# Wed, 05 Nov 2025 19:27:35 GMT
LABEL io.openshift.non-scalable=true
# Wed, 05 Nov 2025 19:27:35 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Wed, 05 Nov 2025 19:27:35 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Wed, 05 Nov 2025 19:27:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Nov 2025 19:27:35 GMT
ARG SONARQUBE_VERSION=2025.5.0.113872
# Wed, 05 Nov 2025 19:27:35 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.5.0.113872.zip
# Wed, 05 Nov 2025 19:27:35 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.5.0.113872 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Wed, 05 Nov 2025 19:27:35 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Wed, 05 Nov 2025 19:27:35 GMT
# ARGS: SONARQUBE_VERSION=2025.5.0.113872 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.5.0.113872.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chown -R sonarqube:root ${SONARQUBE_HOME};     chown -R sonarqube:root "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 05 Nov 2025 19:27:35 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Wed, 05 Nov 2025 19:27:35 GMT
COPY --chown=root:root --chmod=555 entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Wed, 05 Nov 2025 19:27:35 GMT
WORKDIR /opt/sonarqube
# Wed, 05 Nov 2025 19:27:35 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 05 Nov 2025 19:27:35 GMT
USER sonarqube
# Wed, 05 Nov 2025 19:27:35 GMT
STOPSIGNAL SIGINT
# Wed, 05 Nov 2025 19:27:35 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f38e2e092670ef283f8cef3be87ca664b534a953c460e93cfc9ffeebbc8224`  
		Last Modified: Thu, 09 Oct 2025 21:13:36 GMT  
		Size: 17.0 MB (16971757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c474f64746d27f2879d262f6299fbbf510deb0689105ba567ba62c6760583d3`  
		Last Modified: Thu, 09 Oct 2025 21:14:09 GMT  
		Size: 53.0 MB (52968909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1e9704d175f236f24573f3263c46c98ce312c06751ec7feb8aa18adda6c39e`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2326993b9fe603f4efecedec459c92a6f5cbddca94dc55593db837055ac2e4e8`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d14c5d7b708362fc057ea4f0c8bc7d900c2ce66736961c6d229fd6c613d3d0b`  
		Last Modified: Wed, 05 Nov 2025 21:53:09 GMT  
		Size: 1.3 GB (1308464475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ad0f4a5d23883b82cc8562071a98c62f7655e903cc91c92b51463f5d563954`  
		Last Modified: Wed, 05 Nov 2025 19:29:27 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:7014c3b5b1f3e2bf6cc4d6eb4aa3baafd16ed7e5c445c57cee67ac5735673db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4804656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8553a88e4376905741545f5bcfeca6bed944b6f178a7d78e3c9bf9df8c8c9af7`

```dockerfile
```

-	Layers:
	-	`sha256:d626ad0601538a231b5dbda4ba2a1a81315acb85b8dd9dc2eaae5d5dd8b6709d`  
		Last Modified: Wed, 05 Nov 2025 21:52:03 GMT  
		Size: 4.8 MB (4785394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1feab723ca91315736601e6ad8f64a9d0008d838c8da760bfd1ac5e37d6285`  
		Last Modified: Wed, 05 Nov 2025 21:52:04 GMT  
		Size: 19.3 KB (19262 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:enterprise` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:186fe58597c236087019f3e88605af2fa20d4b87c0b8eccb5784f66b0ff03ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1406466954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4fb87ebc590c773f49d5e439d6a223c8cd52db268df2dd7d8764473ea82abe`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 05 Nov 2025 19:25:18 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Wed, 05 Nov 2025 19:25:18 GMT
LABEL io.openshift.min-cpu=400m
# Wed, 05 Nov 2025 19:25:18 GMT
LABEL io.openshift.min-memory=2048M
# Wed, 05 Nov 2025 19:25:18 GMT
LABEL io.openshift.non-scalable=true
# Wed, 05 Nov 2025 19:25:18 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Wed, 05 Nov 2025 19:25:18 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Wed, 05 Nov 2025 19:25:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Nov 2025 19:25:18 GMT
ARG SONARQUBE_VERSION=2025.5.0.113872
# Wed, 05 Nov 2025 19:25:18 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.5.0.113872.zip
# Wed, 05 Nov 2025 19:25:18 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.5.0.113872 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Wed, 05 Nov 2025 19:25:18 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Wed, 05 Nov 2025 19:25:18 GMT
# ARGS: SONARQUBE_VERSION=2025.5.0.113872 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.5.0.113872.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chown -R sonarqube:root ${SONARQUBE_HOME};     chown -R sonarqube:root "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 05 Nov 2025 19:25:18 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Wed, 05 Nov 2025 19:25:18 GMT
COPY --chown=root:root --chmod=555 entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Wed, 05 Nov 2025 19:25:18 GMT
WORKDIR /opt/sonarqube
# Wed, 05 Nov 2025 19:25:18 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 05 Nov 2025 19:25:18 GMT
USER sonarqube
# Wed, 05 Nov 2025 19:25:18 GMT
STOPSIGNAL SIGINT
# Wed, 05 Nov 2025 19:25:18 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf670432170ff54aa7d7fec54b27ad51dc4b767bc00a3178b28176173ef130c`  
		Last Modified: Thu, 09 Oct 2025 21:14:24 GMT  
		Size: 17.0 MB (16989173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d3072b7ee41b26a0c52ffc0714ce586e836d00c7f9936e7f5c4219d8993682`  
		Last Modified: Thu, 09 Oct 2025 21:15:03 GMT  
		Size: 52.1 MB (52148484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd18b9ed8f5e6430b2e5b01ce34688a7c375b5a5ab76ed710e24a610e354cc1e`  
		Last Modified: Thu, 09 Oct 2025 21:14:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a452d8b8a38c043118d3c800c54e6273302aa0642a20b0df0f628b8d0e8866ce`  
		Last Modified: Thu, 09 Oct 2025 21:14:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da59eeb576285b003b05cdecb6b9bb96684f282840ed12ea701cee265fa7f417`  
		Last Modified: Wed, 05 Nov 2025 22:08:26 GMT  
		Size: 1.3 GB (1308464651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e810f9b86d31f4f612d4fbc44dcd1d240994ef049698d37a109e7b648711f4`  
		Last Modified: Wed, 05 Nov 2025 19:26:59 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:e8ddeb35fe4c7f7372caf59b2de342f6140cdd5c3f9c362547eb5c3a79b1afc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4805207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2574703b35b5d846470898c8ee2bd06d39eed97d1656a40ba687fff6dfa961`

```dockerfile
```

-	Layers:
	-	`sha256:231960fcb8011ac2b45cc302acff4da737faf25710a15b5f2a861b4d3dd0e2d5`  
		Last Modified: Wed, 05 Nov 2025 21:52:09 GMT  
		Size: 4.8 MB (4785853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2b5f66b92ac3b9e20238565902c661545e8d74ff45f5a95c16aa1011fed56b3`  
		Last Modified: Wed, 05 Nov 2025 21:52:10 GMT  
		Size: 19.4 KB (19354 bytes)  
		MIME: application/vnd.in-toto+json
