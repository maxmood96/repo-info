## `bonita:latest`

```console
$ docker pull bonita@sha256:b59572720d94ce3292056e8a7aa0682e56157800f4e17fad0e151f85e18c69f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:b56df14d9b24fb66c534ae8678b2f78e0b8108b55f72c5f0d40fae814aad52bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (194997968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d0a696230bffd28e88ef6605c90f7479de81fdbbe0bf358543f640698a6c41`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f495749fce8d8974323f30428c1183168f90592dc90bb94c96edab33ffccc94e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='f499e2d5c596fd531c8427b2fb207c9eeabed783adad32aeed64b03dd476a231';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 07:56:28 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 25 Sep 2025 07:56:28 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach # buildkit
# Thu, 25 Sep 2025 07:56:28 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Thu, 25 Sep 2025 07:56:28 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S -G bonita -h /opt/bonita/ -s /sbin/nologin bonita # buildkit
# Thu, 25 Sep 2025 07:56:28 GMT
ARG BONITA_VERSION
# Thu, 25 Sep 2025 07:56:28 GMT
ARG BRANDING_VERSION
# Thu, 25 Sep 2025 07:56:28 GMT
ARG BONITA_SHA256
# Thu, 25 Sep 2025 07:56:28 GMT
ARG BASE_URL
# Thu, 25 Sep 2025 07:56:28 GMT
ARG BONITA_URL
# Thu, 25 Sep 2025 07:56:28 GMT
ENV BONITA_VERSION=10.3.0
# Thu, 25 Sep 2025 07:56:28 GMT
ENV BRANDING_VERSION=2025.1-u0
# Thu, 25 Sep 2025 07:56:28 GMT
ENV BONITA_SHA256=44c078fad0ffeec0afac2bf512040be16af4b722369039fe3daef1c091594637
# Thu, 25 Sep 2025 07:56:28 GMT
ENV ZIP_FILE=BonitaCommunity-2025.1-u0.zip
# Thu, 25 Sep 2025 07:56:28 GMT
ENV BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat
# Thu, 25 Sep 2025 07:56:28 GMT
ENV BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.3.0/bundle-tomcat-10.3.0.zip
# Thu, 25 Sep 2025 07:56:28 GMT
# ARGS: BONITA_VERSION=10.3.0 BRANDING_VERSION=2025.1-u0 BONITA_SHA256=44c078fad0ffeec0afac2bf512040be16af4b722369039fe3daef1c091594637 BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.3.0/bundle-tomcat-10.3.0.zip
RUN mkdir /opt/files # buildkit
# Thu, 25 Sep 2025 07:56:28 GMT
COPY files /opt/files # buildkit
# Thu, 25 Sep 2025 07:56:28 GMT
# ARGS: BONITA_VERSION=10.3.0 BRANDING_VERSION=2025.1-u0 BONITA_SHA256=44c078fad0ffeec0afac2bf512040be16af4b722369039fe3daef1c091594637 BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.3.0/bundle-tomcat-10.3.0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then       echo "File already present in /opt/files";     else       curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip       && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c -;     fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Thu, 25 Sep 2025 07:56:28 GMT
ENV HTTP_API=false
# Thu, 25 Sep 2025 07:56:28 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 25 Sep 2025 07:56:28 GMT
ENV HTTP_API_PASSWORD=
# Thu, 25 Sep 2025 07:56:28 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 25 Sep 2025 07:56:28 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 25 Sep 2025 07:56:28 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 25 Sep 2025 07:56:28 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 25 Sep 2025 07:56:28 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 25 Sep 2025 07:56:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 25 Sep 2025 07:56:28 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 25 Sep 2025 07:56:28 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 25 Sep 2025 07:56:28 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 25 Sep 2025 07:56:28 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 25 Sep 2025 07:56:28 GMT
COPY templates /opt/templates # buildkit
# Thu, 25 Sep 2025 07:56:28 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Thu, 25 Sep 2025 07:56:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh" "/opt/files/startup.sh"]
# Thu, 25 Sep 2025 07:56:28 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4512b1690d5e061c5da51dd24b31a4d3bf934cb381adc713b1104ffb777758`  
		Last Modified: Wed, 08 Oct 2025 23:02:06 GMT  
		Size: 16.2 MB (16174547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb5deaaa3d9805d4696e9cbd0c4ddcb41f78b10b367371fda8228cb9e1b89d1`  
		Last Modified: Wed, 08 Oct 2025 23:38:09 GMT  
		Size: 53.1 MB (53137917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c4803c3f57ebff9a3f5381ce93d85442cb1d709ab202a9da2a9c3b7d7c27bc`  
		Last Modified: Wed, 08 Oct 2025 23:38:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b1498042c005285e382f16e912c007f6f4df87127e41364eed9103cfb4a1b1`  
		Last Modified: Wed, 08 Oct 2025 23:33:07 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec57e876f03cd650788951af7fd8f4bca52161505bef8fd3e11af275256fa73c`  
		Last Modified: Wed, 08 Oct 2025 23:47:29 GMT  
		Size: 1.9 MB (1889217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df59ce42b57567537517a6b240c56737b36af8c1e8172d6c02474aef73088d43`  
		Last Modified: Wed, 08 Oct 2025 23:47:29 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8a4a014dc940eb42f3114c84bfb91c5122c4bf3a7a058c851afff014f9b281`  
		Last Modified: Wed, 08 Oct 2025 23:47:28 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57280deae762d93f5cc1d4dab5b45e6ab5ead637433635ce06e8b4dd7c707ffe`  
		Last Modified: Wed, 08 Oct 2025 23:47:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b606e7b858ad49709223d364e15c39dd4622f70f2eeaf02acc6f331b57d667b2`  
		Last Modified: Wed, 08 Oct 2025 23:47:28 GMT  
		Size: 3.7 KB (3712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc9f220e80bc3dd2ef6e12eaa803e6c9fb710bc8a946edcc92a80976d38dd95`  
		Last Modified: Wed, 08 Oct 2025 23:47:41 GMT  
		Size: 120.1 MB (120140568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b9d840d266cc5e65dec8ba6f36a26290b905b72ae6768e363d774ab8c18211`  
		Last Modified: Wed, 08 Oct 2025 23:47:28 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:latest` - unknown; unknown

```console
$ docker pull bonita@sha256:ef3ead28827a0ad3139d3d1c24e216c7607437a7b5974407c7e219f34c98bb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1320665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179abfd880c3b5ed3626b265d29a14b68453a1aede9bae59885ed2834f1cefeb`

```dockerfile
```

-	Layers:
	-	`sha256:ce0a3e1c2cbbdb09d55cdf4e3570adb2cf349bfbcba6342302aa55378c0e680d`  
		Last Modified: Thu, 09 Oct 2025 02:55:16 GMT  
		Size: 1.3 MB (1291470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b12e27665ca83cbb406ea77c8e1dc3a969e8b002dac8ee056ff97fce32f7e0d`  
		Last Modified: Thu, 09 Oct 2025 02:55:17 GMT  
		Size: 29.2 KB (29195 bytes)  
		MIME: application/vnd.in-toto+json
