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
$ docker pull bonita@sha256:1f7af758a6dca6bba55c28f36b75b2d79ea624e7b48390f18482160d8fa43379
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:10.2` - linux; amd64

```console
$ docker pull bonita@sha256:aff72fdcdc1abd4b9bbad0c155d337538226d6724f0e50ced51ed4bcbf815bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189935357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8302afd6c116f16b99b8803f90d5e5d93087ce9de24a10d9ab1e9a966f9b9841`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb8a593a4b7726f83576628ca6aa70220bcdcbef9651d003ba88727ce34d9d1`  
		Last Modified: Tue, 12 Nov 2024 02:38:48 GMT  
		Size: 18.3 MB (18307356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441f37ea86bb2ebd3f2d928c64e6d4c39686f25618e8847e957fee5ff58da0e6`  
		Last Modified: Tue, 12 Nov 2024 02:38:49 GMT  
		Size: 46.6 MB (46615858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44818f47c6831f333e1b9a5947c85124e4a12ca670bea7043d4b11beeb3a780b`  
		Last Modified: Tue, 12 Nov 2024 02:38:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cfa7e9b065bacf6029c8a0af5b63bb0e86ef13e828cb645d914da3480fbbfb`  
		Last Modified: Tue, 12 Nov 2024 02:38:48 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282cd84bf85b9e16a5b15f900b8c120135cdd324c624dfefc957b15a5c8f4924`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 1.9 MB (1859693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846171241c7d276eaaa07a72711d35c5fee179900b56800d5ec0c8e937afc5ce`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8646004264a0d08ea69c6cb78588da01faa2819ff6a4a8c61e87fe36f44c75d1`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382f0c1559b8a9d44cdc48b848d6f66a19a9bbccf9eb4c68283330c9424ae256`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb4e9a3063b2241adf74732cf5eff7a4dbc4f0de557e68a18f505c33cbb22f0`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 3.7 KB (3709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b96214236cb294ae2c9d88dd27fb374b2157482e17cfaf5922a1cd7260f7d1`  
		Last Modified: Tue, 12 Nov 2024 03:11:46 GMT  
		Size: 119.5 MB (119515350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f4fcac1efe12c849b5d2ccb6c9ba54211207d66579b86cceecd00c717a268d`  
		Last Modified: Tue, 12 Nov 2024 03:11:45 GMT  
		Size: 5.9 KB (5882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:10.2` - unknown; unknown

```console
$ docker pull bonita@sha256:b6797d0a32115ece7f217354ee93f1518bd21a599ce0d3748974467c286df1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c5d4f1dc1cdfcf2877600fc4dc9290598ae9a34d569ddbbf974eae70cbb2d2`

```dockerfile
```

-	Layers:
	-	`sha256:76e80da520f48790ac44f471f6e9707006debdcc727cf18427d5cff5d4bf676a`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 1.3 MB (1265026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fff7ba6987a0718b554cbd6abdbb95082e916db7b565f8500391ff9e438de050`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:10.2.0`

```console
$ docker pull bonita@sha256:1f7af758a6dca6bba55c28f36b75b2d79ea624e7b48390f18482160d8fa43379
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:10.2.0` - linux; amd64

```console
$ docker pull bonita@sha256:aff72fdcdc1abd4b9bbad0c155d337538226d6724f0e50ced51ed4bcbf815bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189935357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8302afd6c116f16b99b8803f90d5e5d93087ce9de24a10d9ab1e9a966f9b9841`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb8a593a4b7726f83576628ca6aa70220bcdcbef9651d003ba88727ce34d9d1`  
		Last Modified: Tue, 12 Nov 2024 02:38:48 GMT  
		Size: 18.3 MB (18307356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441f37ea86bb2ebd3f2d928c64e6d4c39686f25618e8847e957fee5ff58da0e6`  
		Last Modified: Tue, 12 Nov 2024 02:38:49 GMT  
		Size: 46.6 MB (46615858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44818f47c6831f333e1b9a5947c85124e4a12ca670bea7043d4b11beeb3a780b`  
		Last Modified: Tue, 12 Nov 2024 02:38:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cfa7e9b065bacf6029c8a0af5b63bb0e86ef13e828cb645d914da3480fbbfb`  
		Last Modified: Tue, 12 Nov 2024 02:38:48 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282cd84bf85b9e16a5b15f900b8c120135cdd324c624dfefc957b15a5c8f4924`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 1.9 MB (1859693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846171241c7d276eaaa07a72711d35c5fee179900b56800d5ec0c8e937afc5ce`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8646004264a0d08ea69c6cb78588da01faa2819ff6a4a8c61e87fe36f44c75d1`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382f0c1559b8a9d44cdc48b848d6f66a19a9bbccf9eb4c68283330c9424ae256`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb4e9a3063b2241adf74732cf5eff7a4dbc4f0de557e68a18f505c33cbb22f0`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 3.7 KB (3709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b96214236cb294ae2c9d88dd27fb374b2157482e17cfaf5922a1cd7260f7d1`  
		Last Modified: Tue, 12 Nov 2024 03:11:46 GMT  
		Size: 119.5 MB (119515350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f4fcac1efe12c849b5d2ccb6c9ba54211207d66579b86cceecd00c717a268d`  
		Last Modified: Tue, 12 Nov 2024 03:11:45 GMT  
		Size: 5.9 KB (5882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:10.2.0` - unknown; unknown

```console
$ docker pull bonita@sha256:b6797d0a32115ece7f217354ee93f1518bd21a599ce0d3748974467c286df1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c5d4f1dc1cdfcf2877600fc4dc9290598ae9a34d569ddbbf974eae70cbb2d2`

```dockerfile
```

-	Layers:
	-	`sha256:76e80da520f48790ac44f471f6e9707006debdcc727cf18427d5cff5d4bf676a`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 1.3 MB (1265026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fff7ba6987a0718b554cbd6abdbb95082e916db7b565f8500391ff9e438de050`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2022.2`

```console
$ docker pull bonita@sha256:c39374fcee35ae6c280b3598b22a6a78ad1859255a063d15f52fbc2d5cd4710a
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
$ docker pull bonita@sha256:49fdb0a389ab9a73c82559421885e4417dc67c4e598886e2494ef7dca85549ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185591682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b47cfe98d547bc9492ded96bbf2a60244ede36fa4cbc68f5e2a03586aa56e2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1704e491511327dfa650b4d444b58317f3a0fe58e67c69a6c8976449dd921589`  
		Last Modified: Tue, 12 Nov 2024 02:50:04 GMT  
		Size: 62.8 MB (62767436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0432548f58c3d18ac7cc84193809872251f712ee9600ba6a762e09a7b80f2ff`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d0d960091949bf5ce0cb770766860ec8d3ed66c1fe44e26e638375881183c7`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc31aeed985564402f610e37e3cb6e340379078271cf49947cfab01e7958a1`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1df8a28c973f9c080855cf95bb4e9167a6abff01debb4ea3ce0cb13a13ff219`  
		Last Modified: Tue, 12 Nov 2024 02:50:04 GMT  
		Size: 3.0 KB (2996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024f83debc31564976436c87274625b455cb0de6c38fd50cd0cb5b3db68c199f`  
		Last Modified: Tue, 12 Nov 2024 02:50:06 GMT  
		Size: 119.2 MB (119190759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f927a37aed79931b2ab2a1b07262b98bf430d7db137b6c9011ca38762f74cab6`  
		Last Modified: Tue, 12 Nov 2024 02:50:04 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2` - unknown; unknown

```console
$ docker pull bonita@sha256:cfbff6470515c966d24a9c734ee287e2bde573c68bda1c0ba203f7429e4364c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **923.1 KB (923054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9e14354a23b9eb55f842bb6ffe6920775f36f31412773d578b561aa72cf271`

```dockerfile
```

-	Layers:
	-	`sha256:1b6f7db153fd74bb2d7bf1793ed88b2791ea3e30adae5d5d2ddc939b3e598ad9`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 899.8 KB (899782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dff381108e8f83d7e8123edb6a42f1233705c8fd8b50c29f9423d2d4863e5cf`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 23.3 KB (23272 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ce6a7a351b796e57c271376fa1fa9ef327bdcbbca7b618137bc7313c478bdcd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (185956874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f25a7077c12b4bcae58f4096445dc773a8e2d65eac16c92424867c265d0434`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4243273752f8c627f434b3051f7e45c5fa32ed3cb2318814b498fd999ce94b3d`  
		Last Modified: Sat, 07 Sep 2024 04:47:02 GMT  
		Size: 62.7 MB (62668884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88e30d06e54c9c99eef98f9dc827553050ba338c98bc364b1cae5f97c4368a3`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dc804ca99cd43313a465eac63c4ae60d837bb13473c108b1aaa195bb3cbd48`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230954cd83a5c61457aa349661e2f40cd31bad4249ad5d1fb2165a22b6fff80`  
		Last Modified: Sat, 07 Sep 2024 04:47:00 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6ef67b3171feb38b26e1148b5d5fd9de3289e777bf520407c8f967e987181c`  
		Last Modified: Sat, 07 Sep 2024 04:47:00 GMT  
		Size: 3.0 KB (2991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb2ef7c342ce6703eea1d856ee88d0b539a3c0872d0c26987ba320bd947d7d5`  
		Last Modified: Sat, 07 Sep 2024 04:47:03 GMT  
		Size: 119.2 MB (119190773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3034be95d20eb74b6f2e72890d7c3bc2f2def229cc150c15659abe63065f7f3`  
		Last Modified: Sat, 07 Sep 2024 04:47:01 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2` - unknown; unknown

```console
$ docker pull bonita@sha256:9d999a99eb8185e9967aa74d620561d0ad63e568f0b701f9820beb877cdefed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **895.5 KB (895525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1af6383b7261a722c08531debd3dac797f4071e7eebf545bab305e7216e9606`

```dockerfile
```

-	Layers:
	-	`sha256:7f358a487a3fd110f6f5c0510c419a1f4377873933a38055c96a84f492fb2e0b`  
		Last Modified: Sat, 07 Sep 2024 04:47:00 GMT  
		Size: 872.2 KB (872162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac063d781e61113c6a1154c35eeba6d85c4256e081b944968635c66d2b5c633c`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 23.4 KB (23363 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:be4b4ad368e0d1f3908b8edfd548308c416e9016c8d81fe1234abb5d1dc305b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (181981166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f72f3a3e8e04472091c15e1ec94d8377d4d66a4a2b80ab48da3de5d149ece7`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2cf315af9480a876ed5e7efa86f52cab190a197656dcc25c561183380ba96d`  
		Last Modified: Sat, 07 Sep 2024 06:24:04 GMT  
		Size: 59.2 MB (59208493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c12032181a2e1089fca129cb6666ad1b33b69185233e9dc4cc7f69e6fb1190b`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d840c9bd89b5157b8d6f51fa118c75017552d7d26bfd8808b66f90e2f8ed76d`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a507a4e543c41bca75a33a03239a6c37f78f49709502fe2a536e0cc7e8fc5eb`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4b0d8d01b46d636da0273a5a6acb4721009c229c4de0a724cb3942b315462b`  
		Last Modified: Sat, 07 Sep 2024 06:24:03 GMT  
		Size: 3.0 KB (2996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef106ed190e76072c43f93c68593238430954d9c26a36a8c2c9539bbd477815`  
		Last Modified: Sat, 07 Sep 2024 06:24:07 GMT  
		Size: 119.2 MB (119190672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8e22680d20768d890f881eda838a529835bedb3011f729ea618b0a0b52e551`  
		Last Modified: Sat, 07 Sep 2024 06:24:03 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2` - unknown; unknown

```console
$ docker pull bonita@sha256:edfc3656f7b107c268125fe870f4549d0c20340f959e05b302eb8708493fff68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **893.3 KB (893295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b9b74dae17713ade7c2e7dca3597a9ffccee0628f2ac60b0c1558df72740ab`

```dockerfile
```

-	Layers:
	-	`sha256:4d309829034faf9e9ecba6b97a5773829a09497eacaea869076f563bbf256a63`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 870.2 KB (870186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34356e6e0b4105a93ed8533ea1cf661e635d009c8bd5e91ed73b0b90bcb31dab`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 23.1 KB (23109 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2022.2-u0`

```console
$ docker pull bonita@sha256:c39374fcee35ae6c280b3598b22a6a78ad1859255a063d15f52fbc2d5cd4710a
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
$ docker pull bonita@sha256:49fdb0a389ab9a73c82559421885e4417dc67c4e598886e2494ef7dca85549ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185591682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b47cfe98d547bc9492ded96bbf2a60244ede36fa4cbc68f5e2a03586aa56e2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1704e491511327dfa650b4d444b58317f3a0fe58e67c69a6c8976449dd921589`  
		Last Modified: Tue, 12 Nov 2024 02:50:04 GMT  
		Size: 62.8 MB (62767436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0432548f58c3d18ac7cc84193809872251f712ee9600ba6a762e09a7b80f2ff`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d0d960091949bf5ce0cb770766860ec8d3ed66c1fe44e26e638375881183c7`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc31aeed985564402f610e37e3cb6e340379078271cf49947cfab01e7958a1`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1df8a28c973f9c080855cf95bb4e9167a6abff01debb4ea3ce0cb13a13ff219`  
		Last Modified: Tue, 12 Nov 2024 02:50:04 GMT  
		Size: 3.0 KB (2996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024f83debc31564976436c87274625b455cb0de6c38fd50cd0cb5b3db68c199f`  
		Last Modified: Tue, 12 Nov 2024 02:50:06 GMT  
		Size: 119.2 MB (119190759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f927a37aed79931b2ab2a1b07262b98bf430d7db137b6c9011ca38762f74cab6`  
		Last Modified: Tue, 12 Nov 2024 02:50:04 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:cfbff6470515c966d24a9c734ee287e2bde573c68bda1c0ba203f7429e4364c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **923.1 KB (923054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9e14354a23b9eb55f842bb6ffe6920775f36f31412773d578b561aa72cf271`

```dockerfile
```

-	Layers:
	-	`sha256:1b6f7db153fd74bb2d7bf1793ed88b2791ea3e30adae5d5d2ddc939b3e598ad9`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 899.8 KB (899782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dff381108e8f83d7e8123edb6a42f1233705c8fd8b50c29f9423d2d4863e5cf`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 23.3 KB (23272 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ce6a7a351b796e57c271376fa1fa9ef327bdcbbca7b618137bc7313c478bdcd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (185956874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f25a7077c12b4bcae58f4096445dc773a8e2d65eac16c92424867c265d0434`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4243273752f8c627f434b3051f7e45c5fa32ed3cb2318814b498fd999ce94b3d`  
		Last Modified: Sat, 07 Sep 2024 04:47:02 GMT  
		Size: 62.7 MB (62668884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88e30d06e54c9c99eef98f9dc827553050ba338c98bc364b1cae5f97c4368a3`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dc804ca99cd43313a465eac63c4ae60d837bb13473c108b1aaa195bb3cbd48`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230954cd83a5c61457aa349661e2f40cd31bad4249ad5d1fb2165a22b6fff80`  
		Last Modified: Sat, 07 Sep 2024 04:47:00 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6ef67b3171feb38b26e1148b5d5fd9de3289e777bf520407c8f967e987181c`  
		Last Modified: Sat, 07 Sep 2024 04:47:00 GMT  
		Size: 3.0 KB (2991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb2ef7c342ce6703eea1d856ee88d0b539a3c0872d0c26987ba320bd947d7d5`  
		Last Modified: Sat, 07 Sep 2024 04:47:03 GMT  
		Size: 119.2 MB (119190773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3034be95d20eb74b6f2e72890d7c3bc2f2def229cc150c15659abe63065f7f3`  
		Last Modified: Sat, 07 Sep 2024 04:47:01 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:9d999a99eb8185e9967aa74d620561d0ad63e568f0b701f9820beb877cdefed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **895.5 KB (895525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1af6383b7261a722c08531debd3dac797f4071e7eebf545bab305e7216e9606`

```dockerfile
```

-	Layers:
	-	`sha256:7f358a487a3fd110f6f5c0510c419a1f4377873933a38055c96a84f492fb2e0b`  
		Last Modified: Sat, 07 Sep 2024 04:47:00 GMT  
		Size: 872.2 KB (872162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac063d781e61113c6a1154c35eeba6d85c4256e081b944968635c66d2b5c633c`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 23.4 KB (23363 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:be4b4ad368e0d1f3908b8edfd548308c416e9016c8d81fe1234abb5d1dc305b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (181981166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f72f3a3e8e04472091c15e1ec94d8377d4d66a4a2b80ab48da3de5d149ece7`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2cf315af9480a876ed5e7efa86f52cab190a197656dcc25c561183380ba96d`  
		Last Modified: Sat, 07 Sep 2024 06:24:04 GMT  
		Size: 59.2 MB (59208493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c12032181a2e1089fca129cb6666ad1b33b69185233e9dc4cc7f69e6fb1190b`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d840c9bd89b5157b8d6f51fa118c75017552d7d26bfd8808b66f90e2f8ed76d`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a507a4e543c41bca75a33a03239a6c37f78f49709502fe2a536e0cc7e8fc5eb`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4b0d8d01b46d636da0273a5a6acb4721009c229c4de0a724cb3942b315462b`  
		Last Modified: Sat, 07 Sep 2024 06:24:03 GMT  
		Size: 3.0 KB (2996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef106ed190e76072c43f93c68593238430954d9c26a36a8c2c9539bbd477815`  
		Last Modified: Sat, 07 Sep 2024 06:24:07 GMT  
		Size: 119.2 MB (119190672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8e22680d20768d890f881eda838a529835bedb3011f729ea618b0a0b52e551`  
		Last Modified: Sat, 07 Sep 2024 06:24:03 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:edfc3656f7b107c268125fe870f4549d0c20340f959e05b302eb8708493fff68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **893.3 KB (893295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b9b74dae17713ade7c2e7dca3597a9ffccee0628f2ac60b0c1558df72740ab`

```dockerfile
```

-	Layers:
	-	`sha256:4d309829034faf9e9ecba6b97a5773829a09497eacaea869076f563bbf256a63`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 870.2 KB (870186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34356e6e0b4105a93ed8533ea1cf661e635d009c8bd5e91ed73b0b90bcb31dab`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 23.1 KB (23109 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.1`

```console
$ docker pull bonita@sha256:21d846cb32473e3749489a1eab1a7da6618dd69130bec1ed1e24b032b940e7d0
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
$ docker pull bonita@sha256:4218f6c775c448a22e4a719ff7fa6e76f46b9cd12d8a3ce860311cf3d4b3cb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184580021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3929378e50a8533d02f0c88ee3d80ee03b5a8afa2cad7ba5d2d118433e99e777`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8480ca8de26d9e0236c0a0dfdc07a1a0ac4a6845ae2038cee1445a3d119716`  
		Last Modified: Tue, 12 Nov 2024 02:22:54 GMT  
		Size: 62.8 MB (62767555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb91f6b7744c0f77c75021dfb40ae2efd89ee0087c2509ecd4fd9e450bc46cdd`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3221ab91809a0ae69a9adf0f07fea47954f10f44049151bf15ea2fc9feeb592d`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce565aee31b9d2f404981ee3af0b843bcb1dce277039831e7816f039c6315c02`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb6b1a3d83f44ddd91ee07e1d0e4a569d2493a7fd4293f1e4eb12a62bca7246`  
		Last Modified: Tue, 12 Nov 2024 02:22:54 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040ae48dfbd65a4d48bdcb7dfac9d231955040542e3d6ae87824e860d9a65d89`  
		Last Modified: Tue, 12 Nov 2024 02:22:56 GMT  
		Size: 118.2 MB (118178547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664da2a658cbc810cd8df9c23b7376f958b8b823736ae105038debcac7bc8e6b`  
		Last Modified: Tue, 12 Nov 2024 02:22:54 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1` - unknown; unknown

```console
$ docker pull bonita@sha256:84f41c2dd5dcccd82485d98fa14c7b0c74a5a6fb8ee562912b6290b414ad36f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.1 KB (914097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c620a01ab64f813436c294b33b22212d6ccf18ed3bb435e2a5d493a1b947d2`

```dockerfile
```

-	Layers:
	-	`sha256:5854d41b5b314516c97e1b037436c5d21164865759be9501d22b7e42899149d3`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 890.7 KB (890655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f16d1f9a8ae64e418c261a8be4c39bcd4eaf1684e03e131b8a3d3f07f5a5e1`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 23.4 KB (23442 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:e575d6573d607994e2820e4780593ad6123abf2a5579c998c1e0d16985642252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184945211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f72dd550eded106fc9d85a001904da63e9ce349a4a7c9ee9daa8e0e54e959e`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4243273752f8c627f434b3051f7e45c5fa32ed3cb2318814b498fd999ce94b3d`  
		Last Modified: Sat, 07 Sep 2024 04:47:02 GMT  
		Size: 62.7 MB (62668884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88e30d06e54c9c99eef98f9dc827553050ba338c98bc364b1cae5f97c4368a3`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dc804ca99cd43313a465eac63c4ae60d837bb13473c108b1aaa195bb3cbd48`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2137fd45317c976ac0019844bee4aa6c2946f47a6ae7cedc1d372ed82af00198`  
		Last Modified: Sat, 07 Sep 2024 04:47:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea56f686d5e5055bdfdd4e2ec051e635a80ca760795b50a73d4056986e3a8c90`  
		Last Modified: Sat, 07 Sep 2024 04:47:39 GMT  
		Size: 3.4 KB (3426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2384b6ea4c12cbae020fd6fb1c3f696eefccef0c0db0aefc38f7c8ad4b83d4`  
		Last Modified: Sat, 07 Sep 2024 04:47:42 GMT  
		Size: 118.2 MB (118178673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ca8621f51c14794c88c5133c049ba3d183fff7512c4893f699aaa8875cebbe`  
		Last Modified: Sat, 07 Sep 2024 04:47:39 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1` - unknown; unknown

```console
$ docker pull bonita@sha256:bb7d2067dff1e494929cb5ff1f0d7f26697694fbd85f8ef959568e08508824c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.2 KB (887204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40e7a2cf83a36b84b70266d219d2f4e6acba1c256db988d92254b326aefb505`

```dockerfile
```

-	Layers:
	-	`sha256:97d262124529a99ee6147cc27957526da7b0054c175615860313a9576cf19814`  
		Last Modified: Sat, 07 Sep 2024 04:47:39 GMT  
		Size: 863.7 KB (863671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae28becf682158e882cef4c9fcb3d56f7ffca8649339e11717828b72a3cffbf6`  
		Last Modified: Sat, 07 Sep 2024 04:47:38 GMT  
		Size: 23.5 KB (23533 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:f434b5bed8c8bb2b3a0ddcaf40273b941afd8e06f506d1fe7cf5d5d5df954550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (180969593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a4edab98af130ee0f74ba35a338289cdaf3f85ca0796a3bc28a61c3ca83232`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2cf315af9480a876ed5e7efa86f52cab190a197656dcc25c561183380ba96d`  
		Last Modified: Sat, 07 Sep 2024 06:24:04 GMT  
		Size: 59.2 MB (59208493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c12032181a2e1089fca129cb6666ad1b33b69185233e9dc4cc7f69e6fb1190b`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d840c9bd89b5157b8d6f51fa118c75017552d7d26bfd8808b66f90e2f8ed76d`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5edcc189a6b81a889c8457d0291083ad7c3560f048f63573367c297b1b30134`  
		Last Modified: Sat, 07 Sep 2024 06:24:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b82d17c34b47566a698eacd5cc51943130a5c8c4d15519d347508aa874d39fd`  
		Last Modified: Sat, 07 Sep 2024 06:24:56 GMT  
		Size: 3.4 KB (3427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f042670bbd3df056a3d76e1be9b57214b1e57df97439a8234052d07862a4dd2f`  
		Last Modified: Sat, 07 Sep 2024 06:25:00 GMT  
		Size: 118.2 MB (118178668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af827620297a61992c2beda050ec0ebafe970d58dcd40cb9b830edf95e5cb2e2`  
		Last Modified: Sat, 07 Sep 2024 06:24:56 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1` - unknown; unknown

```console
$ docker pull bonita@sha256:5e8695ae543a280bfef7dfcb81a4b65f52d6b489edefa9d9de88d0cb9d6d899c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **885.0 KB (884974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e242be6721b5e730019952d803b6aeff57a97680dbd9973c84e2b50c626b363`

```dockerfile
```

-	Layers:
	-	`sha256:0ff466f00f28dce06eb6c84e0e28ebefc1d008244b72361a3b2f88c7bd25ffaf`  
		Last Modified: Sat, 07 Sep 2024 06:24:56 GMT  
		Size: 861.7 KB (861695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0983eda33e9725b8a924260ac2e9ccb3fa36d92236d01fa6fbc1f6019f9c4e`  
		Last Modified: Sat, 07 Sep 2024 06:24:55 GMT  
		Size: 23.3 KB (23279 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.1-u0`

```console
$ docker pull bonita@sha256:21d846cb32473e3749489a1eab1a7da6618dd69130bec1ed1e24b032b940e7d0
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
$ docker pull bonita@sha256:4218f6c775c448a22e4a719ff7fa6e76f46b9cd12d8a3ce860311cf3d4b3cb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184580021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3929378e50a8533d02f0c88ee3d80ee03b5a8afa2cad7ba5d2d118433e99e777`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8480ca8de26d9e0236c0a0dfdc07a1a0ac4a6845ae2038cee1445a3d119716`  
		Last Modified: Tue, 12 Nov 2024 02:22:54 GMT  
		Size: 62.8 MB (62767555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb91f6b7744c0f77c75021dfb40ae2efd89ee0087c2509ecd4fd9e450bc46cdd`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3221ab91809a0ae69a9adf0f07fea47954f10f44049151bf15ea2fc9feeb592d`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce565aee31b9d2f404981ee3af0b843bcb1dce277039831e7816f039c6315c02`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb6b1a3d83f44ddd91ee07e1d0e4a569d2493a7fd4293f1e4eb12a62bca7246`  
		Last Modified: Tue, 12 Nov 2024 02:22:54 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040ae48dfbd65a4d48bdcb7dfac9d231955040542e3d6ae87824e860d9a65d89`  
		Last Modified: Tue, 12 Nov 2024 02:22:56 GMT  
		Size: 118.2 MB (118178547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664da2a658cbc810cd8df9c23b7376f958b8b823736ae105038debcac7bc8e6b`  
		Last Modified: Tue, 12 Nov 2024 02:22:54 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:84f41c2dd5dcccd82485d98fa14c7b0c74a5a6fb8ee562912b6290b414ad36f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.1 KB (914097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c620a01ab64f813436c294b33b22212d6ccf18ed3bb435e2a5d493a1b947d2`

```dockerfile
```

-	Layers:
	-	`sha256:5854d41b5b314516c97e1b037436c5d21164865759be9501d22b7e42899149d3`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 890.7 KB (890655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f16d1f9a8ae64e418c261a8be4c39bcd4eaf1684e03e131b8a3d3f07f5a5e1`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 23.4 KB (23442 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:e575d6573d607994e2820e4780593ad6123abf2a5579c998c1e0d16985642252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184945211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f72dd550eded106fc9d85a001904da63e9ce349a4a7c9ee9daa8e0e54e959e`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4243273752f8c627f434b3051f7e45c5fa32ed3cb2318814b498fd999ce94b3d`  
		Last Modified: Sat, 07 Sep 2024 04:47:02 GMT  
		Size: 62.7 MB (62668884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88e30d06e54c9c99eef98f9dc827553050ba338c98bc364b1cae5f97c4368a3`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dc804ca99cd43313a465eac63c4ae60d837bb13473c108b1aaa195bb3cbd48`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2137fd45317c976ac0019844bee4aa6c2946f47a6ae7cedc1d372ed82af00198`  
		Last Modified: Sat, 07 Sep 2024 04:47:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea56f686d5e5055bdfdd4e2ec051e635a80ca760795b50a73d4056986e3a8c90`  
		Last Modified: Sat, 07 Sep 2024 04:47:39 GMT  
		Size: 3.4 KB (3426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2384b6ea4c12cbae020fd6fb1c3f696eefccef0c0db0aefc38f7c8ad4b83d4`  
		Last Modified: Sat, 07 Sep 2024 04:47:42 GMT  
		Size: 118.2 MB (118178673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ca8621f51c14794c88c5133c049ba3d183fff7512c4893f699aaa8875cebbe`  
		Last Modified: Sat, 07 Sep 2024 04:47:39 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:bb7d2067dff1e494929cb5ff1f0d7f26697694fbd85f8ef959568e08508824c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.2 KB (887204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40e7a2cf83a36b84b70266d219d2f4e6acba1c256db988d92254b326aefb505`

```dockerfile
```

-	Layers:
	-	`sha256:97d262124529a99ee6147cc27957526da7b0054c175615860313a9576cf19814`  
		Last Modified: Sat, 07 Sep 2024 04:47:39 GMT  
		Size: 863.7 KB (863671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae28becf682158e882cef4c9fcb3d56f7ffca8649339e11717828b72a3cffbf6`  
		Last Modified: Sat, 07 Sep 2024 04:47:38 GMT  
		Size: 23.5 KB (23533 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:f434b5bed8c8bb2b3a0ddcaf40273b941afd8e06f506d1fe7cf5d5d5df954550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (180969593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a4edab98af130ee0f74ba35a338289cdaf3f85ca0796a3bc28a61c3ca83232`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2cf315af9480a876ed5e7efa86f52cab190a197656dcc25c561183380ba96d`  
		Last Modified: Sat, 07 Sep 2024 06:24:04 GMT  
		Size: 59.2 MB (59208493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c12032181a2e1089fca129cb6666ad1b33b69185233e9dc4cc7f69e6fb1190b`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d840c9bd89b5157b8d6f51fa118c75017552d7d26bfd8808b66f90e2f8ed76d`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5edcc189a6b81a889c8457d0291083ad7c3560f048f63573367c297b1b30134`  
		Last Modified: Sat, 07 Sep 2024 06:24:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b82d17c34b47566a698eacd5cc51943130a5c8c4d15519d347508aa874d39fd`  
		Last Modified: Sat, 07 Sep 2024 06:24:56 GMT  
		Size: 3.4 KB (3427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f042670bbd3df056a3d76e1be9b57214b1e57df97439a8234052d07862a4dd2f`  
		Last Modified: Sat, 07 Sep 2024 06:25:00 GMT  
		Size: 118.2 MB (118178668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af827620297a61992c2beda050ec0ebafe970d58dcd40cb9b830edf95e5cb2e2`  
		Last Modified: Sat, 07 Sep 2024 06:24:56 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:5e8695ae543a280bfef7dfcb81a4b65f52d6b489edefa9d9de88d0cb9d6d899c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **885.0 KB (884974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e242be6721b5e730019952d803b6aeff57a97680dbd9973c84e2b50c626b363`

```dockerfile
```

-	Layers:
	-	`sha256:0ff466f00f28dce06eb6c84e0e28ebefc1d008244b72361a3b2f88c7bd25ffaf`  
		Last Modified: Sat, 07 Sep 2024 06:24:56 GMT  
		Size: 861.7 KB (861695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0983eda33e9725b8a924260ac2e9ccb3fa36d92236d01fa6fbc1f6019f9c4e`  
		Last Modified: Sat, 07 Sep 2024 06:24:55 GMT  
		Size: 23.3 KB (23279 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.2`

```console
$ docker pull bonita@sha256:3c1ddc72d5cbd274a6a10f1bb3a2fcdbacb974a757f154d5d7c709fd63298dc7
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
$ docker pull bonita@sha256:e79d0e07f10d65b6c5afa60db71d6142797f8564c93ada1ac0bfb9d84f0091e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192422764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9090d91fecc4fb60ec7d5a2268c24ff7d738d790bea83f86fc1a65616302c838`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e27d58aa5cd08a4ec3e14a5ff49a2c43068a2cd245ad147b57681612c84a0f`  
		Last Modified: Tue, 12 Nov 2024 02:49:58 GMT  
		Size: 68.6 MB (68614920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38090d45759a229c46c3322750b3715136d7e209dc2032d5f49408c09d81bbd1`  
		Last Modified: Tue, 12 Nov 2024 02:49:55 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968b5fdc62e2d5049c7976e53a54a0be5a190c237cc49ec2cde7656a6cb59d2e`  
		Last Modified: Tue, 12 Nov 2024 02:49:55 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598e25779fa9888d6193e4ce0cfd9d06354f36d624f5ff68e3f7fb87327475e2`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed5de122744e77b9cff6d039ce1876b40d55901b686b3467a8982d70979edeb`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6cdf2f734f0ec95ca18276b15eec6f8756b60d3cbf504fd317f7261b911475`  
		Last Modified: Tue, 12 Nov 2024 02:50:00 GMT  
		Size: 120.2 MB (120173512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a939d4d0f69f322d82d823c5d7fcf20967dbc988c7b4a79ee342cb599158e38`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 5.6 KB (5622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2` - unknown; unknown

```console
$ docker pull bonita@sha256:48caca26479d0fae9ca12749ef8c57137fa226405270f15a0b8e74e86d1a1d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1373746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb704fdc806ef784534f939b0fffb69f8fc98efb37cd25fe57dda163997898e`

```dockerfile
```

-	Layers:
	-	`sha256:e5044644322f8642c778a9c4b26ae0e2320e333c7ad737ae1ecf3a159856bbd9`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 1.4 MB (1350824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6006bb11389c0831b0c0b525d446ae8097fe627752fbdf849b47193023524f8`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 22.9 KB (22922 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:422bb84dcf94e6a7516e8d97408b479467bb832f801b3171fa44dacbb6b0c32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192802123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7634fee5ecb3b942eb44c54ff13688c5e89b2c6cd7a199c52da621e843f21531`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad1e704a6d1fa12e395283d70a5a0133c73fb678ba3b6c3b26a0cce86cfdfcb`  
		Last Modified: Sat, 07 Sep 2024 04:48:27 GMT  
		Size: 68.5 MB (68530559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe9acc59d4cf3efd7f5465867e8c264e1d9de2935b0524a813c055dcad33beb`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52467723c8400eeaa5a5f3e7df7cbc848e536800e4d3affa0cefee1147eb720b`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f321b22501c11d3c6dd56ca5c0f0760d0215e03eaf0827a21e7099a3107c534d`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952fe924ab1d38d4e5dac8fe880951043a138c1908ca7daefc6bfffb9a58535f`  
		Last Modified: Sat, 07 Sep 2024 04:48:26 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f5fed370a25b3b65a36ad0f4aaca5efbe152661c6a713eb38e4af4074bd070`  
		Last Modified: Sat, 07 Sep 2024 04:48:37 GMT  
		Size: 120.2 MB (120173482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3351df8a519b92043bc3588ab8056a8b9a58225249fad37e6cf14ab7a2d2f867`  
		Last Modified: Sat, 07 Sep 2024 04:48:26 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2` - unknown; unknown

```console
$ docker pull bonita@sha256:fb60570d01afa54dfd8f2e8374960df4c1ea57f4903bde3ca0ff732306c0f533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1346095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48415fe7c00bdac769d09cf30e06c500aae6802758633777cf1ea35dbab3463`

```dockerfile
```

-	Layers:
	-	`sha256:f4d7a112632cda8afdba2b3f9704712a0ee00bf85b4d4c148b0ae36d7ebaaceb`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 1.3 MB (1322772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97281fe5a393279dc74dae4ec620d8250309b33033851eb5a0d2eab130082268`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:6e9b67e96f29d035ddda75ae03c26127a50491d8558aefa7e0648e1f7b029711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189106331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03ad934a10a7f7a1479fcbb3cca95ea4ea997744f1e76da3a6690a6965ac0e9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d642177801827d23412d87d9ce2ceb38ffc4f576892db6d80d73f47ab93168f`  
		Last Modified: Sat, 07 Sep 2024 06:26:03 GMT  
		Size: 65.3 MB (65349946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13426edafdec3f9f8f632cdf1ab7e66b60fccd7355cae13e871493d92a7dcd6b`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9f0bb8319101cf60f7619cb1f4995b8d759be58499701cfb994c36c7aaea96`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497a80e5560abd7b0d41d1b2a03dba788982763fe0c3c07d20a27c5983e15ca9`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77a3274adfcc8bc769e3e413c54716c00b144297f989c7a148a54e2fc003fd5`  
		Last Modified: Sat, 07 Sep 2024 06:26:01 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b76bea0cd8f5e78b919bc340ede75b86eac26c3a85099af7715926f5fbeadba`  
		Last Modified: Sat, 07 Sep 2024 06:26:04 GMT  
		Size: 120.2 MB (120173533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e447752d63defbff6acd3c212ab510a50a57928c1e28d6d925abc22581cb592`  
		Last Modified: Sat, 07 Sep 2024 06:26:01 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2` - unknown; unknown

```console
$ docker pull bonita@sha256:b3b52de39c11fbb0b8b29086bde32211f9ff11b35e3cfa927025eb0ec4417b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1343853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80e06364c0d133e553d85737961c89aa9519f2861708e2ba1ced9b3890fcf6b`

```dockerfile
```

-	Layers:
	-	`sha256:8a2685fceb979d9d9fd8df85b7212754abfa3051695ed0fe4e7a85951f4785b4`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 1.3 MB (1320790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4fd1220f2d92555b5c954d1145f036b1570960e5ba3f32ecc5285079a48d984`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 23.1 KB (23063 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.2-u0`

```console
$ docker pull bonita@sha256:3c1ddc72d5cbd274a6a10f1bb3a2fcdbacb974a757f154d5d7c709fd63298dc7
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
$ docker pull bonita@sha256:e79d0e07f10d65b6c5afa60db71d6142797f8564c93ada1ac0bfb9d84f0091e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192422764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9090d91fecc4fb60ec7d5a2268c24ff7d738d790bea83f86fc1a65616302c838`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e27d58aa5cd08a4ec3e14a5ff49a2c43068a2cd245ad147b57681612c84a0f`  
		Last Modified: Tue, 12 Nov 2024 02:49:58 GMT  
		Size: 68.6 MB (68614920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38090d45759a229c46c3322750b3715136d7e209dc2032d5f49408c09d81bbd1`  
		Last Modified: Tue, 12 Nov 2024 02:49:55 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968b5fdc62e2d5049c7976e53a54a0be5a190c237cc49ec2cde7656a6cb59d2e`  
		Last Modified: Tue, 12 Nov 2024 02:49:55 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598e25779fa9888d6193e4ce0cfd9d06354f36d624f5ff68e3f7fb87327475e2`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed5de122744e77b9cff6d039ce1876b40d55901b686b3467a8982d70979edeb`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6cdf2f734f0ec95ca18276b15eec6f8756b60d3cbf504fd317f7261b911475`  
		Last Modified: Tue, 12 Nov 2024 02:50:00 GMT  
		Size: 120.2 MB (120173512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a939d4d0f69f322d82d823c5d7fcf20967dbc988c7b4a79ee342cb599158e38`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 5.6 KB (5622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:48caca26479d0fae9ca12749ef8c57137fa226405270f15a0b8e74e86d1a1d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1373746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb704fdc806ef784534f939b0fffb69f8fc98efb37cd25fe57dda163997898e`

```dockerfile
```

-	Layers:
	-	`sha256:e5044644322f8642c778a9c4b26ae0e2320e333c7ad737ae1ecf3a159856bbd9`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 1.4 MB (1350824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6006bb11389c0831b0c0b525d446ae8097fe627752fbdf849b47193023524f8`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 22.9 KB (22922 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:422bb84dcf94e6a7516e8d97408b479467bb832f801b3171fa44dacbb6b0c32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192802123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7634fee5ecb3b942eb44c54ff13688c5e89b2c6cd7a199c52da621e843f21531`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad1e704a6d1fa12e395283d70a5a0133c73fb678ba3b6c3b26a0cce86cfdfcb`  
		Last Modified: Sat, 07 Sep 2024 04:48:27 GMT  
		Size: 68.5 MB (68530559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe9acc59d4cf3efd7f5465867e8c264e1d9de2935b0524a813c055dcad33beb`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52467723c8400eeaa5a5f3e7df7cbc848e536800e4d3affa0cefee1147eb720b`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f321b22501c11d3c6dd56ca5c0f0760d0215e03eaf0827a21e7099a3107c534d`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952fe924ab1d38d4e5dac8fe880951043a138c1908ca7daefc6bfffb9a58535f`  
		Last Modified: Sat, 07 Sep 2024 04:48:26 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f5fed370a25b3b65a36ad0f4aaca5efbe152661c6a713eb38e4af4074bd070`  
		Last Modified: Sat, 07 Sep 2024 04:48:37 GMT  
		Size: 120.2 MB (120173482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3351df8a519b92043bc3588ab8056a8b9a58225249fad37e6cf14ab7a2d2f867`  
		Last Modified: Sat, 07 Sep 2024 04:48:26 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:fb60570d01afa54dfd8f2e8374960df4c1ea57f4903bde3ca0ff732306c0f533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1346095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48415fe7c00bdac769d09cf30e06c500aae6802758633777cf1ea35dbab3463`

```dockerfile
```

-	Layers:
	-	`sha256:f4d7a112632cda8afdba2b3f9704712a0ee00bf85b4d4c148b0ae36d7ebaaceb`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 1.3 MB (1322772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97281fe5a393279dc74dae4ec620d8250309b33033851eb5a0d2eab130082268`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:6e9b67e96f29d035ddda75ae03c26127a50491d8558aefa7e0648e1f7b029711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189106331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03ad934a10a7f7a1479fcbb3cca95ea4ea997744f1e76da3a6690a6965ac0e9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d642177801827d23412d87d9ce2ceb38ffc4f576892db6d80d73f47ab93168f`  
		Last Modified: Sat, 07 Sep 2024 06:26:03 GMT  
		Size: 65.3 MB (65349946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13426edafdec3f9f8f632cdf1ab7e66b60fccd7355cae13e871493d92a7dcd6b`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9f0bb8319101cf60f7619cb1f4995b8d759be58499701cfb994c36c7aaea96`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497a80e5560abd7b0d41d1b2a03dba788982763fe0c3c07d20a27c5983e15ca9`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77a3274adfcc8bc769e3e413c54716c00b144297f989c7a148a54e2fc003fd5`  
		Last Modified: Sat, 07 Sep 2024 06:26:01 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b76bea0cd8f5e78b919bc340ede75b86eac26c3a85099af7715926f5fbeadba`  
		Last Modified: Sat, 07 Sep 2024 06:26:04 GMT  
		Size: 120.2 MB (120173533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e447752d63defbff6acd3c212ab510a50a57928c1e28d6d925abc22581cb592`  
		Last Modified: Sat, 07 Sep 2024 06:26:01 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:b3b52de39c11fbb0b8b29086bde32211f9ff11b35e3cfa927025eb0ec4417b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1343853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80e06364c0d133e553d85737961c89aa9519f2861708e2ba1ced9b3890fcf6b`

```dockerfile
```

-	Layers:
	-	`sha256:8a2685fceb979d9d9fd8df85b7212754abfa3051695ed0fe4e7a85951f4785b4`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 1.3 MB (1320790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4fd1220f2d92555b5c954d1145f036b1570960e5ba3f32ecc5285079a48d984`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 23.1 KB (23063 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2024.3`

```console
$ docker pull bonita@sha256:1f7af758a6dca6bba55c28f36b75b2d79ea624e7b48390f18482160d8fa43379
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:2024.3` - linux; amd64

```console
$ docker pull bonita@sha256:aff72fdcdc1abd4b9bbad0c155d337538226d6724f0e50ced51ed4bcbf815bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189935357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8302afd6c116f16b99b8803f90d5e5d93087ce9de24a10d9ab1e9a966f9b9841`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb8a593a4b7726f83576628ca6aa70220bcdcbef9651d003ba88727ce34d9d1`  
		Last Modified: Tue, 12 Nov 2024 02:38:48 GMT  
		Size: 18.3 MB (18307356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441f37ea86bb2ebd3f2d928c64e6d4c39686f25618e8847e957fee5ff58da0e6`  
		Last Modified: Tue, 12 Nov 2024 02:38:49 GMT  
		Size: 46.6 MB (46615858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44818f47c6831f333e1b9a5947c85124e4a12ca670bea7043d4b11beeb3a780b`  
		Last Modified: Tue, 12 Nov 2024 02:38:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cfa7e9b065bacf6029c8a0af5b63bb0e86ef13e828cb645d914da3480fbbfb`  
		Last Modified: Tue, 12 Nov 2024 02:38:48 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282cd84bf85b9e16a5b15f900b8c120135cdd324c624dfefc957b15a5c8f4924`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 1.9 MB (1859693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846171241c7d276eaaa07a72711d35c5fee179900b56800d5ec0c8e937afc5ce`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8646004264a0d08ea69c6cb78588da01faa2819ff6a4a8c61e87fe36f44c75d1`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382f0c1559b8a9d44cdc48b848d6f66a19a9bbccf9eb4c68283330c9424ae256`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb4e9a3063b2241adf74732cf5eff7a4dbc4f0de557e68a18f505c33cbb22f0`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 3.7 KB (3709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b96214236cb294ae2c9d88dd27fb374b2157482e17cfaf5922a1cd7260f7d1`  
		Last Modified: Tue, 12 Nov 2024 03:11:46 GMT  
		Size: 119.5 MB (119515350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f4fcac1efe12c849b5d2ccb6c9ba54211207d66579b86cceecd00c717a268d`  
		Last Modified: Tue, 12 Nov 2024 03:11:45 GMT  
		Size: 5.9 KB (5882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2024.3` - unknown; unknown

```console
$ docker pull bonita@sha256:b6797d0a32115ece7f217354ee93f1518bd21a599ce0d3748974467c286df1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c5d4f1dc1cdfcf2877600fc4dc9290598ae9a34d569ddbbf974eae70cbb2d2`

```dockerfile
```

-	Layers:
	-	`sha256:76e80da520f48790ac44f471f6e9707006debdcc727cf18427d5cff5d4bf676a`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 1.3 MB (1265026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fff7ba6987a0718b554cbd6abdbb95082e916db7b565f8500391ff9e438de050`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2024.3-u0`

```console
$ docker pull bonita@sha256:1f7af758a6dca6bba55c28f36b75b2d79ea624e7b48390f18482160d8fa43379
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:2024.3-u0` - linux; amd64

```console
$ docker pull bonita@sha256:aff72fdcdc1abd4b9bbad0c155d337538226d6724f0e50ced51ed4bcbf815bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189935357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8302afd6c116f16b99b8803f90d5e5d93087ce9de24a10d9ab1e9a966f9b9841`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb8a593a4b7726f83576628ca6aa70220bcdcbef9651d003ba88727ce34d9d1`  
		Last Modified: Tue, 12 Nov 2024 02:38:48 GMT  
		Size: 18.3 MB (18307356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441f37ea86bb2ebd3f2d928c64e6d4c39686f25618e8847e957fee5ff58da0e6`  
		Last Modified: Tue, 12 Nov 2024 02:38:49 GMT  
		Size: 46.6 MB (46615858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44818f47c6831f333e1b9a5947c85124e4a12ca670bea7043d4b11beeb3a780b`  
		Last Modified: Tue, 12 Nov 2024 02:38:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cfa7e9b065bacf6029c8a0af5b63bb0e86ef13e828cb645d914da3480fbbfb`  
		Last Modified: Tue, 12 Nov 2024 02:38:48 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282cd84bf85b9e16a5b15f900b8c120135cdd324c624dfefc957b15a5c8f4924`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 1.9 MB (1859693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846171241c7d276eaaa07a72711d35c5fee179900b56800d5ec0c8e937afc5ce`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8646004264a0d08ea69c6cb78588da01faa2819ff6a4a8c61e87fe36f44c75d1`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382f0c1559b8a9d44cdc48b848d6f66a19a9bbccf9eb4c68283330c9424ae256`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb4e9a3063b2241adf74732cf5eff7a4dbc4f0de557e68a18f505c33cbb22f0`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 3.7 KB (3709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b96214236cb294ae2c9d88dd27fb374b2157482e17cfaf5922a1cd7260f7d1`  
		Last Modified: Tue, 12 Nov 2024 03:11:46 GMT  
		Size: 119.5 MB (119515350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f4fcac1efe12c849b5d2ccb6c9ba54211207d66579b86cceecd00c717a268d`  
		Last Modified: Tue, 12 Nov 2024 03:11:45 GMT  
		Size: 5.9 KB (5882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2024.3-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:b6797d0a32115ece7f217354ee93f1518bd21a599ce0d3748974467c286df1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c5d4f1dc1cdfcf2877600fc4dc9290598ae9a34d569ddbbf974eae70cbb2d2`

```dockerfile
```

-	Layers:
	-	`sha256:76e80da520f48790ac44f471f6e9707006debdcc727cf18427d5cff5d4bf676a`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 1.3 MB (1265026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fff7ba6987a0718b554cbd6abdbb95082e916db7b565f8500391ff9e438de050`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:7.15`

```console
$ docker pull bonita@sha256:c39374fcee35ae6c280b3598b22a6a78ad1859255a063d15f52fbc2d5cd4710a
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
$ docker pull bonita@sha256:49fdb0a389ab9a73c82559421885e4417dc67c4e598886e2494ef7dca85549ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185591682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b47cfe98d547bc9492ded96bbf2a60244ede36fa4cbc68f5e2a03586aa56e2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1704e491511327dfa650b4d444b58317f3a0fe58e67c69a6c8976449dd921589`  
		Last Modified: Tue, 12 Nov 2024 02:50:04 GMT  
		Size: 62.8 MB (62767436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0432548f58c3d18ac7cc84193809872251f712ee9600ba6a762e09a7b80f2ff`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d0d960091949bf5ce0cb770766860ec8d3ed66c1fe44e26e638375881183c7`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc31aeed985564402f610e37e3cb6e340379078271cf49947cfab01e7958a1`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1df8a28c973f9c080855cf95bb4e9167a6abff01debb4ea3ce0cb13a13ff219`  
		Last Modified: Tue, 12 Nov 2024 02:50:04 GMT  
		Size: 3.0 KB (2996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024f83debc31564976436c87274625b455cb0de6c38fd50cd0cb5b3db68c199f`  
		Last Modified: Tue, 12 Nov 2024 02:50:06 GMT  
		Size: 119.2 MB (119190759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f927a37aed79931b2ab2a1b07262b98bf430d7db137b6c9011ca38762f74cab6`  
		Last Modified: Tue, 12 Nov 2024 02:50:04 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15` - unknown; unknown

```console
$ docker pull bonita@sha256:cfbff6470515c966d24a9c734ee287e2bde573c68bda1c0ba203f7429e4364c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **923.1 KB (923054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9e14354a23b9eb55f842bb6ffe6920775f36f31412773d578b561aa72cf271`

```dockerfile
```

-	Layers:
	-	`sha256:1b6f7db153fd74bb2d7bf1793ed88b2791ea3e30adae5d5d2ddc939b3e598ad9`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 899.8 KB (899782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dff381108e8f83d7e8123edb6a42f1233705c8fd8b50c29f9423d2d4863e5cf`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 23.3 KB (23272 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.15` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ce6a7a351b796e57c271376fa1fa9ef327bdcbbca7b618137bc7313c478bdcd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (185956874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f25a7077c12b4bcae58f4096445dc773a8e2d65eac16c92424867c265d0434`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4243273752f8c627f434b3051f7e45c5fa32ed3cb2318814b498fd999ce94b3d`  
		Last Modified: Sat, 07 Sep 2024 04:47:02 GMT  
		Size: 62.7 MB (62668884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88e30d06e54c9c99eef98f9dc827553050ba338c98bc364b1cae5f97c4368a3`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dc804ca99cd43313a465eac63c4ae60d837bb13473c108b1aaa195bb3cbd48`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230954cd83a5c61457aa349661e2f40cd31bad4249ad5d1fb2165a22b6fff80`  
		Last Modified: Sat, 07 Sep 2024 04:47:00 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6ef67b3171feb38b26e1148b5d5fd9de3289e777bf520407c8f967e987181c`  
		Last Modified: Sat, 07 Sep 2024 04:47:00 GMT  
		Size: 3.0 KB (2991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb2ef7c342ce6703eea1d856ee88d0b539a3c0872d0c26987ba320bd947d7d5`  
		Last Modified: Sat, 07 Sep 2024 04:47:03 GMT  
		Size: 119.2 MB (119190773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3034be95d20eb74b6f2e72890d7c3bc2f2def229cc150c15659abe63065f7f3`  
		Last Modified: Sat, 07 Sep 2024 04:47:01 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15` - unknown; unknown

```console
$ docker pull bonita@sha256:9d999a99eb8185e9967aa74d620561d0ad63e568f0b701f9820beb877cdefed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **895.5 KB (895525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1af6383b7261a722c08531debd3dac797f4071e7eebf545bab305e7216e9606`

```dockerfile
```

-	Layers:
	-	`sha256:7f358a487a3fd110f6f5c0510c419a1f4377873933a38055c96a84f492fb2e0b`  
		Last Modified: Sat, 07 Sep 2024 04:47:00 GMT  
		Size: 872.2 KB (872162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac063d781e61113c6a1154c35eeba6d85c4256e081b944968635c66d2b5c633c`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 23.4 KB (23363 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.15` - linux; ppc64le

```console
$ docker pull bonita@sha256:be4b4ad368e0d1f3908b8edfd548308c416e9016c8d81fe1234abb5d1dc305b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (181981166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f72f3a3e8e04472091c15e1ec94d8377d4d66a4a2b80ab48da3de5d149ece7`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2cf315af9480a876ed5e7efa86f52cab190a197656dcc25c561183380ba96d`  
		Last Modified: Sat, 07 Sep 2024 06:24:04 GMT  
		Size: 59.2 MB (59208493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c12032181a2e1089fca129cb6666ad1b33b69185233e9dc4cc7f69e6fb1190b`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d840c9bd89b5157b8d6f51fa118c75017552d7d26bfd8808b66f90e2f8ed76d`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a507a4e543c41bca75a33a03239a6c37f78f49709502fe2a536e0cc7e8fc5eb`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4b0d8d01b46d636da0273a5a6acb4721009c229c4de0a724cb3942b315462b`  
		Last Modified: Sat, 07 Sep 2024 06:24:03 GMT  
		Size: 3.0 KB (2996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef106ed190e76072c43f93c68593238430954d9c26a36a8c2c9539bbd477815`  
		Last Modified: Sat, 07 Sep 2024 06:24:07 GMT  
		Size: 119.2 MB (119190672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8e22680d20768d890f881eda838a529835bedb3011f729ea618b0a0b52e551`  
		Last Modified: Sat, 07 Sep 2024 06:24:03 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15` - unknown; unknown

```console
$ docker pull bonita@sha256:edfc3656f7b107c268125fe870f4549d0c20340f959e05b302eb8708493fff68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **893.3 KB (893295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b9b74dae17713ade7c2e7dca3597a9ffccee0628f2ac60b0c1558df72740ab`

```dockerfile
```

-	Layers:
	-	`sha256:4d309829034faf9e9ecba6b97a5773829a09497eacaea869076f563bbf256a63`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 870.2 KB (870186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34356e6e0b4105a93ed8533ea1cf661e635d009c8bd5e91ed73b0b90bcb31dab`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 23.1 KB (23109 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:7.15.0`

```console
$ docker pull bonita@sha256:c39374fcee35ae6c280b3598b22a6a78ad1859255a063d15f52fbc2d5cd4710a
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
$ docker pull bonita@sha256:49fdb0a389ab9a73c82559421885e4417dc67c4e598886e2494ef7dca85549ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185591682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b47cfe98d547bc9492ded96bbf2a60244ede36fa4cbc68f5e2a03586aa56e2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1704e491511327dfa650b4d444b58317f3a0fe58e67c69a6c8976449dd921589`  
		Last Modified: Tue, 12 Nov 2024 02:50:04 GMT  
		Size: 62.8 MB (62767436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0432548f58c3d18ac7cc84193809872251f712ee9600ba6a762e09a7b80f2ff`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d0d960091949bf5ce0cb770766860ec8d3ed66c1fe44e26e638375881183c7`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dc31aeed985564402f610e37e3cb6e340379078271cf49947cfab01e7958a1`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1df8a28c973f9c080855cf95bb4e9167a6abff01debb4ea3ce0cb13a13ff219`  
		Last Modified: Tue, 12 Nov 2024 02:50:04 GMT  
		Size: 3.0 KB (2996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024f83debc31564976436c87274625b455cb0de6c38fd50cd0cb5b3db68c199f`  
		Last Modified: Tue, 12 Nov 2024 02:50:06 GMT  
		Size: 119.2 MB (119190759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f927a37aed79931b2ab2a1b07262b98bf430d7db137b6c9011ca38762f74cab6`  
		Last Modified: Tue, 12 Nov 2024 02:50:04 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15.0` - unknown; unknown

```console
$ docker pull bonita@sha256:cfbff6470515c966d24a9c734ee287e2bde573c68bda1c0ba203f7429e4364c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **923.1 KB (923054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9e14354a23b9eb55f842bb6ffe6920775f36f31412773d578b561aa72cf271`

```dockerfile
```

-	Layers:
	-	`sha256:1b6f7db153fd74bb2d7bf1793ed88b2791ea3e30adae5d5d2ddc939b3e598ad9`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 899.8 KB (899782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dff381108e8f83d7e8123edb6a42f1233705c8fd8b50c29f9423d2d4863e5cf`  
		Last Modified: Tue, 12 Nov 2024 02:50:03 GMT  
		Size: 23.3 KB (23272 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.15.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ce6a7a351b796e57c271376fa1fa9ef327bdcbbca7b618137bc7313c478bdcd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (185956874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f25a7077c12b4bcae58f4096445dc773a8e2d65eac16c92424867c265d0434`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4243273752f8c627f434b3051f7e45c5fa32ed3cb2318814b498fd999ce94b3d`  
		Last Modified: Sat, 07 Sep 2024 04:47:02 GMT  
		Size: 62.7 MB (62668884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88e30d06e54c9c99eef98f9dc827553050ba338c98bc364b1cae5f97c4368a3`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dc804ca99cd43313a465eac63c4ae60d837bb13473c108b1aaa195bb3cbd48`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f230954cd83a5c61457aa349661e2f40cd31bad4249ad5d1fb2165a22b6fff80`  
		Last Modified: Sat, 07 Sep 2024 04:47:00 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6ef67b3171feb38b26e1148b5d5fd9de3289e777bf520407c8f967e987181c`  
		Last Modified: Sat, 07 Sep 2024 04:47:00 GMT  
		Size: 3.0 KB (2991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb2ef7c342ce6703eea1d856ee88d0b539a3c0872d0c26987ba320bd947d7d5`  
		Last Modified: Sat, 07 Sep 2024 04:47:03 GMT  
		Size: 119.2 MB (119190773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3034be95d20eb74b6f2e72890d7c3bc2f2def229cc150c15659abe63065f7f3`  
		Last Modified: Sat, 07 Sep 2024 04:47:01 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15.0` - unknown; unknown

```console
$ docker pull bonita@sha256:9d999a99eb8185e9967aa74d620561d0ad63e568f0b701f9820beb877cdefed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **895.5 KB (895525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1af6383b7261a722c08531debd3dac797f4071e7eebf545bab305e7216e9606`

```dockerfile
```

-	Layers:
	-	`sha256:7f358a487a3fd110f6f5c0510c419a1f4377873933a38055c96a84f492fb2e0b`  
		Last Modified: Sat, 07 Sep 2024 04:47:00 GMT  
		Size: 872.2 KB (872162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac063d781e61113c6a1154c35eeba6d85c4256e081b944968635c66d2b5c633c`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 23.4 KB (23363 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.15.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:be4b4ad368e0d1f3908b8edfd548308c416e9016c8d81fe1234abb5d1dc305b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (181981166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f72f3a3e8e04472091c15e1ec94d8377d4d66a4a2b80ab48da3de5d149ece7`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2cf315af9480a876ed5e7efa86f52cab190a197656dcc25c561183380ba96d`  
		Last Modified: Sat, 07 Sep 2024 06:24:04 GMT  
		Size: 59.2 MB (59208493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c12032181a2e1089fca129cb6666ad1b33b69185233e9dc4cc7f69e6fb1190b`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d840c9bd89b5157b8d6f51fa118c75017552d7d26bfd8808b66f90e2f8ed76d`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a507a4e543c41bca75a33a03239a6c37f78f49709502fe2a536e0cc7e8fc5eb`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4b0d8d01b46d636da0273a5a6acb4721009c229c4de0a724cb3942b315462b`  
		Last Modified: Sat, 07 Sep 2024 06:24:03 GMT  
		Size: 3.0 KB (2996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef106ed190e76072c43f93c68593238430954d9c26a36a8c2c9539bbd477815`  
		Last Modified: Sat, 07 Sep 2024 06:24:07 GMT  
		Size: 119.2 MB (119190672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8e22680d20768d890f881eda838a529835bedb3011f729ea618b0a0b52e551`  
		Last Modified: Sat, 07 Sep 2024 06:24:03 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15.0` - unknown; unknown

```console
$ docker pull bonita@sha256:edfc3656f7b107c268125fe870f4549d0c20340f959e05b302eb8708493fff68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **893.3 KB (893295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b9b74dae17713ade7c2e7dca3597a9ffccee0628f2ac60b0c1558df72740ab`

```dockerfile
```

-	Layers:
	-	`sha256:4d309829034faf9e9ecba6b97a5773829a09497eacaea869076f563bbf256a63`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 870.2 KB (870186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34356e6e0b4105a93ed8533ea1cf661e635d009c8bd5e91ed73b0b90bcb31dab`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 23.1 KB (23109 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:8.0`

```console
$ docker pull bonita@sha256:21d846cb32473e3749489a1eab1a7da6618dd69130bec1ed1e24b032b940e7d0
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
$ docker pull bonita@sha256:4218f6c775c448a22e4a719ff7fa6e76f46b9cd12d8a3ce860311cf3d4b3cb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184580021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3929378e50a8533d02f0c88ee3d80ee03b5a8afa2cad7ba5d2d118433e99e777`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8480ca8de26d9e0236c0a0dfdc07a1a0ac4a6845ae2038cee1445a3d119716`  
		Last Modified: Tue, 12 Nov 2024 02:22:54 GMT  
		Size: 62.8 MB (62767555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb91f6b7744c0f77c75021dfb40ae2efd89ee0087c2509ecd4fd9e450bc46cdd`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3221ab91809a0ae69a9adf0f07fea47954f10f44049151bf15ea2fc9feeb592d`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce565aee31b9d2f404981ee3af0b843bcb1dce277039831e7816f039c6315c02`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb6b1a3d83f44ddd91ee07e1d0e4a569d2493a7fd4293f1e4eb12a62bca7246`  
		Last Modified: Tue, 12 Nov 2024 02:22:54 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040ae48dfbd65a4d48bdcb7dfac9d231955040542e3d6ae87824e860d9a65d89`  
		Last Modified: Tue, 12 Nov 2024 02:22:56 GMT  
		Size: 118.2 MB (118178547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664da2a658cbc810cd8df9c23b7376f958b8b823736ae105038debcac7bc8e6b`  
		Last Modified: Tue, 12 Nov 2024 02:22:54 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0` - unknown; unknown

```console
$ docker pull bonita@sha256:84f41c2dd5dcccd82485d98fa14c7b0c74a5a6fb8ee562912b6290b414ad36f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.1 KB (914097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c620a01ab64f813436c294b33b22212d6ccf18ed3bb435e2a5d493a1b947d2`

```dockerfile
```

-	Layers:
	-	`sha256:5854d41b5b314516c97e1b037436c5d21164865759be9501d22b7e42899149d3`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 890.7 KB (890655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f16d1f9a8ae64e418c261a8be4c39bcd4eaf1684e03e131b8a3d3f07f5a5e1`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 23.4 KB (23442 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:8.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:e575d6573d607994e2820e4780593ad6123abf2a5579c998c1e0d16985642252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184945211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f72dd550eded106fc9d85a001904da63e9ce349a4a7c9ee9daa8e0e54e959e`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4243273752f8c627f434b3051f7e45c5fa32ed3cb2318814b498fd999ce94b3d`  
		Last Modified: Sat, 07 Sep 2024 04:47:02 GMT  
		Size: 62.7 MB (62668884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88e30d06e54c9c99eef98f9dc827553050ba338c98bc364b1cae5f97c4368a3`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dc804ca99cd43313a465eac63c4ae60d837bb13473c108b1aaa195bb3cbd48`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2137fd45317c976ac0019844bee4aa6c2946f47a6ae7cedc1d372ed82af00198`  
		Last Modified: Sat, 07 Sep 2024 04:47:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea56f686d5e5055bdfdd4e2ec051e635a80ca760795b50a73d4056986e3a8c90`  
		Last Modified: Sat, 07 Sep 2024 04:47:39 GMT  
		Size: 3.4 KB (3426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2384b6ea4c12cbae020fd6fb1c3f696eefccef0c0db0aefc38f7c8ad4b83d4`  
		Last Modified: Sat, 07 Sep 2024 04:47:42 GMT  
		Size: 118.2 MB (118178673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ca8621f51c14794c88c5133c049ba3d183fff7512c4893f699aaa8875cebbe`  
		Last Modified: Sat, 07 Sep 2024 04:47:39 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0` - unknown; unknown

```console
$ docker pull bonita@sha256:bb7d2067dff1e494929cb5ff1f0d7f26697694fbd85f8ef959568e08508824c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.2 KB (887204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40e7a2cf83a36b84b70266d219d2f4e6acba1c256db988d92254b326aefb505`

```dockerfile
```

-	Layers:
	-	`sha256:97d262124529a99ee6147cc27957526da7b0054c175615860313a9576cf19814`  
		Last Modified: Sat, 07 Sep 2024 04:47:39 GMT  
		Size: 863.7 KB (863671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae28becf682158e882cef4c9fcb3d56f7ffca8649339e11717828b72a3cffbf6`  
		Last Modified: Sat, 07 Sep 2024 04:47:38 GMT  
		Size: 23.5 KB (23533 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:8.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:f434b5bed8c8bb2b3a0ddcaf40273b941afd8e06f506d1fe7cf5d5d5df954550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (180969593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a4edab98af130ee0f74ba35a338289cdaf3f85ca0796a3bc28a61c3ca83232`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2cf315af9480a876ed5e7efa86f52cab190a197656dcc25c561183380ba96d`  
		Last Modified: Sat, 07 Sep 2024 06:24:04 GMT  
		Size: 59.2 MB (59208493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c12032181a2e1089fca129cb6666ad1b33b69185233e9dc4cc7f69e6fb1190b`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d840c9bd89b5157b8d6f51fa118c75017552d7d26bfd8808b66f90e2f8ed76d`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5edcc189a6b81a889c8457d0291083ad7c3560f048f63573367c297b1b30134`  
		Last Modified: Sat, 07 Sep 2024 06:24:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b82d17c34b47566a698eacd5cc51943130a5c8c4d15519d347508aa874d39fd`  
		Last Modified: Sat, 07 Sep 2024 06:24:56 GMT  
		Size: 3.4 KB (3427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f042670bbd3df056a3d76e1be9b57214b1e57df97439a8234052d07862a4dd2f`  
		Last Modified: Sat, 07 Sep 2024 06:25:00 GMT  
		Size: 118.2 MB (118178668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af827620297a61992c2beda050ec0ebafe970d58dcd40cb9b830edf95e5cb2e2`  
		Last Modified: Sat, 07 Sep 2024 06:24:56 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0` - unknown; unknown

```console
$ docker pull bonita@sha256:5e8695ae543a280bfef7dfcb81a4b65f52d6b489edefa9d9de88d0cb9d6d899c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **885.0 KB (884974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e242be6721b5e730019952d803b6aeff57a97680dbd9973c84e2b50c626b363`

```dockerfile
```

-	Layers:
	-	`sha256:0ff466f00f28dce06eb6c84e0e28ebefc1d008244b72361a3b2f88c7bd25ffaf`  
		Last Modified: Sat, 07 Sep 2024 06:24:56 GMT  
		Size: 861.7 KB (861695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0983eda33e9725b8a924260ac2e9ccb3fa36d92236d01fa6fbc1f6019f9c4e`  
		Last Modified: Sat, 07 Sep 2024 06:24:55 GMT  
		Size: 23.3 KB (23279 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:8.0.0`

```console
$ docker pull bonita@sha256:21d846cb32473e3749489a1eab1a7da6618dd69130bec1ed1e24b032b940e7d0
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
$ docker pull bonita@sha256:4218f6c775c448a22e4a719ff7fa6e76f46b9cd12d8a3ce860311cf3d4b3cb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184580021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3929378e50a8533d02f0c88ee3d80ee03b5a8afa2cad7ba5d2d118433e99e777`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8480ca8de26d9e0236c0a0dfdc07a1a0ac4a6845ae2038cee1445a3d119716`  
		Last Modified: Tue, 12 Nov 2024 02:22:54 GMT  
		Size: 62.8 MB (62767555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb91f6b7744c0f77c75021dfb40ae2efd89ee0087c2509ecd4fd9e450bc46cdd`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3221ab91809a0ae69a9adf0f07fea47954f10f44049151bf15ea2fc9feeb592d`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce565aee31b9d2f404981ee3af0b843bcb1dce277039831e7816f039c6315c02`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb6b1a3d83f44ddd91ee07e1d0e4a569d2493a7fd4293f1e4eb12a62bca7246`  
		Last Modified: Tue, 12 Nov 2024 02:22:54 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040ae48dfbd65a4d48bdcb7dfac9d231955040542e3d6ae87824e860d9a65d89`  
		Last Modified: Tue, 12 Nov 2024 02:22:56 GMT  
		Size: 118.2 MB (118178547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664da2a658cbc810cd8df9c23b7376f958b8b823736ae105038debcac7bc8e6b`  
		Last Modified: Tue, 12 Nov 2024 02:22:54 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:84f41c2dd5dcccd82485d98fa14c7b0c74a5a6fb8ee562912b6290b414ad36f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.1 KB (914097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c620a01ab64f813436c294b33b22212d6ccf18ed3bb435e2a5d493a1b947d2`

```dockerfile
```

-	Layers:
	-	`sha256:5854d41b5b314516c97e1b037436c5d21164865759be9501d22b7e42899149d3`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 890.7 KB (890655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f16d1f9a8ae64e418c261a8be4c39bcd4eaf1684e03e131b8a3d3f07f5a5e1`  
		Last Modified: Tue, 12 Nov 2024 02:22:53 GMT  
		Size: 23.4 KB (23442 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:8.0.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:e575d6573d607994e2820e4780593ad6123abf2a5579c998c1e0d16985642252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184945211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f72dd550eded106fc9d85a001904da63e9ce349a4a7c9ee9daa8e0e54e959e`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4243273752f8c627f434b3051f7e45c5fa32ed3cb2318814b498fd999ce94b3d`  
		Last Modified: Sat, 07 Sep 2024 04:47:02 GMT  
		Size: 62.7 MB (62668884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88e30d06e54c9c99eef98f9dc827553050ba338c98bc364b1cae5f97c4368a3`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dc804ca99cd43313a465eac63c4ae60d837bb13473c108b1aaa195bb3cbd48`  
		Last Modified: Sat, 07 Sep 2024 04:46:59 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2137fd45317c976ac0019844bee4aa6c2946f47a6ae7cedc1d372ed82af00198`  
		Last Modified: Sat, 07 Sep 2024 04:47:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea56f686d5e5055bdfdd4e2ec051e635a80ca760795b50a73d4056986e3a8c90`  
		Last Modified: Sat, 07 Sep 2024 04:47:39 GMT  
		Size: 3.4 KB (3426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2384b6ea4c12cbae020fd6fb1c3f696eefccef0c0db0aefc38f7c8ad4b83d4`  
		Last Modified: Sat, 07 Sep 2024 04:47:42 GMT  
		Size: 118.2 MB (118178673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ca8621f51c14794c88c5133c049ba3d183fff7512c4893f699aaa8875cebbe`  
		Last Modified: Sat, 07 Sep 2024 04:47:39 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:bb7d2067dff1e494929cb5ff1f0d7f26697694fbd85f8ef959568e08508824c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.2 KB (887204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40e7a2cf83a36b84b70266d219d2f4e6acba1c256db988d92254b326aefb505`

```dockerfile
```

-	Layers:
	-	`sha256:97d262124529a99ee6147cc27957526da7b0054c175615860313a9576cf19814`  
		Last Modified: Sat, 07 Sep 2024 04:47:39 GMT  
		Size: 863.7 KB (863671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae28becf682158e882cef4c9fcb3d56f7ffca8649339e11717828b72a3cffbf6`  
		Last Modified: Sat, 07 Sep 2024 04:47:38 GMT  
		Size: 23.5 KB (23533 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:8.0.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:f434b5bed8c8bb2b3a0ddcaf40273b941afd8e06f506d1fe7cf5d5d5df954550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (180969593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a4edab98af130ee0f74ba35a338289cdaf3f85ca0796a3bc28a61c3ca83232`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2cf315af9480a876ed5e7efa86f52cab190a197656dcc25c561183380ba96d`  
		Last Modified: Sat, 07 Sep 2024 06:24:04 GMT  
		Size: 59.2 MB (59208493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c12032181a2e1089fca129cb6666ad1b33b69185233e9dc4cc7f69e6fb1190b`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d840c9bd89b5157b8d6f51fa118c75017552d7d26bfd8808b66f90e2f8ed76d`  
		Last Modified: Sat, 07 Sep 2024 06:24:02 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5edcc189a6b81a889c8457d0291083ad7c3560f048f63573367c297b1b30134`  
		Last Modified: Sat, 07 Sep 2024 06:24:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b82d17c34b47566a698eacd5cc51943130a5c8c4d15519d347508aa874d39fd`  
		Last Modified: Sat, 07 Sep 2024 06:24:56 GMT  
		Size: 3.4 KB (3427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f042670bbd3df056a3d76e1be9b57214b1e57df97439a8234052d07862a4dd2f`  
		Last Modified: Sat, 07 Sep 2024 06:25:00 GMT  
		Size: 118.2 MB (118178668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af827620297a61992c2beda050ec0ebafe970d58dcd40cb9b830edf95e5cb2e2`  
		Last Modified: Sat, 07 Sep 2024 06:24:56 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:5e8695ae543a280bfef7dfcb81a4b65f52d6b489edefa9d9de88d0cb9d6d899c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **885.0 KB (884974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e242be6721b5e730019952d803b6aeff57a97680dbd9973c84e2b50c626b363`

```dockerfile
```

-	Layers:
	-	`sha256:0ff466f00f28dce06eb6c84e0e28ebefc1d008244b72361a3b2f88c7bd25ffaf`  
		Last Modified: Sat, 07 Sep 2024 06:24:56 GMT  
		Size: 861.7 KB (861695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0983eda33e9725b8a924260ac2e9ccb3fa36d92236d01fa6fbc1f6019f9c4e`  
		Last Modified: Sat, 07 Sep 2024 06:24:55 GMT  
		Size: 23.3 KB (23279 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:9.0`

```console
$ docker pull bonita@sha256:3c1ddc72d5cbd274a6a10f1bb3a2fcdbacb974a757f154d5d7c709fd63298dc7
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
$ docker pull bonita@sha256:e79d0e07f10d65b6c5afa60db71d6142797f8564c93ada1ac0bfb9d84f0091e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192422764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9090d91fecc4fb60ec7d5a2268c24ff7d738d790bea83f86fc1a65616302c838`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e27d58aa5cd08a4ec3e14a5ff49a2c43068a2cd245ad147b57681612c84a0f`  
		Last Modified: Tue, 12 Nov 2024 02:49:58 GMT  
		Size: 68.6 MB (68614920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38090d45759a229c46c3322750b3715136d7e209dc2032d5f49408c09d81bbd1`  
		Last Modified: Tue, 12 Nov 2024 02:49:55 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968b5fdc62e2d5049c7976e53a54a0be5a190c237cc49ec2cde7656a6cb59d2e`  
		Last Modified: Tue, 12 Nov 2024 02:49:55 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598e25779fa9888d6193e4ce0cfd9d06354f36d624f5ff68e3f7fb87327475e2`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed5de122744e77b9cff6d039ce1876b40d55901b686b3467a8982d70979edeb`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6cdf2f734f0ec95ca18276b15eec6f8756b60d3cbf504fd317f7261b911475`  
		Last Modified: Tue, 12 Nov 2024 02:50:00 GMT  
		Size: 120.2 MB (120173512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a939d4d0f69f322d82d823c5d7fcf20967dbc988c7b4a79ee342cb599158e38`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 5.6 KB (5622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0` - unknown; unknown

```console
$ docker pull bonita@sha256:48caca26479d0fae9ca12749ef8c57137fa226405270f15a0b8e74e86d1a1d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1373746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb704fdc806ef784534f939b0fffb69f8fc98efb37cd25fe57dda163997898e`

```dockerfile
```

-	Layers:
	-	`sha256:e5044644322f8642c778a9c4b26ae0e2320e333c7ad737ae1ecf3a159856bbd9`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 1.4 MB (1350824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6006bb11389c0831b0c0b525d446ae8097fe627752fbdf849b47193023524f8`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 22.9 KB (22922 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:9.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:422bb84dcf94e6a7516e8d97408b479467bb832f801b3171fa44dacbb6b0c32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192802123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7634fee5ecb3b942eb44c54ff13688c5e89b2c6cd7a199c52da621e843f21531`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad1e704a6d1fa12e395283d70a5a0133c73fb678ba3b6c3b26a0cce86cfdfcb`  
		Last Modified: Sat, 07 Sep 2024 04:48:27 GMT  
		Size: 68.5 MB (68530559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe9acc59d4cf3efd7f5465867e8c264e1d9de2935b0524a813c055dcad33beb`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52467723c8400eeaa5a5f3e7df7cbc848e536800e4d3affa0cefee1147eb720b`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f321b22501c11d3c6dd56ca5c0f0760d0215e03eaf0827a21e7099a3107c534d`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952fe924ab1d38d4e5dac8fe880951043a138c1908ca7daefc6bfffb9a58535f`  
		Last Modified: Sat, 07 Sep 2024 04:48:26 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f5fed370a25b3b65a36ad0f4aaca5efbe152661c6a713eb38e4af4074bd070`  
		Last Modified: Sat, 07 Sep 2024 04:48:37 GMT  
		Size: 120.2 MB (120173482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3351df8a519b92043bc3588ab8056a8b9a58225249fad37e6cf14ab7a2d2f867`  
		Last Modified: Sat, 07 Sep 2024 04:48:26 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0` - unknown; unknown

```console
$ docker pull bonita@sha256:fb60570d01afa54dfd8f2e8374960df4c1ea57f4903bde3ca0ff732306c0f533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1346095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48415fe7c00bdac769d09cf30e06c500aae6802758633777cf1ea35dbab3463`

```dockerfile
```

-	Layers:
	-	`sha256:f4d7a112632cda8afdba2b3f9704712a0ee00bf85b4d4c148b0ae36d7ebaaceb`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 1.3 MB (1322772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97281fe5a393279dc74dae4ec620d8250309b33033851eb5a0d2eab130082268`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:9.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:6e9b67e96f29d035ddda75ae03c26127a50491d8558aefa7e0648e1f7b029711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189106331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03ad934a10a7f7a1479fcbb3cca95ea4ea997744f1e76da3a6690a6965ac0e9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d642177801827d23412d87d9ce2ceb38ffc4f576892db6d80d73f47ab93168f`  
		Last Modified: Sat, 07 Sep 2024 06:26:03 GMT  
		Size: 65.3 MB (65349946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13426edafdec3f9f8f632cdf1ab7e66b60fccd7355cae13e871493d92a7dcd6b`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9f0bb8319101cf60f7619cb1f4995b8d759be58499701cfb994c36c7aaea96`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497a80e5560abd7b0d41d1b2a03dba788982763fe0c3c07d20a27c5983e15ca9`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77a3274adfcc8bc769e3e413c54716c00b144297f989c7a148a54e2fc003fd5`  
		Last Modified: Sat, 07 Sep 2024 06:26:01 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b76bea0cd8f5e78b919bc340ede75b86eac26c3a85099af7715926f5fbeadba`  
		Last Modified: Sat, 07 Sep 2024 06:26:04 GMT  
		Size: 120.2 MB (120173533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e447752d63defbff6acd3c212ab510a50a57928c1e28d6d925abc22581cb592`  
		Last Modified: Sat, 07 Sep 2024 06:26:01 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0` - unknown; unknown

```console
$ docker pull bonita@sha256:b3b52de39c11fbb0b8b29086bde32211f9ff11b35e3cfa927025eb0ec4417b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1343853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80e06364c0d133e553d85737961c89aa9519f2861708e2ba1ced9b3890fcf6b`

```dockerfile
```

-	Layers:
	-	`sha256:8a2685fceb979d9d9fd8df85b7212754abfa3051695ed0fe4e7a85951f4785b4`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 1.3 MB (1320790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4fd1220f2d92555b5c954d1145f036b1570960e5ba3f32ecc5285079a48d984`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 23.1 KB (23063 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:9.0.0`

```console
$ docker pull bonita@sha256:3c1ddc72d5cbd274a6a10f1bb3a2fcdbacb974a757f154d5d7c709fd63298dc7
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
$ docker pull bonita@sha256:e79d0e07f10d65b6c5afa60db71d6142797f8564c93ada1ac0bfb9d84f0091e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192422764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9090d91fecc4fb60ec7d5a2268c24ff7d738d790bea83f86fc1a65616302c838`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e27d58aa5cd08a4ec3e14a5ff49a2c43068a2cd245ad147b57681612c84a0f`  
		Last Modified: Tue, 12 Nov 2024 02:49:58 GMT  
		Size: 68.6 MB (68614920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38090d45759a229c46c3322750b3715136d7e209dc2032d5f49408c09d81bbd1`  
		Last Modified: Tue, 12 Nov 2024 02:49:55 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968b5fdc62e2d5049c7976e53a54a0be5a190c237cc49ec2cde7656a6cb59d2e`  
		Last Modified: Tue, 12 Nov 2024 02:49:55 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598e25779fa9888d6193e4ce0cfd9d06354f36d624f5ff68e3f7fb87327475e2`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed5de122744e77b9cff6d039ce1876b40d55901b686b3467a8982d70979edeb`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6cdf2f734f0ec95ca18276b15eec6f8756b60d3cbf504fd317f7261b911475`  
		Last Modified: Tue, 12 Nov 2024 02:50:00 GMT  
		Size: 120.2 MB (120173512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a939d4d0f69f322d82d823c5d7fcf20967dbc988c7b4a79ee342cb599158e38`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 5.6 KB (5622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:48caca26479d0fae9ca12749ef8c57137fa226405270f15a0b8e74e86d1a1d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1373746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb704fdc806ef784534f939b0fffb69f8fc98efb37cd25fe57dda163997898e`

```dockerfile
```

-	Layers:
	-	`sha256:e5044644322f8642c778a9c4b26ae0e2320e333c7ad737ae1ecf3a159856bbd9`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 1.4 MB (1350824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6006bb11389c0831b0c0b525d446ae8097fe627752fbdf849b47193023524f8`  
		Last Modified: Tue, 12 Nov 2024 02:49:56 GMT  
		Size: 22.9 KB (22922 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:9.0.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:422bb84dcf94e6a7516e8d97408b479467bb832f801b3171fa44dacbb6b0c32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192802123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7634fee5ecb3b942eb44c54ff13688c5e89b2c6cd7a199c52da621e843f21531`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad1e704a6d1fa12e395283d70a5a0133c73fb678ba3b6c3b26a0cce86cfdfcb`  
		Last Modified: Sat, 07 Sep 2024 04:48:27 GMT  
		Size: 68.5 MB (68530559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe9acc59d4cf3efd7f5465867e8c264e1d9de2935b0524a813c055dcad33beb`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52467723c8400eeaa5a5f3e7df7cbc848e536800e4d3affa0cefee1147eb720b`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f321b22501c11d3c6dd56ca5c0f0760d0215e03eaf0827a21e7099a3107c534d`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952fe924ab1d38d4e5dac8fe880951043a138c1908ca7daefc6bfffb9a58535f`  
		Last Modified: Sat, 07 Sep 2024 04:48:26 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f5fed370a25b3b65a36ad0f4aaca5efbe152661c6a713eb38e4af4074bd070`  
		Last Modified: Sat, 07 Sep 2024 04:48:37 GMT  
		Size: 120.2 MB (120173482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3351df8a519b92043bc3588ab8056a8b9a58225249fad37e6cf14ab7a2d2f867`  
		Last Modified: Sat, 07 Sep 2024 04:48:26 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:fb60570d01afa54dfd8f2e8374960df4c1ea57f4903bde3ca0ff732306c0f533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1346095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48415fe7c00bdac769d09cf30e06c500aae6802758633777cf1ea35dbab3463`

```dockerfile
```

-	Layers:
	-	`sha256:f4d7a112632cda8afdba2b3f9704712a0ee00bf85b4d4c148b0ae36d7ebaaceb`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 1.3 MB (1322772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97281fe5a393279dc74dae4ec620d8250309b33033851eb5a0d2eab130082268`  
		Last Modified: Sat, 07 Sep 2024 04:48:25 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:9.0.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:6e9b67e96f29d035ddda75ae03c26127a50491d8558aefa7e0648e1f7b029711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189106331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03ad934a10a7f7a1479fcbb3cca95ea4ea997744f1e76da3a6690a6965ac0e9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d642177801827d23412d87d9ce2ceb38ffc4f576892db6d80d73f47ab93168f`  
		Last Modified: Sat, 07 Sep 2024 06:26:03 GMT  
		Size: 65.3 MB (65349946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13426edafdec3f9f8f632cdf1ab7e66b60fccd7355cae13e871493d92a7dcd6b`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9f0bb8319101cf60f7619cb1f4995b8d759be58499701cfb994c36c7aaea96`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497a80e5560abd7b0d41d1b2a03dba788982763fe0c3c07d20a27c5983e15ca9`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77a3274adfcc8bc769e3e413c54716c00b144297f989c7a148a54e2fc003fd5`  
		Last Modified: Sat, 07 Sep 2024 06:26:01 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b76bea0cd8f5e78b919bc340ede75b86eac26c3a85099af7715926f5fbeadba`  
		Last Modified: Sat, 07 Sep 2024 06:26:04 GMT  
		Size: 120.2 MB (120173533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e447752d63defbff6acd3c212ab510a50a57928c1e28d6d925abc22581cb592`  
		Last Modified: Sat, 07 Sep 2024 06:26:01 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:b3b52de39c11fbb0b8b29086bde32211f9ff11b35e3cfa927025eb0ec4417b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1343853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80e06364c0d133e553d85737961c89aa9519f2861708e2ba1ced9b3890fcf6b`

```dockerfile
```

-	Layers:
	-	`sha256:8a2685fceb979d9d9fd8df85b7212754abfa3051695ed0fe4e7a85951f4785b4`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 1.3 MB (1320790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4fd1220f2d92555b5c954d1145f036b1570960e5ba3f32ecc5285079a48d984`  
		Last Modified: Sat, 07 Sep 2024 06:26:00 GMT  
		Size: 23.1 KB (23063 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:latest`

```console
$ docker pull bonita@sha256:1f7af758a6dca6bba55c28f36b75b2d79ea624e7b48390f18482160d8fa43379
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:aff72fdcdc1abd4b9bbad0c155d337538226d6724f0e50ced51ed4bcbf815bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189935357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8302afd6c116f16b99b8803f90d5e5d93087ce9de24a10d9ab1e9a966f9b9841`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb8a593a4b7726f83576628ca6aa70220bcdcbef9651d003ba88727ce34d9d1`  
		Last Modified: Tue, 12 Nov 2024 02:38:48 GMT  
		Size: 18.3 MB (18307356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441f37ea86bb2ebd3f2d928c64e6d4c39686f25618e8847e957fee5ff58da0e6`  
		Last Modified: Tue, 12 Nov 2024 02:38:49 GMT  
		Size: 46.6 MB (46615858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44818f47c6831f333e1b9a5947c85124e4a12ca670bea7043d4b11beeb3a780b`  
		Last Modified: Tue, 12 Nov 2024 02:38:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cfa7e9b065bacf6029c8a0af5b63bb0e86ef13e828cb645d914da3480fbbfb`  
		Last Modified: Tue, 12 Nov 2024 02:38:48 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282cd84bf85b9e16a5b15f900b8c120135cdd324c624dfefc957b15a5c8f4924`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 1.9 MB (1859693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846171241c7d276eaaa07a72711d35c5fee179900b56800d5ec0c8e937afc5ce`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8646004264a0d08ea69c6cb78588da01faa2819ff6a4a8c61e87fe36f44c75d1`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382f0c1559b8a9d44cdc48b848d6f66a19a9bbccf9eb4c68283330c9424ae256`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb4e9a3063b2241adf74732cf5eff7a4dbc4f0de557e68a18f505c33cbb22f0`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 3.7 KB (3709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b96214236cb294ae2c9d88dd27fb374b2157482e17cfaf5922a1cd7260f7d1`  
		Last Modified: Tue, 12 Nov 2024 03:11:46 GMT  
		Size: 119.5 MB (119515350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f4fcac1efe12c849b5d2ccb6c9ba54211207d66579b86cceecd00c717a268d`  
		Last Modified: Tue, 12 Nov 2024 03:11:45 GMT  
		Size: 5.9 KB (5882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:latest` - unknown; unknown

```console
$ docker pull bonita@sha256:b6797d0a32115ece7f217354ee93f1518bd21a599ce0d3748974467c286df1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c5d4f1dc1cdfcf2877600fc4dc9290598ae9a34d569ddbbf974eae70cbb2d2`

```dockerfile
```

-	Layers:
	-	`sha256:76e80da520f48790ac44f471f6e9707006debdcc727cf18427d5cff5d4bf676a`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 1.3 MB (1265026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fff7ba6987a0718b554cbd6abdbb95082e916db7b565f8500391ff9e438de050`  
		Last Modified: Tue, 12 Nov 2024 03:11:44 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json
