<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `bonita`

-	[`bonita:10.2`](#bonita102)
-	[`bonita:10.2.0`](#bonita1020)
-	[`bonita:2022.2`](#bonita20222)
-	[`bonita:2022.2-u0`](#bonita20222-u0)
-	[`bonita:2023.1`](#bonita20231)
-	[`bonita:2023.1-u0`](#bonita20231-u0)
-	[`bonita:2023.2`](#bonita20232)
-	[`bonita:2023.2-u0`](#bonita20232-u0)
-	[`bonita:2024.3`](#bonita20243)
-	[`bonita:2024.3-u0`](#bonita20243-u0)
-	[`bonita:7.15`](#bonita715)
-	[`bonita:7.15.0`](#bonita7150)
-	[`bonita:8.0`](#bonita80)
-	[`bonita:8.0.0`](#bonita800)
-	[`bonita:9.0`](#bonita90)
-	[`bonita:9.0.0`](#bonita900)
-	[`bonita:latest`](#bonitalatest)

## `bonita:10.2`

```console
$ docker pull bonita@sha256:3381055815a9fcf2826ddf2c094cbca56e32af792687425889866a865b9a716a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:10.2` - linux; amd64

```console
$ docker pull bonita@sha256:d31017b19b1e2abac3a7e877137f6aa0d29f19990dae4c5b948ea35ad9d4a436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187653756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bf9d639f2ac0407be063a1a5c0ce440f4521df9866772a3e6060176c13948e`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 15 Oct 2024 08:31:30 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
CMD ["/bin/sh"]
# Tue, 15 Oct 2024 08:31:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Oct 2024 08:31:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 08:31:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7a2df4e2f86eca649af1e17d990ab8e354cb6dee389606025b9d05f75623c388';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 15 Oct 2024 08:31:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 15 Oct 2024 08:31:30 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S -G bonita -h /opt/bonita/ -s /sbin/nologin bonita # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BONITA_VERSION
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BRANDING_VERSION
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BONITA_SHA256
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BASE_URL
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BONITA_URL
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BONITA_VERSION=10.2.0
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BRANDING_VERSION=2024.3-u0
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BONITA_SHA256=75ad51a50cba484d3f74637584bf5144bf0cf28c06ae7a5efe1a804cdc996d86
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ZIP_FILE=BonitaCommunity-2024.3-u0.zip
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.2.0/bundle-tomcat-10.2.0.zip
# Tue, 15 Oct 2024 08:31:30 GMT
# ARGS: BONITA_VERSION=10.2.0 BRANDING_VERSION=2024.3-u0 BONITA_SHA256=75ad51a50cba484d3f74637584bf5144bf0cf28c06ae7a5efe1a804cdc996d86 BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.2.0/bundle-tomcat-10.2.0.zip
RUN mkdir /opt/files # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
COPY files /opt/files # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
# ARGS: BONITA_VERSION=10.2.0 BRANDING_VERSION=2024.3-u0 BONITA_SHA256=75ad51a50cba484d3f74637584bf5144bf0cf28c06ae7a5efe1a804cdc996d86 BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.2.0/bundle-tomcat-10.2.0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_API=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_API_PASSWORD=
# Tue, 15 Oct 2024 08:31:30 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 15 Oct 2024 08:31:30 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 15 Oct 2024 08:31:30 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 15 Oct 2024 08:31:30 GMT
COPY templates /opt/templates # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Tue, 15 Oct 2024 08:31:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh" "/opt/files/startup.sh"]
# Tue, 15 Oct 2024 08:31:30 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503acc57a2d3003e19b5c5340cba736f16b29a0bc3e999c0d1416c991795736c`  
		Last Modified: Tue, 14 Jan 2025 20:34:37 GMT  
		Size: 16.0 MB (16022381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8817feb2b110cc1789fe20f09dcc5c51f115ba14d2835e68c75d641a587590`  
		Last Modified: Tue, 14 Jan 2025 20:33:26 GMT  
		Size: 46.6 MB (46615830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5df38f82b8b06ef5d393e7b14812384815dcaf3ff17dfb71ca2c5b2ee6e6dee`  
		Last Modified: Wed, 08 Jan 2025 19:16:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e977457afcf675805fa147640a44466ed600bc1164300a1c25fc66452ba4e49`  
		Last Modified: Wed, 08 Jan 2025 19:16:59 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf913f8832f656d70ec770a5fd5aa0facd3d9956498b994110dd3f1b2887b8b`  
		Last Modified: Wed, 08 Jan 2025 20:33:12 GMT  
		Size: 1.9 MB (1860780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9c5994d5129eaf63e216754bf2dbbf2182b5a4897ea8b4138d4d7d1c64fc2d`  
		Last Modified: Wed, 15 Jan 2025 02:12:51 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875274e038f9cc07698bba33d02eb6cd80c4a30516e485a38ceea8a9979d0692`  
		Last Modified: Wed, 08 Jan 2025 20:33:11 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9105fd74f07a097e7a3444a88a182a82204912df8dd572c0dc1d81989fe2f55`  
		Last Modified: Tue, 14 Jan 2025 21:43:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80600160768888c5ab508d46c15d2a8aaf5f52d4648e1234c6b0dd43129abd1`  
		Last Modified: Tue, 14 Jan 2025 21:43:21 GMT  
		Size: 3.7 KB (3709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f480dc8b10a9c6b713edb69d58292ad9becf5e50e2a95f83d2841e088d060320`  
		Last Modified: Wed, 15 Jan 2025 00:59:17 GMT  
		Size: 119.5 MB (119515308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0a9b544bb55acb774b760e93a67a8918c1d5f3123d79f7c6bc5b21d37eaba4`  
		Last Modified: Wed, 08 Jan 2025 20:33:12 GMT  
		Size: 5.9 KB (5885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:10.2` - unknown; unknown

```console
$ docker pull bonita@sha256:c017b1a60834ff3beb5110ecdadd13e0e42cea9282e1eed33d20e72d4042d982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1287875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bc5e8c6d2907265b7c82c290dcd772d56f5d44ebec370e9b60612103071db3`

```dockerfile
```

-	Layers:
	-	`sha256:37a851d11e941644bb5118316c7cc248134e88055dea7611e07660ae63b8ecb2`  
		Last Modified: Wed, 08 Jan 2025 20:33:11 GMT  
		Size: 1.3 MB (1258906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2443d3987f9befb2a74f68534a424ca5c0b11eea6737e117a206226aa5b4dff1`  
		Last Modified: Wed, 08 Jan 2025 20:33:11 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:10.2.0`

```console
$ docker pull bonita@sha256:3381055815a9fcf2826ddf2c094cbca56e32af792687425889866a865b9a716a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:10.2.0` - linux; amd64

```console
$ docker pull bonita@sha256:d31017b19b1e2abac3a7e877137f6aa0d29f19990dae4c5b948ea35ad9d4a436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187653756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bf9d639f2ac0407be063a1a5c0ce440f4521df9866772a3e6060176c13948e`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 15 Oct 2024 08:31:30 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
CMD ["/bin/sh"]
# Tue, 15 Oct 2024 08:31:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Oct 2024 08:31:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 08:31:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7a2df4e2f86eca649af1e17d990ab8e354cb6dee389606025b9d05f75623c388';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 15 Oct 2024 08:31:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 15 Oct 2024 08:31:30 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S -G bonita -h /opt/bonita/ -s /sbin/nologin bonita # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BONITA_VERSION
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BRANDING_VERSION
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BONITA_SHA256
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BASE_URL
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BONITA_URL
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BONITA_VERSION=10.2.0
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BRANDING_VERSION=2024.3-u0
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BONITA_SHA256=75ad51a50cba484d3f74637584bf5144bf0cf28c06ae7a5efe1a804cdc996d86
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ZIP_FILE=BonitaCommunity-2024.3-u0.zip
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.2.0/bundle-tomcat-10.2.0.zip
# Tue, 15 Oct 2024 08:31:30 GMT
# ARGS: BONITA_VERSION=10.2.0 BRANDING_VERSION=2024.3-u0 BONITA_SHA256=75ad51a50cba484d3f74637584bf5144bf0cf28c06ae7a5efe1a804cdc996d86 BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.2.0/bundle-tomcat-10.2.0.zip
RUN mkdir /opt/files # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
COPY files /opt/files # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
# ARGS: BONITA_VERSION=10.2.0 BRANDING_VERSION=2024.3-u0 BONITA_SHA256=75ad51a50cba484d3f74637584bf5144bf0cf28c06ae7a5efe1a804cdc996d86 BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.2.0/bundle-tomcat-10.2.0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_API=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_API_PASSWORD=
# Tue, 15 Oct 2024 08:31:30 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 15 Oct 2024 08:31:30 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 15 Oct 2024 08:31:30 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 15 Oct 2024 08:31:30 GMT
COPY templates /opt/templates # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Tue, 15 Oct 2024 08:31:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh" "/opt/files/startup.sh"]
# Tue, 15 Oct 2024 08:31:30 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503acc57a2d3003e19b5c5340cba736f16b29a0bc3e999c0d1416c991795736c`  
		Last Modified: Tue, 14 Jan 2025 20:34:37 GMT  
		Size: 16.0 MB (16022381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8817feb2b110cc1789fe20f09dcc5c51f115ba14d2835e68c75d641a587590`  
		Last Modified: Tue, 14 Jan 2025 20:33:26 GMT  
		Size: 46.6 MB (46615830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5df38f82b8b06ef5d393e7b14812384815dcaf3ff17dfb71ca2c5b2ee6e6dee`  
		Last Modified: Wed, 08 Jan 2025 19:16:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e977457afcf675805fa147640a44466ed600bc1164300a1c25fc66452ba4e49`  
		Last Modified: Wed, 08 Jan 2025 19:16:59 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf913f8832f656d70ec770a5fd5aa0facd3d9956498b994110dd3f1b2887b8b`  
		Last Modified: Wed, 08 Jan 2025 20:33:12 GMT  
		Size: 1.9 MB (1860780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9c5994d5129eaf63e216754bf2dbbf2182b5a4897ea8b4138d4d7d1c64fc2d`  
		Last Modified: Wed, 15 Jan 2025 02:12:51 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875274e038f9cc07698bba33d02eb6cd80c4a30516e485a38ceea8a9979d0692`  
		Last Modified: Wed, 08 Jan 2025 20:33:11 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9105fd74f07a097e7a3444a88a182a82204912df8dd572c0dc1d81989fe2f55`  
		Last Modified: Tue, 14 Jan 2025 21:43:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80600160768888c5ab508d46c15d2a8aaf5f52d4648e1234c6b0dd43129abd1`  
		Last Modified: Tue, 14 Jan 2025 21:43:21 GMT  
		Size: 3.7 KB (3709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f480dc8b10a9c6b713edb69d58292ad9becf5e50e2a95f83d2841e088d060320`  
		Last Modified: Wed, 15 Jan 2025 00:59:17 GMT  
		Size: 119.5 MB (119515308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0a9b544bb55acb774b760e93a67a8918c1d5f3123d79f7c6bc5b21d37eaba4`  
		Last Modified: Wed, 08 Jan 2025 20:33:12 GMT  
		Size: 5.9 KB (5885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:10.2.0` - unknown; unknown

```console
$ docker pull bonita@sha256:c017b1a60834ff3beb5110ecdadd13e0e42cea9282e1eed33d20e72d4042d982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1287875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bc5e8c6d2907265b7c82c290dcd772d56f5d44ebec370e9b60612103071db3`

```dockerfile
```

-	Layers:
	-	`sha256:37a851d11e941644bb5118316c7cc248134e88055dea7611e07660ae63b8ecb2`  
		Last Modified: Wed, 08 Jan 2025 20:33:11 GMT  
		Size: 1.3 MB (1258906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2443d3987f9befb2a74f68534a424ca5c0b11eea6737e117a206226aa5b4dff1`  
		Last Modified: Wed, 08 Jan 2025 20:33:11 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2022.2`

```console
$ docker pull bonita@sha256:a613bf574688e911834d54b11f22e9ea42e86574bb16825088a422a2f3345939
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bonita:2022.2` - linux; amd64

```console
$ docker pull bonita@sha256:5188e32eeb271cead0ecec62485650f5ca149702d3452f6aa612fae5e33358d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185598300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3471e8eaf5d7ecd3f0b3aa3824977c6193002a9e6fba2de6cb03a99e83d1571`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcce85a2d1c46d81f0ac2e80db005d94000aabed38b8ea64b20c1d2a6d38ca7`  
		Last Modified: Tue, 14 Jan 2025 21:28:14 GMT  
		Size: 62.8 MB (62771721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6c44d72b624209f41bb11468131325ebb11e7620aea3c56fec8d454370fe89`  
		Last Modified: Tue, 14 Jan 2025 21:28:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c067e3d716b220e2a521799ccc31cc2f81aa8483376a0eb816725296ba0e12f`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd401cc65ee90d0558b9b5eef05e5a8e34c8f743d54c493313019d77dd12663`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f86759833c16d14dbf6a1c2285f9a35eef3d64dd1c2e94c3f0ce61a1009c505`  
		Last Modified: Wed, 08 Jan 2025 18:16:52 GMT  
		Size: 3.0 KB (2992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4488c046b2b3dcfb9e4f454e0d27a3a5327bef30aaf70c5dbc3d6857e26fa6d`  
		Last Modified: Tue, 14 Jan 2025 23:32:08 GMT  
		Size: 119.2 MB (119190746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078953c12b2583edab0584a367d6b2796d74604bd12d6b390f76f2f9012b7e40`  
		Last Modified: Wed, 08 Jan 2025 18:16:52 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2` - unknown; unknown

```console
$ docker pull bonita@sha256:401ff348594a0b9ec35547e456d392e8123fa01b465e6cce6f5d6df6e5f979a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.0 KB (919966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3235cacdeb59c6372172164372ba20c0ca84da872eb0c468afca23bd2c69f1a`

```dockerfile
```

-	Layers:
	-	`sha256:1262c903057882def4c6095f99d576167e990ec9757b7dd9c57ef0fdde1e826c`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 896.7 KB (896694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98e116b1eda94c3ef8c44c8667f38f779a2bc174162e20575d839da409604244`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 23.3 KB (23272 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:149f7f95f9cb43421652de30aba851a95b1676a49dca69d699b0e550768d7b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (186002724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c06d6d28a1ec622cb6d9a5561f8c039458c0ba0f83b9b4eaf514412f38f9dd`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c71ee63c722e93ab0a09e7f66235af257cac264a53da18a8ad7c84930a1fefc`  
		Last Modified: Thu, 09 Jan 2025 05:59:20 GMT  
		Size: 62.7 MB (62711604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9d28a79bdd6833db0090f53bc09d9cb1733688098b60fe749dfcedb78c03e0`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb01ce373a0ab369bb1831f0375ddfdab2c678f1ffbbbab82c2507994ab87dc`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667e2cd51bbe61f599b9fd230c4680e52b52bc5795b540a9059f4fbba49abd1`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e92e38af8ad7b71573a168106e5cfe82d7d79c94b0f20d87253bc1844733ec7`  
		Last Modified: Thu, 09 Jan 2025 05:59:19 GMT  
		Size: 3.0 KB (2996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ac96db730bddd1c9fd403fbb5c9e917de6eac9df4ad3f32a58627d47b9faf3`  
		Last Modified: Thu, 09 Jan 2025 05:59:22 GMT  
		Size: 119.2 MB (119190774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd481cfcad1d53df462c245dc3eac22973aadf68ffbb8bca0aa9c4bcd7ab2ac`  
		Last Modified: Thu, 09 Jan 2025 05:59:19 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2` - unknown; unknown

```console
$ docker pull bonita@sha256:b97f28da6a6b3152959d0a80c86b8670d567354c21b8f5e51c1264f52da4a087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **919.2 KB (919227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8acadc16c974bac9f96f0674ea0fa0ca9a34aae0bc92079ed434c5f4b68d449d`

```dockerfile
```

-	Layers:
	-	`sha256:2736e60eb5967860fc66d6203b7d5620cb81bdff629e8592d0fdf67074a11eb6`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 895.8 KB (895791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9314740782b672dc878868ee66677bd97b2c5de76d4a716d299de94a1a1e20a0`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 23.4 KB (23436 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:11c7a754e0c78837202c123edf418ac2b4951009c332eb7476366f6cf7d50e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182019586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ba534660d88e296326a52414fa81f88a0ae64e6a8fe5c3ce2b141d274da393`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc39fc6cc5bb6cff536f0a7f21976f885040a6a78549abb0ec94136a5e890b1`  
		Last Modified: Thu, 09 Jan 2025 00:54:19 GMT  
		Size: 59.2 MB (59244850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed01549de2f2f8ab82b5507dc72db94fd49ce7348446c48d545ac4c49884fc`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b6902feeafff27b9132f63e252595ed37cd3432ea4084e342610e7039bad45`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691dfb31babe98ecd811daf886e5bb2904f6651be231ba9b3e201c3dc87095ea`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e970ed5ae42bf870c81edb5016cece7d875e50fa0e058ed793886f5d0448c`  
		Last Modified: Thu, 09 Jan 2025 00:54:18 GMT  
		Size: 3.0 KB (2997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4066da33f2e3e51b0a837856dd42a595127f761948ef5e7743bc91ce93261a81`  
		Last Modified: Thu, 09 Jan 2025 00:54:22 GMT  
		Size: 119.2 MB (119190748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbace5f00e6ce8c05517232df85abfd9597ffad5e40273325a02b9f1b493e148`  
		Last Modified: Thu, 09 Jan 2025 00:54:18 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2` - unknown; unknown

```console
$ docker pull bonita@sha256:649cde818b1527e97ee598651e3cdf38a8adf0171bc553569eda705be0c849fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **917.1 KB (917142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9d2aadfc4c368a23f16b9d9188f01f6a421224d109e952119f980a227c0c07`

```dockerfile
```

-	Layers:
	-	`sha256:9ea11d0c422c85457f4a64f428bb8d8215df92e2460a0d102ac5809d7cd2e57d`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 893.8 KB (893818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30419c438167b976783cf8c1c7eb715c097ed23119fc0892d887d10c1e0e086`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 23.3 KB (23324 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2022.2-u0`

```console
$ docker pull bonita@sha256:a613bf574688e911834d54b11f22e9ea42e86574bb16825088a422a2f3345939
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bonita:2022.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:5188e32eeb271cead0ecec62485650f5ca149702d3452f6aa612fae5e33358d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185598300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3471e8eaf5d7ecd3f0b3aa3824977c6193002a9e6fba2de6cb03a99e83d1571`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcce85a2d1c46d81f0ac2e80db005d94000aabed38b8ea64b20c1d2a6d38ca7`  
		Last Modified: Tue, 14 Jan 2025 21:28:14 GMT  
		Size: 62.8 MB (62771721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6c44d72b624209f41bb11468131325ebb11e7620aea3c56fec8d454370fe89`  
		Last Modified: Tue, 14 Jan 2025 21:28:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c067e3d716b220e2a521799ccc31cc2f81aa8483376a0eb816725296ba0e12f`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd401cc65ee90d0558b9b5eef05e5a8e34c8f743d54c493313019d77dd12663`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f86759833c16d14dbf6a1c2285f9a35eef3d64dd1c2e94c3f0ce61a1009c505`  
		Last Modified: Wed, 08 Jan 2025 18:16:52 GMT  
		Size: 3.0 KB (2992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4488c046b2b3dcfb9e4f454e0d27a3a5327bef30aaf70c5dbc3d6857e26fa6d`  
		Last Modified: Tue, 14 Jan 2025 23:32:08 GMT  
		Size: 119.2 MB (119190746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078953c12b2583edab0584a367d6b2796d74604bd12d6b390f76f2f9012b7e40`  
		Last Modified: Wed, 08 Jan 2025 18:16:52 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:401ff348594a0b9ec35547e456d392e8123fa01b465e6cce6f5d6df6e5f979a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.0 KB (919966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3235cacdeb59c6372172164372ba20c0ca84da872eb0c468afca23bd2c69f1a`

```dockerfile
```

-	Layers:
	-	`sha256:1262c903057882def4c6095f99d576167e990ec9757b7dd9c57ef0fdde1e826c`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 896.7 KB (896694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98e116b1eda94c3ef8c44c8667f38f779a2bc174162e20575d839da409604244`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 23.3 KB (23272 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:149f7f95f9cb43421652de30aba851a95b1676a49dca69d699b0e550768d7b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (186002724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c06d6d28a1ec622cb6d9a5561f8c039458c0ba0f83b9b4eaf514412f38f9dd`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c71ee63c722e93ab0a09e7f66235af257cac264a53da18a8ad7c84930a1fefc`  
		Last Modified: Thu, 09 Jan 2025 05:59:20 GMT  
		Size: 62.7 MB (62711604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9d28a79bdd6833db0090f53bc09d9cb1733688098b60fe749dfcedb78c03e0`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb01ce373a0ab369bb1831f0375ddfdab2c678f1ffbbbab82c2507994ab87dc`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667e2cd51bbe61f599b9fd230c4680e52b52bc5795b540a9059f4fbba49abd1`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e92e38af8ad7b71573a168106e5cfe82d7d79c94b0f20d87253bc1844733ec7`  
		Last Modified: Thu, 09 Jan 2025 05:59:19 GMT  
		Size: 3.0 KB (2996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ac96db730bddd1c9fd403fbb5c9e917de6eac9df4ad3f32a58627d47b9faf3`  
		Last Modified: Thu, 09 Jan 2025 05:59:22 GMT  
		Size: 119.2 MB (119190774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd481cfcad1d53df462c245dc3eac22973aadf68ffbb8bca0aa9c4bcd7ab2ac`  
		Last Modified: Thu, 09 Jan 2025 05:59:19 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:b97f28da6a6b3152959d0a80c86b8670d567354c21b8f5e51c1264f52da4a087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **919.2 KB (919227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8acadc16c974bac9f96f0674ea0fa0ca9a34aae0bc92079ed434c5f4b68d449d`

```dockerfile
```

-	Layers:
	-	`sha256:2736e60eb5967860fc66d6203b7d5620cb81bdff629e8592d0fdf67074a11eb6`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 895.8 KB (895791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9314740782b672dc878868ee66677bd97b2c5de76d4a716d299de94a1a1e20a0`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 23.4 KB (23436 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:11c7a754e0c78837202c123edf418ac2b4951009c332eb7476366f6cf7d50e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182019586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ba534660d88e296326a52414fa81f88a0ae64e6a8fe5c3ce2b141d274da393`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc39fc6cc5bb6cff536f0a7f21976f885040a6a78549abb0ec94136a5e890b1`  
		Last Modified: Thu, 09 Jan 2025 00:54:19 GMT  
		Size: 59.2 MB (59244850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed01549de2f2f8ab82b5507dc72db94fd49ce7348446c48d545ac4c49884fc`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b6902feeafff27b9132f63e252595ed37cd3432ea4084e342610e7039bad45`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691dfb31babe98ecd811daf886e5bb2904f6651be231ba9b3e201c3dc87095ea`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e970ed5ae42bf870c81edb5016cece7d875e50fa0e058ed793886f5d0448c`  
		Last Modified: Thu, 09 Jan 2025 00:54:18 GMT  
		Size: 3.0 KB (2997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4066da33f2e3e51b0a837856dd42a595127f761948ef5e7743bc91ce93261a81`  
		Last Modified: Thu, 09 Jan 2025 00:54:22 GMT  
		Size: 119.2 MB (119190748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbace5f00e6ce8c05517232df85abfd9597ffad5e40273325a02b9f1b493e148`  
		Last Modified: Thu, 09 Jan 2025 00:54:18 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:649cde818b1527e97ee598651e3cdf38a8adf0171bc553569eda705be0c849fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **917.1 KB (917142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9d2aadfc4c368a23f16b9d9188f01f6a421224d109e952119f980a227c0c07`

```dockerfile
```

-	Layers:
	-	`sha256:9ea11d0c422c85457f4a64f428bb8d8215df92e2460a0d102ac5809d7cd2e57d`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 893.8 KB (893818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30419c438167b976783cf8c1c7eb715c097ed23119fc0892d887d10c1e0e086`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 23.3 KB (23324 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.1`

```console
$ docker pull bonita@sha256:83107fe06f2af584024a2557c45fb7a6cc70567767dc9ae297a5889a0893c842
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bonita:2023.1` - linux; amd64

```console
$ docker pull bonita@sha256:839309576f921c062eb32d00c7306f8548c63eb2d641d8ea9e64427cd9123457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184586621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7c6d117c8bfb97c3e0b76314f01f64289353cd58923b97f3f86965d9f839e3`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87131e99d38b287035dfa2ac9ba12e0c61cdd62f01e64d80b9691672ebed5c6`  
		Last Modified: Wed, 08 Jan 2025 18:17:04 GMT  
		Size: 62.8 MB (62771776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebce3f7a9f918d324689aa8d9a204324d3abd229dd393c335c31947eceb29ed1`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625a766af4de10c10600747bd7996532f5ba388e68d36670ebf6b1f9a8298fe7`  
		Last Modified: Wed, 08 Jan 2025 18:17:02 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cac6e828598e8210b7fcd84264ee99829eb8a06f8b3fba37071d837309f2b1`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39d6b0d3105a1df4ff48246622351cd7236dd2a81e0fede1723e5a8c850c722`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 3.4 KB (3428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fc52347d1507c9706d8761cc789ddb1f73ed80b9840ad971b12befa51e3f0b`  
		Last Modified: Wed, 08 Jan 2025 18:17:05 GMT  
		Size: 118.2 MB (118178571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85222b2078f6c0397db8db28ba785a42db30c2b6219c34e9e7215735c54006b3`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1` - unknown; unknown

```console
$ docker pull bonita@sha256:3b40932a2cb7e60369bd084fecd38501a2a07e2d55b5286298f2f40a1cabfe12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.2 KB (911229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95c5e7ed59899afb163cb554d405050d9252d0b93d791a3f4a3006173d62906`

```dockerfile
```

-	Layers:
	-	`sha256:f03d081fb4baf16cd1a9b4ded32a8f6477033290a9bc3bf851ae1e40176a90b2`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 887.8 KB (887788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98e50441ea5d86128b4f4960b415a4218f82c16f1c16415781c8b02e7307cff`  
		Last Modified: Wed, 08 Jan 2025 18:17:02 GMT  
		Size: 23.4 KB (23441 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:4d23ced20e270cb79ab21845f99d318b86e1cda969daee67458a83ca3156f0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (184990940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e755ccbf8200e03ed2a498641c5d6d9d9de5396fee111d6a318b820f048907b8`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c71ee63c722e93ab0a09e7f66235af257cac264a53da18a8ad7c84930a1fefc`  
		Last Modified: Thu, 09 Jan 2025 05:59:20 GMT  
		Size: 62.7 MB (62711604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9d28a79bdd6833db0090f53bc09d9cb1733688098b60fe749dfcedb78c03e0`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb01ce373a0ab369bb1831f0375ddfdab2c678f1ffbbbab82c2507994ab87dc`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12612b3bd7cbc452059b073f49e94db0655d7822be8c364c6238fa7c60cd7e84`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea6af1bdb35bf00ee3573be784751630bc6fef21a415c8d02b081060e50f937`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c662642e29ee619a453047d983e5eb42790398c67e2d5e113d1078dda5fb49e`  
		Last Modified: Thu, 09 Jan 2025 05:59:52 GMT  
		Size: 118.2 MB (118178554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5326b2ad238fe1afe051e24ea07dbb166c1253b7a069fc2af7e3c5914469dd`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1` - unknown; unknown

```console
$ docker pull bonita@sha256:dec1921e6356f42a756693dbec2c7f13f9f802f73e64bcfa613a749db0498ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **910.5 KB (910491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f5e35ca2dd5e505725c68db2c4201772adee39a1a1021ff8756dfd1b022c28`

```dockerfile
```

-	Layers:
	-	`sha256:32ac41b0f82ca6c0cfac4b018f36c489494f74c5baeed6367248751082ca1fa4`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 886.9 KB (886885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01a9bbd5c91669aca4b3faf9d4c15ab0959ea48bd9649e9dff733eefb42ab4a`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 23.6 KB (23606 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:36c45dc9a35b65511e36092bbd57d3ec698816307359edb7d5c39254a553393e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181007832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7de5521b20151090ebca53c86b087ea237d1fdcd5c9e18873e4abd97be55362`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc39fc6cc5bb6cff536f0a7f21976f885040a6a78549abb0ec94136a5e890b1`  
		Last Modified: Thu, 09 Jan 2025 00:54:19 GMT  
		Size: 59.2 MB (59244850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed01549de2f2f8ab82b5507dc72db94fd49ce7348446c48d545ac4c49884fc`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b6902feeafff27b9132f63e252595ed37cd3432ea4084e342610e7039bad45`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17919c04b675f92c0aa1b927df53b5ea084a3f32f22c4b459432c370c62da2f9`  
		Last Modified: Thu, 09 Jan 2025 00:55:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52bf702c4dbcdf5cf776f521f260db5038ffc8a4a15014ad26acd4d36aa4076`  
		Last Modified: Thu, 09 Jan 2025 00:55:09 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7204c2340eed8f2487060d100468121249746be2def2bb602698eb3cc43842ef`  
		Last Modified: Thu, 09 Jan 2025 00:55:13 GMT  
		Size: 118.2 MB (118178561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6950c60595d40a223673a395499e29ccdb7e55b5ffe8cfcb16e28f528c68621f`  
		Last Modified: Thu, 09 Jan 2025 00:55:09 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1` - unknown; unknown

```console
$ docker pull bonita@sha256:c401cf069abaa9f2299f98de971d21c36cffc6903df57960bf9b2e056851fedc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **908.4 KB (908406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8deedf98ace90dc24939153fda3844199e8ba2955c46849be30a347259f922bf`

```dockerfile
```

-	Layers:
	-	`sha256:6439dd62b0f68192ca49b61056f70906e097c130e6de94ba0ec473111a55b827`  
		Last Modified: Thu, 09 Jan 2025 00:55:10 GMT  
		Size: 884.9 KB (884912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b34b1489729f0cbe6fa2fec694daeda2e7a7661ce59da9c836c02102e06fc56`  
		Last Modified: Thu, 09 Jan 2025 00:55:09 GMT  
		Size: 23.5 KB (23494 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.1-u0`

```console
$ docker pull bonita@sha256:83107fe06f2af584024a2557c45fb7a6cc70567767dc9ae297a5889a0893c842
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bonita:2023.1-u0` - linux; amd64

```console
$ docker pull bonita@sha256:839309576f921c062eb32d00c7306f8548c63eb2d641d8ea9e64427cd9123457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184586621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7c6d117c8bfb97c3e0b76314f01f64289353cd58923b97f3f86965d9f839e3`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87131e99d38b287035dfa2ac9ba12e0c61cdd62f01e64d80b9691672ebed5c6`  
		Last Modified: Wed, 08 Jan 2025 18:17:04 GMT  
		Size: 62.8 MB (62771776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebce3f7a9f918d324689aa8d9a204324d3abd229dd393c335c31947eceb29ed1`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625a766af4de10c10600747bd7996532f5ba388e68d36670ebf6b1f9a8298fe7`  
		Last Modified: Wed, 08 Jan 2025 18:17:02 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cac6e828598e8210b7fcd84264ee99829eb8a06f8b3fba37071d837309f2b1`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39d6b0d3105a1df4ff48246622351cd7236dd2a81e0fede1723e5a8c850c722`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 3.4 KB (3428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fc52347d1507c9706d8761cc789ddb1f73ed80b9840ad971b12befa51e3f0b`  
		Last Modified: Wed, 08 Jan 2025 18:17:05 GMT  
		Size: 118.2 MB (118178571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85222b2078f6c0397db8db28ba785a42db30c2b6219c34e9e7215735c54006b3`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:3b40932a2cb7e60369bd084fecd38501a2a07e2d55b5286298f2f40a1cabfe12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.2 KB (911229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95c5e7ed59899afb163cb554d405050d9252d0b93d791a3f4a3006173d62906`

```dockerfile
```

-	Layers:
	-	`sha256:f03d081fb4baf16cd1a9b4ded32a8f6477033290a9bc3bf851ae1e40176a90b2`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 887.8 KB (887788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98e50441ea5d86128b4f4960b415a4218f82c16f1c16415781c8b02e7307cff`  
		Last Modified: Wed, 08 Jan 2025 18:17:02 GMT  
		Size: 23.4 KB (23441 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:4d23ced20e270cb79ab21845f99d318b86e1cda969daee67458a83ca3156f0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (184990940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e755ccbf8200e03ed2a498641c5d6d9d9de5396fee111d6a318b820f048907b8`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c71ee63c722e93ab0a09e7f66235af257cac264a53da18a8ad7c84930a1fefc`  
		Last Modified: Thu, 09 Jan 2025 05:59:20 GMT  
		Size: 62.7 MB (62711604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9d28a79bdd6833db0090f53bc09d9cb1733688098b60fe749dfcedb78c03e0`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb01ce373a0ab369bb1831f0375ddfdab2c678f1ffbbbab82c2507994ab87dc`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12612b3bd7cbc452059b073f49e94db0655d7822be8c364c6238fa7c60cd7e84`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea6af1bdb35bf00ee3573be784751630bc6fef21a415c8d02b081060e50f937`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c662642e29ee619a453047d983e5eb42790398c67e2d5e113d1078dda5fb49e`  
		Last Modified: Thu, 09 Jan 2025 05:59:52 GMT  
		Size: 118.2 MB (118178554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5326b2ad238fe1afe051e24ea07dbb166c1253b7a069fc2af7e3c5914469dd`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:dec1921e6356f42a756693dbec2c7f13f9f802f73e64bcfa613a749db0498ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **910.5 KB (910491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f5e35ca2dd5e505725c68db2c4201772adee39a1a1021ff8756dfd1b022c28`

```dockerfile
```

-	Layers:
	-	`sha256:32ac41b0f82ca6c0cfac4b018f36c489494f74c5baeed6367248751082ca1fa4`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 886.9 KB (886885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01a9bbd5c91669aca4b3faf9d4c15ab0959ea48bd9649e9dff733eefb42ab4a`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 23.6 KB (23606 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:36c45dc9a35b65511e36092bbd57d3ec698816307359edb7d5c39254a553393e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181007832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7de5521b20151090ebca53c86b087ea237d1fdcd5c9e18873e4abd97be55362`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc39fc6cc5bb6cff536f0a7f21976f885040a6a78549abb0ec94136a5e890b1`  
		Last Modified: Thu, 09 Jan 2025 00:54:19 GMT  
		Size: 59.2 MB (59244850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed01549de2f2f8ab82b5507dc72db94fd49ce7348446c48d545ac4c49884fc`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b6902feeafff27b9132f63e252595ed37cd3432ea4084e342610e7039bad45`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17919c04b675f92c0aa1b927df53b5ea084a3f32f22c4b459432c370c62da2f9`  
		Last Modified: Thu, 09 Jan 2025 00:55:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52bf702c4dbcdf5cf776f521f260db5038ffc8a4a15014ad26acd4d36aa4076`  
		Last Modified: Thu, 09 Jan 2025 00:55:09 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7204c2340eed8f2487060d100468121249746be2def2bb602698eb3cc43842ef`  
		Last Modified: Thu, 09 Jan 2025 00:55:13 GMT  
		Size: 118.2 MB (118178561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6950c60595d40a223673a395499e29ccdb7e55b5ffe8cfcb16e28f528c68621f`  
		Last Modified: Thu, 09 Jan 2025 00:55:09 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:c401cf069abaa9f2299f98de971d21c36cffc6903df57960bf9b2e056851fedc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **908.4 KB (908406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8deedf98ace90dc24939153fda3844199e8ba2955c46849be30a347259f922bf`

```dockerfile
```

-	Layers:
	-	`sha256:6439dd62b0f68192ca49b61056f70906e097c130e6de94ba0ec473111a55b827`  
		Last Modified: Thu, 09 Jan 2025 00:55:10 GMT  
		Size: 884.9 KB (884912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b34b1489729f0cbe6fa2fec694daeda2e7a7661ce59da9c836c02102e06fc56`  
		Last Modified: Thu, 09 Jan 2025 00:55:09 GMT  
		Size: 23.5 KB (23494 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.2`

```console
$ docker pull bonita@sha256:befe3da733a9f2ae6c7f1cd9ff873d3a5d4e5646f9ce7f85992d8dadee7abdc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bonita:2023.2` - linux; amd64

```console
$ docker pull bonita@sha256:9a7b8be0335eca51240e576921f54fcdfb8c82472b0f9e04d39a33fe80a02eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192425524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376459bb6aec365e99f615be8f30be5752d17e1c863c39046af72cf1b281b869`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24854979e55d26ea6ba886a62b11271fc3b3aa0b8e58511e1ac900515805461`  
		Last Modified: Wed, 08 Jan 2025 18:16:56 GMT  
		Size: 68.6 MB (68615271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0557c93d928fd0d99725cb493940d90aa4c44c7ed3076499cdef92086c0783`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbbfb5f3be677939423491830e17a3b727b392fa4f92b3cfd5cea6af35825ec`  
		Last Modified: Wed, 08 Jan 2025 18:16:54 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2125cf3931e4bf088b69efea36c25f1989f4fa4172d38e2d95235863f38b11`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48af2960cafbf506204ff417840f1932ae079c8778cac11a93f9990008c9e068`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f74450d11734073a93dc5bad03f3eb7dcfffb65137129c745c71cb5f9852a83`  
		Last Modified: Wed, 15 Jan 2025 00:39:59 GMT  
		Size: 120.2 MB (120173557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4446248ca40e45ab4201f417dbe98c122248cccc1b6377c3c2822041ecb102a`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2` - unknown; unknown

```console
$ docker pull bonita@sha256:76704d018b8dfe83d3e60fe02d283822b78f2829293b0a282b2909a8b7e6c569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1367891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e2ff34cac1e9b80c419920795585de6d8293bbbdc0a4bd8d2e9b890ae10b33`

```dockerfile
```

-	Layers:
	-	`sha256:dbdf90f57620dd34aa6e3e6650d4b430a2db8cafdb875f084e4b8a27135ac9a0`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 1.3 MB (1344969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8555e596e9e84a80f6572cbe66a8ac589269dba921f4a1fdeb8d8ec2761f2d99`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 22.9 KB (22922 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:36746d767c698fdbba5000ab9d97e932cfe1cd9a556c4b766f01d6debf44e3c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192842367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e0f12c71e8cc60c6120fd1acaa162270d14c07b1875f246f7610611af94009`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f93ed4428e400840b905876fa9b313d4a61639fd0dfd34cd6818d47c2c6817`  
		Last Modified: Thu, 09 Jan 2025 06:00:25 GMT  
		Size: 68.6 MB (68567676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeedbee4f06903ae88f843e4aa606a554f851f66d9de03ca19584f6dffd59cd9`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af3c891e0576c57cd330ae29b751a39c84ae7262fad104877e1e948df380b82`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f8ee729bf2650d5723b0d21a87db6d9b5464bf06f2d1319c479565b5290bf`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42026758d938f272fede594a189a65c78b04e9899eb6e3befdcd40908010b966`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0018bb4a9752ba828bd273f3cbef282168a0a91adddea9b7969852e92eeb6c97`  
		Last Modified: Thu, 09 Jan 2025 06:00:27 GMT  
		Size: 120.2 MB (120173487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effd6aa26b4f46552102f4ce1c685a91cac05c6551fceea4d49637215789f600`  
		Last Modified: Thu, 09 Jan 2025 06:00:24 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2` - unknown; unknown

```console
$ docker pull bonita@sha256:93645412491a62bde23a8a1ae7b6477a34953446753906aa5fc6943d02155330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1367152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b469137932f91d588a6534e8500e8f01bcf8a3ac62e0de2ac64d1e86ce908b`

```dockerfile
```

-	Layers:
	-	`sha256:fafe5179e6c558ff4dc2dfc3a195a9f7f91fd089c67c592a03be4f4ca00b0701`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 1.3 MB (1344066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ece7403855922fc99e942417d1c44ca5c3afe898923a5a63df9ca84dc09108a`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 23.1 KB (23086 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:911f63694ee950a485b7478e650aff02ba17e10c32629968f8ad7acf744309bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189147658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c8c54f624a3f20b1e50097de01559ea1910aa25421c20dcd1e770253ed29e2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba9231fd7dafddae6f57c10c1eeee2d4cc54b1fe9ce3bda7015ab8aa9713147`  
		Last Modified: Thu, 09 Jan 2025 00:56:15 GMT  
		Size: 65.4 MB (65389294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240dfdea6771e09e3d9f02f1538602c6f7101d09be850381ad95a32b404a692b`  
		Last Modified: Thu, 09 Jan 2025 00:56:12 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601dcf390b56dc2206b9587480b4fdd9f56cf772bbb8c3ca3aeeb4dcf7c73f68`  
		Last Modified: Thu, 09 Jan 2025 00:56:12 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a558227dd619c5832bfdf25879c1cb5ac351814af85a97774a81c672bec2f62c`  
		Last Modified: Thu, 09 Jan 2025 00:56:12 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e82ece27f9744204bcafa35e1788eab7ca14ce844098613050b7501dd7feb1`  
		Last Modified: Thu, 09 Jan 2025 00:56:13 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a65f81c27e208cf38082e55db3fe539ebd749f2091f235314d7fd53eec78775`  
		Last Modified: Thu, 09 Jan 2025 00:56:17 GMT  
		Size: 120.2 MB (120173521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02dbf3bde71131e36b466675e496d97d1519cd954840f54ff78137d80a7f6b`  
		Last Modified: Thu, 09 Jan 2025 00:56:13 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2` - unknown; unknown

```console
$ docker pull bonita@sha256:15d9d9b7b7d0dd8222ae605e53e995a7c29a18e7a5ba6875f316b97f882e4f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1365067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe469ecd8101d9219ba8f7ab4a5e7c17c13a6fb1ca417b1a78a461dc7902f09`

```dockerfile
```

-	Layers:
	-	`sha256:7d633c084e1881a90b4eda94ce2a13272ee3c03575b26e57375fe21c3f0a7e31`  
		Last Modified: Thu, 09 Jan 2025 00:56:13 GMT  
		Size: 1.3 MB (1342093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b772685440d21b377539497002095f37a3f3dbb759fdb8f94e77c8b1129423e0`  
		Last Modified: Thu, 09 Jan 2025 00:56:12 GMT  
		Size: 23.0 KB (22974 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.2-u0`

```console
$ docker pull bonita@sha256:befe3da733a9f2ae6c7f1cd9ff873d3a5d4e5646f9ce7f85992d8dadee7abdc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bonita:2023.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:9a7b8be0335eca51240e576921f54fcdfb8c82472b0f9e04d39a33fe80a02eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192425524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376459bb6aec365e99f615be8f30be5752d17e1c863c39046af72cf1b281b869`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24854979e55d26ea6ba886a62b11271fc3b3aa0b8e58511e1ac900515805461`  
		Last Modified: Wed, 08 Jan 2025 18:16:56 GMT  
		Size: 68.6 MB (68615271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0557c93d928fd0d99725cb493940d90aa4c44c7ed3076499cdef92086c0783`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbbfb5f3be677939423491830e17a3b727b392fa4f92b3cfd5cea6af35825ec`  
		Last Modified: Wed, 08 Jan 2025 18:16:54 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2125cf3931e4bf088b69efea36c25f1989f4fa4172d38e2d95235863f38b11`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48af2960cafbf506204ff417840f1932ae079c8778cac11a93f9990008c9e068`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f74450d11734073a93dc5bad03f3eb7dcfffb65137129c745c71cb5f9852a83`  
		Last Modified: Wed, 15 Jan 2025 00:39:59 GMT  
		Size: 120.2 MB (120173557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4446248ca40e45ab4201f417dbe98c122248cccc1b6377c3c2822041ecb102a`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:76704d018b8dfe83d3e60fe02d283822b78f2829293b0a282b2909a8b7e6c569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1367891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e2ff34cac1e9b80c419920795585de6d8293bbbdc0a4bd8d2e9b890ae10b33`

```dockerfile
```

-	Layers:
	-	`sha256:dbdf90f57620dd34aa6e3e6650d4b430a2db8cafdb875f084e4b8a27135ac9a0`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 1.3 MB (1344969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8555e596e9e84a80f6572cbe66a8ac589269dba921f4a1fdeb8d8ec2761f2d99`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 22.9 KB (22922 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:36746d767c698fdbba5000ab9d97e932cfe1cd9a556c4b766f01d6debf44e3c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192842367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e0f12c71e8cc60c6120fd1acaa162270d14c07b1875f246f7610611af94009`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f93ed4428e400840b905876fa9b313d4a61639fd0dfd34cd6818d47c2c6817`  
		Last Modified: Thu, 09 Jan 2025 06:00:25 GMT  
		Size: 68.6 MB (68567676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeedbee4f06903ae88f843e4aa606a554f851f66d9de03ca19584f6dffd59cd9`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af3c891e0576c57cd330ae29b751a39c84ae7262fad104877e1e948df380b82`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f8ee729bf2650d5723b0d21a87db6d9b5464bf06f2d1319c479565b5290bf`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42026758d938f272fede594a189a65c78b04e9899eb6e3befdcd40908010b966`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0018bb4a9752ba828bd273f3cbef282168a0a91adddea9b7969852e92eeb6c97`  
		Last Modified: Thu, 09 Jan 2025 06:00:27 GMT  
		Size: 120.2 MB (120173487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effd6aa26b4f46552102f4ce1c685a91cac05c6551fceea4d49637215789f600`  
		Last Modified: Thu, 09 Jan 2025 06:00:24 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:93645412491a62bde23a8a1ae7b6477a34953446753906aa5fc6943d02155330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1367152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b469137932f91d588a6534e8500e8f01bcf8a3ac62e0de2ac64d1e86ce908b`

```dockerfile
```

-	Layers:
	-	`sha256:fafe5179e6c558ff4dc2dfc3a195a9f7f91fd089c67c592a03be4f4ca00b0701`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 1.3 MB (1344066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ece7403855922fc99e942417d1c44ca5c3afe898923a5a63df9ca84dc09108a`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 23.1 KB (23086 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:911f63694ee950a485b7478e650aff02ba17e10c32629968f8ad7acf744309bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189147658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c8c54f624a3f20b1e50097de01559ea1910aa25421c20dcd1e770253ed29e2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba9231fd7dafddae6f57c10c1eeee2d4cc54b1fe9ce3bda7015ab8aa9713147`  
		Last Modified: Thu, 09 Jan 2025 00:56:15 GMT  
		Size: 65.4 MB (65389294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240dfdea6771e09e3d9f02f1538602c6f7101d09be850381ad95a32b404a692b`  
		Last Modified: Thu, 09 Jan 2025 00:56:12 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601dcf390b56dc2206b9587480b4fdd9f56cf772bbb8c3ca3aeeb4dcf7c73f68`  
		Last Modified: Thu, 09 Jan 2025 00:56:12 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a558227dd619c5832bfdf25879c1cb5ac351814af85a97774a81c672bec2f62c`  
		Last Modified: Thu, 09 Jan 2025 00:56:12 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e82ece27f9744204bcafa35e1788eab7ca14ce844098613050b7501dd7feb1`  
		Last Modified: Thu, 09 Jan 2025 00:56:13 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a65f81c27e208cf38082e55db3fe539ebd749f2091f235314d7fd53eec78775`  
		Last Modified: Thu, 09 Jan 2025 00:56:17 GMT  
		Size: 120.2 MB (120173521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02dbf3bde71131e36b466675e496d97d1519cd954840f54ff78137d80a7f6b`  
		Last Modified: Thu, 09 Jan 2025 00:56:13 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:15d9d9b7b7d0dd8222ae605e53e995a7c29a18e7a5ba6875f316b97f882e4f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1365067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe469ecd8101d9219ba8f7ab4a5e7c17c13a6fb1ca417b1a78a461dc7902f09`

```dockerfile
```

-	Layers:
	-	`sha256:7d633c084e1881a90b4eda94ce2a13272ee3c03575b26e57375fe21c3f0a7e31`  
		Last Modified: Thu, 09 Jan 2025 00:56:13 GMT  
		Size: 1.3 MB (1342093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b772685440d21b377539497002095f37a3f3dbb759fdb8f94e77c8b1129423e0`  
		Last Modified: Thu, 09 Jan 2025 00:56:12 GMT  
		Size: 23.0 KB (22974 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2024.3`

```console
$ docker pull bonita@sha256:3381055815a9fcf2826ddf2c094cbca56e32af792687425889866a865b9a716a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:2024.3` - linux; amd64

```console
$ docker pull bonita@sha256:d31017b19b1e2abac3a7e877137f6aa0d29f19990dae4c5b948ea35ad9d4a436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187653756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bf9d639f2ac0407be063a1a5c0ce440f4521df9866772a3e6060176c13948e`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 15 Oct 2024 08:31:30 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
CMD ["/bin/sh"]
# Tue, 15 Oct 2024 08:31:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Oct 2024 08:31:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 08:31:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7a2df4e2f86eca649af1e17d990ab8e354cb6dee389606025b9d05f75623c388';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 15 Oct 2024 08:31:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 15 Oct 2024 08:31:30 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S -G bonita -h /opt/bonita/ -s /sbin/nologin bonita # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BONITA_VERSION
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BRANDING_VERSION
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BONITA_SHA256
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BASE_URL
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BONITA_URL
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BONITA_VERSION=10.2.0
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BRANDING_VERSION=2024.3-u0
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BONITA_SHA256=75ad51a50cba484d3f74637584bf5144bf0cf28c06ae7a5efe1a804cdc996d86
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ZIP_FILE=BonitaCommunity-2024.3-u0.zip
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.2.0/bundle-tomcat-10.2.0.zip
# Tue, 15 Oct 2024 08:31:30 GMT
# ARGS: BONITA_VERSION=10.2.0 BRANDING_VERSION=2024.3-u0 BONITA_SHA256=75ad51a50cba484d3f74637584bf5144bf0cf28c06ae7a5efe1a804cdc996d86 BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.2.0/bundle-tomcat-10.2.0.zip
RUN mkdir /opt/files # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
COPY files /opt/files # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
# ARGS: BONITA_VERSION=10.2.0 BRANDING_VERSION=2024.3-u0 BONITA_SHA256=75ad51a50cba484d3f74637584bf5144bf0cf28c06ae7a5efe1a804cdc996d86 BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.2.0/bundle-tomcat-10.2.0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_API=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_API_PASSWORD=
# Tue, 15 Oct 2024 08:31:30 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 15 Oct 2024 08:31:30 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 15 Oct 2024 08:31:30 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 15 Oct 2024 08:31:30 GMT
COPY templates /opt/templates # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Tue, 15 Oct 2024 08:31:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh" "/opt/files/startup.sh"]
# Tue, 15 Oct 2024 08:31:30 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503acc57a2d3003e19b5c5340cba736f16b29a0bc3e999c0d1416c991795736c`  
		Last Modified: Tue, 14 Jan 2025 20:34:37 GMT  
		Size: 16.0 MB (16022381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8817feb2b110cc1789fe20f09dcc5c51f115ba14d2835e68c75d641a587590`  
		Last Modified: Tue, 14 Jan 2025 20:33:26 GMT  
		Size: 46.6 MB (46615830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5df38f82b8b06ef5d393e7b14812384815dcaf3ff17dfb71ca2c5b2ee6e6dee`  
		Last Modified: Wed, 08 Jan 2025 19:16:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e977457afcf675805fa147640a44466ed600bc1164300a1c25fc66452ba4e49`  
		Last Modified: Wed, 08 Jan 2025 19:16:59 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf913f8832f656d70ec770a5fd5aa0facd3d9956498b994110dd3f1b2887b8b`  
		Last Modified: Wed, 08 Jan 2025 20:33:12 GMT  
		Size: 1.9 MB (1860780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9c5994d5129eaf63e216754bf2dbbf2182b5a4897ea8b4138d4d7d1c64fc2d`  
		Last Modified: Wed, 15 Jan 2025 02:12:51 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875274e038f9cc07698bba33d02eb6cd80c4a30516e485a38ceea8a9979d0692`  
		Last Modified: Wed, 08 Jan 2025 20:33:11 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9105fd74f07a097e7a3444a88a182a82204912df8dd572c0dc1d81989fe2f55`  
		Last Modified: Tue, 14 Jan 2025 21:43:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80600160768888c5ab508d46c15d2a8aaf5f52d4648e1234c6b0dd43129abd1`  
		Last Modified: Tue, 14 Jan 2025 21:43:21 GMT  
		Size: 3.7 KB (3709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f480dc8b10a9c6b713edb69d58292ad9becf5e50e2a95f83d2841e088d060320`  
		Last Modified: Wed, 15 Jan 2025 00:59:17 GMT  
		Size: 119.5 MB (119515308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0a9b544bb55acb774b760e93a67a8918c1d5f3123d79f7c6bc5b21d37eaba4`  
		Last Modified: Wed, 08 Jan 2025 20:33:12 GMT  
		Size: 5.9 KB (5885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2024.3` - unknown; unknown

```console
$ docker pull bonita@sha256:c017b1a60834ff3beb5110ecdadd13e0e42cea9282e1eed33d20e72d4042d982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1287875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bc5e8c6d2907265b7c82c290dcd772d56f5d44ebec370e9b60612103071db3`

```dockerfile
```

-	Layers:
	-	`sha256:37a851d11e941644bb5118316c7cc248134e88055dea7611e07660ae63b8ecb2`  
		Last Modified: Wed, 08 Jan 2025 20:33:11 GMT  
		Size: 1.3 MB (1258906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2443d3987f9befb2a74f68534a424ca5c0b11eea6737e117a206226aa5b4dff1`  
		Last Modified: Wed, 08 Jan 2025 20:33:11 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2024.3-u0`

```console
$ docker pull bonita@sha256:3381055815a9fcf2826ddf2c094cbca56e32af792687425889866a865b9a716a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:2024.3-u0` - linux; amd64

```console
$ docker pull bonita@sha256:d31017b19b1e2abac3a7e877137f6aa0d29f19990dae4c5b948ea35ad9d4a436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187653756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bf9d639f2ac0407be063a1a5c0ce440f4521df9866772a3e6060176c13948e`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 15 Oct 2024 08:31:30 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
CMD ["/bin/sh"]
# Tue, 15 Oct 2024 08:31:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Oct 2024 08:31:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 08:31:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7a2df4e2f86eca649af1e17d990ab8e354cb6dee389606025b9d05f75623c388';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 15 Oct 2024 08:31:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 15 Oct 2024 08:31:30 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S -G bonita -h /opt/bonita/ -s /sbin/nologin bonita # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BONITA_VERSION
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BRANDING_VERSION
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BONITA_SHA256
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BASE_URL
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BONITA_URL
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BONITA_VERSION=10.2.0
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BRANDING_VERSION=2024.3-u0
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BONITA_SHA256=75ad51a50cba484d3f74637584bf5144bf0cf28c06ae7a5efe1a804cdc996d86
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ZIP_FILE=BonitaCommunity-2024.3-u0.zip
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.2.0/bundle-tomcat-10.2.0.zip
# Tue, 15 Oct 2024 08:31:30 GMT
# ARGS: BONITA_VERSION=10.2.0 BRANDING_VERSION=2024.3-u0 BONITA_SHA256=75ad51a50cba484d3f74637584bf5144bf0cf28c06ae7a5efe1a804cdc996d86 BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.2.0/bundle-tomcat-10.2.0.zip
RUN mkdir /opt/files # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
COPY files /opt/files # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
# ARGS: BONITA_VERSION=10.2.0 BRANDING_VERSION=2024.3-u0 BONITA_SHA256=75ad51a50cba484d3f74637584bf5144bf0cf28c06ae7a5efe1a804cdc996d86 BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.2.0/bundle-tomcat-10.2.0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_API=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_API_PASSWORD=
# Tue, 15 Oct 2024 08:31:30 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 15 Oct 2024 08:31:30 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 15 Oct 2024 08:31:30 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 15 Oct 2024 08:31:30 GMT
COPY templates /opt/templates # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Tue, 15 Oct 2024 08:31:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh" "/opt/files/startup.sh"]
# Tue, 15 Oct 2024 08:31:30 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503acc57a2d3003e19b5c5340cba736f16b29a0bc3e999c0d1416c991795736c`  
		Last Modified: Tue, 14 Jan 2025 20:34:37 GMT  
		Size: 16.0 MB (16022381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8817feb2b110cc1789fe20f09dcc5c51f115ba14d2835e68c75d641a587590`  
		Last Modified: Tue, 14 Jan 2025 20:33:26 GMT  
		Size: 46.6 MB (46615830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5df38f82b8b06ef5d393e7b14812384815dcaf3ff17dfb71ca2c5b2ee6e6dee`  
		Last Modified: Wed, 08 Jan 2025 19:16:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e977457afcf675805fa147640a44466ed600bc1164300a1c25fc66452ba4e49`  
		Last Modified: Wed, 08 Jan 2025 19:16:59 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf913f8832f656d70ec770a5fd5aa0facd3d9956498b994110dd3f1b2887b8b`  
		Last Modified: Wed, 08 Jan 2025 20:33:12 GMT  
		Size: 1.9 MB (1860780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9c5994d5129eaf63e216754bf2dbbf2182b5a4897ea8b4138d4d7d1c64fc2d`  
		Last Modified: Wed, 15 Jan 2025 02:12:51 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875274e038f9cc07698bba33d02eb6cd80c4a30516e485a38ceea8a9979d0692`  
		Last Modified: Wed, 08 Jan 2025 20:33:11 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9105fd74f07a097e7a3444a88a182a82204912df8dd572c0dc1d81989fe2f55`  
		Last Modified: Tue, 14 Jan 2025 21:43:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80600160768888c5ab508d46c15d2a8aaf5f52d4648e1234c6b0dd43129abd1`  
		Last Modified: Tue, 14 Jan 2025 21:43:21 GMT  
		Size: 3.7 KB (3709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f480dc8b10a9c6b713edb69d58292ad9becf5e50e2a95f83d2841e088d060320`  
		Last Modified: Wed, 15 Jan 2025 00:59:17 GMT  
		Size: 119.5 MB (119515308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0a9b544bb55acb774b760e93a67a8918c1d5f3123d79f7c6bc5b21d37eaba4`  
		Last Modified: Wed, 08 Jan 2025 20:33:12 GMT  
		Size: 5.9 KB (5885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2024.3-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:c017b1a60834ff3beb5110ecdadd13e0e42cea9282e1eed33d20e72d4042d982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1287875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bc5e8c6d2907265b7c82c290dcd772d56f5d44ebec370e9b60612103071db3`

```dockerfile
```

-	Layers:
	-	`sha256:37a851d11e941644bb5118316c7cc248134e88055dea7611e07660ae63b8ecb2`  
		Last Modified: Wed, 08 Jan 2025 20:33:11 GMT  
		Size: 1.3 MB (1258906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2443d3987f9befb2a74f68534a424ca5c0b11eea6737e117a206226aa5b4dff1`  
		Last Modified: Wed, 08 Jan 2025 20:33:11 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:7.15`

```console
$ docker pull bonita@sha256:a613bf574688e911834d54b11f22e9ea42e86574bb16825088a422a2f3345939
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bonita:7.15` - linux; amd64

```console
$ docker pull bonita@sha256:5188e32eeb271cead0ecec62485650f5ca149702d3452f6aa612fae5e33358d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185598300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3471e8eaf5d7ecd3f0b3aa3824977c6193002a9e6fba2de6cb03a99e83d1571`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcce85a2d1c46d81f0ac2e80db005d94000aabed38b8ea64b20c1d2a6d38ca7`  
		Last Modified: Tue, 14 Jan 2025 21:28:14 GMT  
		Size: 62.8 MB (62771721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6c44d72b624209f41bb11468131325ebb11e7620aea3c56fec8d454370fe89`  
		Last Modified: Tue, 14 Jan 2025 21:28:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c067e3d716b220e2a521799ccc31cc2f81aa8483376a0eb816725296ba0e12f`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd401cc65ee90d0558b9b5eef05e5a8e34c8f743d54c493313019d77dd12663`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f86759833c16d14dbf6a1c2285f9a35eef3d64dd1c2e94c3f0ce61a1009c505`  
		Last Modified: Wed, 08 Jan 2025 18:16:52 GMT  
		Size: 3.0 KB (2992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4488c046b2b3dcfb9e4f454e0d27a3a5327bef30aaf70c5dbc3d6857e26fa6d`  
		Last Modified: Tue, 14 Jan 2025 23:32:08 GMT  
		Size: 119.2 MB (119190746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078953c12b2583edab0584a367d6b2796d74604bd12d6b390f76f2f9012b7e40`  
		Last Modified: Wed, 08 Jan 2025 18:16:52 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15` - unknown; unknown

```console
$ docker pull bonita@sha256:401ff348594a0b9ec35547e456d392e8123fa01b465e6cce6f5d6df6e5f979a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.0 KB (919966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3235cacdeb59c6372172164372ba20c0ca84da872eb0c468afca23bd2c69f1a`

```dockerfile
```

-	Layers:
	-	`sha256:1262c903057882def4c6095f99d576167e990ec9757b7dd9c57ef0fdde1e826c`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 896.7 KB (896694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98e116b1eda94c3ef8c44c8667f38f779a2bc174162e20575d839da409604244`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 23.3 KB (23272 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.15` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:149f7f95f9cb43421652de30aba851a95b1676a49dca69d699b0e550768d7b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (186002724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c06d6d28a1ec622cb6d9a5561f8c039458c0ba0f83b9b4eaf514412f38f9dd`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c71ee63c722e93ab0a09e7f66235af257cac264a53da18a8ad7c84930a1fefc`  
		Last Modified: Thu, 09 Jan 2025 05:59:20 GMT  
		Size: 62.7 MB (62711604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9d28a79bdd6833db0090f53bc09d9cb1733688098b60fe749dfcedb78c03e0`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb01ce373a0ab369bb1831f0375ddfdab2c678f1ffbbbab82c2507994ab87dc`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667e2cd51bbe61f599b9fd230c4680e52b52bc5795b540a9059f4fbba49abd1`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e92e38af8ad7b71573a168106e5cfe82d7d79c94b0f20d87253bc1844733ec7`  
		Last Modified: Thu, 09 Jan 2025 05:59:19 GMT  
		Size: 3.0 KB (2996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ac96db730bddd1c9fd403fbb5c9e917de6eac9df4ad3f32a58627d47b9faf3`  
		Last Modified: Thu, 09 Jan 2025 05:59:22 GMT  
		Size: 119.2 MB (119190774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd481cfcad1d53df462c245dc3eac22973aadf68ffbb8bca0aa9c4bcd7ab2ac`  
		Last Modified: Thu, 09 Jan 2025 05:59:19 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15` - unknown; unknown

```console
$ docker pull bonita@sha256:b97f28da6a6b3152959d0a80c86b8670d567354c21b8f5e51c1264f52da4a087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **919.2 KB (919227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8acadc16c974bac9f96f0674ea0fa0ca9a34aae0bc92079ed434c5f4b68d449d`

```dockerfile
```

-	Layers:
	-	`sha256:2736e60eb5967860fc66d6203b7d5620cb81bdff629e8592d0fdf67074a11eb6`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 895.8 KB (895791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9314740782b672dc878868ee66677bd97b2c5de76d4a716d299de94a1a1e20a0`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 23.4 KB (23436 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.15` - linux; ppc64le

```console
$ docker pull bonita@sha256:11c7a754e0c78837202c123edf418ac2b4951009c332eb7476366f6cf7d50e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182019586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ba534660d88e296326a52414fa81f88a0ae64e6a8fe5c3ce2b141d274da393`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc39fc6cc5bb6cff536f0a7f21976f885040a6a78549abb0ec94136a5e890b1`  
		Last Modified: Thu, 09 Jan 2025 00:54:19 GMT  
		Size: 59.2 MB (59244850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed01549de2f2f8ab82b5507dc72db94fd49ce7348446c48d545ac4c49884fc`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b6902feeafff27b9132f63e252595ed37cd3432ea4084e342610e7039bad45`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691dfb31babe98ecd811daf886e5bb2904f6651be231ba9b3e201c3dc87095ea`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e970ed5ae42bf870c81edb5016cece7d875e50fa0e058ed793886f5d0448c`  
		Last Modified: Thu, 09 Jan 2025 00:54:18 GMT  
		Size: 3.0 KB (2997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4066da33f2e3e51b0a837856dd42a595127f761948ef5e7743bc91ce93261a81`  
		Last Modified: Thu, 09 Jan 2025 00:54:22 GMT  
		Size: 119.2 MB (119190748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbace5f00e6ce8c05517232df85abfd9597ffad5e40273325a02b9f1b493e148`  
		Last Modified: Thu, 09 Jan 2025 00:54:18 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15` - unknown; unknown

```console
$ docker pull bonita@sha256:649cde818b1527e97ee598651e3cdf38a8adf0171bc553569eda705be0c849fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **917.1 KB (917142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9d2aadfc4c368a23f16b9d9188f01f6a421224d109e952119f980a227c0c07`

```dockerfile
```

-	Layers:
	-	`sha256:9ea11d0c422c85457f4a64f428bb8d8215df92e2460a0d102ac5809d7cd2e57d`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 893.8 KB (893818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30419c438167b976783cf8c1c7eb715c097ed23119fc0892d887d10c1e0e086`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 23.3 KB (23324 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:7.15.0`

```console
$ docker pull bonita@sha256:a613bf574688e911834d54b11f22e9ea42e86574bb16825088a422a2f3345939
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bonita:7.15.0` - linux; amd64

```console
$ docker pull bonita@sha256:5188e32eeb271cead0ecec62485650f5ca149702d3452f6aa612fae5e33358d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185598300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3471e8eaf5d7ecd3f0b3aa3824977c6193002a9e6fba2de6cb03a99e83d1571`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcce85a2d1c46d81f0ac2e80db005d94000aabed38b8ea64b20c1d2a6d38ca7`  
		Last Modified: Tue, 14 Jan 2025 21:28:14 GMT  
		Size: 62.8 MB (62771721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6c44d72b624209f41bb11468131325ebb11e7620aea3c56fec8d454370fe89`  
		Last Modified: Tue, 14 Jan 2025 21:28:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c067e3d716b220e2a521799ccc31cc2f81aa8483376a0eb816725296ba0e12f`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd401cc65ee90d0558b9b5eef05e5a8e34c8f743d54c493313019d77dd12663`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f86759833c16d14dbf6a1c2285f9a35eef3d64dd1c2e94c3f0ce61a1009c505`  
		Last Modified: Wed, 08 Jan 2025 18:16:52 GMT  
		Size: 3.0 KB (2992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4488c046b2b3dcfb9e4f454e0d27a3a5327bef30aaf70c5dbc3d6857e26fa6d`  
		Last Modified: Tue, 14 Jan 2025 23:32:08 GMT  
		Size: 119.2 MB (119190746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078953c12b2583edab0584a367d6b2796d74604bd12d6b390f76f2f9012b7e40`  
		Last Modified: Wed, 08 Jan 2025 18:16:52 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15.0` - unknown; unknown

```console
$ docker pull bonita@sha256:401ff348594a0b9ec35547e456d392e8123fa01b465e6cce6f5d6df6e5f979a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.0 KB (919966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3235cacdeb59c6372172164372ba20c0ca84da872eb0c468afca23bd2c69f1a`

```dockerfile
```

-	Layers:
	-	`sha256:1262c903057882def4c6095f99d576167e990ec9757b7dd9c57ef0fdde1e826c`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 896.7 KB (896694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98e116b1eda94c3ef8c44c8667f38f779a2bc174162e20575d839da409604244`  
		Last Modified: Wed, 08 Jan 2025 18:16:51 GMT  
		Size: 23.3 KB (23272 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.15.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:149f7f95f9cb43421652de30aba851a95b1676a49dca69d699b0e550768d7b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (186002724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c06d6d28a1ec622cb6d9a5561f8c039458c0ba0f83b9b4eaf514412f38f9dd`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c71ee63c722e93ab0a09e7f66235af257cac264a53da18a8ad7c84930a1fefc`  
		Last Modified: Thu, 09 Jan 2025 05:59:20 GMT  
		Size: 62.7 MB (62711604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9d28a79bdd6833db0090f53bc09d9cb1733688098b60fe749dfcedb78c03e0`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb01ce373a0ab369bb1831f0375ddfdab2c678f1ffbbbab82c2507994ab87dc`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f667e2cd51bbe61f599b9fd230c4680e52b52bc5795b540a9059f4fbba49abd1`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e92e38af8ad7b71573a168106e5cfe82d7d79c94b0f20d87253bc1844733ec7`  
		Last Modified: Thu, 09 Jan 2025 05:59:19 GMT  
		Size: 3.0 KB (2996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ac96db730bddd1c9fd403fbb5c9e917de6eac9df4ad3f32a58627d47b9faf3`  
		Last Modified: Thu, 09 Jan 2025 05:59:22 GMT  
		Size: 119.2 MB (119190774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd481cfcad1d53df462c245dc3eac22973aadf68ffbb8bca0aa9c4bcd7ab2ac`  
		Last Modified: Thu, 09 Jan 2025 05:59:19 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15.0` - unknown; unknown

```console
$ docker pull bonita@sha256:b97f28da6a6b3152959d0a80c86b8670d567354c21b8f5e51c1264f52da4a087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **919.2 KB (919227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8acadc16c974bac9f96f0674ea0fa0ca9a34aae0bc92079ed434c5f4b68d449d`

```dockerfile
```

-	Layers:
	-	`sha256:2736e60eb5967860fc66d6203b7d5620cb81bdff629e8592d0fdf67074a11eb6`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 895.8 KB (895791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9314740782b672dc878868ee66677bd97b2c5de76d4a716d299de94a1a1e20a0`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 23.4 KB (23436 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.15.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:11c7a754e0c78837202c123edf418ac2b4951009c332eb7476366f6cf7d50e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182019586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ba534660d88e296326a52414fa81f88a0ae64e6a8fe5c3ce2b141d274da393`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc39fc6cc5bb6cff536f0a7f21976f885040a6a78549abb0ec94136a5e890b1`  
		Last Modified: Thu, 09 Jan 2025 00:54:19 GMT  
		Size: 59.2 MB (59244850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed01549de2f2f8ab82b5507dc72db94fd49ce7348446c48d545ac4c49884fc`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b6902feeafff27b9132f63e252595ed37cd3432ea4084e342610e7039bad45`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691dfb31babe98ecd811daf886e5bb2904f6651be231ba9b3e201c3dc87095ea`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e970ed5ae42bf870c81edb5016cece7d875e50fa0e058ed793886f5d0448c`  
		Last Modified: Thu, 09 Jan 2025 00:54:18 GMT  
		Size: 3.0 KB (2997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4066da33f2e3e51b0a837856dd42a595127f761948ef5e7743bc91ce93261a81`  
		Last Modified: Thu, 09 Jan 2025 00:54:22 GMT  
		Size: 119.2 MB (119190748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbace5f00e6ce8c05517232df85abfd9597ffad5e40273325a02b9f1b493e148`  
		Last Modified: Thu, 09 Jan 2025 00:54:18 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15.0` - unknown; unknown

```console
$ docker pull bonita@sha256:649cde818b1527e97ee598651e3cdf38a8adf0171bc553569eda705be0c849fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **917.1 KB (917142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9d2aadfc4c368a23f16b9d9188f01f6a421224d109e952119f980a227c0c07`

```dockerfile
```

-	Layers:
	-	`sha256:9ea11d0c422c85457f4a64f428bb8d8215df92e2460a0d102ac5809d7cd2e57d`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 893.8 KB (893818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30419c438167b976783cf8c1c7eb715c097ed23119fc0892d887d10c1e0e086`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 23.3 KB (23324 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:8.0`

```console
$ docker pull bonita@sha256:83107fe06f2af584024a2557c45fb7a6cc70567767dc9ae297a5889a0893c842
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bonita:8.0` - linux; amd64

```console
$ docker pull bonita@sha256:839309576f921c062eb32d00c7306f8548c63eb2d641d8ea9e64427cd9123457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184586621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7c6d117c8bfb97c3e0b76314f01f64289353cd58923b97f3f86965d9f839e3`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87131e99d38b287035dfa2ac9ba12e0c61cdd62f01e64d80b9691672ebed5c6`  
		Last Modified: Wed, 08 Jan 2025 18:17:04 GMT  
		Size: 62.8 MB (62771776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebce3f7a9f918d324689aa8d9a204324d3abd229dd393c335c31947eceb29ed1`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625a766af4de10c10600747bd7996532f5ba388e68d36670ebf6b1f9a8298fe7`  
		Last Modified: Wed, 08 Jan 2025 18:17:02 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cac6e828598e8210b7fcd84264ee99829eb8a06f8b3fba37071d837309f2b1`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39d6b0d3105a1df4ff48246622351cd7236dd2a81e0fede1723e5a8c850c722`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 3.4 KB (3428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fc52347d1507c9706d8761cc789ddb1f73ed80b9840ad971b12befa51e3f0b`  
		Last Modified: Wed, 08 Jan 2025 18:17:05 GMT  
		Size: 118.2 MB (118178571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85222b2078f6c0397db8db28ba785a42db30c2b6219c34e9e7215735c54006b3`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0` - unknown; unknown

```console
$ docker pull bonita@sha256:3b40932a2cb7e60369bd084fecd38501a2a07e2d55b5286298f2f40a1cabfe12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.2 KB (911229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95c5e7ed59899afb163cb554d405050d9252d0b93d791a3f4a3006173d62906`

```dockerfile
```

-	Layers:
	-	`sha256:f03d081fb4baf16cd1a9b4ded32a8f6477033290a9bc3bf851ae1e40176a90b2`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 887.8 KB (887788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98e50441ea5d86128b4f4960b415a4218f82c16f1c16415781c8b02e7307cff`  
		Last Modified: Wed, 08 Jan 2025 18:17:02 GMT  
		Size: 23.4 KB (23441 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:8.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:4d23ced20e270cb79ab21845f99d318b86e1cda969daee67458a83ca3156f0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (184990940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e755ccbf8200e03ed2a498641c5d6d9d9de5396fee111d6a318b820f048907b8`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c71ee63c722e93ab0a09e7f66235af257cac264a53da18a8ad7c84930a1fefc`  
		Last Modified: Thu, 09 Jan 2025 05:59:20 GMT  
		Size: 62.7 MB (62711604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9d28a79bdd6833db0090f53bc09d9cb1733688098b60fe749dfcedb78c03e0`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb01ce373a0ab369bb1831f0375ddfdab2c678f1ffbbbab82c2507994ab87dc`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12612b3bd7cbc452059b073f49e94db0655d7822be8c364c6238fa7c60cd7e84`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea6af1bdb35bf00ee3573be784751630bc6fef21a415c8d02b081060e50f937`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c662642e29ee619a453047d983e5eb42790398c67e2d5e113d1078dda5fb49e`  
		Last Modified: Thu, 09 Jan 2025 05:59:52 GMT  
		Size: 118.2 MB (118178554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5326b2ad238fe1afe051e24ea07dbb166c1253b7a069fc2af7e3c5914469dd`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0` - unknown; unknown

```console
$ docker pull bonita@sha256:dec1921e6356f42a756693dbec2c7f13f9f802f73e64bcfa613a749db0498ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **910.5 KB (910491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f5e35ca2dd5e505725c68db2c4201772adee39a1a1021ff8756dfd1b022c28`

```dockerfile
```

-	Layers:
	-	`sha256:32ac41b0f82ca6c0cfac4b018f36c489494f74c5baeed6367248751082ca1fa4`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 886.9 KB (886885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01a9bbd5c91669aca4b3faf9d4c15ab0959ea48bd9649e9dff733eefb42ab4a`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 23.6 KB (23606 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:8.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:36c45dc9a35b65511e36092bbd57d3ec698816307359edb7d5c39254a553393e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181007832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7de5521b20151090ebca53c86b087ea237d1fdcd5c9e18873e4abd97be55362`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc39fc6cc5bb6cff536f0a7f21976f885040a6a78549abb0ec94136a5e890b1`  
		Last Modified: Thu, 09 Jan 2025 00:54:19 GMT  
		Size: 59.2 MB (59244850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed01549de2f2f8ab82b5507dc72db94fd49ce7348446c48d545ac4c49884fc`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b6902feeafff27b9132f63e252595ed37cd3432ea4084e342610e7039bad45`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17919c04b675f92c0aa1b927df53b5ea084a3f32f22c4b459432c370c62da2f9`  
		Last Modified: Thu, 09 Jan 2025 00:55:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52bf702c4dbcdf5cf776f521f260db5038ffc8a4a15014ad26acd4d36aa4076`  
		Last Modified: Thu, 09 Jan 2025 00:55:09 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7204c2340eed8f2487060d100468121249746be2def2bb602698eb3cc43842ef`  
		Last Modified: Thu, 09 Jan 2025 00:55:13 GMT  
		Size: 118.2 MB (118178561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6950c60595d40a223673a395499e29ccdb7e55b5ffe8cfcb16e28f528c68621f`  
		Last Modified: Thu, 09 Jan 2025 00:55:09 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0` - unknown; unknown

```console
$ docker pull bonita@sha256:c401cf069abaa9f2299f98de971d21c36cffc6903df57960bf9b2e056851fedc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **908.4 KB (908406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8deedf98ace90dc24939153fda3844199e8ba2955c46849be30a347259f922bf`

```dockerfile
```

-	Layers:
	-	`sha256:6439dd62b0f68192ca49b61056f70906e097c130e6de94ba0ec473111a55b827`  
		Last Modified: Thu, 09 Jan 2025 00:55:10 GMT  
		Size: 884.9 KB (884912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b34b1489729f0cbe6fa2fec694daeda2e7a7661ce59da9c836c02102e06fc56`  
		Last Modified: Thu, 09 Jan 2025 00:55:09 GMT  
		Size: 23.5 KB (23494 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:8.0.0`

```console
$ docker pull bonita@sha256:83107fe06f2af584024a2557c45fb7a6cc70567767dc9ae297a5889a0893c842
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bonita:8.0.0` - linux; amd64

```console
$ docker pull bonita@sha256:839309576f921c062eb32d00c7306f8548c63eb2d641d8ea9e64427cd9123457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184586621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7c6d117c8bfb97c3e0b76314f01f64289353cd58923b97f3f86965d9f839e3`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87131e99d38b287035dfa2ac9ba12e0c61cdd62f01e64d80b9691672ebed5c6`  
		Last Modified: Wed, 08 Jan 2025 18:17:04 GMT  
		Size: 62.8 MB (62771776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebce3f7a9f918d324689aa8d9a204324d3abd229dd393c335c31947eceb29ed1`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625a766af4de10c10600747bd7996532f5ba388e68d36670ebf6b1f9a8298fe7`  
		Last Modified: Wed, 08 Jan 2025 18:17:02 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cac6e828598e8210b7fcd84264ee99829eb8a06f8b3fba37071d837309f2b1`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39d6b0d3105a1df4ff48246622351cd7236dd2a81e0fede1723e5a8c850c722`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 3.4 KB (3428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fc52347d1507c9706d8761cc789ddb1f73ed80b9840ad971b12befa51e3f0b`  
		Last Modified: Wed, 08 Jan 2025 18:17:05 GMT  
		Size: 118.2 MB (118178571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85222b2078f6c0397db8db28ba785a42db30c2b6219c34e9e7215735c54006b3`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:3b40932a2cb7e60369bd084fecd38501a2a07e2d55b5286298f2f40a1cabfe12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.2 KB (911229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95c5e7ed59899afb163cb554d405050d9252d0b93d791a3f4a3006173d62906`

```dockerfile
```

-	Layers:
	-	`sha256:f03d081fb4baf16cd1a9b4ded32a8f6477033290a9bc3bf851ae1e40176a90b2`  
		Last Modified: Wed, 08 Jan 2025 18:17:03 GMT  
		Size: 887.8 KB (887788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98e50441ea5d86128b4f4960b415a4218f82c16f1c16415781c8b02e7307cff`  
		Last Modified: Wed, 08 Jan 2025 18:17:02 GMT  
		Size: 23.4 KB (23441 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:8.0.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:4d23ced20e270cb79ab21845f99d318b86e1cda969daee67458a83ca3156f0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (184990940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e755ccbf8200e03ed2a498641c5d6d9d9de5396fee111d6a318b820f048907b8`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c71ee63c722e93ab0a09e7f66235af257cac264a53da18a8ad7c84930a1fefc`  
		Last Modified: Thu, 09 Jan 2025 05:59:20 GMT  
		Size: 62.7 MB (62711604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9d28a79bdd6833db0090f53bc09d9cb1733688098b60fe749dfcedb78c03e0`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb01ce373a0ab369bb1831f0375ddfdab2c678f1ffbbbab82c2507994ab87dc`  
		Last Modified: Thu, 09 Jan 2025 05:59:18 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12612b3bd7cbc452059b073f49e94db0655d7822be8c364c6238fa7c60cd7e84`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea6af1bdb35bf00ee3573be784751630bc6fef21a415c8d02b081060e50f937`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c662642e29ee619a453047d983e5eb42790398c67e2d5e113d1078dda5fb49e`  
		Last Modified: Thu, 09 Jan 2025 05:59:52 GMT  
		Size: 118.2 MB (118178554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5326b2ad238fe1afe051e24ea07dbb166c1253b7a069fc2af7e3c5914469dd`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:dec1921e6356f42a756693dbec2c7f13f9f802f73e64bcfa613a749db0498ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **910.5 KB (910491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f5e35ca2dd5e505725c68db2c4201772adee39a1a1021ff8756dfd1b022c28`

```dockerfile
```

-	Layers:
	-	`sha256:32ac41b0f82ca6c0cfac4b018f36c489494f74c5baeed6367248751082ca1fa4`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 886.9 KB (886885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01a9bbd5c91669aca4b3faf9d4c15ab0959ea48bd9649e9dff733eefb42ab4a`  
		Last Modified: Thu, 09 Jan 2025 05:59:48 GMT  
		Size: 23.6 KB (23606 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:8.0.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:36c45dc9a35b65511e36092bbd57d3ec698816307359edb7d5c39254a553393e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181007832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7de5521b20151090ebca53c86b087ea237d1fdcd5c9e18873e4abd97be55362`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc39fc6cc5bb6cff536f0a7f21976f885040a6a78549abb0ec94136a5e890b1`  
		Last Modified: Thu, 09 Jan 2025 00:54:19 GMT  
		Size: 59.2 MB (59244850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed01549de2f2f8ab82b5507dc72db94fd49ce7348446c48d545ac4c49884fc`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b6902feeafff27b9132f63e252595ed37cd3432ea4084e342610e7039bad45`  
		Last Modified: Thu, 09 Jan 2025 00:54:17 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17919c04b675f92c0aa1b927df53b5ea084a3f32f22c4b459432c370c62da2f9`  
		Last Modified: Thu, 09 Jan 2025 00:55:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52bf702c4dbcdf5cf776f521f260db5038ffc8a4a15014ad26acd4d36aa4076`  
		Last Modified: Thu, 09 Jan 2025 00:55:09 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7204c2340eed8f2487060d100468121249746be2def2bb602698eb3cc43842ef`  
		Last Modified: Thu, 09 Jan 2025 00:55:13 GMT  
		Size: 118.2 MB (118178561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6950c60595d40a223673a395499e29ccdb7e55b5ffe8cfcb16e28f528c68621f`  
		Last Modified: Thu, 09 Jan 2025 00:55:09 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:c401cf069abaa9f2299f98de971d21c36cffc6903df57960bf9b2e056851fedc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **908.4 KB (908406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8deedf98ace90dc24939153fda3844199e8ba2955c46849be30a347259f922bf`

```dockerfile
```

-	Layers:
	-	`sha256:6439dd62b0f68192ca49b61056f70906e097c130e6de94ba0ec473111a55b827`  
		Last Modified: Thu, 09 Jan 2025 00:55:10 GMT  
		Size: 884.9 KB (884912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b34b1489729f0cbe6fa2fec694daeda2e7a7661ce59da9c836c02102e06fc56`  
		Last Modified: Thu, 09 Jan 2025 00:55:09 GMT  
		Size: 23.5 KB (23494 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:9.0`

```console
$ docker pull bonita@sha256:befe3da733a9f2ae6c7f1cd9ff873d3a5d4e5646f9ce7f85992d8dadee7abdc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bonita:9.0` - linux; amd64

```console
$ docker pull bonita@sha256:9a7b8be0335eca51240e576921f54fcdfb8c82472b0f9e04d39a33fe80a02eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192425524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376459bb6aec365e99f615be8f30be5752d17e1c863c39046af72cf1b281b869`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24854979e55d26ea6ba886a62b11271fc3b3aa0b8e58511e1ac900515805461`  
		Last Modified: Wed, 08 Jan 2025 18:16:56 GMT  
		Size: 68.6 MB (68615271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0557c93d928fd0d99725cb493940d90aa4c44c7ed3076499cdef92086c0783`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbbfb5f3be677939423491830e17a3b727b392fa4f92b3cfd5cea6af35825ec`  
		Last Modified: Wed, 08 Jan 2025 18:16:54 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2125cf3931e4bf088b69efea36c25f1989f4fa4172d38e2d95235863f38b11`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48af2960cafbf506204ff417840f1932ae079c8778cac11a93f9990008c9e068`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f74450d11734073a93dc5bad03f3eb7dcfffb65137129c745c71cb5f9852a83`  
		Last Modified: Wed, 15 Jan 2025 00:39:59 GMT  
		Size: 120.2 MB (120173557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4446248ca40e45ab4201f417dbe98c122248cccc1b6377c3c2822041ecb102a`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0` - unknown; unknown

```console
$ docker pull bonita@sha256:76704d018b8dfe83d3e60fe02d283822b78f2829293b0a282b2909a8b7e6c569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1367891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e2ff34cac1e9b80c419920795585de6d8293bbbdc0a4bd8d2e9b890ae10b33`

```dockerfile
```

-	Layers:
	-	`sha256:dbdf90f57620dd34aa6e3e6650d4b430a2db8cafdb875f084e4b8a27135ac9a0`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 1.3 MB (1344969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8555e596e9e84a80f6572cbe66a8ac589269dba921f4a1fdeb8d8ec2761f2d99`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 22.9 KB (22922 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:9.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:36746d767c698fdbba5000ab9d97e932cfe1cd9a556c4b766f01d6debf44e3c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192842367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e0f12c71e8cc60c6120fd1acaa162270d14c07b1875f246f7610611af94009`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f93ed4428e400840b905876fa9b313d4a61639fd0dfd34cd6818d47c2c6817`  
		Last Modified: Thu, 09 Jan 2025 06:00:25 GMT  
		Size: 68.6 MB (68567676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeedbee4f06903ae88f843e4aa606a554f851f66d9de03ca19584f6dffd59cd9`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af3c891e0576c57cd330ae29b751a39c84ae7262fad104877e1e948df380b82`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f8ee729bf2650d5723b0d21a87db6d9b5464bf06f2d1319c479565b5290bf`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42026758d938f272fede594a189a65c78b04e9899eb6e3befdcd40908010b966`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0018bb4a9752ba828bd273f3cbef282168a0a91adddea9b7969852e92eeb6c97`  
		Last Modified: Thu, 09 Jan 2025 06:00:27 GMT  
		Size: 120.2 MB (120173487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effd6aa26b4f46552102f4ce1c685a91cac05c6551fceea4d49637215789f600`  
		Last Modified: Thu, 09 Jan 2025 06:00:24 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0` - unknown; unknown

```console
$ docker pull bonita@sha256:93645412491a62bde23a8a1ae7b6477a34953446753906aa5fc6943d02155330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1367152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b469137932f91d588a6534e8500e8f01bcf8a3ac62e0de2ac64d1e86ce908b`

```dockerfile
```

-	Layers:
	-	`sha256:fafe5179e6c558ff4dc2dfc3a195a9f7f91fd089c67c592a03be4f4ca00b0701`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 1.3 MB (1344066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ece7403855922fc99e942417d1c44ca5c3afe898923a5a63df9ca84dc09108a`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 23.1 KB (23086 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:9.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:911f63694ee950a485b7478e650aff02ba17e10c32629968f8ad7acf744309bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189147658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c8c54f624a3f20b1e50097de01559ea1910aa25421c20dcd1e770253ed29e2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba9231fd7dafddae6f57c10c1eeee2d4cc54b1fe9ce3bda7015ab8aa9713147`  
		Last Modified: Thu, 09 Jan 2025 00:56:15 GMT  
		Size: 65.4 MB (65389294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240dfdea6771e09e3d9f02f1538602c6f7101d09be850381ad95a32b404a692b`  
		Last Modified: Thu, 09 Jan 2025 00:56:12 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601dcf390b56dc2206b9587480b4fdd9f56cf772bbb8c3ca3aeeb4dcf7c73f68`  
		Last Modified: Thu, 09 Jan 2025 00:56:12 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a558227dd619c5832bfdf25879c1cb5ac351814af85a97774a81c672bec2f62c`  
		Last Modified: Thu, 09 Jan 2025 00:56:12 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e82ece27f9744204bcafa35e1788eab7ca14ce844098613050b7501dd7feb1`  
		Last Modified: Thu, 09 Jan 2025 00:56:13 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a65f81c27e208cf38082e55db3fe539ebd749f2091f235314d7fd53eec78775`  
		Last Modified: Thu, 09 Jan 2025 00:56:17 GMT  
		Size: 120.2 MB (120173521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02dbf3bde71131e36b466675e496d97d1519cd954840f54ff78137d80a7f6b`  
		Last Modified: Thu, 09 Jan 2025 00:56:13 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0` - unknown; unknown

```console
$ docker pull bonita@sha256:15d9d9b7b7d0dd8222ae605e53e995a7c29a18e7a5ba6875f316b97f882e4f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1365067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe469ecd8101d9219ba8f7ab4a5e7c17c13a6fb1ca417b1a78a461dc7902f09`

```dockerfile
```

-	Layers:
	-	`sha256:7d633c084e1881a90b4eda94ce2a13272ee3c03575b26e57375fe21c3f0a7e31`  
		Last Modified: Thu, 09 Jan 2025 00:56:13 GMT  
		Size: 1.3 MB (1342093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b772685440d21b377539497002095f37a3f3dbb759fdb8f94e77c8b1129423e0`  
		Last Modified: Thu, 09 Jan 2025 00:56:12 GMT  
		Size: 23.0 KB (22974 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:9.0.0`

```console
$ docker pull bonita@sha256:befe3da733a9f2ae6c7f1cd9ff873d3a5d4e5646f9ce7f85992d8dadee7abdc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bonita:9.0.0` - linux; amd64

```console
$ docker pull bonita@sha256:9a7b8be0335eca51240e576921f54fcdfb8c82472b0f9e04d39a33fe80a02eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192425524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376459bb6aec365e99f615be8f30be5752d17e1c863c39046af72cf1b281b869`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24854979e55d26ea6ba886a62b11271fc3b3aa0b8e58511e1ac900515805461`  
		Last Modified: Wed, 08 Jan 2025 18:16:56 GMT  
		Size: 68.6 MB (68615271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0557c93d928fd0d99725cb493940d90aa4c44c7ed3076499cdef92086c0783`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbbfb5f3be677939423491830e17a3b727b392fa4f92b3cfd5cea6af35825ec`  
		Last Modified: Wed, 08 Jan 2025 18:16:54 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2125cf3931e4bf088b69efea36c25f1989f4fa4172d38e2d95235863f38b11`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48af2960cafbf506204ff417840f1932ae079c8778cac11a93f9990008c9e068`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f74450d11734073a93dc5bad03f3eb7dcfffb65137129c745c71cb5f9852a83`  
		Last Modified: Wed, 15 Jan 2025 00:39:59 GMT  
		Size: 120.2 MB (120173557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4446248ca40e45ab4201f417dbe98c122248cccc1b6377c3c2822041ecb102a`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:76704d018b8dfe83d3e60fe02d283822b78f2829293b0a282b2909a8b7e6c569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1367891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e2ff34cac1e9b80c419920795585de6d8293bbbdc0a4bd8d2e9b890ae10b33`

```dockerfile
```

-	Layers:
	-	`sha256:dbdf90f57620dd34aa6e3e6650d4b430a2db8cafdb875f084e4b8a27135ac9a0`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 1.3 MB (1344969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8555e596e9e84a80f6572cbe66a8ac589269dba921f4a1fdeb8d8ec2761f2d99`  
		Last Modified: Wed, 08 Jan 2025 18:16:55 GMT  
		Size: 22.9 KB (22922 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:9.0.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:36746d767c698fdbba5000ab9d97e932cfe1cd9a556c4b766f01d6debf44e3c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192842367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e0f12c71e8cc60c6120fd1acaa162270d14c07b1875f246f7610611af94009`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f93ed4428e400840b905876fa9b313d4a61639fd0dfd34cd6818d47c2c6817`  
		Last Modified: Thu, 09 Jan 2025 06:00:25 GMT  
		Size: 68.6 MB (68567676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeedbee4f06903ae88f843e4aa606a554f851f66d9de03ca19584f6dffd59cd9`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af3c891e0576c57cd330ae29b751a39c84ae7262fad104877e1e948df380b82`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f8ee729bf2650d5723b0d21a87db6d9b5464bf06f2d1319c479565b5290bf`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42026758d938f272fede594a189a65c78b04e9899eb6e3befdcd40908010b966`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0018bb4a9752ba828bd273f3cbef282168a0a91adddea9b7969852e92eeb6c97`  
		Last Modified: Thu, 09 Jan 2025 06:00:27 GMT  
		Size: 120.2 MB (120173487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effd6aa26b4f46552102f4ce1c685a91cac05c6551fceea4d49637215789f600`  
		Last Modified: Thu, 09 Jan 2025 06:00:24 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:93645412491a62bde23a8a1ae7b6477a34953446753906aa5fc6943d02155330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1367152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b469137932f91d588a6534e8500e8f01bcf8a3ac62e0de2ac64d1e86ce908b`

```dockerfile
```

-	Layers:
	-	`sha256:fafe5179e6c558ff4dc2dfc3a195a9f7f91fd089c67c592a03be4f4ca00b0701`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 1.3 MB (1344066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ece7403855922fc99e942417d1c44ca5c3afe898923a5a63df9ca84dc09108a`  
		Last Modified: Thu, 09 Jan 2025 06:00:23 GMT  
		Size: 23.1 KB (23086 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:9.0.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:911f63694ee950a485b7478e650aff02ba17e10c32629968f8ad7acf744309bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189147658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c8c54f624a3f20b1e50097de01559ea1910aa25421c20dcd1e770253ed29e2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba9231fd7dafddae6f57c10c1eeee2d4cc54b1fe9ce3bda7015ab8aa9713147`  
		Last Modified: Thu, 09 Jan 2025 00:56:15 GMT  
		Size: 65.4 MB (65389294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240dfdea6771e09e3d9f02f1538602c6f7101d09be850381ad95a32b404a692b`  
		Last Modified: Thu, 09 Jan 2025 00:56:12 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601dcf390b56dc2206b9587480b4fdd9f56cf772bbb8c3ca3aeeb4dcf7c73f68`  
		Last Modified: Thu, 09 Jan 2025 00:56:12 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a558227dd619c5832bfdf25879c1cb5ac351814af85a97774a81c672bec2f62c`  
		Last Modified: Thu, 09 Jan 2025 00:56:12 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e82ece27f9744204bcafa35e1788eab7ca14ce844098613050b7501dd7feb1`  
		Last Modified: Thu, 09 Jan 2025 00:56:13 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a65f81c27e208cf38082e55db3fe539ebd749f2091f235314d7fd53eec78775`  
		Last Modified: Thu, 09 Jan 2025 00:56:17 GMT  
		Size: 120.2 MB (120173521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02dbf3bde71131e36b466675e496d97d1519cd954840f54ff78137d80a7f6b`  
		Last Modified: Thu, 09 Jan 2025 00:56:13 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:15d9d9b7b7d0dd8222ae605e53e995a7c29a18e7a5ba6875f316b97f882e4f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1365067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe469ecd8101d9219ba8f7ab4a5e7c17c13a6fb1ca417b1a78a461dc7902f09`

```dockerfile
```

-	Layers:
	-	`sha256:7d633c084e1881a90b4eda94ce2a13272ee3c03575b26e57375fe21c3f0a7e31`  
		Last Modified: Thu, 09 Jan 2025 00:56:13 GMT  
		Size: 1.3 MB (1342093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b772685440d21b377539497002095f37a3f3dbb759fdb8f94e77c8b1129423e0`  
		Last Modified: Thu, 09 Jan 2025 00:56:12 GMT  
		Size: 23.0 KB (22974 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:latest`

```console
$ docker pull bonita@sha256:3381055815a9fcf2826ddf2c094cbca56e32af792687425889866a865b9a716a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:d31017b19b1e2abac3a7e877137f6aa0d29f19990dae4c5b948ea35ad9d4a436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187653756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bf9d639f2ac0407be063a1a5c0ce440f4521df9866772a3e6060176c13948e`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 15 Oct 2024 08:31:30 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
CMD ["/bin/sh"]
# Tue, 15 Oct 2024 08:31:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Oct 2024 08:31:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 08:31:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7a2df4e2f86eca649af1e17d990ab8e354cb6dee389606025b9d05f75623c388';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 15 Oct 2024 08:31:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 15 Oct 2024 08:31:30 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S -G bonita -h /opt/bonita/ -s /sbin/nologin bonita # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BONITA_VERSION
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BRANDING_VERSION
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BONITA_SHA256
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BASE_URL
# Tue, 15 Oct 2024 08:31:30 GMT
ARG BONITA_URL
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BONITA_VERSION=10.2.0
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BRANDING_VERSION=2024.3-u0
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BONITA_SHA256=75ad51a50cba484d3f74637584bf5144bf0cf28c06ae7a5efe1a804cdc996d86
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ZIP_FILE=BonitaCommunity-2024.3-u0.zip
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat
# Tue, 15 Oct 2024 08:31:30 GMT
ENV BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.2.0/bundle-tomcat-10.2.0.zip
# Tue, 15 Oct 2024 08:31:30 GMT
# ARGS: BONITA_VERSION=10.2.0 BRANDING_VERSION=2024.3-u0 BONITA_SHA256=75ad51a50cba484d3f74637584bf5144bf0cf28c06ae7a5efe1a804cdc996d86 BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.2.0/bundle-tomcat-10.2.0.zip
RUN mkdir /opt/files # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
COPY files /opt/files # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
# ARGS: BONITA_VERSION=10.2.0 BRANDING_VERSION=2024.3-u0 BONITA_SHA256=75ad51a50cba484d3f74637584bf5144bf0cf28c06ae7a5efe1a804cdc996d86 BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.2.0/bundle-tomcat-10.2.0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_API=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_API_PASSWORD=
# Tue, 15 Oct 2024 08:31:30 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 15 Oct 2024 08:31:30 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 15 Oct 2024 08:31:30 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 15 Oct 2024 08:31:30 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 15 Oct 2024 08:31:30 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 15 Oct 2024 08:31:30 GMT
COPY templates /opt/templates # buildkit
# Tue, 15 Oct 2024 08:31:30 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Tue, 15 Oct 2024 08:31:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh" "/opt/files/startup.sh"]
# Tue, 15 Oct 2024 08:31:30 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503acc57a2d3003e19b5c5340cba736f16b29a0bc3e999c0d1416c991795736c`  
		Last Modified: Tue, 14 Jan 2025 20:34:37 GMT  
		Size: 16.0 MB (16022381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8817feb2b110cc1789fe20f09dcc5c51f115ba14d2835e68c75d641a587590`  
		Last Modified: Tue, 14 Jan 2025 20:33:26 GMT  
		Size: 46.6 MB (46615830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5df38f82b8b06ef5d393e7b14812384815dcaf3ff17dfb71ca2c5b2ee6e6dee`  
		Last Modified: Wed, 08 Jan 2025 19:16:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e977457afcf675805fa147640a44466ed600bc1164300a1c25fc66452ba4e49`  
		Last Modified: Wed, 08 Jan 2025 19:16:59 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf913f8832f656d70ec770a5fd5aa0facd3d9956498b994110dd3f1b2887b8b`  
		Last Modified: Wed, 08 Jan 2025 20:33:12 GMT  
		Size: 1.9 MB (1860780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9c5994d5129eaf63e216754bf2dbbf2182b5a4897ea8b4138d4d7d1c64fc2d`  
		Last Modified: Wed, 15 Jan 2025 02:12:51 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875274e038f9cc07698bba33d02eb6cd80c4a30516e485a38ceea8a9979d0692`  
		Last Modified: Wed, 08 Jan 2025 20:33:11 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9105fd74f07a097e7a3444a88a182a82204912df8dd572c0dc1d81989fe2f55`  
		Last Modified: Tue, 14 Jan 2025 21:43:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80600160768888c5ab508d46c15d2a8aaf5f52d4648e1234c6b0dd43129abd1`  
		Last Modified: Tue, 14 Jan 2025 21:43:21 GMT  
		Size: 3.7 KB (3709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f480dc8b10a9c6b713edb69d58292ad9becf5e50e2a95f83d2841e088d060320`  
		Last Modified: Wed, 15 Jan 2025 00:59:17 GMT  
		Size: 119.5 MB (119515308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0a9b544bb55acb774b760e93a67a8918c1d5f3123d79f7c6bc5b21d37eaba4`  
		Last Modified: Wed, 08 Jan 2025 20:33:12 GMT  
		Size: 5.9 KB (5885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:latest` - unknown; unknown

```console
$ docker pull bonita@sha256:c017b1a60834ff3beb5110ecdadd13e0e42cea9282e1eed33d20e72d4042d982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1287875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bc5e8c6d2907265b7c82c290dcd772d56f5d44ebec370e9b60612103071db3`

```dockerfile
```

-	Layers:
	-	`sha256:37a851d11e941644bb5118316c7cc248134e88055dea7611e07660ae63b8ecb2`  
		Last Modified: Wed, 08 Jan 2025 20:33:11 GMT  
		Size: 1.3 MB (1258906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2443d3987f9befb2a74f68534a424ca5c0b11eea6737e117a206226aa5b4dff1`  
		Last Modified: Wed, 08 Jan 2025 20:33:11 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json
