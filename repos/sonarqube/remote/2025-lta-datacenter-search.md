## `sonarqube:2025-lta-datacenter-search`

```console
$ docker pull sonarqube@sha256:6501237d92c9dfd77922cf17f37cd957e7d7c340f391ec0f7adb22d63fb90776
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `sonarqube:2025-lta-datacenter-search` - linux; amd64

```console
$ docker pull sonarqube@sha256:e7edca2de508bbcb7b3fd129e081dfc3de23ebaae53a47c414fb899c64c27314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1203166533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d189a214e12a640d90b913f860d59a151ad51caa43ab0e3dc1f00cd5b118c1b7`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='a8d219a4a97f9c53ba88cb8927910005d4f3d08a87ab1bdebff921ef41afa93d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 12 Mar 2025 16:54:39 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Wed, 12 Mar 2025 16:54:39 GMT
LABEL io.openshift.min-cpu=400m
# Wed, 12 Mar 2025 16:54:39 GMT
LABEL io.openshift.min-memory=2048M
# Wed, 12 Mar 2025 16:54:39 GMT
LABEL io.openshift.non-scalable=false
# Wed, 12 Mar 2025 16:54:39 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Wed, 12 Mar 2025 16:54:39 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Wed, 12 Mar 2025 16:54:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Mar 2025 16:54:39 GMT
ARG SONARQUBE_VERSION=2025.1.1.104738
# Wed, 12 Mar 2025 16:54:39 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.1.104738.zip
# Wed, 12 Mar 2025 16:54:39 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.1.104738 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Wed, 12 Mar 2025 16:54:39 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Wed, 12 Mar 2025 16:54:39 GMT
# ARGS: SONARQUBE_VERSION=2025.1.1.104738 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.1.104738.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 12 Mar 2025 16:54:39 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Wed, 12 Mar 2025 16:54:39 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Wed, 12 Mar 2025 16:54:39 GMT
WORKDIR /opt/sonarqube
# Wed, 12 Mar 2025 16:54:39 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 12 Mar 2025 16:54:39 GMT
USER sonarqube
# Wed, 12 Mar 2025 16:54:39 GMT
STOPSIGNAL SIGINT
# Wed, 12 Mar 2025 16:54:39 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Wed, 12 Mar 2025 16:54:39 GMT
CMD ["/opt/sonarqube/docker/sonar.sh"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab21fde7f674e1262f9a291fb3b148dce3986b16a6afe2b1077240af4411e8d`  
		Last Modified: Tue, 04 Feb 2025 04:40:13 GMT  
		Size: 17.0 MB (16962453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e1027cc04acbd0bbe96f77c4b07270e74687784095964c3f8e1145ed4062a0`  
		Last Modified: Tue, 04 Feb 2025 04:40:14 GMT  
		Size: 52.9 MB (52876121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb109d1b0266a0c777373e83c16fd3b583414425ea70ad73adbf43bf4b8a569e`  
		Last Modified: Tue, 04 Feb 2025 04:40:13 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f09a34126553bccc37644f98b45096297b0127f040e8492684976c77ec2b14a`  
		Last Modified: Tue, 04 Feb 2025 04:40:13 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483cf7cafcdbec0e4497025161a9e85990ff511b26930d42dc05ae3285518124`  
		Last Modified: Wed, 12 Mar 2025 17:29:24 GMT  
		Size: 1.1 GB (1103570368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac46a1f9bb904c6be803bbc77e20d7ff29b6dcd29e0c4452ad7fec495d2a0df3`  
		Last Modified: Wed, 12 Mar 2025 17:28:51 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025-lta-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:8e3e60728c7c6666ef4f2aa5416f79a716bf334935b1f5e88dacc040a4d3b35f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4281169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377ba6b684e4326beebbef0bd0d49fae1c5938f36fcf1fea9bfc67f59bfdac92`

```dockerfile
```

-	Layers:
	-	`sha256:95c74824bd2926e4706ca136068958bbd2c84aff38c7905bf8a48791c5afdeb1`  
		Last Modified: Wed, 12 Mar 2025 17:28:51 GMT  
		Size: 4.3 MB (4261485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42e0ecf47f9ce25632b50f3e133cc0b792a8f857c060a5e71c41b8e80f42af52`  
		Last Modified: Wed, 12 Mar 2025 17:28:50 GMT  
		Size: 19.7 KB (19684 bytes)  
		MIME: application/vnd.in-toto+json

### `sonarqube:2025-lta-datacenter-search` - linux; arm64 variant v8

```console
$ docker pull sonarqube@sha256:a70ad5dd51405623dc933ab2ec93d6371cd91f0e59cb7123358a63799c6ff01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1201542474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f3b23ffa30b157cb7733fbe9dc563bd092c74dddd32d1d26771c699176e15b`
-	Entrypoint: `["\/opt\/sonarqube\/docker\/run.sh"]`
-	Default Command: `["\/opt\/sonarqube\/docker\/sonar.sh"]`

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
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='a8d219a4a97f9c53ba88cb8927910005d4f3d08a87ab1bdebff921ef41afa93d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 12 Mar 2025 16:54:39 GMT
LABEL io.k8s.description=SonarQube Server is a self-managed, automatic code review tool that systematically helps you deliver Clean Code.
# Wed, 12 Mar 2025 16:54:39 GMT
LABEL io.openshift.min-cpu=400m
# Wed, 12 Mar 2025 16:54:39 GMT
LABEL io.openshift.min-memory=2048M
# Wed, 12 Mar 2025 16:54:39 GMT
LABEL io.openshift.non-scalable=false
# Wed, 12 Mar 2025 16:54:39 GMT
LABEL io.openshift.tags=sonarqube,static-code-analysis,code-quality,clean-code
# Wed, 12 Mar 2025 16:54:39 GMT
LABEL org.opencontainers.image.url=https://github.com/SonarSource/docker-sonarqube
# Wed, 12 Mar 2025 16:54:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Mar 2025 16:54:39 GMT
ARG SONARQUBE_VERSION=2025.1.1.104738
# Wed, 12 Mar 2025 16:54:39 GMT
ARG SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.1.104738.zip
# Wed, 12 Mar 2025 16:54:39 GMT
ENV DOCKER_RUNNING=true JAVA_HOME=/opt/java/openjdk SONARQUBE_HOME=/opt/sonarqube SONAR_VERSION=2025.1.1.104738 SQ_DATA_DIR=/opt/sonarqube/data SQ_EXTENSIONS_DIR=/opt/sonarqube/extensions SQ_LOGS_DIR=/opt/sonarqube/logs SQ_TEMP_DIR=/opt/sonarqube/temp SONAR_CLUSTER_NODE_TYPE=search SONAR_CLUSTER_ENABLED=true
# Wed, 12 Mar 2025 16:54:39 GMT
ENV ES_TMPDIR=/opt/sonarqube/temp
# Wed, 12 Mar 2025 16:54:39 GMT
# ARGS: SONARQUBE_VERSION=2025.1.1.104738 SONARQUBE_ZIP_URL=https://binaries.sonarsource.com/CommercialDistribution/sonarqube-datacenter/sonarqube-datacenter-2025.1.1.104738.zip
RUN set -eux;     deluser ubuntu;     useradd --system --uid 1000 --gid 0 sonarqube;     apt-get update;     apt-get --no-install-recommends -y install         bash         curl         fonts-dejavu         gnupg         iproute2         unzip;     echo "networkaddress.cache.ttl=5" >> "${JAVA_HOME}/conf/security/java.security";     sed --in-place --expression="s?securerandom.source=file:/dev/random?securerandom.source=file:/dev/urandom?g" "${JAVA_HOME}/conf/security/java.security";     for server in $(shuf -e hkps://keys.openpgp.org                             hkps://keyserver.ubuntu.com) ; do         gpg --batch --keyserver "${server}" --recv-keys 679F1EE92B19609DE816FDE81DB198F93525EC1A && break || : ;     done;     mkdir --parents /opt;     cd /opt;     curl --fail --location --output sonarqube.zip --silent --show-error "${SONARQUBE_ZIP_URL}";     curl --fail --location --output sonarqube.zip.asc --silent --show-error "${SONARQUBE_ZIP_URL}.asc";     gpg --batch --verify sonarqube.zip.asc sonarqube.zip;     unzip -q sonarqube.zip;     mv "sonarqube-${SONARQUBE_VERSION}" sonarqube;     rm sonarqube.zip*;     rm -rf ${SONARQUBE_HOME}/bin/*;     ln -s "${SONARQUBE_HOME}/lib/sonar-application-${SONARQUBE_VERSION}.jar" "${SONARQUBE_HOME}/lib/sonarqube.jar";     chmod -R 550 ${SONARQUBE_HOME};     chmod -R 770 "${SQ_DATA_DIR}" "${SQ_EXTENSIONS_DIR}" "${SQ_LOGS_DIR}" "${SQ_TEMP_DIR}";     apt-get remove -y gnupg unzip curl;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 12 Mar 2025 16:54:39 GMT
VOLUME [/opt/sonarqube/data /opt/sonarqube/extensions /opt/sonarqube/logs /opt/sonarqube/temp]
# Wed, 12 Mar 2025 16:54:39 GMT
COPY run.sh sonar.sh /opt/sonarqube/docker/ # buildkit
# Wed, 12 Mar 2025 16:54:39 GMT
WORKDIR /opt/sonarqube
# Wed, 12 Mar 2025 16:54:39 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 12 Mar 2025 16:54:39 GMT
USER sonarqube
# Wed, 12 Mar 2025 16:54:39 GMT
STOPSIGNAL SIGINT
# Wed, 12 Mar 2025 16:54:39 GMT
ENTRYPOINT ["/opt/sonarqube/docker/run.sh"]
# Wed, 12 Mar 2025 16:54:39 GMT
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
	-	`sha256:d9cbfadccc4ef79b758e18dd8d1708943e6c36b0c9c7e7b94a5d7ff99d3d28af`  
		Last Modified: Tue, 04 Feb 2025 09:25:48 GMT  
		Size: 52.1 MB (52058738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8426c44160873d09bb23bdec752f80f9f6f3a7b054d0cd8a334eeb2c92fa0ed9`  
		Last Modified: Tue, 04 Feb 2025 09:25:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3daf2a897e045b94b8cf1d4c94f9dc6f09163273fbbf52afcd8dc60a445788`  
		Last Modified: Tue, 04 Feb 2025 09:25:47 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969010a5288e35645453adfc8c4f240e31a297541aa0f22faff1b97605886b41`  
		Last Modified: Wed, 12 Mar 2025 17:35:55 GMT  
		Size: 1.1 GB (1103609433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b183ad577d3c22cc53ec89f77d9eb5b60e76038461c0ff3d8b729deea653e6e`  
		Last Modified: Wed, 12 Mar 2025 17:35:33 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sonarqube:2025-lta-datacenter-search` - unknown; unknown

```console
$ docker pull sonarqube@sha256:5edec88ac8466d4d890dbe32bf9f9dea7a0702fde745732b00a011697c970b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4281756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af93184f1730fe376d036717daf69e14baa8fbe9777654bee9ec444879290a8a`

```dockerfile
```

-	Layers:
	-	`sha256:a5038fd1e6b338344fa4db699842a7e3d07de10e2a42c90850d582f0b574c99c`  
		Last Modified: Wed, 12 Mar 2025 17:35:33 GMT  
		Size: 4.3 MB (4261967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a1ba6da918c276ab452f90c61f2ca311310b9542ae1a9a68d942c44297c5a52`  
		Last Modified: Wed, 12 Mar 2025 17:35:33 GMT  
		Size: 19.8 KB (19789 bytes)  
		MIME: application/vnd.in-toto+json
