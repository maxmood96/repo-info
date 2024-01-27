## `bonita:latest`

```console
$ docker pull bonita@sha256:0bedee63b0d734d177ce304454e3cee8ce837fea6c9abcc5c4e366c2ded7bb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:1875a25a973f3fe9f1fd3707e7dca4a8b9f0d1d810820350621c4d4220fe5ad2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191409773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33bf88dc550ae8d6471edb6ea207e11ba79be09a90d1bca8ec935ce4b92bc25b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:47:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 00:48:02 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Sat, 27 Jan 2024 00:48:03 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 00:48:03 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 00:48:03 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 00:48:03 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 00:48:04 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 00:48:04 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 00:48:04 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 00:48:04 GMT
ENV BONITA_VERSION=9.0.0
# Sat, 27 Jan 2024 00:48:04 GMT
ENV BRANDING_VERSION=2023.2-u0
# Sat, 27 Jan 2024 00:48:04 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Sat, 27 Jan 2024 00:48:04 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Sat, 27 Jan 2024 00:48:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 00:48:04 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Sat, 27 Jan 2024 00:48:05 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 00:48:05 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Sat, 27 Jan 2024 00:48:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 00:48:11 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 00:48:11 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 00:48:11 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 00:48:11 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 00:48:11 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 00:48:12 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 00:48:12 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 00:48:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 00:48:12 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 00:48:12 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 00:48:12 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 00:48:12 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 00:48:12 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 00:48:12 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Sat, 27 Jan 2024 00:48:12 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 27 Jan 2024 00:48:12 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 00:48:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 00:48:13 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c47cd728b5a54f1389e362c147bf19f047a8a0ac0ea8b6046e03ac3e8bb25a0`  
		Last Modified: Sat, 27 Jan 2024 00:49:25 GMT  
		Size: 67.8 MB (67819745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548c3e6cbadca4ba4256c514bb5b89a85c9793c04346dab380b7a2fa098ea102`  
		Last Modified: Sat, 27 Jan 2024 00:49:17 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8297c3f4223b7431c1e35a67ee513ed5a10fe3bc26e7d8be07e88b7c1d841d07`  
		Last Modified: Sat, 27 Jan 2024 00:49:14 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fda2b3e502c61224d20d411d06a9f2635b0ca144d55f42913075fd4de02a9f`  
		Last Modified: Sat, 27 Jan 2024 00:49:15 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9f946307280e1184f6944fb3db9b66594185c2839a660b19ded9282fd4dfd8`  
		Last Modified: Sat, 27 Jan 2024 00:49:14 GMT  
		Size: 3.7 KB (3660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c81e506461e330a3aed398884307025493735d3e0b52ba881d76a441987cd3`  
		Last Modified: Sat, 27 Jan 2024 00:49:21 GMT  
		Size: 120.2 MB (120176605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286434d0492902e7789d7101b1fa23b4dd716c8a6488519e8b22036c07e6fb56`  
		Last Modified: Sat, 27 Jan 2024 00:49:14 GMT  
		Size: 5.7 KB (5661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:b122a00e2202a22a4a1e824e92f3baa07bb46368ed74c1b1e3edb5f7ddbedb81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191236092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd72ab76e24a7dde05b5e89119f0bc84aef546a3e62aa49f485465cf28c35168`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:42:14 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 03:42:18 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Sat, 27 Jan 2024 03:42:19 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 03:42:20 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 03:42:20 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 03:42:20 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 03:42:20 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 03:42:20 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 03:42:20 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 03:42:20 GMT
ENV BONITA_VERSION=9.0.0
# Sat, 27 Jan 2024 03:42:20 GMT
ENV BRANDING_VERSION=2023.2-u0
# Sat, 27 Jan 2024 03:42:20 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Sat, 27 Jan 2024 03:42:20 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Sat, 27 Jan 2024 03:42:20 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 03:42:21 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Sat, 27 Jan 2024 03:42:21 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 03:42:21 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Sat, 27 Jan 2024 03:42:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 03:42:27 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 03:42:27 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 03:42:27 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 03:42:27 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 03:42:27 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 03:42:27 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 03:42:28 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 03:42:28 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 03:42:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 03:42:28 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 03:42:28 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 03:42:28 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 03:42:28 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 03:42:28 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Sat, 27 Jan 2024 03:42:28 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 27 Jan 2024 03:42:28 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 03:42:28 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 03:42:28 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc14a78e4f2af699def1e1c351c9aeb9c057a681d0544dc549a18004d81d3110`  
		Last Modified: Sat, 27 Jan 2024 03:43:37 GMT  
		Size: 67.7 MB (67715231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7dd47befd7676fe00fe4caa15b95dc35477b6164b867a46ef5e4176d604f51`  
		Last Modified: Sat, 27 Jan 2024 03:43:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be4feea8279e26e35b7e505b6008bfbfc7a1ba91d2280409a7706566de9af17`  
		Last Modified: Sat, 27 Jan 2024 03:43:29 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f22c1e34c4bf47a81b366dbfe07c2b9813741a4d3e97b4bdb86057d5657ff0c`  
		Last Modified: Sat, 27 Jan 2024 03:43:29 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e738923d13008f524a4ee22f09a0762f4afaafce1fd4c6586ab5cdf7bcf306`  
		Last Modified: Sat, 27 Jan 2024 03:43:29 GMT  
		Size: 3.7 KB (3662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efcae3b3be0cec99df30aee331564b418f417d15b1927ef698f5b4ad6608350c`  
		Last Modified: Sat, 27 Jan 2024 03:43:34 GMT  
		Size: 120.2 MB (120176616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7878a5ae80ccdc4fc15cbb91d927cac10515539c9a8d0d1bed89c82966b6cece`  
		Last Modified: Sat, 27 Jan 2024 03:43:29 GMT  
		Size: 5.7 KB (5658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:bc79e0ef1d8da08a83a791032423ce792929636c7405abba8a9bc5a8df32466a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188115243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4804cf25e906fca0141705252b78962d257484a2595629a9f2e5f41a9233573e`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:45:52 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 00:46:07 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Sat, 27 Jan 2024 00:46:11 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 00:46:12 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 00:46:13 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 00:46:13 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 00:46:14 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 00:46:15 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 00:46:15 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 00:46:15 GMT
ENV BONITA_VERSION=9.0.0
# Sat, 27 Jan 2024 00:46:16 GMT
ENV BRANDING_VERSION=2023.2-u0
# Sat, 27 Jan 2024 00:46:16 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Sat, 27 Jan 2024 00:46:16 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Sat, 27 Jan 2024 00:46:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 00:46:17 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Sat, 27 Jan 2024 00:46:18 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 00:46:19 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Sat, 27 Jan 2024 00:46:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 00:46:30 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 00:46:30 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 00:46:31 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 00:46:32 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 00:46:33 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 00:46:33 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 00:46:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 00:46:34 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 00:46:35 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 00:46:35 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 00:46:35 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 00:46:36 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 00:46:38 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 00:46:38 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Sat, 27 Jan 2024 00:46:39 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 27 Jan 2024 00:46:39 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 00:46:40 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 00:46:40 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81748eb2d91ddafcd4b1ca527c95cf8cf89284695f14401c2cc8acd7969395bb`  
		Last Modified: Sat, 27 Jan 2024 00:48:04 GMT  
		Size: 64.6 MB (64579264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf942b637bc9207c8720b87cc801a4af821ba35e45677b0f5760a7c851a2809`  
		Last Modified: Sat, 27 Jan 2024 00:47:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33975b85bc5b6dd65b6cdfb9e671aab31ba683f634cb4cf49341237d9d1e82f`  
		Last Modified: Sat, 27 Jan 2024 00:47:50 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10adf0a89cf55e2033dde3a5f200e6c809cc77ad4e5b688ccb8a64f368a7557`  
		Last Modified: Sat, 27 Jan 2024 00:47:50 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee718d66a8524ac51cb741d1a1d288335522c0718939fee3d38c78e6602e9dc6`  
		Last Modified: Sat, 27 Jan 2024 00:47:50 GMT  
		Size: 3.7 KB (3658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17d18445c8d1d27a1db26b2a82206a974753597fb070d4fdf5f1201ff95b0dd`  
		Last Modified: Sat, 27 Jan 2024 00:47:57 GMT  
		Size: 120.2 MB (120176617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ceadac487decd31a02b412b60034325c9bbae0360d650e180def13c8d0102bb`  
		Last Modified: Sat, 27 Jan 2024 00:47:50 GMT  
		Size: 5.7 KB (5655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
