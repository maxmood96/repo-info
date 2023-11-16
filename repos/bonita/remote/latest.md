## `bonita:latest`

```console
$ docker pull bonita@sha256:d39d3d25f2cb1094c71575267defa84d83416cf6074abe1a4818897caf5daa7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:ce72c862ad04f73627fc45952dac9951041d20f55306eba158449dd096286030
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182633333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be82fe324d0817bbc07c96c2d52d747a41049594124520d07c833757b4365058`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:09:03 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:09:07 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:09:08 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:09:08 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:09:08 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:09:09 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:09:20 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 21 Oct 2023 00:09:20 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 21 Oct 2023 00:09:20 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 21 Oct 2023 00:09:20 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:09:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:09:21 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:09:21 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:09:21 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:09:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:09:27 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:09:27 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:09:28 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:09:28 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:09:28 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:09:28 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:09:28 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:09:28 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:09:29 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:09:29 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:09:29 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:09:29 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f838f3f7f32a1b8585aba6ca458e7076072add121932f38000e7b00b134f97`  
		Last Modified: Sat, 21 Oct 2023 00:10:21 GMT  
		Size: 61.6 MB (61635300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d74b097b61ce89e3a232aa48eb9083220655cd4dd7f7a922cf30b1ab03e4b0`  
		Last Modified: Sat, 21 Oct 2023 00:10:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08daa40ce48dc5470d02ebe9b19441e2f3e09c11234e707fc3d534f75400fd14`  
		Last Modified: Sat, 21 Oct 2023 00:10:11 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffad4d027e798d54c282bb4db18de19d9f28c055f248b118731978cb128dbc69`  
		Last Modified: Sat, 21 Oct 2023 00:10:34 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01409892cdf7c7933def01661bab5324433e511d19bcc36ec60eeeba8de8fa77`  
		Last Modified: Sat, 21 Oct 2023 00:10:34 GMT  
		Size: 3.0 KB (3041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1c1150517cfa2f8ac13f869019c2fdddc4bbd8abcdd725483b5734b4da951d`  
		Last Modified: Sat, 21 Oct 2023 00:10:41 GMT  
		Size: 118.2 MB (118180320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e18a2c93da8bb7b138b6ab222d9e736d4278553ba2385a86e0dcbc33c51715f`  
		Last Modified: Sat, 21 Oct 2023 00:10:34 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5e49e27972157aaeb67e156cee61f58f369179492b51e6bde7d91cfffd5207fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191217273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88eb2fdd0963c658b910d4a1c30de1984c0eeea58f616335ea003f723e674060`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Thu, 16 Nov 2023 19:42:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 16 Nov 2023 19:42:45 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Thu, 16 Nov 2023 19:42:47 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 16 Nov 2023 19:42:47 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Thu, 16 Nov 2023 19:42:47 GMT
ARG BONITA_VERSION
# Thu, 16 Nov 2023 19:42:47 GMT
ARG BRANDING_VERSION
# Thu, 16 Nov 2023 19:42:47 GMT
ARG BONITA_SHA256
# Thu, 16 Nov 2023 19:42:47 GMT
ARG BASE_URL
# Thu, 16 Nov 2023 19:42:47 GMT
ARG BONITA_URL
# Thu, 16 Nov 2023 19:42:47 GMT
ENV BONITA_VERSION=9.0.0
# Thu, 16 Nov 2023 19:42:47 GMT
ENV BRANDING_VERSION=2023.2-u0
# Thu, 16 Nov 2023 19:42:48 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Thu, 16 Nov 2023 19:42:48 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 19:42:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 16 Nov 2023 19:42:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 19:42:48 GMT
RUN mkdir /opt/files
# Thu, 16 Nov 2023 19:42:48 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Thu, 16 Nov 2023 19:42:53 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Thu, 16 Nov 2023 19:42:54 GMT
ENV HTTP_API=false
# Thu, 16 Nov 2023 19:42:54 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 16 Nov 2023 19:42:54 GMT
ENV HTTP_API_PASSWORD=
# Thu, 16 Nov 2023 19:42:54 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 16 Nov 2023 19:42:54 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 16 Nov 2023 19:42:54 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 16 Nov 2023 19:42:54 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 16 Nov 2023 19:42:54 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 16 Nov 2023 19:42:54 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 16 Nov 2023 19:42:54 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 16 Nov 2023 19:42:54 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 16 Nov 2023 19:42:55 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 16 Nov 2023 19:42:55 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 16 Nov 2023 19:42:55 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Thu, 16 Nov 2023 19:42:55 GMT
VOLUME [/opt/bonita/conf/logs]
# Thu, 16 Nov 2023 19:42:55 GMT
EXPOSE 8080 9000
# Thu, 16 Nov 2023 19:42:55 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 16 Nov 2023 19:42:55 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b91194eaedc3b0b43820893c72fdfa202cd33a3b6acf36d922f4e8177037dcf`  
		Last Modified: Thu, 16 Nov 2023 19:43:59 GMT  
		Size: 67.7 MB (67697958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c36e7053db3a3ab3898c4cdca5feb35e0c05ddf2a7d2e55eeda499d455e71d`  
		Last Modified: Thu, 16 Nov 2023 19:43:51 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00c9c766bf3b0ffe3dbe1613b0db6ab8bed0084e75afb7d55ef00a833dbe83b`  
		Last Modified: Thu, 16 Nov 2023 19:43:50 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c81d3f6b9a207d3243c64adf9639ea5829c5f6b84cb4973fe9865daa5db6bb`  
		Last Modified: Thu, 16 Nov 2023 19:43:49 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0852a8cc9912224d36d1221295cf3e52dcda226be74e37c58e05849ced2ad22e`  
		Last Modified: Thu, 16 Nov 2023 19:43:49 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e88c035cf8dc48508929584933b4f099c0b1fe07d1b3fb9584959908499711`  
		Last Modified: Thu, 16 Nov 2023 19:43:55 GMT  
		Size: 120.2 MB (120176597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96e77abb8a766509b970a79a33492fe2da41185a441f2fb6e382e02fffe2142`  
		Last Modified: Thu, 16 Nov 2023 19:43:49 GMT  
		Size: 5.7 KB (5658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:4cd0c475c81e6b8fa4fd7224921e86253becd79044f8be18295a5a23133d0b39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178797802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadb48a67d71e387a7df8325e77afed5c2f5f06b0e3c0566dfad9432dedc898c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 07 Aug 2023 20:16:44 GMT
ADD file:b30c2945bf4c873440b2e390c7120f16abe08ec41b10c2fb248b9b1a7ad223fa in / 
# Mon, 07 Aug 2023 20:16:44 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:05:42 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 21 Oct 2023 00:05:52 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 21 Oct 2023 00:05:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 21 Oct 2023 00:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BONITA_VERSION
# Sat, 21 Oct 2023 00:05:58 GMT
ARG BRANDING_VERSION
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_SHA256
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BASE_URL
# Sat, 21 Oct 2023 00:05:59 GMT
ARG BONITA_URL
# Sat, 21 Oct 2023 00:06:33 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 21 Oct 2023 00:06:34 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 21 Oct 2023 00:06:34 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 21 Oct 2023 00:06:35 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:06:36 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 21 Oct 2023 00:06:36 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 21 Oct 2023 00:06:38 GMT
RUN mkdir /opt/files
# Sat, 21 Oct 2023 00:06:38 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 21 Oct 2023 00:06:53 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 21 Oct 2023 00:06:57 GMT
ENV HTTP_API=false
# Sat, 21 Oct 2023 00:06:57 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 21 Oct 2023 00:06:58 GMT
ENV HTTP_API_PASSWORD=
# Sat, 21 Oct 2023 00:06:59 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 21 Oct 2023 00:06:59 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 21 Oct 2023 00:07:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 21 Oct 2023 00:07:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 21 Oct 2023 00:07:01 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 21 Oct 2023 00:07:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 21 Oct 2023 00:07:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 21 Oct 2023 00:07:03 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 21 Oct 2023 00:07:04 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 21 Oct 2023 00:07:04 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 21 Oct 2023 00:07:05 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 21 Oct 2023 00:07:05 GMT
EXPOSE 8080 9000
# Sat, 21 Oct 2023 00:07:05 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 21 Oct 2023 00:07:07 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:cc1a557f8d111cc8c11359cd168abb441e150c9dc42a046349c5e51132461a47`  
		Last Modified: Mon, 07 Aug 2023 20:17:53 GMT  
		Size: 2.8 MB (2802326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a182309e1e789ebba4af94947e2518ea202d9d8c18734bedfae84b3293a348a2`  
		Last Modified: Sat, 21 Oct 2023 00:08:04 GMT  
		Size: 57.8 MB (57805151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a325b17f039f2978acf811ccd2341613817be60d2d8439c2c0e7380a30d3768`  
		Last Modified: Sat, 21 Oct 2023 00:07:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec97000580bedcd89c016b4b68d3e8dab55b97a0b940e19321fc8e147b2f8285`  
		Last Modified: Sat, 21 Oct 2023 00:07:53 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1409806b830f8aa770a64bfea692b19bf3af1e157406ddbe77562d5ec81c0bd8`  
		Last Modified: Sat, 21 Oct 2023 00:08:19 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fa3595e4091924ae135c627ec3ece6800b352ea43abadc7604756850a89a99`  
		Last Modified: Sat, 21 Oct 2023 00:08:19 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae1f9a0a247a5a60e3d1896ec23d581b0263924cb338e027087fc6d5cdd314a`  
		Last Modified: Sat, 21 Oct 2023 00:08:26 GMT  
		Size: 118.2 MB (118180291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189e2255ca4edb354260f1cdc98b57d17c2ccb095d7c1f23eb2e21adeef43e91`  
		Last Modified: Sat, 21 Oct 2023 00:08:19 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
