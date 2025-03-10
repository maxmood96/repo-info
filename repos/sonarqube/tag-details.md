<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sonarqube`

-	[`sonarqube:2025-lta-datacenter-app`](#sonarqube2025-lta-datacenter-app)
-	[`sonarqube:2025-lta-datacenter-search`](#sonarqube2025-lta-datacenter-search)
-	[`sonarqube:2025-lta-developer`](#sonarqube2025-lta-developer)
-	[`sonarqube:2025-lta-enterprise`](#sonarqube2025-lta-enterprise)
-	[`sonarqube:2025.1-datacenter-app`](#sonarqube20251-datacenter-app)
-	[`sonarqube:2025.1-datacenter-search`](#sonarqube20251-datacenter-search)
-	[`sonarqube:2025.1-developer`](#sonarqube20251-developer)
-	[`sonarqube:2025.1-enterprise`](#sonarqube20251-enterprise)
-	[`sonarqube:2025.1.0-datacenter-app`](#sonarqube202510-datacenter-app)
-	[`sonarqube:2025.1.0-datacenter-search`](#sonarqube202510-datacenter-search)
-	[`sonarqube:2025.1.0-developer`](#sonarqube202510-developer)
-	[`sonarqube:2025.1.0-enterprise`](#sonarqube202510-enterprise)
-	[`sonarqube:25.3.0.104237-community`](#sonarqube2530104237-community)
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
-	[`sonarqube:9.9.8-community`](#sonarqube998-community)
-	[`sonarqube:9.9.8-developer`](#sonarqube998-developer)
-	[`sonarqube:9.9.9-datacenter-app`](#sonarqube999-datacenter-app)
-	[`sonarqube:9.9.9-datacenter-search`](#sonarqube999-datacenter-search)
-	[`sonarqube:9.9.9-enterprise`](#sonarqube999-enterprise)
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

## `sonarqube:2025-lta-datacenter-app`

```console
$ docker pull sonarqube@sha256:3c01a66774098de4da5d35c3213f5cd9d79f7338dd71ab38c953373965be7a75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:2025-lta-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:e045593f2e5c7b4850f09fbba380c6c9450cfc3449e02e45b3e0d1453fe75af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1197208142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a1fcfd3a85e321f69e9920002e4d3939095fa9246ea5bfea97a4bc446bfb6f`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=false
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e21bc54673e65f81d2ffc134c57997869f8bdafad81daacc8f192aa995900e`  
		Last Modified: Fri, 07 Feb 2025 01:29:43 GMT  
		Size: 1.1 GB (1103535218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3474bd21b6868e61dc88241206e4b1c395d5324f527f8f4fe0eb143691dfc42`  
		Last Modified: Fri, 07 Feb 2025 01:29:25 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025-lta-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c1524ce02bfd24b137945817e927c6e707f8f18fd02e7e53982334212af3178e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4280552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3268dbfe664179f1e5576fb22755b12a9bc940cae1d91773b1820d6fb20db5`

```dockerfile
```

-	Layers:
	-	`sha256:e672e658b4c96b03d25335d302092702ed81bf53440f6cca12dbe858efd591b7`  
		Last Modified: Fri, 07 Feb 2025 01:29:25 GMT  
		Size: 4.3 MB (4261029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4045135d92cc40fd006c187d6e316adad806e6351f7af5b8e362d36428b03446`  
		Last Modified: Fri, 07 Feb 2025 01:29:25 GMT  
		Size: 19.5 KB (19523 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:2025-lta-datacenter-app` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:1e31a7e3347683b44e1a4b4ee6060c70774f407f686758bda5fc0a8128baf233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1195914349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b8073e5839540b6e025a45e70251c6b6b6022d5c2eabb0a790c8a82d362285`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=false
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92b81d1ba8c2e990435f5c40d82c030f4208f2e43f295ac93253c800a6a3d8c`  
		Last Modified: Tue, 04 Feb 2025 22:27:12 GMT  
		Size: 1.1 GB (1103576057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801fabce23496a0f0cfdba8857acb922e40e1cf36f7daaee24a8b7ecb7881b22`  
		Last Modified: Tue, 04 Feb 2025 22:26:50 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025-lta-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:f6b3123508c80f9a7371f53650aebfe28e5cf7b9b46db8004b18ea4afd970661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4281138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa91a857e1a4630c53a0b36858a2f5f34a9aaa0b8f95cdc8878a2361ddeaaf49`

```dockerfile
```

-	Layers:
	-	`sha256:aeb3cf3d612274d0ef46d26aa4de50c3a37fe2ec6b2effaa498902ba1833bd94`  
		Last Modified: Fri, 07 Feb 2025 03:09:40 GMT  
		Size: 4.3 MB (4261511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f1eb14726a0af5b320bd7867769e18538de0fba57f640bddfd508fdb4c23652`  
		Last Modified: Fri, 07 Feb 2025 03:09:39 GMT  
		Size: 19.6 KB (19627 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:2025-lta-datacenter-search`

```console
$ docker pull sonarqube@sha256:706f5147ce309134d9e3423d293ed21696690b5d813b9a6d700c76ef5ad1e168
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:2025-lta-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:238d957759b73914deb8c9ead2ac0f78e3a0b36ff2b007363ca9b497c3a4ee32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1197207427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8f786b616180afc4ad3e18ef4c2e3cd2e78b20807aa70f69f14b315a702e82`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=false
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c8bebb8263f05c850f5751eb04bbc9e018025ad8857c0f7222ec66b314754e`  
		Last Modified: Fri, 07 Feb 2025 01:29:53 GMT  
		Size: 1.1 GB (1103534689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6014a00175d30f7ed1b74952516c14543e574e6fa84f4308c8cf3fd3685458`  
		Last Modified: Fri, 07 Feb 2025 01:29:37 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025-lta-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:5891ec1f0f00137267efd42f045d0e4eb3d43e9bd4cd35682391c26d539fece6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4278176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d87fe43ce39f389e0c81a8e528b57c78fe118a2077ffaa79efc75154486f39`

```dockerfile
```

-	Layers:
	-	`sha256:5d433fe7b2e029b1e7b2626f314c7b2065c60cf33604d17d41e40d0785ef9198`  
		Last Modified: Fri, 07 Feb 2025 01:29:37 GMT  
		Size: 4.3 MB (4258490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40834093fcb1febec03268e99b071e8cdd850f5f6784f996ce2e5a96cc03cd5e`  
		Last Modified: Fri, 07 Feb 2025 01:29:37 GMT  
		Size: 19.7 KB (19686 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:2025-lta-datacenter-search` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:6fb2c2050f88285fb457f97577b7cf109cf5eff8193ad23fca9f62fb6c5ef0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1195913614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9644546b79e945c3c239ffc50322f62b9ff17e7e3eb44555983fa4f811c0ba08`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=false
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6372a7f96b95d984a1e03d2b9f8017a58a40538f8f4a277d79c5426f551f5d98`  
		Last Modified: Tue, 04 Feb 2025 22:29:37 GMT  
		Size: 1.1 GB (1103575506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde6ec40bc1053b502172a4c3dffa1cfaaddb7d6f8c270fe553ad8641f4b4684`  
		Last Modified: Tue, 04 Feb 2025 22:29:11 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025-lta-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c75b6e6c1de422cfca56f637e24da1e380b722fdc7fa491186cbed705b89492d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4278762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2dd96e4d314d5f23dbf4e3deda1cc5dd0461ef26963419f9e55beb0251d837`

```dockerfile
```

-	Layers:
	-	`sha256:bc2f0ec19e49043d9ab593813955771f223f523dd06935d4a2aa159642dcdb69`  
		Last Modified: Fri, 07 Feb 2025 03:10:48 GMT  
		Size: 4.3 MB (4258972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f6b7d85648c5d6f51684f03d8512e7906ab2e2b1e608c615ee59219bebaf03f`  
		Last Modified: Fri, 07 Feb 2025 03:10:48 GMT  
		Size: 19.8 KB (19790 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:2025-lta-developer`

```console
$ docker pull sonarqube@sha256:2445e50a08f779da5c5a234a4692c147073edfb0e3f653e555ee79c02e40a17f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:2025-lta-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:19c8d0f913b4d934c9c280e14bd9922769469d10d31abf697542eca2f78829aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1152584640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db8cff33c9029701bee1350c11b2b907ee8087c0e2486e96c9f6e4c67a567b9`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=true
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1010402eaefb87aefa2e26f9ca25d9ad2e131b368c543b3c5bead9598db50d46`  
		Last Modified: Fri, 07 Feb 2025 01:29:37 GMT  
		Size: 1.1 GB (1058912279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34944d7881e71fb0314b3dae85b4fab047e5c0aefb6b2d78730058536e21c177`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025-lta-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:7348acacf362c3b194050e8dcfc397da6f4dbed573e26a046dd5ecd9b027fc30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4159652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3699524c8cd5a997121070b1778a2839b8ec826026bc883c8019e811d78aa9c6`

```dockerfile
```

-	Layers:
	-	`sha256:0b5a216ee48827eb059d1a524e05c531ff12d551afb7586fd4bbfc2471e3e739`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 4.1 MB (4140605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e8c5fc00d8a344ce57fb8db20c0fc8bec6ee41acf18bc2ce2810c1baa4377c2`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 19.0 KB (19047 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:2025-lta-developer` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:4d7ee399546c929f025c5e3d1c3d5f8be1d231e1b53066b3529a54114029aeb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1151250366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f882a14ec88d74e8d28493feecc76ba7318ca7ed8a93c2b5c9b4bfd090b20f5f`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=true
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b711f9ed3343feadc371c44cb4d97051def6f8a602be436487b86237bc68aa0`  
		Last Modified: Tue, 04 Feb 2025 22:22:04 GMT  
		Size: 1.1 GB (1058912634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce52742a06136cb786e9c3024590c8d5e3bfb44b8e0ed86c964c69a5655eb583`  
		Last Modified: Tue, 04 Feb 2025 22:21:45 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025-lta-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:60cfd9ae3f12b816d79c3ed50020442f70574c960b0587dcf7465a0282f2afe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4160228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684d06f62c4661dc1d11bc87ae932cda8145fc9bf80d03951d400489a3af9c97`

```dockerfile
```

-	Layers:
	-	`sha256:807171e7ad21dce41de484be7397870205800a731aba4ea67a77a79e221b2445`  
		Last Modified: Fri, 07 Feb 2025 03:07:13 GMT  
		Size: 4.1 MB (4141076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1a79869a44ccbea2167a03974ddb4197573152f0c768be4bfb4d87a3ebcaa08`  
		Last Modified: Fri, 07 Feb 2025 03:07:13 GMT  
		Size: 19.2 KB (19152 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:2025-lta-enterprise`

```console
$ docker pull sonarqube@sha256:f4fca15eb2767ad6904b055f06600da9bb2ec9a9ae6c9f31d5a1f8a0a4632564
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:2025-lta-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:051b5bb64db4d67ce685cfbfe6b612cee9e3d3845e7e30d9f165119bd45a6c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1195176882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff772f29503fdbdf680d8a4ec0c65ab5e7cbedf3a5cbb253f2cdcc6063c70977`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=true
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153734b82608639de6f74daf2d3eaceb27f0982148ca73320787e60722c6e213`  
		Last Modified: Fri, 07 Feb 2025 01:29:39 GMT  
		Size: 1.1 GB (1101504521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b9141f9c8f73cf0d58fc13f517e3579df47d90e8b5b52b564816150062c3bc`  
		Last Modified: Fri, 07 Feb 2025 01:29:23 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025-lta-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:dc4669416390a995c15e95f60711417377e1cf12f4b4dadd1f7dfec802dc3294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80282c785229fe9472e57d5f0fbc5fae77666d2c0d6708c83a18ca2165e5e25c`

```dockerfile
```

-	Layers:
	-	`sha256:1fa177210b8942b78c21d7ff6c768307508c2b61812715486291e36788f51690`  
		Last Modified: Fri, 07 Feb 2025 01:29:23 GMT  
		Size: 4.2 MB (4184086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dfc7bcb99f505d26b9a1357e84d620779ffde33e5e0bba9037dedc7539ff9db`  
		Last Modified: Fri, 07 Feb 2025 01:29:23 GMT  
		Size: 19.1 KB (19064 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:2025-lta-enterprise` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:47c290e53bd77de2f424f8f175e3af8ed89fe10e06d85f97483dc716138d38e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1193842406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5807acd30b73c2a42a242740d6c44dd7576ff7055fa1dddeb5ccd10d62855fd3`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=true
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da32d4f953537ef53f20e5e53a865c3cb427288e5150ae03a7b43f9b7c60aceb`  
		Last Modified: Tue, 04 Feb 2025 22:24:40 GMT  
		Size: 1.1 GB (1101504675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404e90b821f0f9083f833c1c082dd9883a929e40b0c843c38d6d5af79338b470`  
		Last Modified: Tue, 04 Feb 2025 22:24:11 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025-lta-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:9b934fceda3f514b85ed4cdca807d3775beb0c4138f0d785ab0023bea0005aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42d4ea1c36a303ff1a600d85386608804e53714cdc154e331d51837c16076bf`

```dockerfile
```

-	Layers:
	-	`sha256:dcd52cd5ae77b5d7d978a11f3e7de134f1665307c53c545babbfd3671befad48`  
		Last Modified: Fri, 07 Feb 2025 03:08:27 GMT  
		Size: 4.2 MB (4184557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2376259bb6062f6c74aa3ea967cc3070a824ec408e8c83cc419d46604efbea75`  
		Last Modified: Fri, 07 Feb 2025 03:08:27 GMT  
		Size: 19.2 KB (19168 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:2025.1-datacenter-app`

```console
$ docker pull sonarqube@sha256:3c01a66774098de4da5d35c3213f5cd9d79f7338dd71ab38c953373965be7a75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:2025.1-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:e045593f2e5c7b4850f09fbba380c6c9450cfc3449e02e45b3e0d1453fe75af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1197208142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a1fcfd3a85e321f69e9920002e4d3939095fa9246ea5bfea97a4bc446bfb6f`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=false
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e21bc54673e65f81d2ffc134c57997869f8bdafad81daacc8f192aa995900e`  
		Last Modified: Fri, 07 Feb 2025 01:29:43 GMT  
		Size: 1.1 GB (1103535218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3474bd21b6868e61dc88241206e4b1c395d5324f527f8f4fe0eb143691dfc42`  
		Last Modified: Fri, 07 Feb 2025 01:29:25 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025.1-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c1524ce02bfd24b137945817e927c6e707f8f18fd02e7e53982334212af3178e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4280552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3268dbfe664179f1e5576fb22755b12a9bc940cae1d91773b1820d6fb20db5`

```dockerfile
```

-	Layers:
	-	`sha256:e672e658b4c96b03d25335d302092702ed81bf53440f6cca12dbe858efd591b7`  
		Last Modified: Fri, 07 Feb 2025 01:29:25 GMT  
		Size: 4.3 MB (4261029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4045135d92cc40fd006c187d6e316adad806e6351f7af5b8e362d36428b03446`  
		Last Modified: Fri, 07 Feb 2025 01:29:25 GMT  
		Size: 19.5 KB (19523 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:2025.1-datacenter-app` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:1e31a7e3347683b44e1a4b4ee6060c70774f407f686758bda5fc0a8128baf233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1195914349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b8073e5839540b6e025a45e70251c6b6b6022d5c2eabb0a790c8a82d362285`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=false
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92b81d1ba8c2e990435f5c40d82c030f4208f2e43f295ac93253c800a6a3d8c`  
		Last Modified: Tue, 04 Feb 2025 22:27:12 GMT  
		Size: 1.1 GB (1103576057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801fabce23496a0f0cfdba8857acb922e40e1cf36f7daaee24a8b7ecb7881b22`  
		Last Modified: Tue, 04 Feb 2025 22:26:50 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025.1-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:f6b3123508c80f9a7371f53650aebfe28e5cf7b9b46db8004b18ea4afd970661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4281138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa91a857e1a4630c53a0b36858a2f5f34a9aaa0b8f95cdc8878a2361ddeaaf49`

```dockerfile
```

-	Layers:
	-	`sha256:aeb3cf3d612274d0ef46d26aa4de50c3a37fe2ec6b2effaa498902ba1833bd94`  
		Last Modified: Fri, 07 Feb 2025 03:09:40 GMT  
		Size: 4.3 MB (4261511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f1eb14726a0af5b320bd7867769e18538de0fba57f640bddfd508fdb4c23652`  
		Last Modified: Fri, 07 Feb 2025 03:09:39 GMT  
		Size: 19.6 KB (19627 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:2025.1-datacenter-search`

```console
$ docker pull sonarqube@sha256:706f5147ce309134d9e3423d293ed21696690b5d813b9a6d700c76ef5ad1e168
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:2025.1-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:238d957759b73914deb8c9ead2ac0f78e3a0b36ff2b007363ca9b497c3a4ee32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1197207427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8f786b616180afc4ad3e18ef4c2e3cd2e78b20807aa70f69f14b315a702e82`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=false
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c8bebb8263f05c850f5751eb04bbc9e018025ad8857c0f7222ec66b314754e`  
		Last Modified: Fri, 07 Feb 2025 01:29:53 GMT  
		Size: 1.1 GB (1103534689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6014a00175d30f7ed1b74952516c14543e574e6fa84f4308c8cf3fd3685458`  
		Last Modified: Fri, 07 Feb 2025 01:29:37 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025.1-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:5891ec1f0f00137267efd42f045d0e4eb3d43e9bd4cd35682391c26d539fece6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4278176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d87fe43ce39f389e0c81a8e528b57c78fe118a2077ffaa79efc75154486f39`

```dockerfile
```

-	Layers:
	-	`sha256:5d433fe7b2e029b1e7b2626f314c7b2065c60cf33604d17d41e40d0785ef9198`  
		Last Modified: Fri, 07 Feb 2025 01:29:37 GMT  
		Size: 4.3 MB (4258490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40834093fcb1febec03268e99b071e8cdd850f5f6784f996ce2e5a96cc03cd5e`  
		Last Modified: Fri, 07 Feb 2025 01:29:37 GMT  
		Size: 19.7 KB (19686 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:2025.1-datacenter-search` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:6fb2c2050f88285fb457f97577b7cf109cf5eff8193ad23fca9f62fb6c5ef0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1195913614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9644546b79e945c3c239ffc50322f62b9ff17e7e3eb44555983fa4f811c0ba08`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=false
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6372a7f96b95d984a1e03d2b9f8017a58a40538f8f4a277d79c5426f551f5d98`  
		Last Modified: Tue, 04 Feb 2025 22:29:37 GMT  
		Size: 1.1 GB (1103575506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde6ec40bc1053b502172a4c3dffa1cfaaddb7d6f8c270fe553ad8641f4b4684`  
		Last Modified: Tue, 04 Feb 2025 22:29:11 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025.1-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c75b6e6c1de422cfca56f637e24da1e380b722fdc7fa491186cbed705b89492d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4278762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2dd96e4d314d5f23dbf4e3deda1cc5dd0461ef26963419f9e55beb0251d837`

```dockerfile
```

-	Layers:
	-	`sha256:bc2f0ec19e49043d9ab593813955771f223f523dd06935d4a2aa159642dcdb69`  
		Last Modified: Fri, 07 Feb 2025 03:10:48 GMT  
		Size: 4.3 MB (4258972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f6b7d85648c5d6f51684f03d8512e7906ab2e2b1e608c615ee59219bebaf03f`  
		Last Modified: Fri, 07 Feb 2025 03:10:48 GMT  
		Size: 19.8 KB (19790 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:2025.1-developer`

```console
$ docker pull sonarqube@sha256:2445e50a08f779da5c5a234a4692c147073edfb0e3f653e555ee79c02e40a17f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:2025.1-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:19c8d0f913b4d934c9c280e14bd9922769469d10d31abf697542eca2f78829aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1152584640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db8cff33c9029701bee1350c11b2b907ee8087c0e2486e96c9f6e4c67a567b9`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=true
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1010402eaefb87aefa2e26f9ca25d9ad2e131b368c543b3c5bead9598db50d46`  
		Last Modified: Fri, 07 Feb 2025 01:29:37 GMT  
		Size: 1.1 GB (1058912279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34944d7881e71fb0314b3dae85b4fab047e5c0aefb6b2d78730058536e21c177`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025.1-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:7348acacf362c3b194050e8dcfc397da6f4dbed573e26a046dd5ecd9b027fc30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4159652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3699524c8cd5a997121070b1778a2839b8ec826026bc883c8019e811d78aa9c6`

```dockerfile
```

-	Layers:
	-	`sha256:0b5a216ee48827eb059d1a524e05c531ff12d551afb7586fd4bbfc2471e3e739`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 4.1 MB (4140605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e8c5fc00d8a344ce57fb8db20c0fc8bec6ee41acf18bc2ce2810c1baa4377c2`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 19.0 KB (19047 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:2025.1-developer` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:4d7ee399546c929f025c5e3d1c3d5f8be1d231e1b53066b3529a54114029aeb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1151250366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f882a14ec88d74e8d28493feecc76ba7318ca7ed8a93c2b5c9b4bfd090b20f5f`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=true
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b711f9ed3343feadc371c44cb4d97051def6f8a602be436487b86237bc68aa0`  
		Last Modified: Tue, 04 Feb 2025 22:22:04 GMT  
		Size: 1.1 GB (1058912634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce52742a06136cb786e9c3024590c8d5e3bfb44b8e0ed86c964c69a5655eb583`  
		Last Modified: Tue, 04 Feb 2025 22:21:45 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025.1-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:60cfd9ae3f12b816d79c3ed50020442f70574c960b0587dcf7465a0282f2afe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4160228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684d06f62c4661dc1d11bc87ae932cda8145fc9bf80d03951d400489a3af9c97`

```dockerfile
```

-	Layers:
	-	`sha256:807171e7ad21dce41de484be7397870205800a731aba4ea67a77a79e221b2445`  
		Last Modified: Fri, 07 Feb 2025 03:07:13 GMT  
		Size: 4.1 MB (4141076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1a79869a44ccbea2167a03974ddb4197573152f0c768be4bfb4d87a3ebcaa08`  
		Last Modified: Fri, 07 Feb 2025 03:07:13 GMT  
		Size: 19.2 KB (19152 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:2025.1-enterprise`

```console
$ docker pull sonarqube@sha256:f4fca15eb2767ad6904b055f06600da9bb2ec9a9ae6c9f31d5a1f8a0a4632564
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:2025.1-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:051b5bb64db4d67ce685cfbfe6b612cee9e3d3845e7e30d9f165119bd45a6c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1195176882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff772f29503fdbdf680d8a4ec0c65ab5e7cbedf3a5cbb253f2cdcc6063c70977`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=true
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153734b82608639de6f74daf2d3eaceb27f0982148ca73320787e60722c6e213`  
		Last Modified: Fri, 07 Feb 2025 01:29:39 GMT  
		Size: 1.1 GB (1101504521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b9141f9c8f73cf0d58fc13f517e3579df47d90e8b5b52b564816150062c3bc`  
		Last Modified: Fri, 07 Feb 2025 01:29:23 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025.1-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:dc4669416390a995c15e95f60711417377e1cf12f4b4dadd1f7dfec802dc3294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80282c785229fe9472e57d5f0fbc5fae77666d2c0d6708c83a18ca2165e5e25c`

```dockerfile
```

-	Layers:
	-	`sha256:1fa177210b8942b78c21d7ff6c768307508c2b61812715486291e36788f51690`  
		Last Modified: Fri, 07 Feb 2025 01:29:23 GMT  
		Size: 4.2 MB (4184086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dfc7bcb99f505d26b9a1357e84d620779ffde33e5e0bba9037dedc7539ff9db`  
		Last Modified: Fri, 07 Feb 2025 01:29:23 GMT  
		Size: 19.1 KB (19064 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:2025.1-enterprise` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:47c290e53bd77de2f424f8f175e3af8ed89fe10e06d85f97483dc716138d38e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1193842406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5807acd30b73c2a42a242740d6c44dd7576ff7055fa1dddeb5ccd10d62855fd3`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=true
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da32d4f953537ef53f20e5e53a865c3cb427288e5150ae03a7b43f9b7c60aceb`  
		Last Modified: Tue, 04 Feb 2025 22:24:40 GMT  
		Size: 1.1 GB (1101504675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404e90b821f0f9083f833c1c082dd9883a929e40b0c843c38d6d5af79338b470`  
		Last Modified: Tue, 04 Feb 2025 22:24:11 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025.1-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:9b934fceda3f514b85ed4cdca807d3775beb0c4138f0d785ab0023bea0005aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42d4ea1c36a303ff1a600d85386608804e53714cdc154e331d51837c16076bf`

```dockerfile
```

-	Layers:
	-	`sha256:dcd52cd5ae77b5d7d978a11f3e7de134f1665307c53c545babbfd3671befad48`  
		Last Modified: Fri, 07 Feb 2025 03:08:27 GMT  
		Size: 4.2 MB (4184557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2376259bb6062f6c74aa3ea967cc3070a824ec408e8c83cc419d46604efbea75`  
		Last Modified: Fri, 07 Feb 2025 03:08:27 GMT  
		Size: 19.2 KB (19168 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:2025.1.0-datacenter-app`

```console
$ docker pull sonarqube@sha256:3c01a66774098de4da5d35c3213f5cd9d79f7338dd71ab38c953373965be7a75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:2025.1.0-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:e045593f2e5c7b4850f09fbba380c6c9450cfc3449e02e45b3e0d1453fe75af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1197208142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a1fcfd3a85e321f69e9920002e4d3939095fa9246ea5bfea97a4bc446bfb6f`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=false
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e21bc54673e65f81d2ffc134c57997869f8bdafad81daacc8f192aa995900e`  
		Last Modified: Fri, 07 Feb 2025 01:29:43 GMT  
		Size: 1.1 GB (1103535218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3474bd21b6868e61dc88241206e4b1c395d5324f527f8f4fe0eb143691dfc42`  
		Last Modified: Fri, 07 Feb 2025 01:29:25 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025.1.0-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c1524ce02bfd24b137945817e927c6e707f8f18fd02e7e53982334212af3178e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4280552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3268dbfe664179f1e5576fb22755b12a9bc940cae1d91773b1820d6fb20db5`

```dockerfile
```

-	Layers:
	-	`sha256:e672e658b4c96b03d25335d302092702ed81bf53440f6cca12dbe858efd591b7`  
		Last Modified: Fri, 07 Feb 2025 01:29:25 GMT  
		Size: 4.3 MB (4261029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4045135d92cc40fd006c187d6e316adad806e6351f7af5b8e362d36428b03446`  
		Last Modified: Fri, 07 Feb 2025 01:29:25 GMT  
		Size: 19.5 KB (19523 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:2025.1.0-datacenter-app` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:1e31a7e3347683b44e1a4b4ee6060c70774f407f686758bda5fc0a8128baf233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1195914349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b8073e5839540b6e025a45e70251c6b6b6022d5c2eabb0a790c8a82d362285`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=false
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92b81d1ba8c2e990435f5c40d82c030f4208f2e43f295ac93253c800a6a3d8c`  
		Last Modified: Tue, 04 Feb 2025 22:27:12 GMT  
		Size: 1.1 GB (1103576057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801fabce23496a0f0cfdba8857acb922e40e1cf36f7daaee24a8b7ecb7881b22`  
		Last Modified: Tue, 04 Feb 2025 22:26:50 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025.1.0-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:f6b3123508c80f9a7371f53650aebfe28e5cf7b9b46db8004b18ea4afd970661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4281138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa91a857e1a4630c53a0b36858a2f5f34a9aaa0b8f95cdc8878a2361ddeaaf49`

```dockerfile
```

-	Layers:
	-	`sha256:aeb3cf3d612274d0ef46d26aa4de50c3a37fe2ec6b2effaa498902ba1833bd94`  
		Last Modified: Fri, 07 Feb 2025 03:09:40 GMT  
		Size: 4.3 MB (4261511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f1eb14726a0af5b320bd7867769e18538de0fba57f640bddfd508fdb4c23652`  
		Last Modified: Fri, 07 Feb 2025 03:09:39 GMT  
		Size: 19.6 KB (19627 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:2025.1.0-datacenter-search`

```console
$ docker pull sonarqube@sha256:706f5147ce309134d9e3423d293ed21696690b5d813b9a6d700c76ef5ad1e168
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:2025.1.0-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:238d957759b73914deb8c9ead2ac0f78e3a0b36ff2b007363ca9b497c3a4ee32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1197207427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8f786b616180afc4ad3e18ef4c2e3cd2e78b20807aa70f69f14b315a702e82`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=false
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c8bebb8263f05c850f5751eb04bbc9e018025ad8857c0f7222ec66b314754e`  
		Last Modified: Fri, 07 Feb 2025 01:29:53 GMT  
		Size: 1.1 GB (1103534689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6014a00175d30f7ed1b74952516c14543e574e6fa84f4308c8cf3fd3685458`  
		Last Modified: Fri, 07 Feb 2025 01:29:37 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025.1.0-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:5891ec1f0f00137267efd42f045d0e4eb3d43e9bd4cd35682391c26d539fece6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4278176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d87fe43ce39f389e0c81a8e528b57c78fe118a2077ffaa79efc75154486f39`

```dockerfile
```

-	Layers:
	-	`sha256:5d433fe7b2e029b1e7b2626f314c7b2065c60cf33604d17d41e40d0785ef9198`  
		Last Modified: Fri, 07 Feb 2025 01:29:37 GMT  
		Size: 4.3 MB (4258490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40834093fcb1febec03268e99b071e8cdd850f5f6784f996ce2e5a96cc03cd5e`  
		Last Modified: Fri, 07 Feb 2025 01:29:37 GMT  
		Size: 19.7 KB (19686 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:2025.1.0-datacenter-search` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:6fb2c2050f88285fb457f97577b7cf109cf5eff8193ad23fca9f62fb6c5ef0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1195913614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9644546b79e945c3c239ffc50322f62b9ff17e7e3eb44555983fa4f811c0ba08`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=false
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6372a7f96b95d984a1e03d2b9f8017a58a40538f8f4a277d79c5426f551f5d98`  
		Last Modified: Tue, 04 Feb 2025 22:29:37 GMT  
		Size: 1.1 GB (1103575506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde6ec40bc1053b502172a4c3dffa1cfaaddb7d6f8c270fe553ad8641f4b4684`  
		Last Modified: Tue, 04 Feb 2025 22:29:11 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025.1.0-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c75b6e6c1de422cfca56f637e24da1e380b722fdc7fa491186cbed705b89492d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4278762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2dd96e4d314d5f23dbf4e3deda1cc5dd0461ef26963419f9e55beb0251d837`

```dockerfile
```

-	Layers:
	-	`sha256:bc2f0ec19e49043d9ab593813955771f223f523dd06935d4a2aa159642dcdb69`  
		Last Modified: Fri, 07 Feb 2025 03:10:48 GMT  
		Size: 4.3 MB (4258972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f6b7d85648c5d6f51684f03d8512e7906ab2e2b1e608c615ee59219bebaf03f`  
		Last Modified: Fri, 07 Feb 2025 03:10:48 GMT  
		Size: 19.8 KB (19790 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:2025.1.0-developer`

```console
$ docker pull sonarqube@sha256:2445e50a08f779da5c5a234a4692c147073edfb0e3f653e555ee79c02e40a17f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:2025.1.0-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:19c8d0f913b4d934c9c280e14bd9922769469d10d31abf697542eca2f78829aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1152584640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db8cff33c9029701bee1350c11b2b907ee8087c0e2486e96c9f6e4c67a567b9`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=true
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1010402eaefb87aefa2e26f9ca25d9ad2e131b368c543b3c5bead9598db50d46`  
		Last Modified: Fri, 07 Feb 2025 01:29:37 GMT  
		Size: 1.1 GB (1058912279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34944d7881e71fb0314b3dae85b4fab047e5c0aefb6b2d78730058536e21c177`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025.1.0-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:7348acacf362c3b194050e8dcfc397da6f4dbed573e26a046dd5ecd9b027fc30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4159652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3699524c8cd5a997121070b1778a2839b8ec826026bc883c8019e811d78aa9c6`

```dockerfile
```

-	Layers:
	-	`sha256:0b5a216ee48827eb059d1a524e05c531ff12d551afb7586fd4bbfc2471e3e739`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 4.1 MB (4140605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e8c5fc00d8a344ce57fb8db20c0fc8bec6ee41acf18bc2ce2810c1baa4377c2`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 19.0 KB (19047 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:2025.1.0-developer` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:4d7ee399546c929f025c5e3d1c3d5f8be1d231e1b53066b3529a54114029aeb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1151250366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f882a14ec88d74e8d28493feecc76ba7318ca7ed8a93c2b5c9b4bfd090b20f5f`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=true
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b711f9ed3343feadc371c44cb4d97051def6f8a602be436487b86237bc68aa0`  
		Last Modified: Tue, 04 Feb 2025 22:22:04 GMT  
		Size: 1.1 GB (1058912634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce52742a06136cb786e9c3024590c8d5e3bfb44b8e0ed86c964c69a5655eb583`  
		Last Modified: Tue, 04 Feb 2025 22:21:45 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025.1.0-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:60cfd9ae3f12b816d79c3ed50020442f70574c960b0587dcf7465a0282f2afe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4160228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684d06f62c4661dc1d11bc87ae932cda8145fc9bf80d03951d400489a3af9c97`

```dockerfile
```

-	Layers:
	-	`sha256:807171e7ad21dce41de484be7397870205800a731aba4ea67a77a79e221b2445`  
		Last Modified: Fri, 07 Feb 2025 03:07:13 GMT  
		Size: 4.1 MB (4141076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1a79869a44ccbea2167a03974ddb4197573152f0c768be4bfb4d87a3ebcaa08`  
		Last Modified: Fri, 07 Feb 2025 03:07:13 GMT  
		Size: 19.2 KB (19152 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:2025.1.0-enterprise`

```console
$ docker pull sonarqube@sha256:f4fca15eb2767ad6904b055f06600da9bb2ec9a9ae6c9f31d5a1f8a0a4632564
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:2025.1.0-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:051b5bb64db4d67ce685cfbfe6b612cee9e3d3845e7e30d9f165119bd45a6c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1195176882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff772f29503fdbdf680d8a4ec0c65ab5e7cbedf3a5cbb253f2cdcc6063c70977`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=true
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153734b82608639de6f74daf2d3eaceb27f0982148ca73320787e60722c6e213`  
		Last Modified: Fri, 07 Feb 2025 01:29:39 GMT  
		Size: 1.1 GB (1101504521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b9141f9c8f73cf0d58fc13f517e3579df47d90e8b5b52b564816150062c3bc`  
		Last Modified: Fri, 07 Feb 2025 01:29:23 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025.1.0-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:dc4669416390a995c15e95f60711417377e1cf12f4b4dadd1f7dfec802dc3294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80282c785229fe9472e57d5f0fbc5fae77666d2c0d6708c83a18ca2165e5e25c`

```dockerfile
```

-	Layers:
	-	`sha256:1fa177210b8942b78c21d7ff6c768307508c2b61812715486291e36788f51690`  
		Last Modified: Fri, 07 Feb 2025 01:29:23 GMT  
		Size: 4.2 MB (4184086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dfc7bcb99f505d26b9a1357e84d620779ffde33e5e0bba9037dedc7539ff9db`  
		Last Modified: Fri, 07 Feb 2025 01:29:23 GMT  
		Size: 19.1 KB (19064 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:2025.1.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:47c290e53bd77de2f424f8f175e3af8ed89fe10e06d85f97483dc716138d38e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1193842406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5807acd30b73c2a42a242740d6c44dd7576ff7055fa1dddeb5ccd10d62855fd3`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=true
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da32d4f953537ef53f20e5e53a865c3cb427288e5150ae03a7b43f9b7c60aceb`  
		Last Modified: Tue, 04 Feb 2025 22:24:40 GMT  
		Size: 1.1 GB (1101504675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404e90b821f0f9083f833c1c082dd9883a929e40b0c843c38d6d5af79338b470`  
		Last Modified: Tue, 04 Feb 2025 22:24:11 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025.1.0-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:9b934fceda3f514b85ed4cdca807d3775beb0c4138f0d785ab0023bea0005aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42d4ea1c36a303ff1a600d85386608804e53714cdc154e331d51837c16076bf`

```dockerfile
```

-	Layers:
	-	`sha256:dcd52cd5ae77b5d7d978a11f3e7de134f1665307c53c545babbfd3671befad48`  
		Last Modified: Fri, 07 Feb 2025 03:08:27 GMT  
		Size: 4.2 MB (4184557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2376259bb6062f6c74aa3ea967cc3070a824ec408e8c83cc419d46604efbea75`  
		Last Modified: Fri, 07 Feb 2025 03:08:27 GMT  
		Size: 19.2 KB (19168 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:25.3.0.104237-community`

```console
$ docker pull sonarqube@sha256:c0a734bd7e62c1a35794e3a070b4945f5a081b0053201eb926bcb936b0e5d2e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:25.3.0.104237-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:4537ef14a6097a81f6b5dedb2dbf674584e6b0ab70b52fbdcdc03329822d741a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **926.5 MB (926508161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a7de374354b23c76d3c6296244b16ae46b6e1188aff06f81bea35b061ba4e1`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.k8s.description=SonarQube Community Build is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.min-cpu=400m
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.min-memory=2048M
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.non-scalable=true
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Tue, 04 Mar 2025 14:26:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Mar 2025 14:26:37 GMT
ARG SONARQUBE_VERSION=25.3.0.104237
# Tue, 04 Mar 2025 14:26:37 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-25.3.0.104237.zip
# Tue, 04 Mar 2025 14:26:37 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=25.3.0.104237 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Tue, 04 Mar 2025 14:26:37 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Tue, 04 Mar 2025 14:26:37 GMT
# ARGS: SONARQUBE_VERSION=25.3.0.104237 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-25.3.0.104237.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chown -R sonarqube:root ${SONARQUBE_HOME};     chown -R sonarqube:root "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Mar 2025 14:26:37 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Tue, 04 Mar 2025 14:26:37 GMT
COPY --chown=root:root --chmod=555 entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Tue, 04 Mar 2025 14:26:37 GMT
WORKDIR /opt/sonarqube
# Tue, 04 Mar 2025 14:26:37 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Mar 2025 14:26:37 GMT
USER sonarqube
# Tue, 04 Mar 2025 14:26:37 GMT
STOPSIGNAL SIGINT
# Tue, 04 Mar 2025 14:26:37 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9439e8e49454d1cada79e114dd855a92dd3b56cf4cd29fd76e68ffbbde95711`  
		Last Modified: Tue, 04 Mar 2025 18:28:28 GMT  
		Size: 832.8 MB (832835795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f1017e9142664c197cc8ee70dc8391936c10b181c0b6c7b7858cf8089d9a0b`  
		Last Modified: Tue, 04 Mar 2025 18:28:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:25.3.0.104237-community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:dc40b216c134a8462617bffa174633248def5af01b19da6e9d01c88345bc451e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4025432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196fc41ac5cffa8e35e151574cd70ee1b2fa9bca06167f5e20e7de97696f4e11`

```dockerfile
```

-	Layers:
	-	`sha256:0378be74976cb96b01c918dfeb750c9e5675110a443dfd8793a20ee28598161c`  
		Last Modified: Tue, 04 Mar 2025 18:28:11 GMT  
		Size: 4.0 MB (4006260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f890ae483e83b4cdeeeca5c912e5720c1a3e4b1c8c2c7a6350d1392c7dba7ad`  
		Last Modified: Tue, 04 Mar 2025 18:28:11 GMT  
		Size: 19.2 KB (19172 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:25.3.0.104237-community` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:39520ca4f03757d4ffb7b51d796e00a486c3bd2a52a88e49dc337858d18558bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **925.2 MB (925173667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd676a601cab90a3dc967c38da926e0c6597707f620b6eabea7483a8067a0d9`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.k8s.description=SonarQube Community Build is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.min-cpu=400m
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.min-memory=2048M
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.non-scalable=true
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Tue, 04 Mar 2025 14:26:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Mar 2025 14:26:37 GMT
ARG SONARQUBE_VERSION=25.3.0.104237
# Tue, 04 Mar 2025 14:26:37 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-25.3.0.104237.zip
# Tue, 04 Mar 2025 14:26:37 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=25.3.0.104237 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Tue, 04 Mar 2025 14:26:37 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Tue, 04 Mar 2025 14:26:37 GMT
# ARGS: SONARQUBE_VERSION=25.3.0.104237 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-25.3.0.104237.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chown -R sonarqube:root ${SONARQUBE_HOME};     chown -R sonarqube:root "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Mar 2025 14:26:37 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Tue, 04 Mar 2025 14:26:37 GMT
COPY --chown=root:root --chmod=555 entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Tue, 04 Mar 2025 14:26:37 GMT
WORKDIR /opt/sonarqube
# Tue, 04 Mar 2025 14:26:37 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Mar 2025 14:26:37 GMT
USER sonarqube
# Tue, 04 Mar 2025 14:26:37 GMT
STOPSIGNAL SIGINT
# Tue, 04 Mar 2025 14:26:37 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa6bb2ca9de90e5b203b42c785c9e79fa3c087f65e7c584dd230328db41af5b`  
		Last Modified: Tue, 04 Mar 2025 18:28:12 GMT  
		Size: 832.8 MB (832835930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f6ae284075e0ea433ca61298e087d0e6e8c0c5769e6378df68abd162ed8eab`  
		Last Modified: Tue, 04 Mar 2025 18:27:54 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:25.3.0.104237-community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:5f9e91b0dde066d967074c704eb39d7a2739fb130edb497f5b63319655ceaeb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4025982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91cc7e1bda97e08fa8e968b4959405ea598ee8d4870d7a6819592f39f63f6d5c`

```dockerfile
```

-	Layers:
	-	`sha256:dc231aa3fbbeb548fbc347e6d57a384dca6a928e22eb2df2feb4178b1fabab09`  
		Last Modified: Tue, 04 Mar 2025 18:27:55 GMT  
		Size: 4.0 MB (4006719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:117f823a11faed4d51564ddf05781ced65385922d8f09df95a0dd7872978c079`  
		Last Modified: Tue, 04 Mar 2025 18:27:54 GMT  
		Size: 19.3 KB (19263 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9-community`

```console
$ docker pull sonarqube@sha256:95b1826b68e606678882148e28c01c70dc0efe464a0d0c568570b17eedf1a9f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:1793dda70059333e88e59261255ac05ce0861bd1ac17436a5f299cdf68d68241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.1 MB (393064917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522e1399903e00890e27e6ff2fb59d7e9650fc7ea2db8a57af0579b0e8391406`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e1e3bdd7bcf133d27cf8c09c794cf0fb192157136466e889bc1ed58a56a202`  
		Last Modified: Fri, 07 Feb 2025 01:28:44 GMT  
		Size: 300.4 MB (300438235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2dce0ce5cad6cfd437ec91b65e228c9301401a304513fa592813473a3b369d6`  
		Last Modified: Fri, 07 Feb 2025 01:28:39 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:04bfbb3c2ca0d94f91ad10042dc4410788d00a63fdb6d846aa8685d9190ee45a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439b6670621d9cbfa42012e006a94c0f045396dbc6a5a5b6f7d4af4d56661025`

```dockerfile
```

-	Layers:
	-	`sha256:c7c552215db26d6198bcfbaa5fe42a4d2f79d23d8866d8f03e9430a508cef215`  
		Last Modified: Fri, 07 Feb 2025 01:28:39 GMT  
		Size: 4.1 MB (4133976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03eac24c4193ff2cdb41f65b67f791a8ba1490f4856eb4c971cb1e0bc7852f51`  
		Last Modified: Fri, 07 Feb 2025 01:28:38 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9-community` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:237825bcfca59b55eaa7161e9bc6ff71247e65c4cca767794e9b4fd01ff5d5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 MB (390315625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94587ae4679b4d615b4900c1f6bce69d663e159aa1a1bcda6015a43d925ab938`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a5273c76b40c901cd34ddc6b329776011e758462226a5d6d6a2bf692704208`  
		Last Modified: Tue, 04 Feb 2025 22:13:55 GMT  
		Size: 300.4 MB (300438311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afaf2c5463a558e10923a7881fd89d20aa2ee62998bf35266a5fac6d2ca5cd4`  
		Last Modified: Tue, 04 Feb 2025 22:13:47 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:17890e74c762bdc44cd32291050d64fe9e5f404e31feb930bc17171c62cc0450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48d7365baa884419a58aac731e9575ef48acc2adbe08d3accf46a66bc3a04a0`

```dockerfile
```

-	Layers:
	-	`sha256:16afea09f6dc680e0989e4948f7efb9b1fa896dec69e1c93cb0578738b7fbb4e`  
		Last Modified: Fri, 07 Feb 2025 03:13:28 GMT  
		Size: 4.1 MB (4133668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e5ba9f3c5ba2d2be1835e2065f9c807cd093b7e9783d147e5ed32b678a4b51`  
		Last Modified: Fri, 07 Feb 2025 03:13:27 GMT  
		Size: 18.7 KB (18698 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9-datacenter-app`

```console
$ docker pull sonarqube@sha256:5d04ee0f08fb230f3f10b32f2757c7ab4554990b93fc04c9cea4a315ade29350
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:a6feeb6e43281f40d9fd5034e7347a6ed50c84a908e8ac24999913a9d29d0f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.5 MB (531546748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75facf852e1fdfbe4b957e8ccff021702778dc803d404059408a6a607769d161`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bb216a2398d8a5463909660025b276d133396ba687210c44616097299cfb64`  
		Last Modified: Fri, 07 Feb 2025 01:28:56 GMT  
		Size: 438.9 MB (438919509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52803e1b607dfd27e6505fab366485cfb2a6ed54f00df9c54136536642202aa`  
		Last Modified: Fri, 07 Feb 2025 01:28:49 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:f70922c7927090de1c6cb8949cfa9de0f2b0adf4e05f14ae4e175e2f945d23e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4456107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639fa4865a29f3b3ebd938eecf0cc8c49fd3b9e90e66889bcfe9ccba45984a0b`

```dockerfile
```

-	Layers:
	-	`sha256:449daec43370c3b0c62e416e38af28e224571a31f7eadabc213f7a218230c3d6`  
		Last Modified: Fri, 07 Feb 2025 01:28:49 GMT  
		Size: 4.4 MB (4437147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:058333a3306af69c57763436bd70c8befeba827a245d9a394b312dbd1110b8ea`  
		Last Modified: Fri, 07 Feb 2025 01:28:49 GMT  
		Size: 19.0 KB (18960 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9-datacenter-app` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:c8f3485247cec376a19da99e895ab06fd8ba02f46be34a4b3b369e92736c14f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528800665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c246bc1aeaee5ec94a5d5906a02756b5f6b8f132b3296d48544f49d6e7f589`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab11bacc8d25c9b95d7bdf5f6fb0b1c3ba89ed3069b2c2338d7e2ecc7cf5c5e`  
		Last Modified: Tue, 04 Feb 2025 22:17:53 GMT  
		Size: 438.9 MB (438922791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9f39823315acee512d8252198ad0bf1bc6c08f1301ec7d5cbc4b453e0d20f4`  
		Last Modified: Tue, 04 Feb 2025 22:17:43 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:bcb07c4dc43db50c65ca79c34241684f1fc617883f2689333d7302dd46f6bb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4455898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a192d85a866cc452c2128d1351128e9bb35bd0a202279c585648e59b86ad049b`

```dockerfile
```

-	Layers:
	-	`sha256:f664e51d5c6c4aff5ec4ec1eee5c198664d98fdc0066f5809c07f2cefc8ceb07`  
		Last Modified: Fri, 07 Feb 2025 03:15:23 GMT  
		Size: 4.4 MB (4436833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:052d26c5d17b05e70bf73e4b22677ed5a1b821343510c283414ac4fd3227503d`  
		Last Modified: Fri, 07 Feb 2025 03:15:22 GMT  
		Size: 19.1 KB (19065 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9-datacenter-search`

```console
$ docker pull sonarqube@sha256:109b749dd2c49af743d3892854de3da20a6cade98de0b90ba644a3bd5be461e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:05a7551cfa0eaa87fb6f6c101d9a47572809d38c6702eb6226125ad00e506049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.5 MB (531546500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffdd4277c04d6aab2d77af6b787ef62f3be8beb28a499c0e76c8d23d2d977f01`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2617e6ab2c5244df18d84428554a89cc4f5df587d32a066526b4074d2a1f2b4`  
		Last Modified: Fri, 07 Feb 2025 01:29:27 GMT  
		Size: 438.9 MB (438919444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5723db250fb7c4708fbc9189ff8a28a25d6b345d01c0c92bc763619fb136e05b`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:7e7fb19d61e5c4232a47d7f8a21d36301b44ba5d988bf85519bcb3a3a0400b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4456149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a12de4b51d3cccc8a81878bb17581aafba5fefa806da8add81f57b3bff698d5`

```dockerfile
```

-	Layers:
	-	`sha256:f3ec7955615d5f523c50f2066da4abc6872d71ca1bd55209fc422153b8a96c41`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 4.4 MB (4437171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c2021bf88a8c600484057a015770d220597fcd06812306514437fcccbc64fd1`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 19.0 KB (18978 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9-datacenter-search` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:6cc472486e6b0493cc51d53f113afeb482aba80ce625b00006eb792e291c4cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528800551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2676ea07d61c2e77accdf38ecc57f019b30cf003a46539e8b22183174ed366f9`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43927d251893b5820ea8e41a5e65bb9b0e6725f03d9853f8f695e6673ffe43a1`  
		Last Modified: Tue, 04 Feb 2025 22:19:12 GMT  
		Size: 438.9 MB (438922862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef147e890ed3aab6b3c676c928010a33edbcbd24c588b60376c862f1c4639993`  
		Last Modified: Tue, 04 Feb 2025 22:19:03 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:834691057c730f5d4a6cb905650014b5b48763065be633a163b4d04fe1f9acab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4455940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8099ebcdffc1284128de5ace26e7212cdd7c8553aadf3fbd5337519c8ad627ad`

```dockerfile
```

-	Layers:
	-	`sha256:53eba9f2447a9733f25e585a3dcb12ae377a6e3bd135f0cdb3bb58c8ff3bd553`  
		Last Modified: Fri, 07 Feb 2025 03:16:04 GMT  
		Size: 4.4 MB (4436857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c47effa6ac6ec11f3224681375017ca76e881e8672891451966d1d4fdf90c3`  
		Last Modified: Fri, 07 Feb 2025 03:16:03 GMT  
		Size: 19.1 KB (19083 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9-developer`

```console
$ docker pull sonarqube@sha256:a091fd09e00354b9bb7c00657b66f2977504c485230f50388c54bc4b95273f9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:1380f0d3ccab244539fe6f9408ed0622057cf9568abce3648610439720fa1ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.6 MB (487610342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89974ab9b5c4c3ce1ebde44af1ffddc6f46c5b2c47dc25fe66f7fea52493f66a`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5981a81b883229d13c99a276640aab4d6988e3526296535a0a68a49437d6b838`  
		Last Modified: Fri, 07 Feb 2025 01:29:19 GMT  
		Size: 395.0 MB (394983658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5ca70e0ada20f6870969b0456671f4a47acadf73f71f2f7d4778e82718600f`  
		Last Modified: Fri, 07 Feb 2025 01:29:10 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:69b400165adc32292306342565b99f1fa591099bd58f493937d89dd72ba60311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4267989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121fdceea12a6d55335b3fcf80086d311dc5d928908578bb8cd7099b2a438d6a`

```dockerfile
```

-	Layers:
	-	`sha256:f8ff8e30480a2f0b69b32b180885412c6214169240bb879ff8d7565156072c94`  
		Last Modified: Fri, 07 Feb 2025 01:29:10 GMT  
		Size: 4.2 MB (4249635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a39d14ac277dcd1a4590cc6583641f15d0841b8b13f10201848e6a0b152e7a`  
		Last Modified: Fri, 07 Feb 2025 01:29:10 GMT  
		Size: 18.4 KB (18354 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9-developer` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:84076a9f7faf5a3d056bf1df4ffbb095cd12c894ef1c5332b4efb8da6da2a5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.9 MB (484860900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bbde595ab8d6b1f4a35c9402c825b6075b90c65584c1204c800e28df94624d`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2969729581117bd44d01447103c7d718dac4d29b48612f70f183c316a62c043`  
		Last Modified: Tue, 04 Feb 2025 22:15:10 GMT  
		Size: 395.0 MB (394983588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3ecccb316d0d618a12fd4a0c0b4e75488ce71a59cc1a69ac6372234bf1a19a`  
		Last Modified: Tue, 04 Feb 2025 22:14:59 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c0c47bff0e5ba1e7e81814e3cdb40cfa8cd6c44ff39c46b659e6828d02ea0646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4267771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce1a570bb21b4da14257e063b969cb4fa3456096da8234010fa4044401a66c4`

```dockerfile
```

-	Layers:
	-	`sha256:20abdd35fc85ace34a4a1f3609a98ed8fbe7945751c809a52b3ff831a6d3d64f`  
		Last Modified: Fri, 07 Feb 2025 03:14:05 GMT  
		Size: 4.2 MB (4249315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4150f563c4a9d7080f90ad51e1822f7bb6afc7018e5aa7e55c0ceb73c61cfa03`  
		Last Modified: Fri, 07 Feb 2025 03:14:05 GMT  
		Size: 18.5 KB (18456 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9-enterprise`

```console
$ docker pull sonarqube@sha256:b8bbf13192a8d7f85e331e1efd7c19f12f78b0315d4aba0da8595e5fceba88ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:c2281009e888ddf5dea30836232e5a247eab528fbc614be51e60ae31c49c7eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.7 MB (506686525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20afb5215d171b99eaba409c926726b820c335f6d61c746f936e49caad213274`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca27ea1ed4da23390dbc86b09dd1ea1294fb49213e742700f7e803b8d4507b2`  
		Last Modified: Fri, 07 Feb 2025 01:29:30 GMT  
		Size: 414.1 MB (414059843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6aa4df23f28364955efdf59377955ef08044943abe25c61e6f2669e04250a1b`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:1e6ad8237635e7dabaad87958b93281a03853aa202891bd3905680af47900b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4315189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e8885c751ff83519bde734285abcbf73a049f3d39844251cf85da8becf593f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c9b6799024e6a863903dcad594a782efc0e9ae26cdbc831267777a2277d87c`  
		Last Modified: Fri, 07 Feb 2025 01:29:21 GMT  
		Size: 4.3 MB (4296818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e242679751954f6913709ca404d9aabbf3a63e7f9fcbb1a6fe5d1bd360c5501e`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 18.4 KB (18371 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9-enterprise` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:4d190e4d9c8e0cdbfa06f27b3a7ff155e06a5d4dd19b5961be89107b81a51a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.9 MB (503937350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae6d58a613cd8508fb53b3fe305fa825a4bc42e3f1167f9b1dbd89475d33389`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855d0c56bfb8eb577d10236aad4af5876a0facce8b020f247c1029a73b81b32e`  
		Last Modified: Tue, 04 Feb 2025 22:16:27 GMT  
		Size: 414.1 MB (414060035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f42d369e3c2f25c71454a60de0724508fb2ca516c06342edc65da172abdbc25`  
		Last Modified: Tue, 04 Feb 2025 22:16:16 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:7a87483e8eab6e127413f6c791e2328a4111c0725011d342d01412a3f8054f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5527ee4d5358502e3721bd925d414398ec0be00d39b0e616e3d9e07a2582d77`

```dockerfile
```

-	Layers:
	-	`sha256:43561abefabe455972b0db5127d94da3eddede51670b4a880b501dab250cb381`  
		Last Modified: Fri, 07 Feb 2025 03:14:43 GMT  
		Size: 4.3 MB (4296498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:212c0f08cc334a972aecfb0f10c24c260ee6ee5566357a5098dd1e44ef01e38d`  
		Last Modified: Fri, 07 Feb 2025 03:14:42 GMT  
		Size: 18.5 KB (18475 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9.9-community`

```console
$ docker pull sonarqube@sha256:95b1826b68e606678882148e28c01c70dc0efe464a0d0c568570b17eedf1a9f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9.9-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:1793dda70059333e88e59261255ac05ce0861bd1ac17436a5f299cdf68d68241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.1 MB (393064917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522e1399903e00890e27e6ff2fb59d7e9650fc7ea2db8a57af0579b0e8391406`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e1e3bdd7bcf133d27cf8c09c794cf0fb192157136466e889bc1ed58a56a202`  
		Last Modified: Fri, 07 Feb 2025 01:28:44 GMT  
		Size: 300.4 MB (300438235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2dce0ce5cad6cfd437ec91b65e228c9301401a304513fa592813473a3b369d6`  
		Last Modified: Fri, 07 Feb 2025 01:28:39 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9-community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:04bfbb3c2ca0d94f91ad10042dc4410788d00a63fdb6d846aa8685d9190ee45a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439b6670621d9cbfa42012e006a94c0f045396dbc6a5a5b6f7d4af4d56661025`

```dockerfile
```

-	Layers:
	-	`sha256:c7c552215db26d6198bcfbaa5fe42a4d2f79d23d8866d8f03e9430a508cef215`  
		Last Modified: Fri, 07 Feb 2025 01:28:39 GMT  
		Size: 4.1 MB (4133976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03eac24c4193ff2cdb41f65b67f791a8ba1490f4856eb4c971cb1e0bc7852f51`  
		Last Modified: Fri, 07 Feb 2025 01:28:38 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9.9-community` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:237825bcfca59b55eaa7161e9bc6ff71247e65c4cca767794e9b4fd01ff5d5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 MB (390315625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94587ae4679b4d615b4900c1f6bce69d663e159aa1a1bcda6015a43d925ab938`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a5273c76b40c901cd34ddc6b329776011e758462226a5d6d6a2bf692704208`  
		Last Modified: Tue, 04 Feb 2025 22:13:55 GMT  
		Size: 300.4 MB (300438311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afaf2c5463a558e10923a7881fd89d20aa2ee62998bf35266a5fac6d2ca5cd4`  
		Last Modified: Tue, 04 Feb 2025 22:13:47 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9-community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:17890e74c762bdc44cd32291050d64fe9e5f404e31feb930bc17171c62cc0450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48d7365baa884419a58aac731e9575ef48acc2adbe08d3accf46a66bc3a04a0`

```dockerfile
```

-	Layers:
	-	`sha256:16afea09f6dc680e0989e4948f7efb9b1fa896dec69e1c93cb0578738b7fbb4e`  
		Last Modified: Fri, 07 Feb 2025 03:13:28 GMT  
		Size: 4.1 MB (4133668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e5ba9f3c5ba2d2be1835e2065f9c807cd093b7e9783d147e5ed32b678a4b51`  
		Last Modified: Fri, 07 Feb 2025 03:13:27 GMT  
		Size: 18.7 KB (18698 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9.9-datacenter-app`

```console
$ docker pull sonarqube@sha256:5d04ee0f08fb230f3f10b32f2757c7ab4554990b93fc04c9cea4a315ade29350
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9.9-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:a6feeb6e43281f40d9fd5034e7347a6ed50c84a908e8ac24999913a9d29d0f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.5 MB (531546748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75facf852e1fdfbe4b957e8ccff021702778dc803d404059408a6a607769d161`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bb216a2398d8a5463909660025b276d133396ba687210c44616097299cfb64`  
		Last Modified: Fri, 07 Feb 2025 01:28:56 GMT  
		Size: 438.9 MB (438919509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52803e1b607dfd27e6505fab366485cfb2a6ed54f00df9c54136536642202aa`  
		Last Modified: Fri, 07 Feb 2025 01:28:49 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:f70922c7927090de1c6cb8949cfa9de0f2b0adf4e05f14ae4e175e2f945d23e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4456107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639fa4865a29f3b3ebd938eecf0cc8c49fd3b9e90e66889bcfe9ccba45984a0b`

```dockerfile
```

-	Layers:
	-	`sha256:449daec43370c3b0c62e416e38af28e224571a31f7eadabc213f7a218230c3d6`  
		Last Modified: Fri, 07 Feb 2025 01:28:49 GMT  
		Size: 4.4 MB (4437147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:058333a3306af69c57763436bd70c8befeba827a245d9a394b312dbd1110b8ea`  
		Last Modified: Fri, 07 Feb 2025 01:28:49 GMT  
		Size: 19.0 KB (18960 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9.9-datacenter-app` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:c8f3485247cec376a19da99e895ab06fd8ba02f46be34a4b3b369e92736c14f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528800665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c246bc1aeaee5ec94a5d5906a02756b5f6b8f132b3296d48544f49d6e7f589`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab11bacc8d25c9b95d7bdf5f6fb0b1c3ba89ed3069b2c2338d7e2ecc7cf5c5e`  
		Last Modified: Tue, 04 Feb 2025 22:17:53 GMT  
		Size: 438.9 MB (438922791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9f39823315acee512d8252198ad0bf1bc6c08f1301ec7d5cbc4b453e0d20f4`  
		Last Modified: Tue, 04 Feb 2025 22:17:43 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:bcb07c4dc43db50c65ca79c34241684f1fc617883f2689333d7302dd46f6bb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4455898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a192d85a866cc452c2128d1351128e9bb35bd0a202279c585648e59b86ad049b`

```dockerfile
```

-	Layers:
	-	`sha256:f664e51d5c6c4aff5ec4ec1eee5c198664d98fdc0066f5809c07f2cefc8ceb07`  
		Last Modified: Fri, 07 Feb 2025 03:15:23 GMT  
		Size: 4.4 MB (4436833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:052d26c5d17b05e70bf73e4b22677ed5a1b821343510c283414ac4fd3227503d`  
		Last Modified: Fri, 07 Feb 2025 03:15:22 GMT  
		Size: 19.1 KB (19065 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9.9-datacenter-search`

```console
$ docker pull sonarqube@sha256:109b749dd2c49af743d3892854de3da20a6cade98de0b90ba644a3bd5be461e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9.9-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:05a7551cfa0eaa87fb6f6c101d9a47572809d38c6702eb6226125ad00e506049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.5 MB (531546500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffdd4277c04d6aab2d77af6b787ef62f3be8beb28a499c0e76c8d23d2d977f01`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2617e6ab2c5244df18d84428554a89cc4f5df587d32a066526b4074d2a1f2b4`  
		Last Modified: Fri, 07 Feb 2025 01:29:27 GMT  
		Size: 438.9 MB (438919444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5723db250fb7c4708fbc9189ff8a28a25d6b345d01c0c92bc763619fb136e05b`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:7e7fb19d61e5c4232a47d7f8a21d36301b44ba5d988bf85519bcb3a3a0400b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4456149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a12de4b51d3cccc8a81878bb17581aafba5fefa806da8add81f57b3bff698d5`

```dockerfile
```

-	Layers:
	-	`sha256:f3ec7955615d5f523c50f2066da4abc6872d71ca1bd55209fc422153b8a96c41`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 4.4 MB (4437171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c2021bf88a8c600484057a015770d220597fcd06812306514437fcccbc64fd1`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 19.0 KB (18978 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9.9-datacenter-search` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:6cc472486e6b0493cc51d53f113afeb482aba80ce625b00006eb792e291c4cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528800551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2676ea07d61c2e77accdf38ecc57f019b30cf003a46539e8b22183174ed366f9`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43927d251893b5820ea8e41a5e65bb9b0e6725f03d9853f8f695e6673ffe43a1`  
		Last Modified: Tue, 04 Feb 2025 22:19:12 GMT  
		Size: 438.9 MB (438922862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef147e890ed3aab6b3c676c928010a33edbcbd24c588b60376c862f1c4639993`  
		Last Modified: Tue, 04 Feb 2025 22:19:03 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:834691057c730f5d4a6cb905650014b5b48763065be633a163b4d04fe1f9acab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4455940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8099ebcdffc1284128de5ace26e7212cdd7c8553aadf3fbd5337519c8ad627ad`

```dockerfile
```

-	Layers:
	-	`sha256:53eba9f2447a9733f25e585a3dcb12ae377a6e3bd135f0cdb3bb58c8ff3bd553`  
		Last Modified: Fri, 07 Feb 2025 03:16:04 GMT  
		Size: 4.4 MB (4436857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c47effa6ac6ec11f3224681375017ca76e881e8672891451966d1d4fdf90c3`  
		Last Modified: Fri, 07 Feb 2025 03:16:03 GMT  
		Size: 19.1 KB (19083 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9.9-developer`

```console
$ docker pull sonarqube@sha256:a091fd09e00354b9bb7c00657b66f2977504c485230f50388c54bc4b95273f9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9.9-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:1380f0d3ccab244539fe6f9408ed0622057cf9568abce3648610439720fa1ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.6 MB (487610342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89974ab9b5c4c3ce1ebde44af1ffddc6f46c5b2c47dc25fe66f7fea52493f66a`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5981a81b883229d13c99a276640aab4d6988e3526296535a0a68a49437d6b838`  
		Last Modified: Fri, 07 Feb 2025 01:29:19 GMT  
		Size: 395.0 MB (394983658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5ca70e0ada20f6870969b0456671f4a47acadf73f71f2f7d4778e82718600f`  
		Last Modified: Fri, 07 Feb 2025 01:29:10 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:69b400165adc32292306342565b99f1fa591099bd58f493937d89dd72ba60311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4267989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121fdceea12a6d55335b3fcf80086d311dc5d928908578bb8cd7099b2a438d6a`

```dockerfile
```

-	Layers:
	-	`sha256:f8ff8e30480a2f0b69b32b180885412c6214169240bb879ff8d7565156072c94`  
		Last Modified: Fri, 07 Feb 2025 01:29:10 GMT  
		Size: 4.2 MB (4249635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a39d14ac277dcd1a4590cc6583641f15d0841b8b13f10201848e6a0b152e7a`  
		Last Modified: Fri, 07 Feb 2025 01:29:10 GMT  
		Size: 18.4 KB (18354 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9.9-developer` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:84076a9f7faf5a3d056bf1df4ffbb095cd12c894ef1c5332b4efb8da6da2a5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.9 MB (484860900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bbde595ab8d6b1f4a35c9402c825b6075b90c65584c1204c800e28df94624d`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2969729581117bd44d01447103c7d718dac4d29b48612f70f183c316a62c043`  
		Last Modified: Tue, 04 Feb 2025 22:15:10 GMT  
		Size: 395.0 MB (394983588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3ecccb316d0d618a12fd4a0c0b4e75488ce71a59cc1a69ac6372234bf1a19a`  
		Last Modified: Tue, 04 Feb 2025 22:14:59 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c0c47bff0e5ba1e7e81814e3cdb40cfa8cd6c44ff39c46b659e6828d02ea0646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4267771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce1a570bb21b4da14257e063b969cb4fa3456096da8234010fa4044401a66c4`

```dockerfile
```

-	Layers:
	-	`sha256:20abdd35fc85ace34a4a1f3609a98ed8fbe7945751c809a52b3ff831a6d3d64f`  
		Last Modified: Fri, 07 Feb 2025 03:14:05 GMT  
		Size: 4.2 MB (4249315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4150f563c4a9d7080f90ad51e1822f7bb6afc7018e5aa7e55c0ceb73c61cfa03`  
		Last Modified: Fri, 07 Feb 2025 03:14:05 GMT  
		Size: 18.5 KB (18456 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9.9-enterprise`

```console
$ docker pull sonarqube@sha256:b8bbf13192a8d7f85e331e1efd7c19f12f78b0315d4aba0da8595e5fceba88ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9.9-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:c2281009e888ddf5dea30836232e5a247eab528fbc614be51e60ae31c49c7eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.7 MB (506686525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20afb5215d171b99eaba409c926726b820c335f6d61c746f936e49caad213274`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca27ea1ed4da23390dbc86b09dd1ea1294fb49213e742700f7e803b8d4507b2`  
		Last Modified: Fri, 07 Feb 2025 01:29:30 GMT  
		Size: 414.1 MB (414059843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6aa4df23f28364955efdf59377955ef08044943abe25c61e6f2669e04250a1b`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:1e6ad8237635e7dabaad87958b93281a03853aa202891bd3905680af47900b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4315189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e8885c751ff83519bde734285abcbf73a049f3d39844251cf85da8becf593f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c9b6799024e6a863903dcad594a782efc0e9ae26cdbc831267777a2277d87c`  
		Last Modified: Fri, 07 Feb 2025 01:29:21 GMT  
		Size: 4.3 MB (4296818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e242679751954f6913709ca404d9aabbf3a63e7f9fcbb1a6fe5d1bd360c5501e`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 18.4 KB (18371 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9.9-enterprise` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:4d190e4d9c8e0cdbfa06f27b3a7ff155e06a5d4dd19b5961be89107b81a51a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.9 MB (503937350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae6d58a613cd8508fb53b3fe305fa825a4bc42e3f1167f9b1dbd89475d33389`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855d0c56bfb8eb577d10236aad4af5876a0facce8b020f247c1029a73b81b32e`  
		Last Modified: Tue, 04 Feb 2025 22:16:27 GMT  
		Size: 414.1 MB (414060035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f42d369e3c2f25c71454a60de0724508fb2ca516c06342edc65da172abdbc25`  
		Last Modified: Tue, 04 Feb 2025 22:16:16 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:7a87483e8eab6e127413f6c791e2328a4111c0725011d342d01412a3f8054f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5527ee4d5358502e3721bd925d414398ec0be00d39b0e616e3d9e07a2582d77`

```dockerfile
```

-	Layers:
	-	`sha256:43561abefabe455972b0db5127d94da3eddede51670b4a880b501dab250cb381`  
		Last Modified: Fri, 07 Feb 2025 03:14:43 GMT  
		Size: 4.3 MB (4296498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:212c0f08cc334a972aecfb0f10c24c260ee6ee5566357a5098dd1e44ef01e38d`  
		Last Modified: Fri, 07 Feb 2025 03:14:42 GMT  
		Size: 18.5 KB (18475 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9.9.8-community`

```console
$ docker pull sonarqube@sha256:95b1826b68e606678882148e28c01c70dc0efe464a0d0c568570b17eedf1a9f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9.9.8-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:1793dda70059333e88e59261255ac05ce0861bd1ac17436a5f299cdf68d68241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.1 MB (393064917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522e1399903e00890e27e6ff2fb59d7e9650fc7ea2db8a57af0579b0e8391406`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e1e3bdd7bcf133d27cf8c09c794cf0fb192157136466e889bc1ed58a56a202`  
		Last Modified: Fri, 07 Feb 2025 01:28:44 GMT  
		Size: 300.4 MB (300438235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2dce0ce5cad6cfd437ec91b65e228c9301401a304513fa592813473a3b369d6`  
		Last Modified: Fri, 07 Feb 2025 01:28:39 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9.8-community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:04bfbb3c2ca0d94f91ad10042dc4410788d00a63fdb6d846aa8685d9190ee45a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439b6670621d9cbfa42012e006a94c0f045396dbc6a5a5b6f7d4af4d56661025`

```dockerfile
```

-	Layers:
	-	`sha256:c7c552215db26d6198bcfbaa5fe42a4d2f79d23d8866d8f03e9430a508cef215`  
		Last Modified: Fri, 07 Feb 2025 01:28:39 GMT  
		Size: 4.1 MB (4133976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03eac24c4193ff2cdb41f65b67f791a8ba1490f4856eb4c971cb1e0bc7852f51`  
		Last Modified: Fri, 07 Feb 2025 01:28:38 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9.9.8-community` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:237825bcfca59b55eaa7161e9bc6ff71247e65c4cca767794e9b4fd01ff5d5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 MB (390315625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94587ae4679b4d615b4900c1f6bce69d663e159aa1a1bcda6015a43d925ab938`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a5273c76b40c901cd34ddc6b329776011e758462226a5d6d6a2bf692704208`  
		Last Modified: Tue, 04 Feb 2025 22:13:55 GMT  
		Size: 300.4 MB (300438311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afaf2c5463a558e10923a7881fd89d20aa2ee62998bf35266a5fac6d2ca5cd4`  
		Last Modified: Tue, 04 Feb 2025 22:13:47 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9.8-community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:17890e74c762bdc44cd32291050d64fe9e5f404e31feb930bc17171c62cc0450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48d7365baa884419a58aac731e9575ef48acc2adbe08d3accf46a66bc3a04a0`

```dockerfile
```

-	Layers:
	-	`sha256:16afea09f6dc680e0989e4948f7efb9b1fa896dec69e1c93cb0578738b7fbb4e`  
		Last Modified: Fri, 07 Feb 2025 03:13:28 GMT  
		Size: 4.1 MB (4133668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e5ba9f3c5ba2d2be1835e2065f9c807cd093b7e9783d147e5ed32b678a4b51`  
		Last Modified: Fri, 07 Feb 2025 03:13:27 GMT  
		Size: 18.7 KB (18698 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9.9.8-developer`

```console
$ docker pull sonarqube@sha256:a091fd09e00354b9bb7c00657b66f2977504c485230f50388c54bc4b95273f9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:9.9.8-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:1380f0d3ccab244539fe6f9408ed0622057cf9568abce3648610439720fa1ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.6 MB (487610342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89974ab9b5c4c3ce1ebde44af1ffddc6f46c5b2c47dc25fe66f7fea52493f66a`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5981a81b883229d13c99a276640aab4d6988e3526296535a0a68a49437d6b838`  
		Last Modified: Fri, 07 Feb 2025 01:29:19 GMT  
		Size: 395.0 MB (394983658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5ca70e0ada20f6870969b0456671f4a47acadf73f71f2f7d4778e82718600f`  
		Last Modified: Fri, 07 Feb 2025 01:29:10 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9.8-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:69b400165adc32292306342565b99f1fa591099bd58f493937d89dd72ba60311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4267989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121fdceea12a6d55335b3fcf80086d311dc5d928908578bb8cd7099b2a438d6a`

```dockerfile
```

-	Layers:
	-	`sha256:f8ff8e30480a2f0b69b32b180885412c6214169240bb879ff8d7565156072c94`  
		Last Modified: Fri, 07 Feb 2025 01:29:10 GMT  
		Size: 4.2 MB (4249635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a39d14ac277dcd1a4590cc6583641f15d0841b8b13f10201848e6a0b152e7a`  
		Last Modified: Fri, 07 Feb 2025 01:29:10 GMT  
		Size: 18.4 KB (18354 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:9.9.8-developer` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:84076a9f7faf5a3d056bf1df4ffbb095cd12c894ef1c5332b4efb8da6da2a5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.9 MB (484860900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bbde595ab8d6b1f4a35c9402c825b6075b90c65584c1204c800e28df94624d`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2969729581117bd44d01447103c7d718dac4d29b48612f70f183c316a62c043`  
		Last Modified: Tue, 04 Feb 2025 22:15:10 GMT  
		Size: 395.0 MB (394983588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3ecccb316d0d618a12fd4a0c0b4e75488ce71a59cc1a69ac6372234bf1a19a`  
		Last Modified: Tue, 04 Feb 2025 22:14:59 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:9.9.8-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c0c47bff0e5ba1e7e81814e3cdb40cfa8cd6c44ff39c46b659e6828d02ea0646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4267771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce1a570bb21b4da14257e063b969cb4fa3456096da8234010fa4044401a66c4`

```dockerfile
```

-	Layers:
	-	`sha256:20abdd35fc85ace34a4a1f3609a98ed8fbe7945751c809a52b3ff831a6d3d64f`  
		Last Modified: Fri, 07 Feb 2025 03:14:05 GMT  
		Size: 4.2 MB (4249315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4150f563c4a9d7080f90ad51e1822f7bb6afc7018e5aa7e55c0ceb73c61cfa03`  
		Last Modified: Fri, 07 Feb 2025 03:14:05 GMT  
		Size: 18.5 KB (18456 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:9.9.9-datacenter-app`

**does not exist** (yet?)

## `sonarqube:9.9.9-datacenter-search`

**does not exist** (yet?)

## `sonarqube:9.9.9-enterprise`

**does not exist** (yet?)

## `sonarqube:community`

```console
$ docker pull sonarqube@sha256:c0a734bd7e62c1a35794e3a070b4945f5a081b0053201eb926bcb936b0e5d2e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:community` - linux; amd64

```console
$ docker pull sonarqube@sha256:4537ef14a6097a81f6b5dedb2dbf674584e6b0ab70b52fbdcdc03329822d741a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **926.5 MB (926508161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a7de374354b23c76d3c6296244b16ae46b6e1188aff06f81bea35b061ba4e1`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.k8s.description=SonarQube Community Build is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.min-cpu=400m
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.min-memory=2048M
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.non-scalable=true
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Tue, 04 Mar 2025 14:26:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Mar 2025 14:26:37 GMT
ARG SONARQUBE_VERSION=25.3.0.104237
# Tue, 04 Mar 2025 14:26:37 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-25.3.0.104237.zip
# Tue, 04 Mar 2025 14:26:37 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=25.3.0.104237 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Tue, 04 Mar 2025 14:26:37 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Tue, 04 Mar 2025 14:26:37 GMT
# ARGS: SONARQUBE_VERSION=25.3.0.104237 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-25.3.0.104237.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chown -R sonarqube:root ${SONARQUBE_HOME};     chown -R sonarqube:root "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Mar 2025 14:26:37 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Tue, 04 Mar 2025 14:26:37 GMT
COPY --chown=root:root --chmod=555 entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Tue, 04 Mar 2025 14:26:37 GMT
WORKDIR /opt/sonarqube
# Tue, 04 Mar 2025 14:26:37 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Mar 2025 14:26:37 GMT
USER sonarqube
# Tue, 04 Mar 2025 14:26:37 GMT
STOPSIGNAL SIGINT
# Tue, 04 Mar 2025 14:26:37 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9439e8e49454d1cada79e114dd855a92dd3b56cf4cd29fd76e68ffbbde95711`  
		Last Modified: Tue, 04 Mar 2025 18:28:28 GMT  
		Size: 832.8 MB (832835795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f1017e9142664c197cc8ee70dc8391936c10b181c0b6c7b7858cf8089d9a0b`  
		Last Modified: Tue, 04 Mar 2025 18:28:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:dc40b216c134a8462617bffa174633248def5af01b19da6e9d01c88345bc451e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4025432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196fc41ac5cffa8e35e151574cd70ee1b2fa9bca06167f5e20e7de97696f4e11`

```dockerfile
```

-	Layers:
	-	`sha256:0378be74976cb96b01c918dfeb750c9e5675110a443dfd8793a20ee28598161c`  
		Last Modified: Tue, 04 Mar 2025 18:28:11 GMT  
		Size: 4.0 MB (4006260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f890ae483e83b4cdeeeca5c912e5720c1a3e4b1c8c2c7a6350d1392c7dba7ad`  
		Last Modified: Tue, 04 Mar 2025 18:28:11 GMT  
		Size: 19.2 KB (19172 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:community` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:39520ca4f03757d4ffb7b51d796e00a486c3bd2a52a88e49dc337858d18558bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **925.2 MB (925173667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd676a601cab90a3dc967c38da926e0c6597707f620b6eabea7483a8067a0d9`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.k8s.description=SonarQube Community Build is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.min-cpu=400m
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.min-memory=2048M
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.non-scalable=true
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Tue, 04 Mar 2025 14:26:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Mar 2025 14:26:37 GMT
ARG SONARQUBE_VERSION=25.3.0.104237
# Tue, 04 Mar 2025 14:26:37 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-25.3.0.104237.zip
# Tue, 04 Mar 2025 14:26:37 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=25.3.0.104237 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Tue, 04 Mar 2025 14:26:37 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Tue, 04 Mar 2025 14:26:37 GMT
# ARGS: SONARQUBE_VERSION=25.3.0.104237 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-25.3.0.104237.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chown -R sonarqube:root ${SONARQUBE_HOME};     chown -R sonarqube:root "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Mar 2025 14:26:37 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Tue, 04 Mar 2025 14:26:37 GMT
COPY --chown=root:root --chmod=555 entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Tue, 04 Mar 2025 14:26:37 GMT
WORKDIR /opt/sonarqube
# Tue, 04 Mar 2025 14:26:37 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Mar 2025 14:26:37 GMT
USER sonarqube
# Tue, 04 Mar 2025 14:26:37 GMT
STOPSIGNAL SIGINT
# Tue, 04 Mar 2025 14:26:37 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa6bb2ca9de90e5b203b42c785c9e79fa3c087f65e7c584dd230328db41af5b`  
		Last Modified: Tue, 04 Mar 2025 18:28:12 GMT  
		Size: 832.8 MB (832835930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f6ae284075e0ea433ca61298e087d0e6e8c0c5769e6378df68abd162ed8eab`  
		Last Modified: Tue, 04 Mar 2025 18:27:54 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:5f9e91b0dde066d967074c704eb39d7a2739fb130edb497f5b63319655ceaeb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4025982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91cc7e1bda97e08fa8e968b4959405ea598ee8d4870d7a6819592f39f63f6d5c`

```dockerfile
```

-	Layers:
	-	`sha256:dc231aa3fbbeb548fbc347e6d57a384dca6a928e22eb2df2feb4178b1fabab09`  
		Last Modified: Tue, 04 Mar 2025 18:27:55 GMT  
		Size: 4.0 MB (4006719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:117f823a11faed4d51564ddf05781ced65385922d8f09df95a0dd7872978c079`  
		Last Modified: Tue, 04 Mar 2025 18:27:54 GMT  
		Size: 19.3 KB (19263 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:datacenter-app`

```console
$ docker pull sonarqube@sha256:3c01a66774098de4da5d35c3213f5cd9d79f7338dd71ab38c953373965be7a75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:e045593f2e5c7b4850f09fbba380c6c9450cfc3449e02e45b3e0d1453fe75af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1197208142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a1fcfd3a85e321f69e9920002e4d3939095fa9246ea5bfea97a4bc446bfb6f`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=false
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e21bc54673e65f81d2ffc134c57997869f8bdafad81daacc8f192aa995900e`  
		Last Modified: Fri, 07 Feb 2025 01:29:43 GMT  
		Size: 1.1 GB (1103535218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3474bd21b6868e61dc88241206e4b1c395d5324f527f8f4fe0eb143691dfc42`  
		Last Modified: Fri, 07 Feb 2025 01:29:25 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c1524ce02bfd24b137945817e927c6e707f8f18fd02e7e53982334212af3178e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4280552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3268dbfe664179f1e5576fb22755b12a9bc940cae1d91773b1820d6fb20db5`

```dockerfile
```

-	Layers:
	-	`sha256:e672e658b4c96b03d25335d302092702ed81bf53440f6cca12dbe858efd591b7`  
		Last Modified: Fri, 07 Feb 2025 01:29:25 GMT  
		Size: 4.3 MB (4261029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4045135d92cc40fd006c187d6e316adad806e6351f7af5b8e362d36428b03446`  
		Last Modified: Fri, 07 Feb 2025 01:29:25 GMT  
		Size: 19.5 KB (19523 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:datacenter-app` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:1e31a7e3347683b44e1a4b4ee6060c70774f407f686758bda5fc0a8128baf233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1195914349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b8073e5839540b6e025a45e70251c6b6b6022d5c2eabb0a790c8a82d362285`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=false
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92b81d1ba8c2e990435f5c40d82c030f4208f2e43f295ac93253c800a6a3d8c`  
		Last Modified: Tue, 04 Feb 2025 22:27:12 GMT  
		Size: 1.1 GB (1103576057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801fabce23496a0f0cfdba8857acb922e40e1cf36f7daaee24a8b7ecb7881b22`  
		Last Modified: Tue, 04 Feb 2025 22:26:50 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:f6b3123508c80f9a7371f53650aebfe28e5cf7b9b46db8004b18ea4afd970661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4281138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa91a857e1a4630c53a0b36858a2f5f34a9aaa0b8f95cdc8878a2361ddeaaf49`

```dockerfile
```

-	Layers:
	-	`sha256:aeb3cf3d612274d0ef46d26aa4de50c3a37fe2ec6b2effaa498902ba1833bd94`  
		Last Modified: Fri, 07 Feb 2025 03:09:40 GMT  
		Size: 4.3 MB (4261511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f1eb14726a0af5b320bd7867769e18538de0fba57f640bddfd508fdb4c23652`  
		Last Modified: Fri, 07 Feb 2025 03:09:39 GMT  
		Size: 19.6 KB (19627 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:datacenter-search`

```console
$ docker pull sonarqube@sha256:706f5147ce309134d9e3423d293ed21696690b5d813b9a6d700c76ef5ad1e168
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:238d957759b73914deb8c9ead2ac0f78e3a0b36ff2b007363ca9b497c3a4ee32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1197207427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8f786b616180afc4ad3e18ef4c2e3cd2e78b20807aa70f69f14b315a702e82`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=false
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c8bebb8263f05c850f5751eb04bbc9e018025ad8857c0f7222ec66b314754e`  
		Last Modified: Fri, 07 Feb 2025 01:29:53 GMT  
		Size: 1.1 GB (1103534689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6014a00175d30f7ed1b74952516c14543e574e6fa84f4308c8cf3fd3685458`  
		Last Modified: Fri, 07 Feb 2025 01:29:37 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:5891ec1f0f00137267efd42f045d0e4eb3d43e9bd4cd35682391c26d539fece6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4278176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d87fe43ce39f389e0c81a8e528b57c78fe118a2077ffaa79efc75154486f39`

```dockerfile
```

-	Layers:
	-	`sha256:5d433fe7b2e029b1e7b2626f314c7b2065c60cf33604d17d41e40d0785ef9198`  
		Last Modified: Fri, 07 Feb 2025 01:29:37 GMT  
		Size: 4.3 MB (4258490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40834093fcb1febec03268e99b071e8cdd850f5f6784f996ce2e5a96cc03cd5e`  
		Last Modified: Fri, 07 Feb 2025 01:29:37 GMT  
		Size: 19.7 KB (19686 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:datacenter-search` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:6fb2c2050f88285fb457f97577b7cf109cf5eff8193ad23fca9f62fb6c5ef0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1195913614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9644546b79e945c3c239ffc50322f62b9ff17e7e3eb44555983fa4f811c0ba08`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=false
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6372a7f96b95d984a1e03d2b9f8017a58a40538f8f4a277d79c5426f551f5d98`  
		Last Modified: Tue, 04 Feb 2025 22:29:37 GMT  
		Size: 1.1 GB (1103575506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde6ec40bc1053b502172a4c3dffa1cfaaddb7d6f8c270fe553ad8641f4b4684`  
		Last Modified: Tue, 04 Feb 2025 22:29:11 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c75b6e6c1de422cfca56f637e24da1e380b722fdc7fa491186cbed705b89492d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4278762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2dd96e4d314d5f23dbf4e3deda1cc5dd0461ef26963419f9e55beb0251d837`

```dockerfile
```

-	Layers:
	-	`sha256:bc2f0ec19e49043d9ab593813955771f223f523dd06935d4a2aa159642dcdb69`  
		Last Modified: Fri, 07 Feb 2025 03:10:48 GMT  
		Size: 4.3 MB (4258972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f6b7d85648c5d6f51684f03d8512e7906ab2e2b1e608c615ee59219bebaf03f`  
		Last Modified: Fri, 07 Feb 2025 03:10:48 GMT  
		Size: 19.8 KB (19790 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:developer`

```console
$ docker pull sonarqube@sha256:2445e50a08f779da5c5a234a4692c147073edfb0e3f653e555ee79c02e40a17f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:19c8d0f913b4d934c9c280e14bd9922769469d10d31abf697542eca2f78829aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1152584640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db8cff33c9029701bee1350c11b2b907ee8087c0e2486e96c9f6e4c67a567b9`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=true
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1010402eaefb87aefa2e26f9ca25d9ad2e131b368c543b3c5bead9598db50d46`  
		Last Modified: Fri, 07 Feb 2025 01:29:37 GMT  
		Size: 1.1 GB (1058912279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34944d7881e71fb0314b3dae85b4fab047e5c0aefb6b2d78730058536e21c177`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:7348acacf362c3b194050e8dcfc397da6f4dbed573e26a046dd5ecd9b027fc30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4159652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3699524c8cd5a997121070b1778a2839b8ec826026bc883c8019e811d78aa9c6`

```dockerfile
```

-	Layers:
	-	`sha256:0b5a216ee48827eb059d1a524e05c531ff12d551afb7586fd4bbfc2471e3e739`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 4.1 MB (4140605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e8c5fc00d8a344ce57fb8db20c0fc8bec6ee41acf18bc2ce2810c1baa4377c2`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 19.0 KB (19047 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:developer` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:4d7ee399546c929f025c5e3d1c3d5f8be1d231e1b53066b3529a54114029aeb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1151250366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f882a14ec88d74e8d28493feecc76ba7318ca7ed8a93c2b5c9b4bfd090b20f5f`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=true
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b711f9ed3343feadc371c44cb4d97051def6f8a602be436487b86237bc68aa0`  
		Last Modified: Tue, 04 Feb 2025 22:22:04 GMT  
		Size: 1.1 GB (1058912634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce52742a06136cb786e9c3024590c8d5e3bfb44b8e0ed86c964c69a5655eb583`  
		Last Modified: Tue, 04 Feb 2025 22:21:45 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:60cfd9ae3f12b816d79c3ed50020442f70574c960b0587dcf7465a0282f2afe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4160228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684d06f62c4661dc1d11bc87ae932cda8145fc9bf80d03951d400489a3af9c97`

```dockerfile
```

-	Layers:
	-	`sha256:807171e7ad21dce41de484be7397870205800a731aba4ea67a77a79e221b2445`  
		Last Modified: Fri, 07 Feb 2025 03:07:13 GMT  
		Size: 4.1 MB (4141076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1a79869a44ccbea2167a03974ddb4197573152f0c768be4bfb4d87a3ebcaa08`  
		Last Modified: Fri, 07 Feb 2025 03:07:13 GMT  
		Size: 19.2 KB (19152 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:enterprise`

```console
$ docker pull sonarqube@sha256:f4fca15eb2767ad6904b055f06600da9bb2ec9a9ae6c9f31d5a1f8a0a4632564
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:051b5bb64db4d67ce685cfbfe6b612cee9e3d3845e7e30d9f165119bd45a6c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1195176882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff772f29503fdbdf680d8a4ec0c65ab5e7cbedf3a5cbb253f2cdcc6063c70977`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=true
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153734b82608639de6f74daf2d3eaceb27f0982148ca73320787e60722c6e213`  
		Last Modified: Fri, 07 Feb 2025 01:29:39 GMT  
		Size: 1.1 GB (1101504521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b9141f9c8f73cf0d58fc13f517e3579df47d90e8b5b52b564816150062c3bc`  
		Last Modified: Fri, 07 Feb 2025 01:29:23 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:dc4669416390a995c15e95f60711417377e1cf12f4b4dadd1f7dfec802dc3294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80282c785229fe9472e57d5f0fbc5fae77666d2c0d6708c83a18ca2165e5e25c`

```dockerfile
```

-	Layers:
	-	`sha256:1fa177210b8942b78c21d7ff6c768307508c2b61812715486291e36788f51690`  
		Last Modified: Fri, 07 Feb 2025 01:29:23 GMT  
		Size: 4.2 MB (4184086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dfc7bcb99f505d26b9a1357e84d620779ffde33e5e0bba9037dedc7539ff9db`  
		Last Modified: Fri, 07 Feb 2025 01:29:23 GMT  
		Size: 19.1 KB (19064 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:enterprise` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:47c290e53bd77de2f424f8f175e3af8ed89fe10e06d85f97483dc716138d38e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1193842406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5807acd30b73c2a42a242740d6c44dd7576ff7055fa1dddeb5ccd10d62855fd3`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-cpu=400m
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.min-memory=2048M
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.non-scalable=true
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=2025.1.0.102418
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.1.0.102418.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.0.102418 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=2025.1.0.102418 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-2025.1.0.102418.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da32d4f953537ef53f20e5e53a865c3cb427288e5150ae03a7b43f9b7c60aceb`  
		Last Modified: Tue, 04 Feb 2025 22:24:40 GMT  
		Size: 1.1 GB (1101504675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404e90b821f0f9083f833c1c082dd9883a929e40b0c843c38d6d5af79338b470`  
		Last Modified: Tue, 04 Feb 2025 22:24:11 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:9b934fceda3f514b85ed4cdca807d3775beb0c4138f0d785ab0023bea0005aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4203725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42d4ea1c36a303ff1a600d85386608804e53714cdc154e331d51837c16076bf`

```dockerfile
```

-	Layers:
	-	`sha256:dcd52cd5ae77b5d7d978a11f3e7de134f1665307c53c545babbfd3671befad48`  
		Last Modified: Fri, 07 Feb 2025 03:08:27 GMT  
		Size: 4.2 MB (4184557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2376259bb6062f6c74aa3ea967cc3070a824ec408e8c83cc419d46604efbea75`  
		Last Modified: Fri, 07 Feb 2025 03:08:27 GMT  
		Size: 19.2 KB (19168 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:latest`

```console
$ docker pull sonarqube@sha256:c0a734bd7e62c1a35794e3a070b4945f5a081b0053201eb926bcb936b0e5d2e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:latest` - linux; amd64

```console
$ docker pull sonarqube@sha256:4537ef14a6097a81f6b5dedb2dbf674584e6b0ab70b52fbdcdc03329822d741a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **926.5 MB (926508161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a7de374354b23c76d3c6296244b16ae46b6e1188aff06f81bea35b061ba4e1`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.k8s.description=SonarQube Community Build is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.min-cpu=400m
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.min-memory=2048M
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.non-scalable=true
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Tue, 04 Mar 2025 14:26:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Mar 2025 14:26:37 GMT
ARG SONARQUBE_VERSION=25.3.0.104237
# Tue, 04 Mar 2025 14:26:37 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-25.3.0.104237.zip
# Tue, 04 Mar 2025 14:26:37 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=25.3.0.104237 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Tue, 04 Mar 2025 14:26:37 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Tue, 04 Mar 2025 14:26:37 GMT
# ARGS: SONARQUBE_VERSION=25.3.0.104237 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-25.3.0.104237.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chown -R sonarqube:root ${SONARQUBE_HOME};     chown -R sonarqube:root "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Mar 2025 14:26:37 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Tue, 04 Mar 2025 14:26:37 GMT
COPY --chown=root:root --chmod=555 entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Tue, 04 Mar 2025 14:26:37 GMT
WORKDIR /opt/sonarqube
# Tue, 04 Mar 2025 14:26:37 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Mar 2025 14:26:37 GMT
USER sonarqube
# Tue, 04 Mar 2025 14:26:37 GMT
STOPSIGNAL SIGINT
# Tue, 04 Mar 2025 14:26:37 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 04:39:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9439e8e49454d1cada79e114dd855a92dd3b56cf4cd29fd76e68ffbbde95711`  
		Last Modified: Tue, 04 Mar 2025 18:28:28 GMT  
		Size: 832.8 MB (832835795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f1017e9142664c197cc8ee70dc8391936c10b181c0b6c7b7858cf8089d9a0b`  
		Last Modified: Tue, 04 Mar 2025 18:28:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:latest` - unknown; unknown

```console
$ docker pull sonarqube@sha256:dc40b216c134a8462617bffa174633248def5af01b19da6e9d01c88345bc451e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4025432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196fc41ac5cffa8e35e151574cd70ee1b2fa9bca06167f5e20e7de97696f4e11`

```dockerfile
```

-	Layers:
	-	`sha256:0378be74976cb96b01c918dfeb750c9e5675110a443dfd8793a20ee28598161c`  
		Last Modified: Tue, 04 Mar 2025 18:28:11 GMT  
		Size: 4.0 MB (4006260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f890ae483e83b4cdeeeca5c912e5720c1a3e4b1c8c2c7a6350d1392c7dba7ad`  
		Last Modified: Tue, 04 Mar 2025 18:28:11 GMT  
		Size: 19.2 KB (19172 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:latest` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:39520ca4f03757d4ffb7b51d796e00a486c3bd2a52a88e49dc337858d18558bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **925.2 MB (925173667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd676a601cab90a3dc967c38da926e0c6597707f620b6eabea7483a8067a0d9`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.k8s.description=SonarQube Community Build is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.min-cpu=400m
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.min-memory=2048M
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.non-scalable=true
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Tue, 04 Mar 2025 14:26:37 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Tue, 04 Mar 2025 14:26:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Mar 2025 14:26:37 GMT
ARG SONARQUBE_VERSION=25.3.0.104237
# Tue, 04 Mar 2025 14:26:37 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-25.3.0.104237.zip
# Tue, 04 Mar 2025 14:26:37 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=25.3.0.104237 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Tue, 04 Mar 2025 14:26:37 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Tue, 04 Mar 2025 14:26:37 GMT
# ARGS: SONARQUBE_VERSION=25.3.0.104237 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-25.3.0.104237.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chown -R sonarqube:root ${SONARQUBE_HOME};     chown -R sonarqube:root "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 04 Mar 2025 14:26:37 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Tue, 04 Mar 2025 14:26:37 GMT
COPY --chown=root:root --chmod=555 entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Tue, 04 Mar 2025 14:26:37 GMT
WORKDIR /opt/sonarqube
# Tue, 04 Mar 2025 14:26:37 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Mar 2025 14:26:37 GMT
USER sonarqube
# Tue, 04 Mar 2025 14:26:37 GMT
STOPSIGNAL SIGINT
# Tue, 04 Mar 2025 14:26:37 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 09:17:44 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 09:23:22 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 09:23:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa6bb2ca9de90e5b203b42c785c9e79fa3c087f65e7c584dd230328db41af5b`  
		Last Modified: Tue, 04 Mar 2025 18:28:12 GMT  
		Size: 832.8 MB (832835930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f6ae284075e0ea433ca61298e087d0e6e8c0c5769e6378df68abd162ed8eab`  
		Last Modified: Tue, 04 Mar 2025 18:27:54 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:latest` - unknown; unknown

```console
$ docker pull sonarqube@sha256:5f9e91b0dde066d967074c704eb39d7a2739fb130edb497f5b63319655ceaeb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4025982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91cc7e1bda97e08fa8e968b4959405ea598ee8d4870d7a6819592f39f63f6d5c`

```dockerfile
```

-	Layers:
	-	`sha256:dc231aa3fbbeb548fbc347e6d57a384dca6a928e22eb2df2feb4178b1fabab09`  
		Last Modified: Tue, 04 Mar 2025 18:27:55 GMT  
		Size: 4.0 MB (4006719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:117f823a11faed4d51564ddf05781ced65385922d8f09df95a0dd7872978c079`  
		Last Modified: Tue, 04 Mar 2025 18:27:54 GMT  
		Size: 19.3 KB (19263 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:lts`

```console
$ docker pull sonarqube@sha256:95b1826b68e606678882148e28c01c70dc0efe464a0d0c568570b17eedf1a9f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:lts` - linux; amd64

```console
$ docker pull sonarqube@sha256:1793dda70059333e88e59261255ac05ce0861bd1ac17436a5f299cdf68d68241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.1 MB (393064917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522e1399903e00890e27e6ff2fb59d7e9650fc7ea2db8a57af0579b0e8391406`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e1e3bdd7bcf133d27cf8c09c794cf0fb192157136466e889bc1ed58a56a202`  
		Last Modified: Fri, 07 Feb 2025 01:28:44 GMT  
		Size: 300.4 MB (300438235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2dce0ce5cad6cfd437ec91b65e228c9301401a304513fa592813473a3b369d6`  
		Last Modified: Fri, 07 Feb 2025 01:28:39 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts` - unknown; unknown

```console
$ docker pull sonarqube@sha256:04bfbb3c2ca0d94f91ad10042dc4410788d00a63fdb6d846aa8685d9190ee45a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439b6670621d9cbfa42012e006a94c0f045396dbc6a5a5b6f7d4af4d56661025`

```dockerfile
```

-	Layers:
	-	`sha256:c7c552215db26d6198bcfbaa5fe42a4d2f79d23d8866d8f03e9430a508cef215`  
		Last Modified: Fri, 07 Feb 2025 01:28:39 GMT  
		Size: 4.1 MB (4133976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03eac24c4193ff2cdb41f65b67f791a8ba1490f4856eb4c971cb1e0bc7852f51`  
		Last Modified: Fri, 07 Feb 2025 01:28:38 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:lts` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:237825bcfca59b55eaa7161e9bc6ff71247e65c4cca767794e9b4fd01ff5d5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 MB (390315625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94587ae4679b4d615b4900c1f6bce69d663e159aa1a1bcda6015a43d925ab938`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a5273c76b40c901cd34ddc6b329776011e758462226a5d6d6a2bf692704208`  
		Last Modified: Tue, 04 Feb 2025 22:13:55 GMT  
		Size: 300.4 MB (300438311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afaf2c5463a558e10923a7881fd89d20aa2ee62998bf35266a5fac6d2ca5cd4`  
		Last Modified: Tue, 04 Feb 2025 22:13:47 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts` - unknown; unknown

```console
$ docker pull sonarqube@sha256:17890e74c762bdc44cd32291050d64fe9e5f404e31feb930bc17171c62cc0450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48d7365baa884419a58aac731e9575ef48acc2adbe08d3accf46a66bc3a04a0`

```dockerfile
```

-	Layers:
	-	`sha256:16afea09f6dc680e0989e4948f7efb9b1fa896dec69e1c93cb0578738b7fbb4e`  
		Last Modified: Fri, 07 Feb 2025 03:13:28 GMT  
		Size: 4.1 MB (4133668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e5ba9f3c5ba2d2be1835e2065f9c807cd093b7e9783d147e5ed32b678a4b51`  
		Last Modified: Fri, 07 Feb 2025 03:13:27 GMT  
		Size: 18.7 KB (18698 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:lts-community`

```console
$ docker pull sonarqube@sha256:95b1826b68e606678882148e28c01c70dc0efe464a0d0c568570b17eedf1a9f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:lts-community` - linux; amd64

```console
$ docker pull sonarqube@sha256:1793dda70059333e88e59261255ac05ce0861bd1ac17436a5f299cdf68d68241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.1 MB (393064917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522e1399903e00890e27e6ff2fb59d7e9650fc7ea2db8a57af0579b0e8391406`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e1e3bdd7bcf133d27cf8c09c794cf0fb192157136466e889bc1ed58a56a202`  
		Last Modified: Fri, 07 Feb 2025 01:28:44 GMT  
		Size: 300.4 MB (300438235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2dce0ce5cad6cfd437ec91b65e228c9301401a304513fa592813473a3b369d6`  
		Last Modified: Fri, 07 Feb 2025 01:28:39 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts-community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:04bfbb3c2ca0d94f91ad10042dc4410788d00a63fdb6d846aa8685d9190ee45a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439b6670621d9cbfa42012e006a94c0f045396dbc6a5a5b6f7d4af4d56661025`

```dockerfile
```

-	Layers:
	-	`sha256:c7c552215db26d6198bcfbaa5fe42a4d2f79d23d8866d8f03e9430a508cef215`  
		Last Modified: Fri, 07 Feb 2025 01:28:39 GMT  
		Size: 4.1 MB (4133976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03eac24c4193ff2cdb41f65b67f791a8ba1490f4856eb4c971cb1e0bc7852f51`  
		Last Modified: Fri, 07 Feb 2025 01:28:38 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:lts-community` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:237825bcfca59b55eaa7161e9bc6ff71247e65c4cca767794e9b4fd01ff5d5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 MB (390315625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94587ae4679b4d615b4900c1f6bce69d663e159aa1a1bcda6015a43d925ab938`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a5273c76b40c901cd34ddc6b329776011e758462226a5d6d6a2bf692704208`  
		Last Modified: Tue, 04 Feb 2025 22:13:55 GMT  
		Size: 300.4 MB (300438311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afaf2c5463a558e10923a7881fd89d20aa2ee62998bf35266a5fac6d2ca5cd4`  
		Last Modified: Tue, 04 Feb 2025 22:13:47 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts-community` - unknown; unknown

```console
$ docker pull sonarqube@sha256:17890e74c762bdc44cd32291050d64fe9e5f404e31feb930bc17171c62cc0450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48d7365baa884419a58aac731e9575ef48acc2adbe08d3accf46a66bc3a04a0`

```dockerfile
```

-	Layers:
	-	`sha256:16afea09f6dc680e0989e4948f7efb9b1fa896dec69e1c93cb0578738b7fbb4e`  
		Last Modified: Fri, 07 Feb 2025 03:13:28 GMT  
		Size: 4.1 MB (4133668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e5ba9f3c5ba2d2be1835e2065f9c807cd093b7e9783d147e5ed32b678a4b51`  
		Last Modified: Fri, 07 Feb 2025 03:13:27 GMT  
		Size: 18.7 KB (18698 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:lts-datacenter-app`

```console
$ docker pull sonarqube@sha256:5d04ee0f08fb230f3f10b32f2757c7ab4554990b93fc04c9cea4a315ade29350
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:lts-datacenter-app` - linux; amd64

```console
$ docker pull sonarqube@sha256:a6feeb6e43281f40d9fd5034e7347a6ed50c84a908e8ac24999913a9d29d0f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.5 MB (531546748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75facf852e1fdfbe4b957e8ccff021702778dc803d404059408a6a607769d161`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bb216a2398d8a5463909660025b276d133396ba687210c44616097299cfb64`  
		Last Modified: Fri, 07 Feb 2025 01:28:56 GMT  
		Size: 438.9 MB (438919509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52803e1b607dfd27e6505fab366485cfb2a6ed54f00df9c54136536642202aa`  
		Last Modified: Fri, 07 Feb 2025 01:28:49 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:f70922c7927090de1c6cb8949cfa9de0f2b0adf4e05f14ae4e175e2f945d23e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4456107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639fa4865a29f3b3ebd938eecf0cc8c49fd3b9e90e66889bcfe9ccba45984a0b`

```dockerfile
```

-	Layers:
	-	`sha256:449daec43370c3b0c62e416e38af28e224571a31f7eadabc213f7a218230c3d6`  
		Last Modified: Fri, 07 Feb 2025 01:28:49 GMT  
		Size: 4.4 MB (4437147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:058333a3306af69c57763436bd70c8befeba827a245d9a394b312dbd1110b8ea`  
		Last Modified: Fri, 07 Feb 2025 01:28:49 GMT  
		Size: 19.0 KB (18960 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:lts-datacenter-app` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:c8f3485247cec376a19da99e895ab06fd8ba02f46be34a4b3b369e92736c14f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528800665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c246bc1aeaee5ec94a5d5906a02756b5f6b8f132b3296d48544f49d6e7f589`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=application SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab11bacc8d25c9b95d7bdf5f6fb0b1c3ba89ed3069b2c2338d7e2ecc7cf5c5e`  
		Last Modified: Tue, 04 Feb 2025 22:17:53 GMT  
		Size: 438.9 MB (438922791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9f39823315acee512d8252198ad0bf1bc6c08f1301ec7d5cbc4b453e0d20f4`  
		Last Modified: Tue, 04 Feb 2025 22:17:43 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts-datacenter-app` - unknown; unknown

```console
$ docker pull sonarqube@sha256:bcb07c4dc43db50c65ca79c34241684f1fc617883f2689333d7302dd46f6bb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4455898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a192d85a866cc452c2128d1351128e9bb35bd0a202279c585648e59b86ad049b`

```dockerfile
```

-	Layers:
	-	`sha256:f664e51d5c6c4aff5ec4ec1eee5c198664d98fdc0066f5809c07f2cefc8ceb07`  
		Last Modified: Fri, 07 Feb 2025 03:15:23 GMT  
		Size: 4.4 MB (4436833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:052d26c5d17b05e70bf73e4b22677ed5a1b821343510c283414ac4fd3227503d`  
		Last Modified: Fri, 07 Feb 2025 03:15:22 GMT  
		Size: 19.1 KB (19065 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:lts-datacenter-search`

```console
$ docker pull sonarqube@sha256:109b749dd2c49af743d3892854de3da20a6cade98de0b90ba644a3bd5be461e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:lts-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:05a7551cfa0eaa87fb6f6c101d9a47572809d38c6702eb6226125ad00e506049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.5 MB (531546500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffdd4277c04d6aab2d77af6b787ef62f3be8beb28a499c0e76c8d23d2d977f01`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2617e6ab2c5244df18d84428554a89cc4f5df587d32a066526b4074d2a1f2b4`  
		Last Modified: Fri, 07 Feb 2025 01:29:27 GMT  
		Size: 438.9 MB (438919444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5723db250fb7c4708fbc9189ff8a28a25d6b345d01c0c92bc763619fb136e05b`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:7e7fb19d61e5c4232a47d7f8a21d36301b44ba5d988bf85519bcb3a3a0400b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4456149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a12de4b51d3cccc8a81878bb17581aafba5fefa806da8add81f57b3bff698d5`

```dockerfile
```

-	Layers:
	-	`sha256:f3ec7955615d5f523c50f2066da4abc6872d71ca1bd55209fc422153b8a96c41`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 4.4 MB (4437171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c2021bf88a8c600484057a015770d220597fcd06812306514437fcccbc64fd1`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 19.0 KB (18978 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:lts-datacenter-search` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:6cc472486e6b0493cc51d53f113afeb482aba80ce625b00006eb792e291c4cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.8 MB (528800551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2676ea07d61c2e77accdf38ecc57f019b30cf003a46539e8b22183174ed366f9`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43927d251893b5820ea8e41a5e65bb9b0e6725f03d9853f8f695e6673ffe43a1`  
		Last Modified: Tue, 04 Feb 2025 22:19:12 GMT  
		Size: 438.9 MB (438922862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef147e890ed3aab6b3c676c928010a33edbcbd24c588b60376c862f1c4639993`  
		Last Modified: Tue, 04 Feb 2025 22:19:03 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:834691057c730f5d4a6cb905650014b5b48763065be633a163b4d04fe1f9acab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4455940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8099ebcdffc1284128de5ace26e7212cdd7c8553aadf3fbd5337519c8ad627ad`

```dockerfile
```

-	Layers:
	-	`sha256:53eba9f2447a9733f25e585a3dcb12ae377a6e3bd135f0cdb3bb58c8ff3bd553`  
		Last Modified: Fri, 07 Feb 2025 03:16:04 GMT  
		Size: 4.4 MB (4436857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c47effa6ac6ec11f3224681375017ca76e881e8672891451966d1d4fdf90c3`  
		Last Modified: Fri, 07 Feb 2025 03:16:03 GMT  
		Size: 19.1 KB (19083 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:lts-developer`

```console
$ docker pull sonarqube@sha256:a091fd09e00354b9bb7c00657b66f2977504c485230f50388c54bc4b95273f9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:lts-developer` - linux; amd64

```console
$ docker pull sonarqube@sha256:1380f0d3ccab244539fe6f9408ed0622057cf9568abce3648610439720fa1ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.6 MB (487610342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89974ab9b5c4c3ce1ebde44af1ffddc6f46c5b2c47dc25fe66f7fea52493f66a`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5981a81b883229d13c99a276640aab4d6988e3526296535a0a68a49437d6b838`  
		Last Modified: Fri, 07 Feb 2025 01:29:19 GMT  
		Size: 395.0 MB (394983658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5ca70e0ada20f6870969b0456671f4a47acadf73f71f2f7d4778e82718600f`  
		Last Modified: Fri, 07 Feb 2025 01:29:10 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:69b400165adc32292306342565b99f1fa591099bd58f493937d89dd72ba60311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4267989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:121fdceea12a6d55335b3fcf80086d311dc5d928908578bb8cd7099b2a438d6a`

```dockerfile
```

-	Layers:
	-	`sha256:f8ff8e30480a2f0b69b32b180885412c6214169240bb879ff8d7565156072c94`  
		Last Modified: Fri, 07 Feb 2025 01:29:10 GMT  
		Size: 4.2 MB (4249635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a39d14ac277dcd1a4590cc6583641f15d0841b8b13f10201848e6a0b152e7a`  
		Last Modified: Fri, 07 Feb 2025 01:29:10 GMT  
		Size: 18.4 KB (18354 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:lts-developer` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:84076a9f7faf5a3d056bf1df4ffbb095cd12c894ef1c5332b4efb8da6da2a5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.9 MB (484860900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bbde595ab8d6b1f4a35c9402c825b6075b90c65584c1204c800e28df94624d`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-developer/sonarqube-developer-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2969729581117bd44d01447103c7d718dac4d29b48612f70f183c316a62c043`  
		Last Modified: Tue, 04 Feb 2025 22:15:10 GMT  
		Size: 395.0 MB (394983588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3ecccb316d0d618a12fd4a0c0b4e75488ce71a59cc1a69ac6372234bf1a19a`  
		Last Modified: Tue, 04 Feb 2025 22:14:59 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts-developer` - unknown; unknown

```console
$ docker pull sonarqube@sha256:c0c47bff0e5ba1e7e81814e3cdb40cfa8cd6c44ff39c46b659e6828d02ea0646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4267771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce1a570bb21b4da14257e063b969cb4fa3456096da8234010fa4044401a66c4`

```dockerfile
```

-	Layers:
	-	`sha256:20abdd35fc85ace34a4a1f3609a98ed8fbe7945751c809a52b3ff831a6d3d64f`  
		Last Modified: Fri, 07 Feb 2025 03:14:05 GMT  
		Size: 4.2 MB (4249315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4150f563c4a9d7080f90ad51e1822f7bb6afc7018e5aa7e55c0ceb73c61cfa03`  
		Last Modified: Fri, 07 Feb 2025 03:14:05 GMT  
		Size: 18.5 KB (18456 bytes)  
		MIME: application/vnd.in-toto+json

## `sonarqube:lts-enterprise`

```console
$ docker pull sonarqube@sha256:b8bbf13192a8d7f85e331e1efd7c19f12f78b0315d4aba0da8595e5fceba88ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:lts-enterprise` - linux; amd64

```console
$ docker pull sonarqube@sha256:c2281009e888ddf5dea30836232e5a247eab528fbc614be51e60ae31c49c7eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.7 MB (506686525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20afb5215d171b99eaba409c926726b820c335f6d61c746f936e49caad213274`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 04:40:07 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 04:40:08 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 04:40:06 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca27ea1ed4da23390dbc86b09dd1ea1294fb49213e742700f7e803b8d4507b2`  
		Last Modified: Fri, 07 Feb 2025 01:29:30 GMT  
		Size: 414.1 MB (414059843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6aa4df23f28364955efdf59377955ef08044943abe25c61e6f2669e04250a1b`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:1e6ad8237635e7dabaad87958b93281a03853aa202891bd3905680af47900b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4315189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e8885c751ff83519bde734285abcbf73a049f3d39844251cf85da8becf593f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c9b6799024e6a863903dcad594a782efc0e9ae26cdbc831267777a2277d87c`  
		Last Modified: Fri, 07 Feb 2025 01:29:21 GMT  
		Size: 4.3 MB (4296818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e242679751954f6913709ca404d9aabbf3a63e7f9fcbb1a6fe5d1bd360c5501e`  
		Last Modified: Fri, 07 Feb 2025 01:29:20 GMT  
		Size: 18.4 KB (18371 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:lts-enterprise` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:4d190e4d9c8e0cdbfa06f27b3a7ff155e06a5d4dd19b5961be89107b81a51a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.9 MB (503937350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae6d58a613cd8508fb53b3fe305fa825a4bc42e3f1167f9b1dbd89475d33389`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/entrypoint.sh"]`

```dockerfile
# Mon, 20 Jan 2025 15:15:41 GMT
ARG RELEASE
# Mon, 20 Jan 2025 15:15:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 20 Jan 2025 15:15:41 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Mon, 20 Jan 2025 15:15:41 GMT
CMD ["/bin/bash"]
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:15:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Jan 2025 15:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_VERSION=9.9.8.100196
# Mon, 20 Jan 2025 15:15:41 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.8.100196.zip
# Mon, 20 Jan 2025 15:15:41 GMT
ENV JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=9.9.8.100196 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp
# Mon, 20 Jan 2025 15:15:41 GMT
# ARGS: SONARQUBE_VERSION=9.9.8.100196 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-enterprise/sonarqube-enterprise-9.9.8.100196.zip
RUN set -eux;     groupadd --system --gid 1000 sonarqube;     useradd --system --uid 1000 --gid sonarqube sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 555 ${SONARQUBE_HOME};     chmod -R ugo+wrX "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
COPY entrypoint.sh /opt/sonarqube/docker/ # buildkit
# Mon, 20 Jan 2025 15:15:41 GMT
WORKDIR /opt/sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 20 Jan 2025 15:15:41 GMT
USER sonarqube
# Mon, 20 Jan 2025 15:15:41 GMT
STOPSIGNAL SIGINT
# Mon, 20 Jan 2025 15:15:41 GMT
ENTRYPOINT ["/opt/sonarqube/docker/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 09:16:50 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 09:22:57 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 09:22:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855d0c56bfb8eb577d10236aad4af5876a0facce8b020f247c1029a73b81b32e`  
		Last Modified: Tue, 04 Feb 2025 22:16:27 GMT  
		Size: 414.1 MB (414060035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f42d369e3c2f25c71454a60de0724508fb2ca516c06342edc65da172abdbc25`  
		Last Modified: Tue, 04 Feb 2025 22:16:16 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:lts-enterprise` - unknown; unknown

```console
$ docker pull sonarqube@sha256:7a87483e8eab6e127413f6c791e2328a4111c0725011d342d01412a3f8054f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5527ee4d5358502e3721bd925d414398ec0be00d39b0e616e3d9e07a2582d77`

```dockerfile
```

-	Layers:
	-	`sha256:43561abefabe455972b0db5127d94da3eddede51670b4a880b501dab250cb381`  
		Last Modified: Fri, 07 Feb 2025 03:14:43 GMT  
		Size: 4.3 MB (4296498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:212c0f08cc334a972aecfb0f10c24c260ee6ee5566357a5098dd1e44ef01e38d`  
		Last Modified: Fri, 07 Feb 2025 03:14:42 GMT  
		Size: 18.5 KB (18475 bytes)  
		MIME: application/vnd.in-toto+json
