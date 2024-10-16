## `bonita:latest`

```console
$ docker pull bonita@sha256:fda6f92cac9db5627406a8fed339fd21542d969350ace0e51cd293cd93cb50dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:91aa46f4c3cb5f516995021bba3d8a4e784e720592bc26749d95c4520c753bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.3 MB (182335848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516647ce1c8076d692fa9584257f395909cefeb7a5a53fd425bad70de990c2a1`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='63bae276cc322532b451ae7473127c92a75db16cc95473577f133cd09349822a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb0eeeb44ea727a6840e888ba4140371726ac8b86f199aa403faf61b4de2106`  
		Last Modified: Fri, 06 Sep 2024 22:43:01 GMT  
		Size: 9.4 MB (9388900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7791704841fa984e499820b14f4a9070bb669900fdcabc1951944d2e952883`  
		Last Modified: Fri, 06 Sep 2024 22:44:43 GMT  
		Size: 47.0 MB (46988364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3b00e444c6625213587a909171f8f0a2279a12e83451b651fd700dd85c3d60`  
		Last Modified: Fri, 06 Sep 2024 22:44:37 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b1e77fd7988ec41a23e821bba0badc2b6953115b3982062190fe1e87b02fa5`  
		Last Modified: Fri, 06 Sep 2024 22:44:37 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9084b3ffa8b71a0017cf375941ab96bccff949988d412b627989d5ccf93aa1`  
		Last Modified: Wed, 16 Oct 2024 16:12:25 GMT  
		Size: 2.8 MB (2806407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8897f8ec15d44b60df98aee120d8d235b08559877170690b5481da4235315b`  
		Last Modified: Wed, 16 Oct 2024 16:12:25 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3689b72ded0c13251ed178c446d9b188a6d2bf85d0df16805861182b37637162`  
		Last Modified: Wed, 16 Oct 2024 16:12:25 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eda2d3d00180d9d6dc544722142044beb455a9f81ab36f375c6e303bf664ede`  
		Last Modified: Wed, 16 Oct 2024 16:12:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d7128c5d6a3d5a76342a98a74c95f95ecf0d843338284e7ad8c07da2d3c961`  
		Last Modified: Wed, 16 Oct 2024 16:12:25 GMT  
		Size: 3.7 KB (3708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eea00283fbf8a88630072755cc0f002f22ee4aee20445a9de5fcb0a5c925504`  
		Last Modified: Wed, 16 Oct 2024 16:12:27 GMT  
		Size: 119.5 MB (119515334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb15917b2a2bd664cae301258dff585f9bdde444d3409f772085c3e34f8f55a`  
		Last Modified: Wed, 16 Oct 2024 16:12:25 GMT  
		Size: 5.9 KB (5885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:latest` - unknown; unknown

```console
$ docker pull bonita@sha256:919010064a52336a9b5bce6b851662f97887b4e80de0d6f703636fd0c9c6cfdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1200845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cffad779b433d6bf0f36e2d13310a566ad7b4e1aa17186eda997aa1b4a1a51b`

```dockerfile
```

-	Layers:
	-	`sha256:19c0dcc37a50577ea499e3f209dae78ca9297c424546b3350b75eb30ed7a7c19`  
		Last Modified: Wed, 16 Oct 2024 16:12:25 GMT  
		Size: 1.2 MB (1171814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a273d2e003700adf734ae75e756688dd01c0ea460ace5e27a40c34c7d585109`  
		Last Modified: Wed, 16 Oct 2024 16:12:24 GMT  
		Size: 29.0 KB (29031 bytes)  
		MIME: application/vnd.in-toto+json
