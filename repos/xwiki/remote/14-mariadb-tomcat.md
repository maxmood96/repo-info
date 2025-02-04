## `xwiki:14-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:853bca946f7e881323d8f6eb9b957287b38becb5f4547a76db226009d859e15b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:14-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:2f14de9702c9843e59aef19c2c1a649fdfeace18a0939a8272d85e07d3a6cace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.7 MB (605694391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd18acc60cc144f8bdb35238eec33acf8c7951514ae0d72e707b6b4f5f347ee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 13 Feb 2024 09:10:03 GMT
ARG RELEASE
# Tue, 13 Feb 2024 09:10:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Feb 2024 09:10:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
WORKDIR /usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_MAJOR=9
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_VERSION=9.0.98
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Tue, 13 Feb 2024 09:10:03 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT []
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["catalina.sh" "run"]
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 13 Feb 2024 09:10:03 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_VERSION=14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=72a634e2aeb085878dce2629a3e5e6136887d0c22712dcee5a284be8143135ea
# Tue, 13 Feb 2024 09:10:03 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_VERSION=3.3.2
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_SHA256=2a67ef3cc1ca481965a0e7f2d4174d126f3464d02b4055a441261fad8c196769
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.2
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.2.jar
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.2.jar
# Tue, 13 Feb 2024 09:10:03 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
VOLUME [/usr/local/xwiki]
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["xwiki"]
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
	-	`sha256:f85dc2acf5a16639a7be82e8637250672ad5125225b58c9b846d91de85ff6aa6`  
		Last Modified: Tue, 04 Feb 2025 06:16:23 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99235fcf52ce91d2f6724171207a06a43c2f4c7059bb7a1226d844a764632c49`  
		Last Modified: Tue, 04 Feb 2025 06:16:23 GMT  
		Size: 13.4 MB (13440276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217af25a5cb00117e44167a05441d8a2f787184289080a645fb0a0668346fe8b`  
		Last Modified: Tue, 04 Feb 2025 06:16:23 GMT  
		Size: 223.6 KB (223636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d50fac20fa7e80b98ef41200d1079458fb54f0f57e1ee64ddbc110baab5928`  
		Last Modified: Tue, 04 Feb 2025 07:15:05 GMT  
		Size: 191.2 MB (191192216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2b795bf1ea319e76cee980f807d10f563ee0cb2441afaa0e25d5eec726e204`  
		Last Modified: Tue, 04 Feb 2025 07:15:07 GMT  
		Size: 306.5 MB (306538808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528614fe17592c9a572407b76ac3f39a721c609ab671cfa3c118d4ce87908edb`  
		Last Modified: Tue, 04 Feb 2025 07:15:03 GMT  
		Size: 615.1 KB (615142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f9401cf661bb437535df4aabc3432c53b258cfe22e068663870014e5062bf4`  
		Last Modified: Tue, 04 Feb 2025 07:15:02 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746fd9335939cf3e9783daeca9dd7f6a0a6aa7deb0a6f6e73cca9a26edc68850`  
		Last Modified: Tue, 04 Feb 2025 07:15:03 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353114b6adf07a778e8c80a33eb905745da3fbfe84ecc9c86ea8350c010fd7f1`  
		Last Modified: Tue, 04 Feb 2025 07:15:03 GMT  
		Size: 6.1 KB (6138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a954df60ce4e06f7767e4fea72469baf0fd39983660a3df20301dbed962646a0`  
		Last Modified: Tue, 04 Feb 2025 07:15:04 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:14-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:10cf8df5494d89350bab886e9b18d565317287ace0e24bd4a5fecb3a8ff76743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8772148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04b094cb90dfd1fa41680a3522a8d5fc97c3b718fe9fa048d82c3cd3158c8c4`

```dockerfile
```

-	Layers:
	-	`sha256:22c153c280801c37a475ef18b4c556b0fae4bbfd00de82fe0d4d393a9ae65ba8`  
		Last Modified: Tue, 04 Feb 2025 07:15:03 GMT  
		Size: 8.7 MB (8732364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e672b414fd6aac5771ffc51bafb0e1b55210f310898d4e7f98c8c419cc7d9bb`  
		Last Modified: Tue, 04 Feb 2025 07:15:02 GMT  
		Size: 39.8 KB (39784 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:14-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:e1bbdbcfdd8d02c692d2ef2c1b1a9f81f6214255b226bfe676004d970261b332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.5 MB (603548416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f273c5515ac0db50a0fd79475b0608461d5050cb70683001c6b79ec774ee5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 13 Feb 2024 09:10:03 GMT
ARG RELEASE
# Tue, 13 Feb 2024 09:10:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Feb 2024 09:10:03 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
WORKDIR /usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_MAJOR=9
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_VERSION=9.0.98
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Tue, 13 Feb 2024 09:10:03 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT []
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["catalina.sh" "run"]
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 13 Feb 2024 09:10:03 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_VERSION=14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=72a634e2aeb085878dce2629a3e5e6136887d0c22712dcee5a284be8143135ea
# Tue, 13 Feb 2024 09:10:03 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_VERSION=3.3.2
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_SHA256=2a67ef3cc1ca481965a0e7f2d4174d126f3464d02b4055a441261fad8c196769
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.2
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.2.jar
# Tue, 13 Feb 2024 09:10:03 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.2.jar
# Tue, 13 Feb 2024 09:10:03 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
VOLUME [/usr/local/xwiki]
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdf56be796e06869f79797ec2f94851f8273a303e6f3fcaa6988296b5f77381`  
		Last Modified: Fri, 31 Jan 2025 01:43:22 GMT  
		Size: 46.5 MB (46463806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8260ceaafcab9714596ba4d69c9f23aebab641359adc1720ffc705e75c749d`  
		Last Modified: Fri, 31 Jan 2025 01:43:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3b39d002240b6b685d23574f681a9673bbcbf96ce4f75330ddbbe567a30fea`  
		Last Modified: Fri, 31 Jan 2025 01:43:20 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d58e4f194d0b58022fafe44639a90285027e946462e92a94b2965769ad371d`  
		Last Modified: Fri, 31 Jan 2025 06:13:38 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5314e98cd979c198bdc695433cd6a9e0a38aa07bbea7238b25ac04180ce35435`  
		Last Modified: Fri, 31 Jan 2025 06:17:46 GMT  
		Size: 13.5 MB (13450931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017832980dae7c4519b73359aaa965e79ef87f99096b93da845fc9ca44cf072c`  
		Last Modified: Fri, 31 Jan 2025 06:17:45 GMT  
		Size: 1.7 MB (1721623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b20fb92ee746216d142bbea87821d905f9e89a56676fd74fec6ac7db7c35a84`  
		Last Modified: Fri, 31 Jan 2025 07:14:13 GMT  
		Size: 188.9 MB (188867811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98c6daa9e17cc0bba9c422bbf022cd80d229c44307a958cc79d7cf986ce3f43`  
		Last Modified: Fri, 31 Jan 2025 07:19:35 GMT  
		Size: 306.5 MB (306538704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a992532a50a573ef1b7c789f8e38dc2284a2cc463745348a77f75bc305772ca`  
		Last Modified: Fri, 31 Jan 2025 07:22:16 GMT  
		Size: 615.1 KB (615141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887c412078bf814449ea4fbffdcaf3d8ca75270212981f814b2486257afe99e6`  
		Last Modified: Fri, 31 Jan 2025 07:22:16 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af07e5cf43847582a2b93a223e56aad276897834de07028e0e6df4810316a2a`  
		Last Modified: Fri, 31 Jan 2025 07:22:16 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aedd2aa2ae2d1b6ca8f04909368d87b2e1969080fcc6afd7c505b920f4ac058`  
		Last Modified: Fri, 31 Jan 2025 07:22:17 GMT  
		Size: 6.1 KB (6140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8226b9762e5518944812a14b56780b49f5d802d7f4a6b84915a37046cf807a2`  
		Last Modified: Fri, 31 Jan 2025 07:22:17 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:14-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:67882f33826827a23d9e3b4922454ecaba8c0e26eeef13a35ea17b795e5e60a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8769652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ad6b0337d1767528be14fce3b2a36b984df9451614bbb818e037c5016fe04d`

```dockerfile
```

-	Layers:
	-	`sha256:356ecee6b03799d946ab7aaeddbf5998a2c4c584577d50ac9d9039f4b2d02e9c`  
		Last Modified: Fri, 31 Jan 2025 07:22:17 GMT  
		Size: 8.7 MB (8729723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d33f6ed81d6e1935b5af8aebabcb2126c03bb94583e6cf5fb23c483026a6eed8`  
		Last Modified: Fri, 31 Jan 2025 07:22:16 GMT  
		Size: 39.9 KB (39929 bytes)  
		MIME: application/vnd.in-toto+json
