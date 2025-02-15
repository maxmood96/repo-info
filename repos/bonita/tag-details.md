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
$ docker pull bonita@sha256:134ee951ab6e55d45d758e1c0d273ac388d622853f676ed5f3462ac52351a29e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:10.2` - linux; amd64

```console
$ docker pull bonita@sha256:4f590e8340bc6fbb05798bfe7ae5f0f272eec52b2194d67f45f02dcb534085e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187821017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7f800b63dc06000cb37aef6303d1b99195db2980f2f0e56a8e27a3249552b8`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 15 Oct 2024 08:31:30 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='9dcc53a30676692e604571a6e0bd13ac0c1b15f4bc2b78d19f88bd316075f84a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cc66ba0a96819420d8faf6f4c52e8d945d6b63a95860584022a8a19e6e7826`  
		Last Modified: Fri, 14 Feb 2025 20:34:33 GMT  
		Size: 16.2 MB (16175644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2830fdce3f8490cef419b2649bc04882f36bbb72656a0e08c4b4b851191b46f`  
		Last Modified: Fri, 14 Feb 2025 20:34:35 GMT  
		Size: 46.6 MB (46619385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d359e0dcce06e171a793aefe4843a8de78a18e661c1037ef36dfd3cce3e4852d`  
		Last Modified: Fri, 14 Feb 2025 20:34:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51631fe5dc907fa7751b1ea513749d84083935f3b79726f22e765131db943325`  
		Last Modified: Fri, 14 Feb 2025 20:34:32 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecb00b45addf0adf25df4741ec907c2d5248ccc343e2d8b3f930e009db677a7`  
		Last Modified: Sat, 15 Feb 2025 03:18:26 GMT  
		Size: 1.9 MB (1855214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f4bba9a8b0c9e35e9891885a780dd4b94347863afeee368957aa0cef56f60c`  
		Last Modified: Sat, 15 Feb 2025 03:18:27 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f3ca3297a9ed12be94f81a1378413242276e438b2e0e91983f6326bd865448`  
		Last Modified: Sat, 15 Feb 2025 03:18:26 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102a82a150eb2e63b4462bb6f8f56464ddbb723d590c7e4c785497b03b846f68`  
		Last Modified: Sat, 15 Feb 2025 03:18:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddacd56a6f2da123bd4e056e677a86effd63ce5f1c8d07a706b5415c8030c1de`  
		Last Modified: Fri, 14 Feb 2025 22:49:20 GMT  
		Size: 3.7 KB (3710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4251ca8b51619fc69f65b5a9daaa38869a261e0a013903d9360cd12bfe644c45`  
		Last Modified: Sat, 15 Feb 2025 03:18:26 GMT  
		Size: 119.5 MB (119515340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f32d0428af9a86a974af6ec7139de25179633359f9187379931f46ffc96de68`  
		Last Modified: Fri, 14 Feb 2025 22:49:23 GMT  
		Size: 5.9 KB (5885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:10.2` - unknown; unknown

```console
$ docker pull bonita@sha256:58abc6523a7aec7a4b61cd23df18c4c7ae611c042c1e7e605ed7cf034ef3c817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1294787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fd26982a9b37a9c0e07623d1372adac34087cf1ad89c8d1de459a88b435a31`

```dockerfile
```

-	Layers:
	-	`sha256:370f6f956e0a3f4b22ad7f78bea4cd46ca9e581988ce05c4541fb55b1bc6dca9`  
		Last Modified: Sat, 15 Feb 2025 00:55:16 GMT  
		Size: 1.3 MB (1265823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11a02b4899680bf7cc81a79ad506f66875063b4de182dbf2d223da113ff943bf`  
		Last Modified: Sat, 15 Feb 2025 00:55:16 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:10.2.0`

```console
$ docker pull bonita@sha256:134ee951ab6e55d45d758e1c0d273ac388d622853f676ed5f3462ac52351a29e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:10.2.0` - linux; amd64

```console
$ docker pull bonita@sha256:4f590e8340bc6fbb05798bfe7ae5f0f272eec52b2194d67f45f02dcb534085e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187821017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7f800b63dc06000cb37aef6303d1b99195db2980f2f0e56a8e27a3249552b8`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 15 Oct 2024 08:31:30 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='9dcc53a30676692e604571a6e0bd13ac0c1b15f4bc2b78d19f88bd316075f84a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cc66ba0a96819420d8faf6f4c52e8d945d6b63a95860584022a8a19e6e7826`  
		Last Modified: Fri, 14 Feb 2025 20:34:33 GMT  
		Size: 16.2 MB (16175644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2830fdce3f8490cef419b2649bc04882f36bbb72656a0e08c4b4b851191b46f`  
		Last Modified: Fri, 14 Feb 2025 20:34:35 GMT  
		Size: 46.6 MB (46619385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d359e0dcce06e171a793aefe4843a8de78a18e661c1037ef36dfd3cce3e4852d`  
		Last Modified: Fri, 14 Feb 2025 20:34:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51631fe5dc907fa7751b1ea513749d84083935f3b79726f22e765131db943325`  
		Last Modified: Fri, 14 Feb 2025 20:34:32 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecb00b45addf0adf25df4741ec907c2d5248ccc343e2d8b3f930e009db677a7`  
		Last Modified: Sat, 15 Feb 2025 03:18:26 GMT  
		Size: 1.9 MB (1855214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f4bba9a8b0c9e35e9891885a780dd4b94347863afeee368957aa0cef56f60c`  
		Last Modified: Sat, 15 Feb 2025 03:18:27 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f3ca3297a9ed12be94f81a1378413242276e438b2e0e91983f6326bd865448`  
		Last Modified: Sat, 15 Feb 2025 03:18:26 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102a82a150eb2e63b4462bb6f8f56464ddbb723d590c7e4c785497b03b846f68`  
		Last Modified: Sat, 15 Feb 2025 03:18:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddacd56a6f2da123bd4e056e677a86effd63ce5f1c8d07a706b5415c8030c1de`  
		Last Modified: Fri, 14 Feb 2025 22:49:20 GMT  
		Size: 3.7 KB (3710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4251ca8b51619fc69f65b5a9daaa38869a261e0a013903d9360cd12bfe644c45`  
		Last Modified: Sat, 15 Feb 2025 03:18:26 GMT  
		Size: 119.5 MB (119515340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f32d0428af9a86a974af6ec7139de25179633359f9187379931f46ffc96de68`  
		Last Modified: Fri, 14 Feb 2025 22:49:23 GMT  
		Size: 5.9 KB (5885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:10.2.0` - unknown; unknown

```console
$ docker pull bonita@sha256:58abc6523a7aec7a4b61cd23df18c4c7ae611c042c1e7e605ed7cf034ef3c817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1294787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fd26982a9b37a9c0e07623d1372adac34087cf1ad89c8d1de459a88b435a31`

```dockerfile
```

-	Layers:
	-	`sha256:370f6f956e0a3f4b22ad7f78bea4cd46ca9e581988ce05c4541fb55b1bc6dca9`  
		Last Modified: Sat, 15 Feb 2025 00:55:16 GMT  
		Size: 1.3 MB (1265823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11a02b4899680bf7cc81a79ad506f66875063b4de182dbf2d223da113ff943bf`  
		Last Modified: Sat, 15 Feb 2025 00:55:16 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2022.2`

```console
$ docker pull bonita@sha256:6a90a3e6e0052ed3a1dec4aba9c62f2ac753eb0f82c00df9adb7876e996dba37
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
$ docker pull bonita@sha256:70f89f736a99b5b301c6d6dfbff07f7b619d31b4adf2e0d82caee1db5f6c907e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185603049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948ea68a35b10493075f119ba9fcd5a311cde12b54a2d9c5d4dc290d3093f5a7`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523fdbc1ebd0ff5ea0bddb1c78e85cd5ada9c52f16e616d103d28c8e34daced5`  
		Last Modified: Fri, 14 Feb 2025 22:18:59 GMT  
		Size: 62.8 MB (62775905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807027b182dbca3c83f7a4b7c0ab6c5110ccf960048478b4f9f82e02623c7060`  
		Last Modified: Fri, 14 Feb 2025 22:18:53 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa3fd3faea58dcceee96a0d7d19b00fce1ae76b38a6839dbdbd0639bebe12dc`  
		Last Modified: Fri, 14 Feb 2025 22:18:54 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b193a61cd79b690bd189b2cf8fd958483b2b13c8f9e3eb0f487c4d494db47ea3`  
		Last Modified: Fri, 14 Feb 2025 22:18:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaf676ec4672ed0a8aa9d023fcfcd677b648d75784291f4f631424b14c350f1`  
		Last Modified: Fri, 14 Feb 2025 22:18:56 GMT  
		Size: 3.0 KB (2991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3290e54d39bccaf82a1db3849bf6a8f5c306ecf871f8c85dc775d5e6de5da4`  
		Last Modified: Fri, 14 Feb 2025 22:19:03 GMT  
		Size: 119.2 MB (119190673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095d9120e4d9d9e5701bb65bd04aed095651a4a07d5150be0d20bdd632351cdb`  
		Last Modified: Fri, 14 Feb 2025 22:18:51 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2` - unknown; unknown

```console
$ docker pull bonita@sha256:68f055518ad58ade390c32087acbea25f8eeed4d28852e4ad5581719b09197ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.0 KB (919966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cbba8fd9afb1559459138173cbe558c5a552e07ac2607eb032e13f6d0a4a7f`

```dockerfile
```

-	Layers:
	-	`sha256:6c6bacb2a90e57e286c54f78de54b9db0c84f88050e9cbb0797c7da62ea4a0e7`  
		Last Modified: Fri, 14 Feb 2025 21:55:23 GMT  
		Size: 896.7 KB (896694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a08458d95e6d7cef0d973a6cab0ebc812bac92ca26127a5fa3a4e779cef9bb3c`  
		Last Modified: Fri, 14 Feb 2025 21:55:18 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:19 GMT  
		Size: 895.8 KB (895791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9314740782b672dc878868ee66677bd97b2c5de76d4a716d299de94a1a1e20a0`  
		Last Modified: Fri, 14 Feb 2025 21:55:20 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:21 GMT  
		Size: 893.8 KB (893818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30419c438167b976783cf8c1c7eb715c097ed23119fc0892d887d10c1e0e086`  
		Last Modified: Fri, 14 Feb 2025 21:55:21 GMT  
		Size: 23.3 KB (23324 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2022.2-u0`

```console
$ docker pull bonita@sha256:6a90a3e6e0052ed3a1dec4aba9c62f2ac753eb0f82c00df9adb7876e996dba37
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
$ docker pull bonita@sha256:70f89f736a99b5b301c6d6dfbff07f7b619d31b4adf2e0d82caee1db5f6c907e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185603049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948ea68a35b10493075f119ba9fcd5a311cde12b54a2d9c5d4dc290d3093f5a7`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523fdbc1ebd0ff5ea0bddb1c78e85cd5ada9c52f16e616d103d28c8e34daced5`  
		Last Modified: Fri, 14 Feb 2025 22:18:59 GMT  
		Size: 62.8 MB (62775905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807027b182dbca3c83f7a4b7c0ab6c5110ccf960048478b4f9f82e02623c7060`  
		Last Modified: Fri, 14 Feb 2025 22:18:53 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa3fd3faea58dcceee96a0d7d19b00fce1ae76b38a6839dbdbd0639bebe12dc`  
		Last Modified: Fri, 14 Feb 2025 22:18:54 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b193a61cd79b690bd189b2cf8fd958483b2b13c8f9e3eb0f487c4d494db47ea3`  
		Last Modified: Fri, 14 Feb 2025 22:18:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaf676ec4672ed0a8aa9d023fcfcd677b648d75784291f4f631424b14c350f1`  
		Last Modified: Fri, 14 Feb 2025 22:18:56 GMT  
		Size: 3.0 KB (2991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3290e54d39bccaf82a1db3849bf6a8f5c306ecf871f8c85dc775d5e6de5da4`  
		Last Modified: Fri, 14 Feb 2025 22:19:03 GMT  
		Size: 119.2 MB (119190673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095d9120e4d9d9e5701bb65bd04aed095651a4a07d5150be0d20bdd632351cdb`  
		Last Modified: Fri, 14 Feb 2025 22:18:51 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:68f055518ad58ade390c32087acbea25f8eeed4d28852e4ad5581719b09197ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.0 KB (919966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cbba8fd9afb1559459138173cbe558c5a552e07ac2607eb032e13f6d0a4a7f`

```dockerfile
```

-	Layers:
	-	`sha256:6c6bacb2a90e57e286c54f78de54b9db0c84f88050e9cbb0797c7da62ea4a0e7`  
		Last Modified: Fri, 14 Feb 2025 21:55:23 GMT  
		Size: 896.7 KB (896694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a08458d95e6d7cef0d973a6cab0ebc812bac92ca26127a5fa3a4e779cef9bb3c`  
		Last Modified: Fri, 14 Feb 2025 21:55:18 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:19 GMT  
		Size: 895.8 KB (895791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9314740782b672dc878868ee66677bd97b2c5de76d4a716d299de94a1a1e20a0`  
		Last Modified: Fri, 14 Feb 2025 21:55:20 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:21 GMT  
		Size: 893.8 KB (893818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30419c438167b976783cf8c1c7eb715c097ed23119fc0892d887d10c1e0e086`  
		Last Modified: Fri, 14 Feb 2025 21:55:21 GMT  
		Size: 23.3 KB (23324 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.1`

```console
$ docker pull bonita@sha256:e5081366ec7c08a2f38f80fc6d9f5fe66e45498daffb58247e7ed366f85333cf
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
$ docker pull bonita@sha256:cdb8ffc5cddd33dc9f250ccfae6e22633a609f4e843aa1be8e750a0fa69b8994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184591507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b236b7b0358da64543c95e4edaa22b03cdb12dadab10d1fbaf5add343ab7030a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13145fc1171fabf4af2d3c1ad0bd5ed564749159be62b3e548dbc4ff5d49c7a`  
		Last Modified: Sat, 15 Feb 2025 01:23:11 GMT  
		Size: 62.8 MB (62775995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807027b182dbca3c83f7a4b7c0ab6c5110ccf960048478b4f9f82e02623c7060`  
		Last Modified: Fri, 14 Feb 2025 22:18:53 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3301db75859980fc852122645a33ade496f8242c546c5b29031e8c513e5a718d`  
		Last Modified: Sat, 15 Feb 2025 01:23:09 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5433cb1bdcba2e078eb912ea3767bfea9b6fedb460e1e86b950cbb4eceb33885`  
		Last Modified: Sat, 15 Feb 2025 01:23:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ca30e7b9752bee5d04fd5c093d680c61643c09039d136aea13a74643e4747b`  
		Last Modified: Sat, 15 Feb 2025 01:23:10 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ded21e469f71fa71e7f0be89bfbb18481349efa8ac3803378ae7300f158aef`  
		Last Modified: Sat, 15 Feb 2025 01:23:15 GMT  
		Size: 118.2 MB (118178602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a392c45766f3f4792b9e68430757187fd39864d9d16e4ee2f261d4d3d408c8`  
		Last Modified: Sat, 15 Feb 2025 01:23:10 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1` - unknown; unknown

```console
$ docker pull bonita@sha256:08148a6437ee13b3ae20da95d9d1c09335472c5101989f42dab30dd202e20aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.2 KB (911230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4438cb73f7a56dfdfdc6057107e9bed21cd680e2f3054d4d426cec3fda394025`

```dockerfile
```

-	Layers:
	-	`sha256:33826888a67d381b39952a2beb2b5b345f8acdc6dc5bd56f5d9083f5b99f712c`  
		Last Modified: Fri, 14 Feb 2025 21:55:24 GMT  
		Size: 887.8 KB (887788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64f9d04552673758063271d345662fde8f3a69efd7635ff28c6c35929cf853e8`  
		Last Modified: Fri, 14 Feb 2025 21:55:24 GMT  
		Size: 23.4 KB (23442 bytes)  
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
		Last Modified: Fri, 14 Feb 2025 21:55:25 GMT  
		Size: 886.9 KB (886885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01a9bbd5c91669aca4b3faf9d4c15ab0959ea48bd9649e9dff733eefb42ab4a`  
		Last Modified: Fri, 14 Feb 2025 21:55:26 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:27 GMT  
		Size: 884.9 KB (884912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b34b1489729f0cbe6fa2fec694daeda2e7a7661ce59da9c836c02102e06fc56`  
		Last Modified: Fri, 14 Feb 2025 21:55:28 GMT  
		Size: 23.5 KB (23494 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.1-u0`

```console
$ docker pull bonita@sha256:e5081366ec7c08a2f38f80fc6d9f5fe66e45498daffb58247e7ed366f85333cf
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
$ docker pull bonita@sha256:cdb8ffc5cddd33dc9f250ccfae6e22633a609f4e843aa1be8e750a0fa69b8994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184591507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b236b7b0358da64543c95e4edaa22b03cdb12dadab10d1fbaf5add343ab7030a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13145fc1171fabf4af2d3c1ad0bd5ed564749159be62b3e548dbc4ff5d49c7a`  
		Last Modified: Sat, 15 Feb 2025 01:23:11 GMT  
		Size: 62.8 MB (62775995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807027b182dbca3c83f7a4b7c0ab6c5110ccf960048478b4f9f82e02623c7060`  
		Last Modified: Fri, 14 Feb 2025 22:18:53 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3301db75859980fc852122645a33ade496f8242c546c5b29031e8c513e5a718d`  
		Last Modified: Sat, 15 Feb 2025 01:23:09 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5433cb1bdcba2e078eb912ea3767bfea9b6fedb460e1e86b950cbb4eceb33885`  
		Last Modified: Sat, 15 Feb 2025 01:23:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ca30e7b9752bee5d04fd5c093d680c61643c09039d136aea13a74643e4747b`  
		Last Modified: Sat, 15 Feb 2025 01:23:10 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ded21e469f71fa71e7f0be89bfbb18481349efa8ac3803378ae7300f158aef`  
		Last Modified: Sat, 15 Feb 2025 01:23:15 GMT  
		Size: 118.2 MB (118178602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a392c45766f3f4792b9e68430757187fd39864d9d16e4ee2f261d4d3d408c8`  
		Last Modified: Sat, 15 Feb 2025 01:23:10 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:08148a6437ee13b3ae20da95d9d1c09335472c5101989f42dab30dd202e20aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.2 KB (911230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4438cb73f7a56dfdfdc6057107e9bed21cd680e2f3054d4d426cec3fda394025`

```dockerfile
```

-	Layers:
	-	`sha256:33826888a67d381b39952a2beb2b5b345f8acdc6dc5bd56f5d9083f5b99f712c`  
		Last Modified: Fri, 14 Feb 2025 21:55:24 GMT  
		Size: 887.8 KB (887788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64f9d04552673758063271d345662fde8f3a69efd7635ff28c6c35929cf853e8`  
		Last Modified: Fri, 14 Feb 2025 21:55:24 GMT  
		Size: 23.4 KB (23442 bytes)  
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
		Last Modified: Fri, 14 Feb 2025 21:55:25 GMT  
		Size: 886.9 KB (886885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01a9bbd5c91669aca4b3faf9d4c15ab0959ea48bd9649e9dff733eefb42ab4a`  
		Last Modified: Fri, 14 Feb 2025 21:55:26 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:27 GMT  
		Size: 884.9 KB (884912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b34b1489729f0cbe6fa2fec694daeda2e7a7661ce59da9c836c02102e06fc56`  
		Last Modified: Fri, 14 Feb 2025 21:55:28 GMT  
		Size: 23.5 KB (23494 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.2`

```console
$ docker pull bonita@sha256:5af9c79d51bbdff07350c304bd325c08293e8e772cb53473f313d58476eb2c70
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
$ docker pull bonita@sha256:ef910d7b657e33952bb471aa34ecf472883eede9712fc4bbd6379bf515d72047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192428769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ead5818ecc4bdd2cdb00586a92a8889227c07cac9d480de52038e4d3ddf1893`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4e0a6d799194f177f53394044f2b9724b409b0a5593fcaa9f0ccd254303c16`  
		Last Modified: Sat, 15 Feb 2025 00:37:29 GMT  
		Size: 68.6 MB (68617926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ff6056fe17f4cbcf81b924dfdaa7afe1f624eda4fbb134fbc7f283247a397f`  
		Last Modified: Sat, 15 Feb 2025 00:37:26 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beba003a0ca74fdf053479aad78f22b5cf914e713b417411ae545d93c139b1d9`  
		Last Modified: Sat, 15 Feb 2025 00:37:27 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efb76d89d0ba0c29ce10949762ae31ae4a95b7f346e3b950585a60a633231b1`  
		Last Modified: Sat, 15 Feb 2025 00:37:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c528df8226c8a0f5a1fa1842dc60c4a94068c0025e9f5cf17b3046586d5c464`  
		Last Modified: Sat, 15 Feb 2025 00:37:28 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94873e8d73c29d17c861d8b6bad6e521bcf81f2131b8cc836cdbdb289c71057b`  
		Last Modified: Sat, 15 Feb 2025 00:37:33 GMT  
		Size: 120.2 MB (120173511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e80f6d0a1d5cb60a605878ebeda021e110d188cab1596b368db0e89d597b63`  
		Last Modified: Sat, 15 Feb 2025 00:37:29 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2` - unknown; unknown

```console
$ docker pull bonita@sha256:5b1dc241e2d5b5b262c358ccd73e80124d15b44fba1c1db635c77a3badd2b818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1367891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e3bde056d7f2c038cd39fdb8ae07a213b5bf8f8ee0c5b5ed49232384122a3f`

```dockerfile
```

-	Layers:
	-	`sha256:384c23da5dd3a3103dfebd666434ccc740905669f7787bb6ccb6cf559deaf204`  
		Last Modified: Fri, 14 Feb 2025 21:55:29 GMT  
		Size: 1.3 MB (1344969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d3dc27997ea5ca06d7074f60d5ccf00683ec7d77eadfaf5e6aa63f55e2eaab2`  
		Last Modified: Fri, 14 Feb 2025 21:55:29 GMT  
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
		Last Modified: Wed, 05 Feb 2025 14:22:51 GMT  
		Size: 68.6 MB (68567676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeedbee4f06903ae88f843e4aa606a554f851f66d9de03ca19584f6dffd59cd9`  
		Last Modified: Wed, 05 Feb 2025 14:22:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af3c891e0576c57cd330ae29b751a39c84ae7262fad104877e1e948df380b82`  
		Last Modified: Sat, 08 Feb 2025 01:45:58 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f8ee729bf2650d5723b0d21a87db6d9b5464bf06f2d1319c479565b5290bf`  
		Last Modified: Sat, 08 Feb 2025 01:45:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42026758d938f272fede594a189a65c78b04e9899eb6e3befdcd40908010b966`  
		Last Modified: Wed, 05 Feb 2025 14:22:37 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0018bb4a9752ba828bd273f3cbef282168a0a91adddea9b7969852e92eeb6c97`  
		Last Modified: Sat, 08 Feb 2025 01:46:11 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:31 GMT  
		Size: 1.3 MB (1344066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ece7403855922fc99e942417d1c44ca5c3afe898923a5a63df9ca84dc09108a`  
		Last Modified: Fri, 14 Feb 2025 21:55:31 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:32 GMT  
		Size: 1.3 MB (1342093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b772685440d21b377539497002095f37a3f3dbb759fdb8f94e77c8b1129423e0`  
		Last Modified: Fri, 14 Feb 2025 21:55:32 GMT  
		Size: 23.0 KB (22974 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.2-u0`

```console
$ docker pull bonita@sha256:5af9c79d51bbdff07350c304bd325c08293e8e772cb53473f313d58476eb2c70
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
$ docker pull bonita@sha256:ef910d7b657e33952bb471aa34ecf472883eede9712fc4bbd6379bf515d72047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192428769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ead5818ecc4bdd2cdb00586a92a8889227c07cac9d480de52038e4d3ddf1893`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4e0a6d799194f177f53394044f2b9724b409b0a5593fcaa9f0ccd254303c16`  
		Last Modified: Sat, 15 Feb 2025 00:37:29 GMT  
		Size: 68.6 MB (68617926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ff6056fe17f4cbcf81b924dfdaa7afe1f624eda4fbb134fbc7f283247a397f`  
		Last Modified: Sat, 15 Feb 2025 00:37:26 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beba003a0ca74fdf053479aad78f22b5cf914e713b417411ae545d93c139b1d9`  
		Last Modified: Sat, 15 Feb 2025 00:37:27 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efb76d89d0ba0c29ce10949762ae31ae4a95b7f346e3b950585a60a633231b1`  
		Last Modified: Sat, 15 Feb 2025 00:37:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c528df8226c8a0f5a1fa1842dc60c4a94068c0025e9f5cf17b3046586d5c464`  
		Last Modified: Sat, 15 Feb 2025 00:37:28 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94873e8d73c29d17c861d8b6bad6e521bcf81f2131b8cc836cdbdb289c71057b`  
		Last Modified: Sat, 15 Feb 2025 00:37:33 GMT  
		Size: 120.2 MB (120173511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e80f6d0a1d5cb60a605878ebeda021e110d188cab1596b368db0e89d597b63`  
		Last Modified: Sat, 15 Feb 2025 00:37:29 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:5b1dc241e2d5b5b262c358ccd73e80124d15b44fba1c1db635c77a3badd2b818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1367891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e3bde056d7f2c038cd39fdb8ae07a213b5bf8f8ee0c5b5ed49232384122a3f`

```dockerfile
```

-	Layers:
	-	`sha256:384c23da5dd3a3103dfebd666434ccc740905669f7787bb6ccb6cf559deaf204`  
		Last Modified: Fri, 14 Feb 2025 21:55:29 GMT  
		Size: 1.3 MB (1344969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d3dc27997ea5ca06d7074f60d5ccf00683ec7d77eadfaf5e6aa63f55e2eaab2`  
		Last Modified: Fri, 14 Feb 2025 21:55:29 GMT  
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
		Last Modified: Wed, 05 Feb 2025 14:22:51 GMT  
		Size: 68.6 MB (68567676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeedbee4f06903ae88f843e4aa606a554f851f66d9de03ca19584f6dffd59cd9`  
		Last Modified: Wed, 05 Feb 2025 14:22:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af3c891e0576c57cd330ae29b751a39c84ae7262fad104877e1e948df380b82`  
		Last Modified: Sat, 08 Feb 2025 01:45:58 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f8ee729bf2650d5723b0d21a87db6d9b5464bf06f2d1319c479565b5290bf`  
		Last Modified: Sat, 08 Feb 2025 01:45:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42026758d938f272fede594a189a65c78b04e9899eb6e3befdcd40908010b966`  
		Last Modified: Wed, 05 Feb 2025 14:22:37 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0018bb4a9752ba828bd273f3cbef282168a0a91adddea9b7969852e92eeb6c97`  
		Last Modified: Sat, 08 Feb 2025 01:46:11 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:31 GMT  
		Size: 1.3 MB (1344066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ece7403855922fc99e942417d1c44ca5c3afe898923a5a63df9ca84dc09108a`  
		Last Modified: Fri, 14 Feb 2025 21:55:31 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:32 GMT  
		Size: 1.3 MB (1342093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b772685440d21b377539497002095f37a3f3dbb759fdb8f94e77c8b1129423e0`  
		Last Modified: Fri, 14 Feb 2025 21:55:32 GMT  
		Size: 23.0 KB (22974 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2024.3`

```console
$ docker pull bonita@sha256:134ee951ab6e55d45d758e1c0d273ac388d622853f676ed5f3462ac52351a29e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:2024.3` - linux; amd64

```console
$ docker pull bonita@sha256:4f590e8340bc6fbb05798bfe7ae5f0f272eec52b2194d67f45f02dcb534085e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187821017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7f800b63dc06000cb37aef6303d1b99195db2980f2f0e56a8e27a3249552b8`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 15 Oct 2024 08:31:30 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='9dcc53a30676692e604571a6e0bd13ac0c1b15f4bc2b78d19f88bd316075f84a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cc66ba0a96819420d8faf6f4c52e8d945d6b63a95860584022a8a19e6e7826`  
		Last Modified: Fri, 14 Feb 2025 20:34:33 GMT  
		Size: 16.2 MB (16175644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2830fdce3f8490cef419b2649bc04882f36bbb72656a0e08c4b4b851191b46f`  
		Last Modified: Fri, 14 Feb 2025 20:34:35 GMT  
		Size: 46.6 MB (46619385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d359e0dcce06e171a793aefe4843a8de78a18e661c1037ef36dfd3cce3e4852d`  
		Last Modified: Fri, 14 Feb 2025 20:34:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51631fe5dc907fa7751b1ea513749d84083935f3b79726f22e765131db943325`  
		Last Modified: Fri, 14 Feb 2025 20:34:32 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecb00b45addf0adf25df4741ec907c2d5248ccc343e2d8b3f930e009db677a7`  
		Last Modified: Sat, 15 Feb 2025 03:18:26 GMT  
		Size: 1.9 MB (1855214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f4bba9a8b0c9e35e9891885a780dd4b94347863afeee368957aa0cef56f60c`  
		Last Modified: Sat, 15 Feb 2025 03:18:27 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f3ca3297a9ed12be94f81a1378413242276e438b2e0e91983f6326bd865448`  
		Last Modified: Sat, 15 Feb 2025 03:18:26 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102a82a150eb2e63b4462bb6f8f56464ddbb723d590c7e4c785497b03b846f68`  
		Last Modified: Sat, 15 Feb 2025 03:18:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddacd56a6f2da123bd4e056e677a86effd63ce5f1c8d07a706b5415c8030c1de`  
		Last Modified: Fri, 14 Feb 2025 22:49:20 GMT  
		Size: 3.7 KB (3710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4251ca8b51619fc69f65b5a9daaa38869a261e0a013903d9360cd12bfe644c45`  
		Last Modified: Sat, 15 Feb 2025 03:18:26 GMT  
		Size: 119.5 MB (119515340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f32d0428af9a86a974af6ec7139de25179633359f9187379931f46ffc96de68`  
		Last Modified: Fri, 14 Feb 2025 22:49:23 GMT  
		Size: 5.9 KB (5885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2024.3` - unknown; unknown

```console
$ docker pull bonita@sha256:58abc6523a7aec7a4b61cd23df18c4c7ae611c042c1e7e605ed7cf034ef3c817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1294787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fd26982a9b37a9c0e07623d1372adac34087cf1ad89c8d1de459a88b435a31`

```dockerfile
```

-	Layers:
	-	`sha256:370f6f956e0a3f4b22ad7f78bea4cd46ca9e581988ce05c4541fb55b1bc6dca9`  
		Last Modified: Sat, 15 Feb 2025 00:55:16 GMT  
		Size: 1.3 MB (1265823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11a02b4899680bf7cc81a79ad506f66875063b4de182dbf2d223da113ff943bf`  
		Last Modified: Sat, 15 Feb 2025 00:55:16 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2024.3-u0`

```console
$ docker pull bonita@sha256:134ee951ab6e55d45d758e1c0d273ac388d622853f676ed5f3462ac52351a29e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:2024.3-u0` - linux; amd64

```console
$ docker pull bonita@sha256:4f590e8340bc6fbb05798bfe7ae5f0f272eec52b2194d67f45f02dcb534085e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187821017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7f800b63dc06000cb37aef6303d1b99195db2980f2f0e56a8e27a3249552b8`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 15 Oct 2024 08:31:30 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='9dcc53a30676692e604571a6e0bd13ac0c1b15f4bc2b78d19f88bd316075f84a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cc66ba0a96819420d8faf6f4c52e8d945d6b63a95860584022a8a19e6e7826`  
		Last Modified: Fri, 14 Feb 2025 20:34:33 GMT  
		Size: 16.2 MB (16175644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2830fdce3f8490cef419b2649bc04882f36bbb72656a0e08c4b4b851191b46f`  
		Last Modified: Fri, 14 Feb 2025 20:34:35 GMT  
		Size: 46.6 MB (46619385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d359e0dcce06e171a793aefe4843a8de78a18e661c1037ef36dfd3cce3e4852d`  
		Last Modified: Fri, 14 Feb 2025 20:34:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51631fe5dc907fa7751b1ea513749d84083935f3b79726f22e765131db943325`  
		Last Modified: Fri, 14 Feb 2025 20:34:32 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecb00b45addf0adf25df4741ec907c2d5248ccc343e2d8b3f930e009db677a7`  
		Last Modified: Sat, 15 Feb 2025 03:18:26 GMT  
		Size: 1.9 MB (1855214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f4bba9a8b0c9e35e9891885a780dd4b94347863afeee368957aa0cef56f60c`  
		Last Modified: Sat, 15 Feb 2025 03:18:27 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f3ca3297a9ed12be94f81a1378413242276e438b2e0e91983f6326bd865448`  
		Last Modified: Sat, 15 Feb 2025 03:18:26 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102a82a150eb2e63b4462bb6f8f56464ddbb723d590c7e4c785497b03b846f68`  
		Last Modified: Sat, 15 Feb 2025 03:18:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddacd56a6f2da123bd4e056e677a86effd63ce5f1c8d07a706b5415c8030c1de`  
		Last Modified: Fri, 14 Feb 2025 22:49:20 GMT  
		Size: 3.7 KB (3710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4251ca8b51619fc69f65b5a9daaa38869a261e0a013903d9360cd12bfe644c45`  
		Last Modified: Sat, 15 Feb 2025 03:18:26 GMT  
		Size: 119.5 MB (119515340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f32d0428af9a86a974af6ec7139de25179633359f9187379931f46ffc96de68`  
		Last Modified: Fri, 14 Feb 2025 22:49:23 GMT  
		Size: 5.9 KB (5885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2024.3-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:58abc6523a7aec7a4b61cd23df18c4c7ae611c042c1e7e605ed7cf034ef3c817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1294787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fd26982a9b37a9c0e07623d1372adac34087cf1ad89c8d1de459a88b435a31`

```dockerfile
```

-	Layers:
	-	`sha256:370f6f956e0a3f4b22ad7f78bea4cd46ca9e581988ce05c4541fb55b1bc6dca9`  
		Last Modified: Sat, 15 Feb 2025 00:55:16 GMT  
		Size: 1.3 MB (1265823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11a02b4899680bf7cc81a79ad506f66875063b4de182dbf2d223da113ff943bf`  
		Last Modified: Sat, 15 Feb 2025 00:55:16 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:7.15`

```console
$ docker pull bonita@sha256:6a90a3e6e0052ed3a1dec4aba9c62f2ac753eb0f82c00df9adb7876e996dba37
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
$ docker pull bonita@sha256:70f89f736a99b5b301c6d6dfbff07f7b619d31b4adf2e0d82caee1db5f6c907e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185603049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948ea68a35b10493075f119ba9fcd5a311cde12b54a2d9c5d4dc290d3093f5a7`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523fdbc1ebd0ff5ea0bddb1c78e85cd5ada9c52f16e616d103d28c8e34daced5`  
		Last Modified: Fri, 14 Feb 2025 22:18:59 GMT  
		Size: 62.8 MB (62775905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807027b182dbca3c83f7a4b7c0ab6c5110ccf960048478b4f9f82e02623c7060`  
		Last Modified: Fri, 14 Feb 2025 22:18:53 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa3fd3faea58dcceee96a0d7d19b00fce1ae76b38a6839dbdbd0639bebe12dc`  
		Last Modified: Fri, 14 Feb 2025 22:18:54 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b193a61cd79b690bd189b2cf8fd958483b2b13c8f9e3eb0f487c4d494db47ea3`  
		Last Modified: Fri, 14 Feb 2025 22:18:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaf676ec4672ed0a8aa9d023fcfcd677b648d75784291f4f631424b14c350f1`  
		Last Modified: Fri, 14 Feb 2025 22:18:56 GMT  
		Size: 3.0 KB (2991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3290e54d39bccaf82a1db3849bf6a8f5c306ecf871f8c85dc775d5e6de5da4`  
		Last Modified: Fri, 14 Feb 2025 22:19:03 GMT  
		Size: 119.2 MB (119190673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095d9120e4d9d9e5701bb65bd04aed095651a4a07d5150be0d20bdd632351cdb`  
		Last Modified: Fri, 14 Feb 2025 22:18:51 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15` - unknown; unknown

```console
$ docker pull bonita@sha256:68f055518ad58ade390c32087acbea25f8eeed4d28852e4ad5581719b09197ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.0 KB (919966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cbba8fd9afb1559459138173cbe558c5a552e07ac2607eb032e13f6d0a4a7f`

```dockerfile
```

-	Layers:
	-	`sha256:6c6bacb2a90e57e286c54f78de54b9db0c84f88050e9cbb0797c7da62ea4a0e7`  
		Last Modified: Fri, 14 Feb 2025 21:55:23 GMT  
		Size: 896.7 KB (896694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a08458d95e6d7cef0d973a6cab0ebc812bac92ca26127a5fa3a4e779cef9bb3c`  
		Last Modified: Fri, 14 Feb 2025 21:55:18 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:19 GMT  
		Size: 895.8 KB (895791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9314740782b672dc878868ee66677bd97b2c5de76d4a716d299de94a1a1e20a0`  
		Last Modified: Fri, 14 Feb 2025 21:55:20 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:21 GMT  
		Size: 893.8 KB (893818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30419c438167b976783cf8c1c7eb715c097ed23119fc0892d887d10c1e0e086`  
		Last Modified: Fri, 14 Feb 2025 21:55:21 GMT  
		Size: 23.3 KB (23324 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:7.15.0`

```console
$ docker pull bonita@sha256:6a90a3e6e0052ed3a1dec4aba9c62f2ac753eb0f82c00df9adb7876e996dba37
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
$ docker pull bonita@sha256:70f89f736a99b5b301c6d6dfbff07f7b619d31b4adf2e0d82caee1db5f6c907e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185603049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948ea68a35b10493075f119ba9fcd5a311cde12b54a2d9c5d4dc290d3093f5a7`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523fdbc1ebd0ff5ea0bddb1c78e85cd5ada9c52f16e616d103d28c8e34daced5`  
		Last Modified: Fri, 14 Feb 2025 22:18:59 GMT  
		Size: 62.8 MB (62775905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807027b182dbca3c83f7a4b7c0ab6c5110ccf960048478b4f9f82e02623c7060`  
		Last Modified: Fri, 14 Feb 2025 22:18:53 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa3fd3faea58dcceee96a0d7d19b00fce1ae76b38a6839dbdbd0639bebe12dc`  
		Last Modified: Fri, 14 Feb 2025 22:18:54 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b193a61cd79b690bd189b2cf8fd958483b2b13c8f9e3eb0f487c4d494db47ea3`  
		Last Modified: Fri, 14 Feb 2025 22:18:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaf676ec4672ed0a8aa9d023fcfcd677b648d75784291f4f631424b14c350f1`  
		Last Modified: Fri, 14 Feb 2025 22:18:56 GMT  
		Size: 3.0 KB (2991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3290e54d39bccaf82a1db3849bf6a8f5c306ecf871f8c85dc775d5e6de5da4`  
		Last Modified: Fri, 14 Feb 2025 22:19:03 GMT  
		Size: 119.2 MB (119190673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095d9120e4d9d9e5701bb65bd04aed095651a4a07d5150be0d20bdd632351cdb`  
		Last Modified: Fri, 14 Feb 2025 22:18:51 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15.0` - unknown; unknown

```console
$ docker pull bonita@sha256:68f055518ad58ade390c32087acbea25f8eeed4d28852e4ad5581719b09197ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.0 KB (919966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8cbba8fd9afb1559459138173cbe558c5a552e07ac2607eb032e13f6d0a4a7f`

```dockerfile
```

-	Layers:
	-	`sha256:6c6bacb2a90e57e286c54f78de54b9db0c84f88050e9cbb0797c7da62ea4a0e7`  
		Last Modified: Fri, 14 Feb 2025 21:55:23 GMT  
		Size: 896.7 KB (896694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a08458d95e6d7cef0d973a6cab0ebc812bac92ca26127a5fa3a4e779cef9bb3c`  
		Last Modified: Fri, 14 Feb 2025 21:55:18 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:19 GMT  
		Size: 895.8 KB (895791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9314740782b672dc878868ee66677bd97b2c5de76d4a716d299de94a1a1e20a0`  
		Last Modified: Fri, 14 Feb 2025 21:55:20 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:21 GMT  
		Size: 893.8 KB (893818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30419c438167b976783cf8c1c7eb715c097ed23119fc0892d887d10c1e0e086`  
		Last Modified: Fri, 14 Feb 2025 21:55:21 GMT  
		Size: 23.3 KB (23324 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:8.0`

```console
$ docker pull bonita@sha256:e5081366ec7c08a2f38f80fc6d9f5fe66e45498daffb58247e7ed366f85333cf
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
$ docker pull bonita@sha256:cdb8ffc5cddd33dc9f250ccfae6e22633a609f4e843aa1be8e750a0fa69b8994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184591507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b236b7b0358da64543c95e4edaa22b03cdb12dadab10d1fbaf5add343ab7030a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13145fc1171fabf4af2d3c1ad0bd5ed564749159be62b3e548dbc4ff5d49c7a`  
		Last Modified: Sat, 15 Feb 2025 01:23:11 GMT  
		Size: 62.8 MB (62775995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807027b182dbca3c83f7a4b7c0ab6c5110ccf960048478b4f9f82e02623c7060`  
		Last Modified: Fri, 14 Feb 2025 22:18:53 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3301db75859980fc852122645a33ade496f8242c546c5b29031e8c513e5a718d`  
		Last Modified: Sat, 15 Feb 2025 01:23:09 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5433cb1bdcba2e078eb912ea3767bfea9b6fedb460e1e86b950cbb4eceb33885`  
		Last Modified: Sat, 15 Feb 2025 01:23:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ca30e7b9752bee5d04fd5c093d680c61643c09039d136aea13a74643e4747b`  
		Last Modified: Sat, 15 Feb 2025 01:23:10 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ded21e469f71fa71e7f0be89bfbb18481349efa8ac3803378ae7300f158aef`  
		Last Modified: Sat, 15 Feb 2025 01:23:15 GMT  
		Size: 118.2 MB (118178602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a392c45766f3f4792b9e68430757187fd39864d9d16e4ee2f261d4d3d408c8`  
		Last Modified: Sat, 15 Feb 2025 01:23:10 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0` - unknown; unknown

```console
$ docker pull bonita@sha256:08148a6437ee13b3ae20da95d9d1c09335472c5101989f42dab30dd202e20aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.2 KB (911230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4438cb73f7a56dfdfdc6057107e9bed21cd680e2f3054d4d426cec3fda394025`

```dockerfile
```

-	Layers:
	-	`sha256:33826888a67d381b39952a2beb2b5b345f8acdc6dc5bd56f5d9083f5b99f712c`  
		Last Modified: Fri, 14 Feb 2025 21:55:24 GMT  
		Size: 887.8 KB (887788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64f9d04552673758063271d345662fde8f3a69efd7635ff28c6c35929cf853e8`  
		Last Modified: Fri, 14 Feb 2025 21:55:24 GMT  
		Size: 23.4 KB (23442 bytes)  
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
		Last Modified: Fri, 14 Feb 2025 21:55:25 GMT  
		Size: 886.9 KB (886885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01a9bbd5c91669aca4b3faf9d4c15ab0959ea48bd9649e9dff733eefb42ab4a`  
		Last Modified: Fri, 14 Feb 2025 21:55:26 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:27 GMT  
		Size: 884.9 KB (884912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b34b1489729f0cbe6fa2fec694daeda2e7a7661ce59da9c836c02102e06fc56`  
		Last Modified: Fri, 14 Feb 2025 21:55:28 GMT  
		Size: 23.5 KB (23494 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:8.0.0`

```console
$ docker pull bonita@sha256:e5081366ec7c08a2f38f80fc6d9f5fe66e45498daffb58247e7ed366f85333cf
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
$ docker pull bonita@sha256:cdb8ffc5cddd33dc9f250ccfae6e22633a609f4e843aa1be8e750a0fa69b8994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184591507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b236b7b0358da64543c95e4edaa22b03cdb12dadab10d1fbaf5add343ab7030a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13145fc1171fabf4af2d3c1ad0bd5ed564749159be62b3e548dbc4ff5d49c7a`  
		Last Modified: Sat, 15 Feb 2025 01:23:11 GMT  
		Size: 62.8 MB (62775995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807027b182dbca3c83f7a4b7c0ab6c5110ccf960048478b4f9f82e02623c7060`  
		Last Modified: Fri, 14 Feb 2025 22:18:53 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3301db75859980fc852122645a33ade496f8242c546c5b29031e8c513e5a718d`  
		Last Modified: Sat, 15 Feb 2025 01:23:09 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5433cb1bdcba2e078eb912ea3767bfea9b6fedb460e1e86b950cbb4eceb33885`  
		Last Modified: Sat, 15 Feb 2025 01:23:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ca30e7b9752bee5d04fd5c093d680c61643c09039d136aea13a74643e4747b`  
		Last Modified: Sat, 15 Feb 2025 01:23:10 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ded21e469f71fa71e7f0be89bfbb18481349efa8ac3803378ae7300f158aef`  
		Last Modified: Sat, 15 Feb 2025 01:23:15 GMT  
		Size: 118.2 MB (118178602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a392c45766f3f4792b9e68430757187fd39864d9d16e4ee2f261d4d3d408c8`  
		Last Modified: Sat, 15 Feb 2025 01:23:10 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:08148a6437ee13b3ae20da95d9d1c09335472c5101989f42dab30dd202e20aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.2 KB (911230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4438cb73f7a56dfdfdc6057107e9bed21cd680e2f3054d4d426cec3fda394025`

```dockerfile
```

-	Layers:
	-	`sha256:33826888a67d381b39952a2beb2b5b345f8acdc6dc5bd56f5d9083f5b99f712c`  
		Last Modified: Fri, 14 Feb 2025 21:55:24 GMT  
		Size: 887.8 KB (887788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64f9d04552673758063271d345662fde8f3a69efd7635ff28c6c35929cf853e8`  
		Last Modified: Fri, 14 Feb 2025 21:55:24 GMT  
		Size: 23.4 KB (23442 bytes)  
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
		Last Modified: Fri, 14 Feb 2025 21:55:25 GMT  
		Size: 886.9 KB (886885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01a9bbd5c91669aca4b3faf9d4c15ab0959ea48bd9649e9dff733eefb42ab4a`  
		Last Modified: Fri, 14 Feb 2025 21:55:26 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:27 GMT  
		Size: 884.9 KB (884912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b34b1489729f0cbe6fa2fec694daeda2e7a7661ce59da9c836c02102e06fc56`  
		Last Modified: Fri, 14 Feb 2025 21:55:28 GMT  
		Size: 23.5 KB (23494 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:9.0`

```console
$ docker pull bonita@sha256:5af9c79d51bbdff07350c304bd325c08293e8e772cb53473f313d58476eb2c70
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
$ docker pull bonita@sha256:ef910d7b657e33952bb471aa34ecf472883eede9712fc4bbd6379bf515d72047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192428769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ead5818ecc4bdd2cdb00586a92a8889227c07cac9d480de52038e4d3ddf1893`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4e0a6d799194f177f53394044f2b9724b409b0a5593fcaa9f0ccd254303c16`  
		Last Modified: Sat, 15 Feb 2025 00:37:29 GMT  
		Size: 68.6 MB (68617926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ff6056fe17f4cbcf81b924dfdaa7afe1f624eda4fbb134fbc7f283247a397f`  
		Last Modified: Sat, 15 Feb 2025 00:37:26 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beba003a0ca74fdf053479aad78f22b5cf914e713b417411ae545d93c139b1d9`  
		Last Modified: Sat, 15 Feb 2025 00:37:27 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efb76d89d0ba0c29ce10949762ae31ae4a95b7f346e3b950585a60a633231b1`  
		Last Modified: Sat, 15 Feb 2025 00:37:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c528df8226c8a0f5a1fa1842dc60c4a94068c0025e9f5cf17b3046586d5c464`  
		Last Modified: Sat, 15 Feb 2025 00:37:28 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94873e8d73c29d17c861d8b6bad6e521bcf81f2131b8cc836cdbdb289c71057b`  
		Last Modified: Sat, 15 Feb 2025 00:37:33 GMT  
		Size: 120.2 MB (120173511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e80f6d0a1d5cb60a605878ebeda021e110d188cab1596b368db0e89d597b63`  
		Last Modified: Sat, 15 Feb 2025 00:37:29 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0` - unknown; unknown

```console
$ docker pull bonita@sha256:5b1dc241e2d5b5b262c358ccd73e80124d15b44fba1c1db635c77a3badd2b818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1367891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e3bde056d7f2c038cd39fdb8ae07a213b5bf8f8ee0c5b5ed49232384122a3f`

```dockerfile
```

-	Layers:
	-	`sha256:384c23da5dd3a3103dfebd666434ccc740905669f7787bb6ccb6cf559deaf204`  
		Last Modified: Fri, 14 Feb 2025 21:55:29 GMT  
		Size: 1.3 MB (1344969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d3dc27997ea5ca06d7074f60d5ccf00683ec7d77eadfaf5e6aa63f55e2eaab2`  
		Last Modified: Fri, 14 Feb 2025 21:55:29 GMT  
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
		Last Modified: Wed, 05 Feb 2025 14:22:51 GMT  
		Size: 68.6 MB (68567676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeedbee4f06903ae88f843e4aa606a554f851f66d9de03ca19584f6dffd59cd9`  
		Last Modified: Wed, 05 Feb 2025 14:22:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af3c891e0576c57cd330ae29b751a39c84ae7262fad104877e1e948df380b82`  
		Last Modified: Sat, 08 Feb 2025 01:45:58 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f8ee729bf2650d5723b0d21a87db6d9b5464bf06f2d1319c479565b5290bf`  
		Last Modified: Sat, 08 Feb 2025 01:45:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42026758d938f272fede594a189a65c78b04e9899eb6e3befdcd40908010b966`  
		Last Modified: Wed, 05 Feb 2025 14:22:37 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0018bb4a9752ba828bd273f3cbef282168a0a91adddea9b7969852e92eeb6c97`  
		Last Modified: Sat, 08 Feb 2025 01:46:11 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:31 GMT  
		Size: 1.3 MB (1344066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ece7403855922fc99e942417d1c44ca5c3afe898923a5a63df9ca84dc09108a`  
		Last Modified: Fri, 14 Feb 2025 21:55:31 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:32 GMT  
		Size: 1.3 MB (1342093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b772685440d21b377539497002095f37a3f3dbb759fdb8f94e77c8b1129423e0`  
		Last Modified: Fri, 14 Feb 2025 21:55:32 GMT  
		Size: 23.0 KB (22974 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:9.0.0`

```console
$ docker pull bonita@sha256:5af9c79d51bbdff07350c304bd325c08293e8e772cb53473f313d58476eb2c70
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
$ docker pull bonita@sha256:ef910d7b657e33952bb471aa34ecf472883eede9712fc4bbd6379bf515d72047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192428769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ead5818ecc4bdd2cdb00586a92a8889227c07cac9d480de52038e4d3ddf1893`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4e0a6d799194f177f53394044f2b9724b409b0a5593fcaa9f0ccd254303c16`  
		Last Modified: Sat, 15 Feb 2025 00:37:29 GMT  
		Size: 68.6 MB (68617926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ff6056fe17f4cbcf81b924dfdaa7afe1f624eda4fbb134fbc7f283247a397f`  
		Last Modified: Sat, 15 Feb 2025 00:37:26 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beba003a0ca74fdf053479aad78f22b5cf914e713b417411ae545d93c139b1d9`  
		Last Modified: Sat, 15 Feb 2025 00:37:27 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efb76d89d0ba0c29ce10949762ae31ae4a95b7f346e3b950585a60a633231b1`  
		Last Modified: Sat, 15 Feb 2025 00:37:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c528df8226c8a0f5a1fa1842dc60c4a94068c0025e9f5cf17b3046586d5c464`  
		Last Modified: Sat, 15 Feb 2025 00:37:28 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94873e8d73c29d17c861d8b6bad6e521bcf81f2131b8cc836cdbdb289c71057b`  
		Last Modified: Sat, 15 Feb 2025 00:37:33 GMT  
		Size: 120.2 MB (120173511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e80f6d0a1d5cb60a605878ebeda021e110d188cab1596b368db0e89d597b63`  
		Last Modified: Sat, 15 Feb 2025 00:37:29 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:5b1dc241e2d5b5b262c358ccd73e80124d15b44fba1c1db635c77a3badd2b818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1367891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e3bde056d7f2c038cd39fdb8ae07a213b5bf8f8ee0c5b5ed49232384122a3f`

```dockerfile
```

-	Layers:
	-	`sha256:384c23da5dd3a3103dfebd666434ccc740905669f7787bb6ccb6cf559deaf204`  
		Last Modified: Fri, 14 Feb 2025 21:55:29 GMT  
		Size: 1.3 MB (1344969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d3dc27997ea5ca06d7074f60d5ccf00683ec7d77eadfaf5e6aa63f55e2eaab2`  
		Last Modified: Fri, 14 Feb 2025 21:55:29 GMT  
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
		Last Modified: Wed, 05 Feb 2025 14:22:51 GMT  
		Size: 68.6 MB (68567676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeedbee4f06903ae88f843e4aa606a554f851f66d9de03ca19584f6dffd59cd9`  
		Last Modified: Wed, 05 Feb 2025 14:22:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af3c891e0576c57cd330ae29b751a39c84ae7262fad104877e1e948df380b82`  
		Last Modified: Sat, 08 Feb 2025 01:45:58 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f8ee729bf2650d5723b0d21a87db6d9b5464bf06f2d1319c479565b5290bf`  
		Last Modified: Sat, 08 Feb 2025 01:45:58 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42026758d938f272fede594a189a65c78b04e9899eb6e3befdcd40908010b966`  
		Last Modified: Wed, 05 Feb 2025 14:22:37 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0018bb4a9752ba828bd273f3cbef282168a0a91adddea9b7969852e92eeb6c97`  
		Last Modified: Sat, 08 Feb 2025 01:46:11 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:31 GMT  
		Size: 1.3 MB (1344066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ece7403855922fc99e942417d1c44ca5c3afe898923a5a63df9ca84dc09108a`  
		Last Modified: Fri, 14 Feb 2025 21:55:31 GMT  
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
		Last Modified: Fri, 14 Feb 2025 21:55:32 GMT  
		Size: 1.3 MB (1342093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b772685440d21b377539497002095f37a3f3dbb759fdb8f94e77c8b1129423e0`  
		Last Modified: Fri, 14 Feb 2025 21:55:32 GMT  
		Size: 23.0 KB (22974 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:latest`

```console
$ docker pull bonita@sha256:134ee951ab6e55d45d758e1c0d273ac388d622853f676ed5f3462ac52351a29e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:4f590e8340bc6fbb05798bfe7ae5f0f272eec52b2194d67f45f02dcb534085e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.8 MB (187821017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7f800b63dc06000cb37aef6303d1b99195db2980f2f0e56a8e27a3249552b8`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 15 Oct 2024 08:31:30 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 15 Oct 2024 08:31:30 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='9dcc53a30676692e604571a6e0bd13ac0c1b15f4bc2b78d19f88bd316075f84a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cc66ba0a96819420d8faf6f4c52e8d945d6b63a95860584022a8a19e6e7826`  
		Last Modified: Fri, 14 Feb 2025 20:34:33 GMT  
		Size: 16.2 MB (16175644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2830fdce3f8490cef419b2649bc04882f36bbb72656a0e08c4b4b851191b46f`  
		Last Modified: Fri, 14 Feb 2025 20:34:35 GMT  
		Size: 46.6 MB (46619385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d359e0dcce06e171a793aefe4843a8de78a18e661c1037ef36dfd3cce3e4852d`  
		Last Modified: Fri, 14 Feb 2025 20:34:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51631fe5dc907fa7751b1ea513749d84083935f3b79726f22e765131db943325`  
		Last Modified: Fri, 14 Feb 2025 20:34:32 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecb00b45addf0adf25df4741ec907c2d5248ccc343e2d8b3f930e009db677a7`  
		Last Modified: Sat, 15 Feb 2025 03:18:26 GMT  
		Size: 1.9 MB (1855214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f4bba9a8b0c9e35e9891885a780dd4b94347863afeee368957aa0cef56f60c`  
		Last Modified: Sat, 15 Feb 2025 03:18:27 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f3ca3297a9ed12be94f81a1378413242276e438b2e0e91983f6326bd865448`  
		Last Modified: Sat, 15 Feb 2025 03:18:26 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102a82a150eb2e63b4462bb6f8f56464ddbb723d590c7e4c785497b03b846f68`  
		Last Modified: Sat, 15 Feb 2025 03:18:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddacd56a6f2da123bd4e056e677a86effd63ce5f1c8d07a706b5415c8030c1de`  
		Last Modified: Fri, 14 Feb 2025 22:49:20 GMT  
		Size: 3.7 KB (3710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4251ca8b51619fc69f65b5a9daaa38869a261e0a013903d9360cd12bfe644c45`  
		Last Modified: Sat, 15 Feb 2025 03:18:26 GMT  
		Size: 119.5 MB (119515340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f32d0428af9a86a974af6ec7139de25179633359f9187379931f46ffc96de68`  
		Last Modified: Fri, 14 Feb 2025 22:49:23 GMT  
		Size: 5.9 KB (5885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:latest` - unknown; unknown

```console
$ docker pull bonita@sha256:58abc6523a7aec7a4b61cd23df18c4c7ae611c042c1e7e605ed7cf034ef3c817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1294787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fd26982a9b37a9c0e07623d1372adac34087cf1ad89c8d1de459a88b435a31`

```dockerfile
```

-	Layers:
	-	`sha256:370f6f956e0a3f4b22ad7f78bea4cd46ca9e581988ce05c4541fb55b1bc6dca9`  
		Last Modified: Sat, 15 Feb 2025 00:55:16 GMT  
		Size: 1.3 MB (1265823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11a02b4899680bf7cc81a79ad506f66875063b4de182dbf2d223da113ff943bf`  
		Last Modified: Sat, 15 Feb 2025 00:55:16 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
