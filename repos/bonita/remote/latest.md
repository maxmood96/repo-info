## `bonita:latest`

```console
$ docker pull bonita@sha256:48fe1a388de4f57a67014c8ee26f65ca3a26b95c3c39a23069bc97dbae778d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:a0e583c8fb0b878fc3d6d2d0dead5c833576f1993366621d624af1ae30dc09ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191407593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9f5448fa5015f8437eba2d74276cadcd10e449aeca92e0ce67c260f2e52995`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:53:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 08:53:20 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Sat, 16 Mar 2024 08:53:21 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 08:53:22 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 08:53:22 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 08:53:22 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 08:53:22 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 08:53:22 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 08:53:22 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 08:53:22 GMT
ENV BONITA_VERSION=9.0.0
# Sat, 16 Mar 2024 08:53:22 GMT
ENV BRANDING_VERSION=2023.2-u0
# Sat, 16 Mar 2024 08:53:22 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Sat, 16 Mar 2024 08:53:22 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Sat, 16 Mar 2024 08:53:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 08:53:23 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Sat, 16 Mar 2024 08:53:23 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 08:53:23 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Sat, 16 Mar 2024 08:53:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 08:53:28 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 08:53:28 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 08:53:28 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 08:53:28 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 08:53:28 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 08:53:28 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 08:53:28 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 08:53:28 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 08:53:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 08:53:29 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 08:53:29 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 08:53:29 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 08:53:29 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 08:53:29 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Sat, 16 Mar 2024 08:53:29 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 16 Mar 2024 08:53:29 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 08:53:29 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 08:53:29 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9084deaf8eef07da5f3aa6b3014bb4b958d1c4e0d8f55eaa65269c88584d40`  
		Last Modified: Sat, 16 Mar 2024 08:54:58 GMT  
		Size: 67.8 MB (67817536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a766dce101ece1edb4401082df9ef45459f4bda6063c4a8bed7d18b80aeed39e`  
		Last Modified: Sat, 16 Mar 2024 08:54:50 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1597773fb6fbd845cbc21441f0990d180ac0eaa7373c90eb1866b66e7941b1df`  
		Last Modified: Sat, 16 Mar 2024 08:54:48 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743bbc5be7dff0bdf43f59d557de8d34b75e8fd936d62cb9a72c594b8384d058`  
		Last Modified: Sat, 16 Mar 2024 08:54:48 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d37efadae491c0d69a0debc3b3565816cf80b8e6b9594c7ea973d48d113124`  
		Last Modified: Sat, 16 Mar 2024 08:54:48 GMT  
		Size: 3.7 KB (3664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2f1f47851bda5811941afc4efa871a3d497dd5b958b8596b2a9e49b87f50ee`  
		Last Modified: Sat, 16 Mar 2024 08:54:54 GMT  
		Size: 120.2 MB (120176625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861b86aac749dce24284c22ae38932dd8cbea99e67ec5403cac20dd7a077ddad`  
		Last Modified: Sat, 16 Mar 2024 08:54:48 GMT  
		Size: 5.7 KB (5661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:b1164886c1dd37fe4af8bca0ed0e04889790b9b03aff1cddbf946ac49d2cee31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191233926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098d293bf0e7d1ba0f27df5a266d5ae350255339e55944146554f0968765a3d3`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:03:00 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 03:03:04 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Sat, 16 Mar 2024 03:03:05 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 03:03:06 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 03:03:06 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 03:03:06 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 03:03:06 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 03:03:06 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 03:03:06 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 03:03:06 GMT
ENV BONITA_VERSION=9.0.0
# Sat, 16 Mar 2024 03:03:06 GMT
ENV BRANDING_VERSION=2023.2-u0
# Sat, 16 Mar 2024 03:03:06 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Sat, 16 Mar 2024 03:03:06 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Sat, 16 Mar 2024 03:03:06 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 03:03:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Sat, 16 Mar 2024 03:03:07 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 03:03:07 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Sat, 16 Mar 2024 03:03:12 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 03:03:13 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 03:03:13 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 03:03:13 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 03:03:13 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 03:03:13 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 03:03:13 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 03:03:14 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 03:03:14 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 03:03:14 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 03:03:14 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 03:03:14 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 03:03:14 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 03:03:14 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 03:03:14 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Sat, 16 Mar 2024 03:03:14 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 16 Mar 2024 03:03:14 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 03:03:14 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 03:03:14 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3524d916d3935a95d196223f428da7c2bac02a995bf8d7b1170c1d22d5dc51`  
		Last Modified: Sat, 16 Mar 2024 03:04:40 GMT  
		Size: 67.7 MB (67713083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea4dfaf95e5f6f22599c04b75441b23ba4aa894f2d13ddadc5cbcf4d6498d957`  
		Last Modified: Sat, 16 Mar 2024 03:04:33 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52991c844332decf9c503f309af997fe05a6bf424e9fc5f7fffa29f388914a2f`  
		Last Modified: Sat, 16 Mar 2024 03:04:31 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6505227614460968958f19284ddd228c3c068f1902b6dc463e56e28ab7369982`  
		Last Modified: Sat, 16 Mar 2024 03:04:31 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3788bfef5a144858b67df232f998074dd09cd31c7e789039b0c64f76d73086`  
		Last Modified: Sat, 16 Mar 2024 03:04:31 GMT  
		Size: 3.7 KB (3662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d851e1070f9c2182e864ae894b6a5c7a1a66ced1fe05abf8fcfddd2a0564e5b2`  
		Last Modified: Sat, 16 Mar 2024 03:04:36 GMT  
		Size: 120.2 MB (120176597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd77394c2e5df545aa7359de0c43dcdb3f1debff34cebfc5ffb9fa298a45ec77`  
		Last Modified: Sat, 16 Mar 2024 03:04:31 GMT  
		Size: 5.7 KB (5657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:79933c76b003f95c346f03f6749abe1c8365180f614e5c65c7a5597b10692562
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188112718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd38b100a80a8874028a1044bdb23eb10c89562152b41c6adfe96eb0483decc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:59:26 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 15 Mar 2024 23:59:36 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Fri, 15 Mar 2024 23:59:39 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 15 Mar 2024 23:59:40 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 15 Mar 2024 23:59:41 GMT
ARG BONITA_VERSION
# Fri, 15 Mar 2024 23:59:41 GMT
ARG BRANDING_VERSION
# Fri, 15 Mar 2024 23:59:41 GMT
ARG BONITA_SHA256
# Fri, 15 Mar 2024 23:59:42 GMT
ARG BASE_URL
# Fri, 15 Mar 2024 23:59:42 GMT
ARG BONITA_URL
# Fri, 15 Mar 2024 23:59:42 GMT
ENV BONITA_VERSION=9.0.0
# Fri, 15 Mar 2024 23:59:43 GMT
ENV BRANDING_VERSION=2023.2-u0
# Fri, 15 Mar 2024 23:59:43 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Fri, 15 Mar 2024 23:59:43 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Fri, 15 Mar 2024 23:59:43 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 15 Mar 2024 23:59:44 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Fri, 15 Mar 2024 23:59:45 GMT
RUN mkdir /opt/files
# Fri, 15 Mar 2024 23:59:45 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Fri, 15 Mar 2024 23:59:53 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 15 Mar 2024 23:59:55 GMT
ENV HTTP_API=false
# Fri, 15 Mar 2024 23:59:56 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 15 Mar 2024 23:59:56 GMT
ENV HTTP_API_PASSWORD=
# Fri, 15 Mar 2024 23:59:56 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 15 Mar 2024 23:59:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 15 Mar 2024 23:59:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 15 Mar 2024 23:59:58 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 15 Mar 2024 23:59:58 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 15 Mar 2024 23:59:58 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 15 Mar 2024 23:59:59 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 15 Mar 2024 23:59:59 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 00:00:00 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 00:00:00 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 00:00:00 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Sat, 16 Mar 2024 00:00:01 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 16 Mar 2024 00:00:01 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 00:00:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 00:00:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6384f1a239251220f0358d4b91437867a003641be33f6cdf9cc3dcddd7986a`  
		Last Modified: Sat, 16 Mar 2024 00:01:52 GMT  
		Size: 64.6 MB (64576693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6884479c73e42435e5f40e00ce4843fad97c06bcaf6bf1f1a0ab9cf89279d370`  
		Last Modified: Sat, 16 Mar 2024 00:01:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717e8af53e6402303a36ec826c3eaefeca25020481553fc0859b2cee6c0bc42a`  
		Last Modified: Sat, 16 Mar 2024 00:01:40 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c10fb94484bef1885fd4f76be882e4c01c0bf4e6d9b4d3464753f423585b87b`  
		Last Modified: Sat, 16 Mar 2024 00:01:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b80682af534935101c96c7017b281cc7a4e415ed75b635be5c45d94decc7b0`  
		Last Modified: Sat, 16 Mar 2024 00:01:40 GMT  
		Size: 3.7 KB (3665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6ddabb5d83deb266ad54000e90c2abde05929817e21cce416e94df7767bf3f`  
		Last Modified: Sat, 16 Mar 2024 00:01:49 GMT  
		Size: 120.2 MB (120176649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d87b97109455a1126f72104f329dedb80b49cbde63f11273ea44205d2b20749`  
		Last Modified: Sat, 16 Mar 2024 00:01:40 GMT  
		Size: 5.7 KB (5659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
