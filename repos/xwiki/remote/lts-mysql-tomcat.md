## `xwiki:lts-mysql-tomcat`

```console
$ docker pull xwiki@sha256:2ebf82cdb8d038dff6d2309c2468cce61508d6af997a215b5f3710e8d77574b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:820be9639f2b013a6c0ec40e0897a1385f891d4858dd35628a9523ee73a6f2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.7 MB (617697585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072700238364d4f72a582521b55fc3819184da6e1d8e3e99c0fa8d57dca2b0a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 06 Jan 2025 23:11:14 GMT
ARG RELEASE
# Mon, 06 Jan 2025 23:11:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 06 Jan 2025 23:11:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 06 Jan 2025 23:11:14 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 06 Jan 2025 23:11:14 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 06 Jan 2025 23:11:14 GMT
CMD ["/bin/bash"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
WORKDIR /usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_MAJOR=9
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_VERSION=9.0.98
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Mon, 06 Jan 2025 23:11:14 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT []
# Mon, 06 Jan 2025 23:11:14 GMT
CMD ["catalina.sh" "run"]
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 28 Jan 2025 16:59:47 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
ENV XWIKI_VERSION=16.10.3
# Tue, 28 Jan 2025 16:59:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.3
# Tue, 28 Jan 2025 16:59:47 GMT
ENV XWIKI_DOWNLOAD_SHA256=bf1f77ad964b2285c5a7695ae279bbb26f23df01ea83982bcc644af45a658405
# Tue, 28 Jan 2025 16:59:47 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_VERSION=9.1.0
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Tue, 28 Jan 2025 16:59:47 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
VOLUME [/usr/local/xwiki]
# Tue, 28 Jan 2025 16:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 16:59:47 GMT
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
	-	`sha256:d8cea8bfbc7a7f5bd94a92420adc49b5653ee353352183cf9e184227022c15a4`  
		Last Modified: Tue, 04 Feb 2025 07:14:55 GMT  
		Size: 191.2 MB (191192590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08932600be8071c4c011a40924ad60b560b791470f9f02ea03674e622c084fe9`  
		Last Modified: Tue, 04 Feb 2025 07:14:59 GMT  
		Size: 316.7 MB (316721988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ac57f735a4b6ca4ca070eefc6af3247006c00005d47535d5c29d42b7c463b3`  
		Last Modified: Tue, 04 Feb 2025 07:14:53 GMT  
		Size: 2.4 MB (2434171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b672355cff01cc6effa9ebf1a8874ff73d1c9fc1ccba3d165ed785f7bbde167`  
		Last Modified: Tue, 04 Feb 2025 07:14:53 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12383bfb1ba9c009c79414fd8ccf95175e073ac22776d58f96a15d80aff3dc9c`  
		Last Modified: Tue, 04 Feb 2025 07:14:53 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f0c0cc66c6654e47768ed04ef0f92f38faf9af4cdb34e93f0bce5865bcccaa`  
		Last Modified: Tue, 04 Feb 2025 07:14:54 GMT  
		Size: 6.6 KB (6623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f6b3b9c3929ea8bf7a6a4cfd8b079b1d9977ce90d1a93e323208e1697b5bd5`  
		Last Modified: Tue, 04 Feb 2025 07:14:54 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:301f73dcf3e876731fcc02caaf567308beed1758615c8931a6ec15e2f5029ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8798839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d288dc30bf6bd46fba5cec046757c43c576b9a3945201fb2383f92b9106c36e`

```dockerfile
```

-	Layers:
	-	`sha256:850d94af6ce64a081bd89e5a56c1d10e9be5529eeba3d3327521542500e24e51`  
		Last Modified: Tue, 04 Feb 2025 07:14:53 GMT  
		Size: 8.8 MB (8757313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9340f4a6387461fdde79514d3855a7e53c5b2f707cc17da457d594b0ee5f05`  
		Last Modified: Tue, 04 Feb 2025 07:14:53 GMT  
		Size: 41.5 KB (41526 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:78e0d4f414f7ff752f6925f64ff745d27227c7b36e05eab2828d97cfd65d2c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.6 MB (615551357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96298df5f9f461969e1f5bf2a7661bd4bde024a81694ef34d46211d5f5f2e3da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
WORKDIR /usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_MAJOR=9
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_VERSION=9.0.98
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Mon, 06 Jan 2025 23:11:14 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT []
# Mon, 06 Jan 2025 23:11:14 GMT
CMD ["catalina.sh" "run"]
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 28 Jan 2025 16:59:47 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
ENV XWIKI_VERSION=16.10.3
# Tue, 28 Jan 2025 16:59:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.3
# Tue, 28 Jan 2025 16:59:47 GMT
ENV XWIKI_DOWNLOAD_SHA256=bf1f77ad964b2285c5a7695ae279bbb26f23df01ea83982bcc644af45a658405
# Tue, 28 Jan 2025 16:59:47 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_VERSION=9.1.0
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Tue, 28 Jan 2025 16:59:47 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
VOLUME [/usr/local/xwiki]
# Tue, 28 Jan 2025 16:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 16:59:47 GMT
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
	-	`sha256:87d2fc41bce992426331151d3250dac98e23439ac1d98e09aff5693e96d4bfc3`  
		Last Modified: Fri, 31 Jan 2025 07:14:16 GMT  
		Size: 316.7 MB (316721997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dc301872025cb686040bb3b61aa2e0fa33a1c45f10ee31c54f9ec28da3fd65`  
		Last Modified: Fri, 31 Jan 2025 07:14:09 GMT  
		Size: 2.4 MB (2434170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93073ded09448f9c7bbfb40624631427968bb2684e8148484cfc329af3ed414`  
		Last Modified: Fri, 31 Jan 2025 07:14:09 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ec0126bc56c617ffc4ae6032c58fad2d0e61ed6223fcbe0d353b8b38817592`  
		Last Modified: Fri, 31 Jan 2025 07:14:10 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0feaa15b20e58e41a362fd6f4e4c0ef497caab68d9f4e5f6e89325c6be854bac`  
		Last Modified: Fri, 31 Jan 2025 07:14:10 GMT  
		Size: 6.6 KB (6624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e4466e39512fdfbd1a9f0cb2c4f47ebb690eab0e2ee71d1e6f535037bd9864`  
		Last Modified: Fri, 31 Jan 2025 07:14:11 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:0e81fef5cc78e587db45f64573326af824278bfc37dec1638e21041945948716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8796488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d234e073ddd813cb2c157dd1e8470b52436128054f709d68f2b19b5da5b04be5`

```dockerfile
```

-	Layers:
	-	`sha256:e38b65599f6c4990bb67bdf85b23937dd2d91d42ae6de7e0da8f269090cd7eb1`  
		Last Modified: Fri, 31 Jan 2025 07:14:10 GMT  
		Size: 8.8 MB (8754744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7650a7d61e3846c5dbccd976ae9f9271652f83740867e808085b78bb1cbc60a`  
		Last Modified: Fri, 31 Jan 2025 07:14:09 GMT  
		Size: 41.7 KB (41744 bytes)  
		MIME: application/vnd.in-toto+json
