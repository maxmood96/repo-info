## `bonita:latest`

```console
$ docker pull bonita@sha256:59c1b8e00cb98bc2d8867426c387385e948285a1e3a789928ce059552e0d23e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:bd3a68d57ffac271431557c75cb3cc8f07780aa6b39973d32f63973218d5f3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186632659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5497e60cca722c4fe02e826e8ff2ee1c6ffd3a6c74b8f9e8c08b7c793486235b`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 00:00:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:00:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:00:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:00:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 08 May 2026 00:00:05 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:00:11 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='33399db5fb4f542df36a706d6642a3ba1fab3d247da707273a11ef29e39f0705';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='b75c9f0dd052adfd213f0c2c1cc0c8a6d4539a8de9f7947d2b8fc45d18289975';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 08 May 2026 00:00:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:00:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:00:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:25:54 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 08 May 2026 00:25:54 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach # buildkit
# Fri, 08 May 2026 00:25:54 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Fri, 08 May 2026 00:25:54 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S -G bonita -h /opt/bonita/ -s /sbin/nologin bonita # buildkit
# Fri, 08 May 2026 00:25:54 GMT
ARG BONITA_VERSION
# Fri, 08 May 2026 00:25:54 GMT
ARG BRANDING_VERSION
# Fri, 08 May 2026 00:25:54 GMT
ARG BONITA_SHA256
# Fri, 08 May 2026 00:25:54 GMT
ARG BASE_URL
# Fri, 08 May 2026 00:25:54 GMT
ARG BONITA_URL
# Fri, 08 May 2026 00:25:54 GMT
ARG PROGRADE_VERSION=1.1.1
# Fri, 08 May 2026 00:25:54 GMT
ARG PROGRADE_JAR_SHA1=300d7ee29d79cc0ad8aad8e7abe17588ad3d33c5
# Fri, 08 May 2026 00:25:54 GMT
ENV BONITA_VERSION=11.0.0
# Fri, 08 May 2026 00:25:54 GMT
ENV BRANDING_VERSION=2026.1-u0
# Fri, 08 May 2026 00:25:54 GMT
ENV BONITA_SHA256=a3a0c80b975b51e247c630a204170beb675f4a83139ff2d1c533c1b7db17a25b
# Fri, 08 May 2026 00:25:54 GMT
ENV ZIP_FILE=BonitaCommunity-2026.1-u0.zip
# Fri, 08 May 2026 00:25:54 GMT
ENV BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat
# Fri, 08 May 2026 00:25:54 GMT
ENV BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/11.0.0/bundle-tomcat-11.0.0.zip
# Fri, 08 May 2026 00:25:54 GMT
# ARGS: BONITA_VERSION=11.0.0 BRANDING_VERSION=2026.1-u0 BONITA_SHA256=a3a0c80b975b51e247c630a204170beb675f4a83139ff2d1c533c1b7db17a25b BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/11.0.0/bundle-tomcat-11.0.0.zip PROGRADE_VERSION=1.1.1 PROGRADE_JAR_SHA1=300d7ee29d79cc0ad8aad8e7abe17588ad3d33c5
RUN mkdir /opt/files # buildkit
# Fri, 08 May 2026 00:25:54 GMT
COPY files /opt/files # buildkit
# Fri, 08 May 2026 00:25:59 GMT
# ARGS: BONITA_VERSION=11.0.0 BRANDING_VERSION=2026.1-u0 BONITA_SHA256=a3a0c80b975b51e247c630a204170beb675f4a83139ff2d1c533c1b7db17a25b BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/11.0.0/bundle-tomcat-11.0.0.zip PROGRADE_VERSION=1.1.1 PROGRADE_JAR_SHA1=300d7ee29d79cc0ad8aad8e7abe17588ad3d33c5
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then       echo "File already present in /opt/files";     else       curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip       && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c -;     fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/conf/prograde   && mv /opt/files/prograde.policy /opt/bonita/conf/prograde/   && wget -nv -O pro-grade.jar https://repo1.maven.org/maven2/net/sourceforge/pro-grade/pro-grade/${PROGRADE_VERSION}/pro-grade-${PROGRADE_VERSION}.jar   && echo "${PROGRADE_JAR_SHA1}  pro-grade.jar" | sha1sum -c -   && mv pro-grade.jar /opt/bonita/server/lib/ext/pro-grade.jar   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Fri, 08 May 2026 00:25:59 GMT
ENV HTTP_API=false
# Fri, 08 May 2026 00:25:59 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 08 May 2026 00:25:59 GMT
ENV HTTP_API_PASSWORD=
# Fri, 08 May 2026 00:25:59 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 08 May 2026 00:25:59 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 08 May 2026 00:25:59 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 08 May 2026 00:25:59 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 08 May 2026 00:25:59 GMT
ENV PRO_GRADE=true
# Fri, 08 May 2026 00:25:59 GMT
ENV PRO_GRADE_POLICY_PATH=/opt/bonita/conf/prograde
# Fri, 08 May 2026 00:25:59 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 08 May 2026 00:25:59 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 08 May 2026 00:25:59 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 08 May 2026 00:25:59 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 08 May 2026 00:25:59 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 08 May 2026 00:25:59 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 08 May 2026 00:25:59 GMT
COPY templates /opt/templates # buildkit
# Fri, 08 May 2026 00:25:59 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Fri, 08 May 2026 00:25:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh" "/opt/files/startup.sh"]
# Fri, 08 May 2026 00:25:59 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef4bf1bda3522f6b64c24ee154ed6739c8ab26c1be19e7b9e564bf0f39cbf22`  
		Last Modified: Fri, 08 May 2026 00:00:23 GMT  
		Size: 16.9 MB (16857117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e338134b21e530c8c101d288f216594c45a122a53f0d095568b2d0e943d8fec`  
		Last Modified: Fri, 08 May 2026 00:00:24 GMT  
		Size: 53.3 MB (53301871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42516208460b63f47d0044aef98b70571ce7765cc9108b0a3d14ae7fa16d7566`  
		Last Modified: Fri, 08 May 2026 00:00:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1a277377d10ae29a58277bdefa13f3a1cfffb295a5b7bce5ad0b0d82661629`  
		Last Modified: Fri, 08 May 2026 00:00:22 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f4a66bd7106c9c54ff70be675789e42a5982b1419219e7f4e2ad69b58ee130`  
		Last Modified: Fri, 08 May 2026 00:26:10 GMT  
		Size: 1.6 MB (1642719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1331fb898705e9cf3ae044c406faeff2d70193735d71f5fac247d8b24cbbaed5`  
		Last Modified: Fri, 08 May 2026 00:26:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a78056de134cf7c1fda4e14d377b17d8c802b03b41419eae0740570ed16ad54`  
		Last Modified: Fri, 08 May 2026 00:26:09 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e658fc8919922f83a19088f8415f6bfad3aee78d9b8da0d560179fb24b4211f5`  
		Last Modified: Fri, 08 May 2026 00:26:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd065a0d4ccc89e73ffbaaa4195485bc76a3717e7769f59d9997aa1f9d6c672`  
		Last Modified: Fri, 08 May 2026 00:26:10 GMT  
		Size: 4.9 KB (4924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4293dc877d1c6c5d31e1403dbc2bb07910cd8af390388d8a48aa82414dcabe`  
		Last Modified: Fri, 08 May 2026 00:26:16 GMT  
		Size: 111.0 MB (110952298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c270b5bb6613b307097b3e9878096c9601e08ad54a1d858f43706fc761fea3`  
		Last Modified: Fri, 08 May 2026 00:26:11 GMT  
		Size: 6.0 KB (5950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:latest` - unknown; unknown

```console
$ docker pull bonita@sha256:05c4610743d8352990f947cfba02aafb72f2ad2c17fbf1748f66d48ee63098f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1253934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a0ddbde5c4fdf36c0fda46807c720c621f469f6ca4ef8390001a4627a89748`

```dockerfile
```

-	Layers:
	-	`sha256:5089bb79c5aec19db02c52401c73861ba778e0368c3dc68c65064b2597e2bcf6`  
		Last Modified: Fri, 08 May 2026 00:26:09 GMT  
		Size: 1.2 MB (1223228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfefec41699d93ee3f502320236780e11e7de416e1133704c4d336d3d13503cc`  
		Last Modified: Fri, 08 May 2026 00:26:09 GMT  
		Size: 30.7 KB (30706 bytes)  
		MIME: application/vnd.in-toto+json
