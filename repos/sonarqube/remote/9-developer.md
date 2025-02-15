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
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13876c96bdc55c77f6254664d5f176d7f50a7fb7ada211636087b9bd0def390d`  
		Last Modified: Tue, 04 Feb 2025 08:00:24 GMT  
		Size: 16.1 MB (16135218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdfc9faee8bf6e06068e1c5753941a27fe6d35151d4155831258da20ae307b`  
		Last Modified: Tue, 04 Feb 2025 07:44:36 GMT  
		Size: 47.0 MB (46952602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b682cc54ed354f1c6d670fbf6e6599f0ba1055ce9b7d5191df7692cb3bc23041`  
		Last Modified: Tue, 04 Feb 2025 07:29:34 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4615ed3a34072f1486c2a464bafdc2e9a4d720abe8690b20f20232864aa7971c`  
		Last Modified: Tue, 04 Feb 2025 07:22:44 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5981a81b883229d13c99a276640aab4d6988e3526296535a0a68a49437d6b838`  
		Last Modified: Fri, 07 Feb 2025 03:57:27 GMT  
		Size: 395.0 MB (394983658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5ca70e0ada20f6870969b0456671f4a47acadf73f71f2f7d4778e82718600f`  
		Last Modified: Fri, 07 Feb 2025 03:53:15 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
		Last Modified: Sat, 15 Feb 2025 09:06:05 GMT  
		Size: 4.2 MB (4249635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a39d14ac277dcd1a4590cc6583641f15d0841b8b13f10201848e6a0b152e7a`  
		Last Modified: Tue, 11 Feb 2025 00:00:22 GMT  
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
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b542dd916502bedf4dd14bd9610d5843b919aed4757a473c4043de50c9ba83`  
		Last Modified: Tue, 04 Feb 2025 11:06:23 GMT  
		Size: 16.1 MB (16052648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6776cda46620adc2b59f56ab611b9aceea84112b098d4b493c32131d86e5ad`  
		Last Modified: Tue, 04 Feb 2025 13:23:17 GMT  
		Size: 46.5 MB (46463561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e53bec90429d4b30e4f831703f86a19f5205af4af5aa9b019cf93023e8c8a1`  
		Last Modified: Tue, 04 Feb 2025 13:40:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32cdfb555e64515082ddfaf9f92db7b1f24a06238df2f4337aeadc294afb76`  
		Last Modified: Tue, 04 Feb 2025 13:45:31 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2969729581117bd44d01447103c7d718dac4d29b48612f70f183c316a62c043`  
		Last Modified: Fri, 07 Feb 2025 02:53:33 GMT  
		Size: 395.0 MB (394983588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3ecccb316d0d618a12fd4a0c0b4e75488ce71a59cc1a69ac6372234bf1a19a`  
		Last Modified: Wed, 05 Feb 2025 17:39:53 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
		Last Modified: Wed, 12 Feb 2025 00:00:22 GMT  
		Size: 4.2 MB (4249315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4150f563c4a9d7080f90ad51e1822f7bb6afc7018e5aa7e55c0ceb73c61cfa03`  
		Last Modified: Mon, 10 Feb 2025 21:58:47 GMT  
		Size: 18.5 KB (18456 bytes)  
		MIME: application/vnd.in-toto+json
