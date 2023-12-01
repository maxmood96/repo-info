<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `bonita`

-	[`bonita:2022.1`](#bonita20221)
-	[`bonita:2022.1-u0`](#bonita20221-u0)
-	[`bonita:2022.2`](#bonita20222)
-	[`bonita:2022.2-u0`](#bonita20222-u0)
-	[`bonita:2023.1`](#bonita20231)
-	[`bonita:2023.1-u0`](#bonita20231-u0)
-	[`bonita:2023.2`](#bonita20232)
-	[`bonita:2023.2-u0`](#bonita20232-u0)
-	[`bonita:7.14`](#bonita714)
-	[`bonita:7.14.0`](#bonita7140)
-	[`bonita:7.15`](#bonita715)
-	[`bonita:7.15.0`](#bonita7150)
-	[`bonita:8.0`](#bonita80)
-	[`bonita:8.0.0`](#bonita800)
-	[`bonita:9.0`](#bonita90)
-	[`bonita:9.0.0`](#bonita900)
-	[`bonita:latest`](#bonitalatest)

## `bonita:2022.1`

```console
$ docker pull bonita@sha256:d1b1430817862e6ec2c949a051a0bf7bb3e3ed8bb217b964f2c46b5e3bf36b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1` - linux; amd64

```console
$ docker pull bonita@sha256:0b39da2fce5692d9da1a30cd501131b6e38f2d8d7f4c454d567cc82254bbf15a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177053705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0258731632cbf3e4b1f4b3d21d34872a63e5ac8e9186f1e7f51a2b1c06bf5788`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:11 GMT
ADD file:aa1af71c6b66d2dddee4797236e3e526f70f904ab641cc0dd6b41445cfedf9b4 in / 
# Thu, 30 Nov 2023 23:23:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:29:01 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 06:29:05 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Dec 2023 06:29:05 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 06:29:06 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 06:29:06 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 06:29:06 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 06:29:06 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 06:29:07 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 06:29:07 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Dec 2023 06:29:07 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 06:29:08 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 06:29:08 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Fri, 01 Dec 2023 06:29:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 06:29:14 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 06:29:14 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 06:29:14 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 06:29:14 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 06:29:14 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 06:29:14 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 06:29:14 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 06:29:14 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 06:29:15 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 06:29:15 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 06:29:15 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 06:29:15 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 06:29:15 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 06:29:15 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 06:29:15 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 06:29:15 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 06:29:15 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d078792c4f9122259f14b539315bd92cbd9490ed73e08255a08689122b143108`  
		Last Modified: Thu, 30 Nov 2023 23:23:58 GMT  
		Size: 2.8 MB (2826431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720903041dfea054157f0f8e02d15889b59f92d15f9373669cd656f3da7773a2`  
		Last Modified: Fri, 01 Dec 2023 06:30:32 GMT  
		Size: 57.5 MB (57526462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8b1eade48114cc215530a5fd3a710d8fd96acf48c364a2a691960d59d8faea`  
		Last Modified: Fri, 01 Dec 2023 06:30:25 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ea7f05601ee30eed9e05274375dac2ea16463d74aeb50d58abba1ffdeddaf9`  
		Last Modified: Fri, 01 Dec 2023 06:30:23 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0815d21a20ea1c45842afcdde1de40d39337db7094e8f61a0e11ccf9c5a0a10d`  
		Last Modified: Fri, 01 Dec 2023 06:30:23 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8766f4cf6def8bec3f20e5f90c9da59325373efb39992b084ec0c7c3bf4f4f18`  
		Last Modified: Fri, 01 Dec 2023 06:30:23 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99052a5d3014117b87fecafd7b0d7cf27cbd3a34fe1d7d85d9fe737830707d94`  
		Last Modified: Fri, 01 Dec 2023 06:30:29 GMT  
		Size: 116.7 MB (116690799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b516060d37ff54116afdc197fc3150f36297f14f8448c709e9cbf458f37447cd`  
		Last Modified: Fri, 01 Dec 2023 06:30:23 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5b2d6e8f90985f1de8f8b28e2a782ba28fc48da05bc65485b3c117791b2f4662
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176271411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca911ae550fef027e875b85611f163a81c7e5df66e509418ea1c699963491e72`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:15 GMT
ADD file:3982c510455cc0ceea8cf8dd0b50b69588e35fd4f84522cb4000582c73781672 in / 
# Thu, 30 Nov 2023 23:11:15 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:20:55 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 07:21:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Dec 2023 07:21:03 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 07:21:03 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 07:21:03 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Dec 2023 07:21:04 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Dec 2023 07:21:04 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Dec 2023 07:21:04 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 07:21:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 07:21:04 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 07:21:04 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 07:21:04 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Fri, 01 Dec 2023 07:21:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 07:21:09 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 07:21:09 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 07:21:09 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 07:21:09 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 07:21:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 07:21:10 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 07:21:10 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 07:21:10 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 07:21:10 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 07:21:10 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 07:21:10 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8bc1ab4b84041d57f21a792410a00820f73fda7efe08bcd2ca6245349a40299d`  
		Last Modified: Thu, 30 Nov 2023 23:12:02 GMT  
		Size: 2.7 MB (2721527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5e6cbcb0fca87ea4c61fb0fc77a95a1b8c482b3257d7e52066502c605068d1`  
		Last Modified: Fri, 01 Dec 2023 07:22:22 GMT  
		Size: 56.8 MB (56849089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0faf7acb59acd13bf013b0078c5f3948b15b31f957f2b5497512f4b3c3b0ba18`  
		Last Modified: Fri, 01 Dec 2023 07:22:16 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef1bb09dff2e07150d1104f4210eed7c8fda7eedbd5b739bb2f0b47b6b6f2d0`  
		Last Modified: Fri, 01 Dec 2023 07:22:14 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41803d4b8416ee3140ef2796b457827220da427dc50cf8db98eb2b7f1d634807`  
		Last Modified: Fri, 01 Dec 2023 07:22:14 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4486bc124197eeea5df6efd4991ecc2fe969e4a50c8ee55370452d85b9f9c418`  
		Last Modified: Fri, 01 Dec 2023 07:22:14 GMT  
		Size: 3.0 KB (3029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc06e6c0fa652cfec6694f1edf2c1bba9471645fd3b10a8223416d08e94514bb`  
		Last Modified: Fri, 01 Dec 2023 07:22:19 GMT  
		Size: 116.7 MB (116690782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e43f009336775c04263616cecdb475be8ee1c617b50ae8fce9129ceaa9b56d8`  
		Last Modified: Fri, 01 Dec 2023 07:22:14 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:068d06940e82702e726661c460e3be27f5d565a7b9f93576990762c035bf664e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172865596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c84db852a7ad8f0d11d7b6dd282f9d5457b0ee7e11adfa999c206549f46be8d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:36 GMT
ADD file:35af09f43b08c93abd4c6b8679d43e8ac40893bf5932c4c21f1bb037f53bb62c in / 
# Thu, 30 Nov 2023 23:19:41 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:28:31 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 05:28:55 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Dec 2023 05:28:59 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 05:29:01 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 05:29:07 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 05:29:12 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 05:29:15 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 05:29:17 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 05:29:24 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 05:29:30 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Dec 2023 05:29:33 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Dec 2023 05:29:34 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Dec 2023 05:29:35 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 05:29:37 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 05:29:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 05:29:49 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 05:29:52 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Fri, 01 Dec 2023 05:30:15 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 05:30:19 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 05:30:20 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 05:30:21 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 05:30:23 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 05:30:24 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 05:30:26 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 05:30:26 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 05:30:26 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 05:30:27 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 05:30:32 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 05:30:34 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 05:30:40 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 05:30:44 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 05:30:45 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 05:30:49 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 05:30:50 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 05:30:51 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:080a2fea3a772fa995cb0b07b4601e7cd57650fa4e8a50866da1de707946d7b3`  
		Last Modified: Thu, 30 Nov 2023 23:20:38 GMT  
		Size: 2.8 MB (2812474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7420ac528be0bd3985f1816f664fcf08a6b7c88d0d09e580515ca1153a86221a`  
		Last Modified: Fri, 01 Dec 2023 05:40:28 GMT  
		Size: 53.4 MB (53352308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eef1b0eab1321b515733639ecd9f305475419760c18cef29e353310cd577313`  
		Last Modified: Fri, 01 Dec 2023 05:40:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d529f71c424cdf78262a4162fcf4336300e28774ea5c4f62a575dfb33d1756`  
		Last Modified: Fri, 01 Dec 2023 05:40:17 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2d0175f87e6ba072091cd2711155ce23dc4db4473b0f2277e2ed297888b030`  
		Last Modified: Fri, 01 Dec 2023 05:40:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58211a662c2e1e63d65ed200a9e16f2442d20bc2edbedd458b612e4b8e421629`  
		Last Modified: Fri, 01 Dec 2023 05:40:17 GMT  
		Size: 3.0 KB (3036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed339e0ee12d30b9e48457389cfd9c9bc6f3e5b42b16b0c9be853eb4b2960688`  
		Last Modified: Fri, 01 Dec 2023 05:40:24 GMT  
		Size: 116.7 MB (116690791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534da3656bc472aaf3c3ab4f6b3dc316c7d886d7ceae90ed93e1b2455f609e14`  
		Last Modified: Fri, 01 Dec 2023 05:40:17 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.1-u0`

```console
$ docker pull bonita@sha256:d1b1430817862e6ec2c949a051a0bf7bb3e3ed8bb217b964f2c46b5e3bf36b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1-u0` - linux; amd64

```console
$ docker pull bonita@sha256:0b39da2fce5692d9da1a30cd501131b6e38f2d8d7f4c454d567cc82254bbf15a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177053705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0258731632cbf3e4b1f4b3d21d34872a63e5ac8e9186f1e7f51a2b1c06bf5788`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:11 GMT
ADD file:aa1af71c6b66d2dddee4797236e3e526f70f904ab641cc0dd6b41445cfedf9b4 in / 
# Thu, 30 Nov 2023 23:23:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:29:01 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 06:29:05 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Dec 2023 06:29:05 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 06:29:06 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 06:29:06 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 06:29:06 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 06:29:06 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 06:29:07 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 06:29:07 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Dec 2023 06:29:07 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 06:29:08 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 06:29:08 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Fri, 01 Dec 2023 06:29:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 06:29:14 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 06:29:14 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 06:29:14 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 06:29:14 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 06:29:14 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 06:29:14 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 06:29:14 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 06:29:14 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 06:29:15 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 06:29:15 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 06:29:15 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 06:29:15 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 06:29:15 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 06:29:15 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 06:29:15 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 06:29:15 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 06:29:15 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d078792c4f9122259f14b539315bd92cbd9490ed73e08255a08689122b143108`  
		Last Modified: Thu, 30 Nov 2023 23:23:58 GMT  
		Size: 2.8 MB (2826431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720903041dfea054157f0f8e02d15889b59f92d15f9373669cd656f3da7773a2`  
		Last Modified: Fri, 01 Dec 2023 06:30:32 GMT  
		Size: 57.5 MB (57526462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8b1eade48114cc215530a5fd3a710d8fd96acf48c364a2a691960d59d8faea`  
		Last Modified: Fri, 01 Dec 2023 06:30:25 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ea7f05601ee30eed9e05274375dac2ea16463d74aeb50d58abba1ffdeddaf9`  
		Last Modified: Fri, 01 Dec 2023 06:30:23 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0815d21a20ea1c45842afcdde1de40d39337db7094e8f61a0e11ccf9c5a0a10d`  
		Last Modified: Fri, 01 Dec 2023 06:30:23 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8766f4cf6def8bec3f20e5f90c9da59325373efb39992b084ec0c7c3bf4f4f18`  
		Last Modified: Fri, 01 Dec 2023 06:30:23 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99052a5d3014117b87fecafd7b0d7cf27cbd3a34fe1d7d85d9fe737830707d94`  
		Last Modified: Fri, 01 Dec 2023 06:30:29 GMT  
		Size: 116.7 MB (116690799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b516060d37ff54116afdc197fc3150f36297f14f8448c709e9cbf458f37447cd`  
		Last Modified: Fri, 01 Dec 2023 06:30:23 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5b2d6e8f90985f1de8f8b28e2a782ba28fc48da05bc65485b3c117791b2f4662
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176271411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca911ae550fef027e875b85611f163a81c7e5df66e509418ea1c699963491e72`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:15 GMT
ADD file:3982c510455cc0ceea8cf8dd0b50b69588e35fd4f84522cb4000582c73781672 in / 
# Thu, 30 Nov 2023 23:11:15 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:20:55 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 07:21:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Dec 2023 07:21:03 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 07:21:03 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 07:21:03 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Dec 2023 07:21:04 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Dec 2023 07:21:04 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Dec 2023 07:21:04 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 07:21:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 07:21:04 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 07:21:04 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 07:21:04 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Fri, 01 Dec 2023 07:21:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 07:21:09 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 07:21:09 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 07:21:09 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 07:21:09 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 07:21:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 07:21:10 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 07:21:10 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 07:21:10 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 07:21:10 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 07:21:10 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 07:21:10 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8bc1ab4b84041d57f21a792410a00820f73fda7efe08bcd2ca6245349a40299d`  
		Last Modified: Thu, 30 Nov 2023 23:12:02 GMT  
		Size: 2.7 MB (2721527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5e6cbcb0fca87ea4c61fb0fc77a95a1b8c482b3257d7e52066502c605068d1`  
		Last Modified: Fri, 01 Dec 2023 07:22:22 GMT  
		Size: 56.8 MB (56849089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0faf7acb59acd13bf013b0078c5f3948b15b31f957f2b5497512f4b3c3b0ba18`  
		Last Modified: Fri, 01 Dec 2023 07:22:16 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef1bb09dff2e07150d1104f4210eed7c8fda7eedbd5b739bb2f0b47b6b6f2d0`  
		Last Modified: Fri, 01 Dec 2023 07:22:14 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41803d4b8416ee3140ef2796b457827220da427dc50cf8db98eb2b7f1d634807`  
		Last Modified: Fri, 01 Dec 2023 07:22:14 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4486bc124197eeea5df6efd4991ecc2fe969e4a50c8ee55370452d85b9f9c418`  
		Last Modified: Fri, 01 Dec 2023 07:22:14 GMT  
		Size: 3.0 KB (3029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc06e6c0fa652cfec6694f1edf2c1bba9471645fd3b10a8223416d08e94514bb`  
		Last Modified: Fri, 01 Dec 2023 07:22:19 GMT  
		Size: 116.7 MB (116690782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e43f009336775c04263616cecdb475be8ee1c617b50ae8fce9129ceaa9b56d8`  
		Last Modified: Fri, 01 Dec 2023 07:22:14 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:068d06940e82702e726661c460e3be27f5d565a7b9f93576990762c035bf664e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172865596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c84db852a7ad8f0d11d7b6dd282f9d5457b0ee7e11adfa999c206549f46be8d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:36 GMT
ADD file:35af09f43b08c93abd4c6b8679d43e8ac40893bf5932c4c21f1bb037f53bb62c in / 
# Thu, 30 Nov 2023 23:19:41 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:28:31 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 05:28:55 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Dec 2023 05:28:59 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 05:29:01 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 05:29:07 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 05:29:12 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 05:29:15 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 05:29:17 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 05:29:24 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 05:29:30 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Dec 2023 05:29:33 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Dec 2023 05:29:34 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Dec 2023 05:29:35 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 05:29:37 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 05:29:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 05:29:49 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 05:29:52 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Fri, 01 Dec 2023 05:30:15 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 05:30:19 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 05:30:20 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 05:30:21 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 05:30:23 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 05:30:24 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 05:30:26 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 05:30:26 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 05:30:26 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 05:30:27 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 05:30:32 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 05:30:34 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 05:30:40 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 05:30:44 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 05:30:45 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 05:30:49 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 05:30:50 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 05:30:51 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:080a2fea3a772fa995cb0b07b4601e7cd57650fa4e8a50866da1de707946d7b3`  
		Last Modified: Thu, 30 Nov 2023 23:20:38 GMT  
		Size: 2.8 MB (2812474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7420ac528be0bd3985f1816f664fcf08a6b7c88d0d09e580515ca1153a86221a`  
		Last Modified: Fri, 01 Dec 2023 05:40:28 GMT  
		Size: 53.4 MB (53352308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eef1b0eab1321b515733639ecd9f305475419760c18cef29e353310cd577313`  
		Last Modified: Fri, 01 Dec 2023 05:40:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d529f71c424cdf78262a4162fcf4336300e28774ea5c4f62a575dfb33d1756`  
		Last Modified: Fri, 01 Dec 2023 05:40:17 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2d0175f87e6ba072091cd2711155ce23dc4db4473b0f2277e2ed297888b030`  
		Last Modified: Fri, 01 Dec 2023 05:40:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58211a662c2e1e63d65ed200a9e16f2442d20bc2edbedd458b612e4b8e421629`  
		Last Modified: Fri, 01 Dec 2023 05:40:17 GMT  
		Size: 3.0 KB (3036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed339e0ee12d30b9e48457389cfd9c9bc6f3e5b42b16b0c9be853eb4b2960688`  
		Last Modified: Fri, 01 Dec 2023 05:40:24 GMT  
		Size: 116.7 MB (116690791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534da3656bc472aaf3c3ab4f6b3dc316c7d886d7ceae90ed93e1b2455f609e14`  
		Last Modified: Fri, 01 Dec 2023 05:40:17 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.2`

```console
$ docker pull bonita@sha256:c0c2f82754fe504249cbbcdf6da14d58e44b7d93c48e229d91195d1c3391f150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.2` - linux; amd64

```console
$ docker pull bonita@sha256:3f2a5f8cfecaeaf44d261a21a77bfa458a2483cdeec432f9eff23378b16e4a57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183640846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e2d2abc2adec54eeb1113166ba8069f9d1cdbd3a6389bc40beb0b9b13af299`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:05 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Thu, 30 Nov 2023 23:23:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:29:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 06:29:22 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 06:29:23 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 06:29:23 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 01 Dec 2023 06:29:24 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 06:29:25 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 06:29:25 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 01 Dec 2023 06:29:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 06:29:31 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 06:29:31 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 06:29:31 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 06:29:31 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 06:29:31 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 06:29:32 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 06:29:32 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 06:29:32 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 06:29:32 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 06:29:33 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 06:29:33 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a7de4dd1fa340a3596f9d87c144afbb221013d7aefe3b7bbee5e0f8c59b41a`  
		Last Modified: Fri, 01 Dec 2023 06:30:54 GMT  
		Size: 61.6 MB (61630058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c4a4f912a26d2f76e4ff02776754e420088c57ce9a2ca5a9b89b8eb620ee44`  
		Last Modified: Fri, 01 Dec 2023 06:30:47 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b79bf571108e3cb631de296157b86f89d6eed4a1eededa3644117f1d85ba78`  
		Last Modified: Fri, 01 Dec 2023 06:30:45 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db28c2c54c787fd6c58d30ad534265bbc1338c02d781d3cfda5c02388a9f8f8`  
		Last Modified: Fri, 01 Dec 2023 06:30:45 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3461a9fee92b21925964cc37dc6bf0a25c9a5c6f924c5cf4962ea1dce1987d7d`  
		Last Modified: Fri, 01 Dec 2023 06:30:45 GMT  
		Size: 3.0 KB (3044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658661c2e2e29e312ee825cee3b35b8d783db9381f0070354cb050f31ad995a1`  
		Last Modified: Fri, 01 Dec 2023 06:30:51 GMT  
		Size: 119.2 MB (119192973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bf11e4b849c7501942c46a5e836fab7ba2f3f2fee7281108ebd82fb495248d`  
		Last Modified: Fri, 01 Dec 2023 06:30:45 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:d47f702a4834ac9a23b879c41aed4849f1a139dcf5c39916efcbd23dea0154bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182784874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0626d39cdc1a9b4ab6f1d99851a09bdaf0da1a668b607118ed2cd62e8b37356e`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:11 GMT
ADD file:1efd26ad638f3c262f37eb81a32e3f026121dcd60479e91c42097bfc8329ed3b in / 
# Thu, 30 Nov 2023 23:11:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:21:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 07:21:19 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 07:21:21 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 07:21:21 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 01 Dec 2023 07:21:22 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 07:21:22 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 07:21:22 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 01 Dec 2023 07:21:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 07:21:27 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 07:21:27 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 07:21:27 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 07:21:27 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 07:21:28 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 07:21:28 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 07:21:28 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 07:21:28 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 07:21:28 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 07:21:28 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 07:21:28 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5362b5901f8a9898f2bcc8eb6c3e6990364aa058617afaae388bdb9f437d3d7e`  
		Last Modified: Thu, 30 Nov 2023 23:11:54 GMT  
		Size: 2.7 MB (2708293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfdfa4a3ddfa0317a5e137139992df18ed494662fe2cc4f5be0247ed5155238`  
		Last Modified: Fri, 01 Dec 2023 07:22:43 GMT  
		Size: 60.9 MB (60873558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29ea4642e8d305ab859fd91f1ce689f57e12ad7630c304d8d9f7ddbfc96c07a`  
		Last Modified: Fri, 01 Dec 2023 07:22:37 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454548b04a05907ccddbb4aa1f7d1f58a91fb1fbc23014dec45bf8277623a1eb`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb7828220892b0903efff7d253cd0beb56715c99199479a4ecc80e9a36ce54b`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8bb0f9bf23bab691b57f756f3c9998ed2474ce674492d761794256d6548fb5`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
		Size: 3.0 KB (3046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f855eea8850dd9cb6c6ed7df85416d77eefbf1f42794b129ec5993ed929668`  
		Last Modified: Fri, 01 Dec 2023 07:22:41 GMT  
		Size: 119.2 MB (119192991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc168c3b2cc1201a16844ebd5288631728bb808d3585998199bca718762b3dc9`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:b5827c5ffbcbae64d6821b4feacb0476e34467277b92b5414f80128caa651859
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179806702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb7a710960b5cab6c75e386f5a69e52630e3a5f6317a1a248548d630359a77b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:25 GMT
ADD file:41dd492ac8086a6a7ae54f70f208d397f81d19c9ada61f7e52b1f678c0e08ae3 in / 
# Thu, 30 Nov 2023 23:19:27 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:31:06 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 05:31:26 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 05:31:31 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 05:31:32 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 05:31:34 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 05:31:35 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 05:31:49 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 05:31:55 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 05:31:57 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 05:32:04 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 01 Dec 2023 05:32:08 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 01 Dec 2023 05:32:11 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 01 Dec 2023 05:32:13 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 05:32:14 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 05:32:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 05:32:32 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 05:32:33 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 01 Dec 2023 05:32:48 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 05:32:56 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 05:33:02 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 05:33:04 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 05:33:04 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 05:33:06 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 05:33:12 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 05:33:19 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 05:33:22 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 05:33:25 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 05:33:36 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 05:33:39 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 05:33:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 05:33:52 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 05:33:55 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 05:34:00 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 05:34:04 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 05:34:05 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ae6fb3870f7991147b39ddb2fee9e659464482f341bd584e2b45ba18fbe5b39d`  
		Last Modified: Thu, 30 Nov 2023 23:20:26 GMT  
		Size: 2.8 MB (2802949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a180d699c8c360717c7eba33d0346981db37ea03c89c0d483ecddafe62bb5066`  
		Last Modified: Fri, 01 Dec 2023 05:40:52 GMT  
		Size: 57.8 MB (57800737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4590040fa20c114ac9f1f795422716f99906b0cb674ffd52dc71368d562ef76e`  
		Last Modified: Fri, 01 Dec 2023 05:40:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ccd8ef1233df0bf4568230ebf74b871c8d1153960acee58e821367107ec68e`  
		Last Modified: Fri, 01 Dec 2023 05:40:42 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119ead57f8cdb954c992554a8622ef32e8f725f5d892211dac7014b418dbf6e8`  
		Last Modified: Fri, 01 Dec 2023 05:40:42 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5278384accac2af10c39fe2289ecb50e9edcf8411cb1d0ba83b6005f303a5a`  
		Last Modified: Fri, 01 Dec 2023 05:40:42 GMT  
		Size: 3.0 KB (3046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e62d2db76ebe310466af4838bedeb78892639f72eb679148a3e4b0955a917e`  
		Last Modified: Fri, 01 Dec 2023 05:40:49 GMT  
		Size: 119.2 MB (119192984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3415f15bcd4e066124af7d9f887e3c4c1814d4990976b5fa0ca155eff1d8aa`  
		Last Modified: Fri, 01 Dec 2023 05:40:42 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.2-u0`

```console
$ docker pull bonita@sha256:c0c2f82754fe504249cbbcdf6da14d58e44b7d93c48e229d91195d1c3391f150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:3f2a5f8cfecaeaf44d261a21a77bfa458a2483cdeec432f9eff23378b16e4a57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183640846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e2d2abc2adec54eeb1113166ba8069f9d1cdbd3a6389bc40beb0b9b13af299`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:05 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Thu, 30 Nov 2023 23:23:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:29:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 06:29:22 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 06:29:23 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 06:29:23 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 01 Dec 2023 06:29:24 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 06:29:25 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 06:29:25 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 01 Dec 2023 06:29:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 06:29:31 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 06:29:31 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 06:29:31 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 06:29:31 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 06:29:31 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 06:29:32 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 06:29:32 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 06:29:32 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 06:29:32 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 06:29:33 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 06:29:33 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a7de4dd1fa340a3596f9d87c144afbb221013d7aefe3b7bbee5e0f8c59b41a`  
		Last Modified: Fri, 01 Dec 2023 06:30:54 GMT  
		Size: 61.6 MB (61630058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c4a4f912a26d2f76e4ff02776754e420088c57ce9a2ca5a9b89b8eb620ee44`  
		Last Modified: Fri, 01 Dec 2023 06:30:47 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b79bf571108e3cb631de296157b86f89d6eed4a1eededa3644117f1d85ba78`  
		Last Modified: Fri, 01 Dec 2023 06:30:45 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db28c2c54c787fd6c58d30ad534265bbc1338c02d781d3cfda5c02388a9f8f8`  
		Last Modified: Fri, 01 Dec 2023 06:30:45 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3461a9fee92b21925964cc37dc6bf0a25c9a5c6f924c5cf4962ea1dce1987d7d`  
		Last Modified: Fri, 01 Dec 2023 06:30:45 GMT  
		Size: 3.0 KB (3044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658661c2e2e29e312ee825cee3b35b8d783db9381f0070354cb050f31ad995a1`  
		Last Modified: Fri, 01 Dec 2023 06:30:51 GMT  
		Size: 119.2 MB (119192973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bf11e4b849c7501942c46a5e836fab7ba2f3f2fee7281108ebd82fb495248d`  
		Last Modified: Fri, 01 Dec 2023 06:30:45 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:d47f702a4834ac9a23b879c41aed4849f1a139dcf5c39916efcbd23dea0154bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182784874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0626d39cdc1a9b4ab6f1d99851a09bdaf0da1a668b607118ed2cd62e8b37356e`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:11 GMT
ADD file:1efd26ad638f3c262f37eb81a32e3f026121dcd60479e91c42097bfc8329ed3b in / 
# Thu, 30 Nov 2023 23:11:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:21:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 07:21:19 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 07:21:21 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 07:21:21 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 01 Dec 2023 07:21:22 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 07:21:22 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 07:21:22 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 01 Dec 2023 07:21:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 07:21:27 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 07:21:27 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 07:21:27 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 07:21:27 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 07:21:28 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 07:21:28 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 07:21:28 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 07:21:28 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 07:21:28 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 07:21:28 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 07:21:28 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5362b5901f8a9898f2bcc8eb6c3e6990364aa058617afaae388bdb9f437d3d7e`  
		Last Modified: Thu, 30 Nov 2023 23:11:54 GMT  
		Size: 2.7 MB (2708293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfdfa4a3ddfa0317a5e137139992df18ed494662fe2cc4f5be0247ed5155238`  
		Last Modified: Fri, 01 Dec 2023 07:22:43 GMT  
		Size: 60.9 MB (60873558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29ea4642e8d305ab859fd91f1ce689f57e12ad7630c304d8d9f7ddbfc96c07a`  
		Last Modified: Fri, 01 Dec 2023 07:22:37 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454548b04a05907ccddbb4aa1f7d1f58a91fb1fbc23014dec45bf8277623a1eb`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb7828220892b0903efff7d253cd0beb56715c99199479a4ecc80e9a36ce54b`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8bb0f9bf23bab691b57f756f3c9998ed2474ce674492d761794256d6548fb5`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
		Size: 3.0 KB (3046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f855eea8850dd9cb6c6ed7df85416d77eefbf1f42794b129ec5993ed929668`  
		Last Modified: Fri, 01 Dec 2023 07:22:41 GMT  
		Size: 119.2 MB (119192991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc168c3b2cc1201a16844ebd5288631728bb808d3585998199bca718762b3dc9`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:b5827c5ffbcbae64d6821b4feacb0476e34467277b92b5414f80128caa651859
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179806702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb7a710960b5cab6c75e386f5a69e52630e3a5f6317a1a248548d630359a77b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:25 GMT
ADD file:41dd492ac8086a6a7ae54f70f208d397f81d19c9ada61f7e52b1f678c0e08ae3 in / 
# Thu, 30 Nov 2023 23:19:27 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:31:06 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 05:31:26 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 05:31:31 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 05:31:32 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 05:31:34 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 05:31:35 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 05:31:49 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 05:31:55 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 05:31:57 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 05:32:04 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 01 Dec 2023 05:32:08 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 01 Dec 2023 05:32:11 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 01 Dec 2023 05:32:13 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 05:32:14 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 05:32:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 05:32:32 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 05:32:33 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 01 Dec 2023 05:32:48 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 05:32:56 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 05:33:02 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 05:33:04 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 05:33:04 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 05:33:06 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 05:33:12 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 05:33:19 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 05:33:22 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 05:33:25 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 05:33:36 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 05:33:39 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 05:33:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 05:33:52 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 05:33:55 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 05:34:00 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 05:34:04 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 05:34:05 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ae6fb3870f7991147b39ddb2fee9e659464482f341bd584e2b45ba18fbe5b39d`  
		Last Modified: Thu, 30 Nov 2023 23:20:26 GMT  
		Size: 2.8 MB (2802949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a180d699c8c360717c7eba33d0346981db37ea03c89c0d483ecddafe62bb5066`  
		Last Modified: Fri, 01 Dec 2023 05:40:52 GMT  
		Size: 57.8 MB (57800737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4590040fa20c114ac9f1f795422716f99906b0cb674ffd52dc71368d562ef76e`  
		Last Modified: Fri, 01 Dec 2023 05:40:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ccd8ef1233df0bf4568230ebf74b871c8d1153960acee58e821367107ec68e`  
		Last Modified: Fri, 01 Dec 2023 05:40:42 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119ead57f8cdb954c992554a8622ef32e8f725f5d892211dac7014b418dbf6e8`  
		Last Modified: Fri, 01 Dec 2023 05:40:42 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5278384accac2af10c39fe2289ecb50e9edcf8411cb1d0ba83b6005f303a5a`  
		Last Modified: Fri, 01 Dec 2023 05:40:42 GMT  
		Size: 3.0 KB (3046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e62d2db76ebe310466af4838bedeb78892639f72eb679148a3e4b0955a917e`  
		Last Modified: Fri, 01 Dec 2023 05:40:49 GMT  
		Size: 119.2 MB (119192984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3415f15bcd4e066124af7d9f887e3c4c1814d4990976b5fa0ca155eff1d8aa`  
		Last Modified: Fri, 01 Dec 2023 05:40:42 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2023.1`

```console
$ docker pull bonita@sha256:595f821ed1906bda1063d6102f3a9388bae83e74e82980ac1166aa8e304f179d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2023.1` - linux; amd64

```console
$ docker pull bonita@sha256:27684b4460a71b658929080fa6440da3414d6ff24344d9dc307fddb0a7e12ec6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183367603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31d2def8ee84ece08cf6db5d4b61eae62b97ce7d4734a4583d69d0ccab2c6825`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:29:35 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 06:29:39 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 06:29:40 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 06:29:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 06:29:41 GMT
ENV BONITA_VERSION=8.0.0
# Fri, 01 Dec 2023 06:29:41 GMT
ENV BRANDING_VERSION=2023.1-u0
# Fri, 01 Dec 2023 06:29:41 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Fri, 01 Dec 2023 06:29:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 06:29:42 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 06:29:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 06:29:42 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 06:29:42 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Fri, 01 Dec 2023 06:29:48 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 06:29:49 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 06:29:49 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 06:29:49 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 06:29:49 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 06:29:49 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 06:29:50 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 06:29:50 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Fri, 01 Dec 2023 06:29:50 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 06:29:50 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 06:29:50 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 06:29:50 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 06:29:50 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d74e11a0112260e7b840d15299041dd0568d302eec189bedd8abb935332ea1`  
		Last Modified: Fri, 01 Dec 2023 06:31:18 GMT  
		Size: 61.8 MB (61797112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42e036991f3a84d939c7c6d48a4ddb89d38194279b5f9ec881066175adcf2e6`  
		Last Modified: Fri, 01 Dec 2023 06:31:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c796a39d096f71a13c40ba1791426c302de88d76d500464883e8cd04d2985324`  
		Last Modified: Fri, 01 Dec 2023 06:31:08 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4baf4b33675b5d662a05df47b3de1f109d8a8dc3d95b632e91082817cac5d22d`  
		Last Modified: Fri, 01 Dec 2023 06:31:08 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658b5f03ae7a4659ee2fb15ea42334cfa233e34e22360c111a053fec4bb6c2ba`  
		Last Modified: Fri, 01 Dec 2023 06:31:08 GMT  
		Size: 3.5 KB (3475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2742b3e147382eda8c208f2c9ba80f96363f8d3b2149b8d97401bc37b69f453f`  
		Last Modified: Fri, 01 Dec 2023 06:31:14 GMT  
		Size: 118.2 MB (118180712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78dae36aa635a5196e661723c089b2c9d84297f0a6cd76fd01834ab319909958`  
		Last Modified: Fri, 01 Dec 2023 06:31:08 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:53363f2aa72cec59d9a702afc3fa426edd50ac4c3b6c59d39cd70410b6838fb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182518550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ea2fac76ce24aa06981d274ce5446591c9452afad8582bc135026e18ba2289`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:07 GMT
ADD file:e5c66967d6570e36da50c9d42dd8f8f55e6c6a65b92c79601ea9e750c076fa2a in / 
# Thu, 30 Nov 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:21:31 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 07:21:34 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 07:21:36 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 07:21:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BONITA_VERSION=8.0.0
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BRANDING_VERSION=2023.1-u0
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Fri, 01 Dec 2023 07:21:37 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 07:21:37 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 07:21:37 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Fri, 01 Dec 2023 07:21:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 07:21:42 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 07:21:42 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 07:21:42 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 07:21:43 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 07:21:43 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 07:21:43 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 07:21:43 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 07:21:43 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Fri, 01 Dec 2023 07:21:43 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 07:21:43 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 07:21:44 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 07:21:44 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 07:21:44 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b8180c93b172865af87a7c0e7e3c8bcb139e0d0c92e19c96467ff2cd4c8919ad`  
		Last Modified: Thu, 30 Nov 2023 23:11:45 GMT  
		Size: 3.3 MB (3258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17510e0ab09797198fef6127cabda527677df530cf6c16d613023485511b5f20`  
		Last Modified: Fri, 01 Dec 2023 07:23:06 GMT  
		Size: 61.1 MB (61069059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6794cf279bea6f7eb4a687b6d18cdafdfcb28a23cac1247613012b1f0a4e80d`  
		Last Modified: Fri, 01 Dec 2023 07:22:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319792810c396c636f3ec7a717a42cbb48763e227e423ebf0d4d93c1d975d4a6`  
		Last Modified: Fri, 01 Dec 2023 07:22:57 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeed99097524233839fe793aa9e2d839106de4b09a9a05bc9c300506db874ad`  
		Last Modified: Fri, 01 Dec 2023 07:22:57 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bebb77c53322de314d781c965f628915bccfd0daddf6c46db4ac7040c7c991`  
		Last Modified: Fri, 01 Dec 2023 07:22:57 GMT  
		Size: 3.5 KB (3477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d9df902eb4c460ed7f99e869f9f6aa757e44c78eb770a60f1686b927870446`  
		Last Modified: Fri, 01 Dec 2023 07:23:02 GMT  
		Size: 118.2 MB (118180680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36d68596a295c7cfbd8fbb7b60126065faa30cc2f19e1736e29acbf123d7e20`  
		Last Modified: Fri, 01 Dec 2023 07:22:57 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:2373cfe2822b0323615cd2d0aca47bba003ddf843d4a5cadfef38708a3baf190
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179562198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae2d8b1f7de69bfc6027007a22cfeb82ba701f811f42e984caee19feeb7babe`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:15 GMT
ADD file:e3eb0ea4f652282ad08228d0d146f33998b9e93641756d780ac0205aa828c070 in / 
# Thu, 30 Nov 2023 23:19:17 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:34:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 05:34:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 05:34:45 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 05:34:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 05:35:01 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 05:35:09 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 05:35:14 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 05:35:16 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 05:35:18 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 05:35:19 GMT
ENV BONITA_VERSION=8.0.0
# Fri, 01 Dec 2023 05:35:21 GMT
ENV BRANDING_VERSION=2023.1-u0
# Fri, 01 Dec 2023 05:35:26 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Fri, 01 Dec 2023 05:35:29 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 05:35:35 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 05:35:38 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 05:35:46 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 05:35:48 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Fri, 01 Dec 2023 05:36:05 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 05:36:14 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 05:36:15 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 05:36:18 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 05:36:23 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 05:36:33 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 05:36:37 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 05:36:39 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 05:36:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 05:36:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 05:36:42 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 05:36:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 05:36:47 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 05:36:52 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 05:36:55 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Fri, 01 Dec 2023 05:36:56 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 05:36:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 05:36:59 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 05:36:59 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 05:37:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c7d387f1f267ea360529df8d70b246f949e1afdb2317cdf84b028cda80a093d1`  
		Last Modified: Thu, 30 Nov 2023 23:20:17 GMT  
		Size: 3.4 MB (3391875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78644523bcfce42d84b446e010aee3442e2b970c87dbe17b0bf6def281c949a5`  
		Last Modified: Fri, 01 Dec 2023 05:41:18 GMT  
		Size: 58.0 MB (57979123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbf4876168f16d5cfe7e004dd600549c9882f62024084cf6025dd18976929e5`  
		Last Modified: Fri, 01 Dec 2023 05:41:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79a5b5a41bc29110bca4445e405d5d1769a3c1e7ef568b1e1da22571c19ab85`  
		Last Modified: Fri, 01 Dec 2023 05:41:07 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55fe42767d60b790259ab149f4d55f6aa4e364d5ba56466e288b83d22e5ff82`  
		Last Modified: Fri, 01 Dec 2023 05:41:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eca127dad012e2e68b066de5c368b4f2e8d0a5799a7ad531ebe5e3af9482bae`  
		Last Modified: Fri, 01 Dec 2023 05:41:07 GMT  
		Size: 3.5 KB (3481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9c3b7a7b97ce37611a9fa9d7286f04bc398cc48945419794a13cf9726eeb77`  
		Last Modified: Fri, 01 Dec 2023 05:41:14 GMT  
		Size: 118.2 MB (118180724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fba0861aef0e1fea57016a45d4cd36a81f1ac6a61982a379693920904ea8d1`  
		Last Modified: Fri, 01 Dec 2023 05:41:07 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2023.1-u0`

```console
$ docker pull bonita@sha256:595f821ed1906bda1063d6102f3a9388bae83e74e82980ac1166aa8e304f179d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2023.1-u0` - linux; amd64

```console
$ docker pull bonita@sha256:27684b4460a71b658929080fa6440da3414d6ff24344d9dc307fddb0a7e12ec6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183367603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31d2def8ee84ece08cf6db5d4b61eae62b97ce7d4734a4583d69d0ccab2c6825`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:29:35 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 06:29:39 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 06:29:40 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 06:29:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 06:29:41 GMT
ENV BONITA_VERSION=8.0.0
# Fri, 01 Dec 2023 06:29:41 GMT
ENV BRANDING_VERSION=2023.1-u0
# Fri, 01 Dec 2023 06:29:41 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Fri, 01 Dec 2023 06:29:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 06:29:42 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 06:29:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 06:29:42 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 06:29:42 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Fri, 01 Dec 2023 06:29:48 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 06:29:49 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 06:29:49 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 06:29:49 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 06:29:49 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 06:29:49 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 06:29:50 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 06:29:50 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Fri, 01 Dec 2023 06:29:50 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 06:29:50 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 06:29:50 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 06:29:50 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 06:29:50 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d74e11a0112260e7b840d15299041dd0568d302eec189bedd8abb935332ea1`  
		Last Modified: Fri, 01 Dec 2023 06:31:18 GMT  
		Size: 61.8 MB (61797112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42e036991f3a84d939c7c6d48a4ddb89d38194279b5f9ec881066175adcf2e6`  
		Last Modified: Fri, 01 Dec 2023 06:31:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c796a39d096f71a13c40ba1791426c302de88d76d500464883e8cd04d2985324`  
		Last Modified: Fri, 01 Dec 2023 06:31:08 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4baf4b33675b5d662a05df47b3de1f109d8a8dc3d95b632e91082817cac5d22d`  
		Last Modified: Fri, 01 Dec 2023 06:31:08 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658b5f03ae7a4659ee2fb15ea42334cfa233e34e22360c111a053fec4bb6c2ba`  
		Last Modified: Fri, 01 Dec 2023 06:31:08 GMT  
		Size: 3.5 KB (3475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2742b3e147382eda8c208f2c9ba80f96363f8d3b2149b8d97401bc37b69f453f`  
		Last Modified: Fri, 01 Dec 2023 06:31:14 GMT  
		Size: 118.2 MB (118180712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78dae36aa635a5196e661723c089b2c9d84297f0a6cd76fd01834ab319909958`  
		Last Modified: Fri, 01 Dec 2023 06:31:08 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:53363f2aa72cec59d9a702afc3fa426edd50ac4c3b6c59d39cd70410b6838fb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182518550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ea2fac76ce24aa06981d274ce5446591c9452afad8582bc135026e18ba2289`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:07 GMT
ADD file:e5c66967d6570e36da50c9d42dd8f8f55e6c6a65b92c79601ea9e750c076fa2a in / 
# Thu, 30 Nov 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:21:31 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 07:21:34 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 07:21:36 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 07:21:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BONITA_VERSION=8.0.0
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BRANDING_VERSION=2023.1-u0
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Fri, 01 Dec 2023 07:21:37 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 07:21:37 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 07:21:37 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Fri, 01 Dec 2023 07:21:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 07:21:42 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 07:21:42 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 07:21:42 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 07:21:43 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 07:21:43 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 07:21:43 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 07:21:43 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 07:21:43 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Fri, 01 Dec 2023 07:21:43 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 07:21:43 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 07:21:44 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 07:21:44 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 07:21:44 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b8180c93b172865af87a7c0e7e3c8bcb139e0d0c92e19c96467ff2cd4c8919ad`  
		Last Modified: Thu, 30 Nov 2023 23:11:45 GMT  
		Size: 3.3 MB (3258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17510e0ab09797198fef6127cabda527677df530cf6c16d613023485511b5f20`  
		Last Modified: Fri, 01 Dec 2023 07:23:06 GMT  
		Size: 61.1 MB (61069059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6794cf279bea6f7eb4a687b6d18cdafdfcb28a23cac1247613012b1f0a4e80d`  
		Last Modified: Fri, 01 Dec 2023 07:22:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319792810c396c636f3ec7a717a42cbb48763e227e423ebf0d4d93c1d975d4a6`  
		Last Modified: Fri, 01 Dec 2023 07:22:57 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeed99097524233839fe793aa9e2d839106de4b09a9a05bc9c300506db874ad`  
		Last Modified: Fri, 01 Dec 2023 07:22:57 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bebb77c53322de314d781c965f628915bccfd0daddf6c46db4ac7040c7c991`  
		Last Modified: Fri, 01 Dec 2023 07:22:57 GMT  
		Size: 3.5 KB (3477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d9df902eb4c460ed7f99e869f9f6aa757e44c78eb770a60f1686b927870446`  
		Last Modified: Fri, 01 Dec 2023 07:23:02 GMT  
		Size: 118.2 MB (118180680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36d68596a295c7cfbd8fbb7b60126065faa30cc2f19e1736e29acbf123d7e20`  
		Last Modified: Fri, 01 Dec 2023 07:22:57 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:2373cfe2822b0323615cd2d0aca47bba003ddf843d4a5cadfef38708a3baf190
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179562198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae2d8b1f7de69bfc6027007a22cfeb82ba701f811f42e984caee19feeb7babe`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:15 GMT
ADD file:e3eb0ea4f652282ad08228d0d146f33998b9e93641756d780ac0205aa828c070 in / 
# Thu, 30 Nov 2023 23:19:17 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:34:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 05:34:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 05:34:45 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 05:34:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 05:35:01 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 05:35:09 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 05:35:14 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 05:35:16 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 05:35:18 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 05:35:19 GMT
ENV BONITA_VERSION=8.0.0
# Fri, 01 Dec 2023 05:35:21 GMT
ENV BRANDING_VERSION=2023.1-u0
# Fri, 01 Dec 2023 05:35:26 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Fri, 01 Dec 2023 05:35:29 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 05:35:35 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 05:35:38 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 05:35:46 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 05:35:48 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Fri, 01 Dec 2023 05:36:05 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 05:36:14 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 05:36:15 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 05:36:18 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 05:36:23 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 05:36:33 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 05:36:37 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 05:36:39 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 05:36:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 05:36:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 05:36:42 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 05:36:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 05:36:47 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 05:36:52 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 05:36:55 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Fri, 01 Dec 2023 05:36:56 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 05:36:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 05:36:59 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 05:36:59 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 05:37:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c7d387f1f267ea360529df8d70b246f949e1afdb2317cdf84b028cda80a093d1`  
		Last Modified: Thu, 30 Nov 2023 23:20:17 GMT  
		Size: 3.4 MB (3391875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78644523bcfce42d84b446e010aee3442e2b970c87dbe17b0bf6def281c949a5`  
		Last Modified: Fri, 01 Dec 2023 05:41:18 GMT  
		Size: 58.0 MB (57979123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbf4876168f16d5cfe7e004dd600549c9882f62024084cf6025dd18976929e5`  
		Last Modified: Fri, 01 Dec 2023 05:41:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79a5b5a41bc29110bca4445e405d5d1769a3c1e7ef568b1e1da22571c19ab85`  
		Last Modified: Fri, 01 Dec 2023 05:41:07 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55fe42767d60b790259ab149f4d55f6aa4e364d5ba56466e288b83d22e5ff82`  
		Last Modified: Fri, 01 Dec 2023 05:41:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eca127dad012e2e68b066de5c368b4f2e8d0a5799a7ad531ebe5e3af9482bae`  
		Last Modified: Fri, 01 Dec 2023 05:41:07 GMT  
		Size: 3.5 KB (3481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9c3b7a7b97ce37611a9fa9d7286f04bc398cc48945419794a13cf9726eeb77`  
		Last Modified: Fri, 01 Dec 2023 05:41:14 GMT  
		Size: 118.2 MB (118180724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fba0861aef0e1fea57016a45d4cd36a81f1ac6a61982a379693920904ea8d1`  
		Last Modified: Fri, 01 Dec 2023 05:41:07 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2023.2`

```console
$ docker pull bonita@sha256:79ace3619e7ca496f76b98433d4ca2047128b714292078dc1272621b82f62d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2023.2` - linux; amd64

```console
$ docker pull bonita@sha256:c2908f6f685ed1f4f19f56c9e93c76b77fcb8a7e0c644449909abc668413d280
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191362756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc511cde66b30fbc95e9d8ac98ed63de355bbfc78c577dc358f5da38bf27fb2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:29:56 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 06:30:00 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Fri, 01 Dec 2023 06:30:00 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 06:30:01 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 06:30:01 GMT
ENV BONITA_VERSION=9.0.0
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BRANDING_VERSION=2023.2-u0
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Fri, 01 Dec 2023 06:30:02 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 06:30:03 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 06:30:03 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Fri, 01 Dec 2023 06:30:08 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 06:30:08 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 06:30:08 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 06:30:09 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 06:30:09 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 06:30:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 06:30:09 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 06:30:09 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 06:30:09 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Fri, 01 Dec 2023 06:30:10 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 06:30:10 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 06:30:10 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 06:30:10 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8b9b9109619bd1c6b81bbc9ce4cecf24a7c2483fa9ecd2f813c0972cf018a0`  
		Last Modified: Fri, 01 Dec 2023 06:31:41 GMT  
		Size: 67.8 MB (67772846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076a1aa334a7b6eef088b4579bea958db5ad822017fe925ce57904a88cbee41d`  
		Last Modified: Fri, 01 Dec 2023 06:31:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d4d210bdf5ed96d7c4ee451e041b794cad6ce92ade9051714deeff815a4fa1`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0aeec3883498c38ebc9b066c4b119e783b7bd43cc90d5a104bf2abe034fa58`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e65d13ed7440987448e4ae294c6aa58f56eb639fc0f608bb1b18f1b6f17640`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee750d61171d80ab6d953bb21293f56e935aebe5e11fd103af20c860f98fd0f1`  
		Last Modified: Fri, 01 Dec 2023 06:31:38 GMT  
		Size: 120.2 MB (120176606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24a6648d8163c0174830c2f9f3af83ce399a9f2d702053a183d5a52bd63524c`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 5.7 KB (5657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:34c10898f477a7221a95893b57de3dcc23d4490708b50c5ff96cc632b7013d7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191218643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6765a28afb0cac1f9e3d96ac4cbf7909d9e495ecdd4597e1b33fe273b733fefc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:21:47 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 07:21:51 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Fri, 01 Dec 2023 07:21:52 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 07:21:53 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 07:21:53 GMT
ENV BONITA_VERSION=9.0.0
# Fri, 01 Dec 2023 07:21:53 GMT
ENV BRANDING_VERSION=2023.2-u0
# Fri, 01 Dec 2023 07:21:53 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Fri, 01 Dec 2023 07:21:53 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 07:21:54 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 07:21:54 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 07:21:54 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 07:21:54 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Fri, 01 Dec 2023 07:21:59 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 07:22:00 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 07:22:00 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 07:22:00 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 07:22:00 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 07:22:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 07:22:01 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 07:22:01 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Fri, 01 Dec 2023 07:22:01 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 07:22:01 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 07:22:01 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 07:22:01 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9d5c4d5cb627eed83e30a9f8cd45148519b03192374c37165c80843b69c944`  
		Last Modified: Fri, 01 Dec 2023 07:23:28 GMT  
		Size: 67.7 MB (67698077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7014c128521a3f66b5ecefcc308f824bc20824823772421ff1f33dfb925b8bec`  
		Last Modified: Fri, 01 Dec 2023 07:23:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efafcd70e05ac8cb6f234da4f4afb662b5e8a56e65f75a3fb2ef8d172ff9fe73`  
		Last Modified: Fri, 01 Dec 2023 07:23:18 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f0efdd3e80a7ce9b04f66c7b25197ef1fa5656cbde2701ddbe23e21f24f81`  
		Last Modified: Fri, 01 Dec 2023 07:23:19 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4b59d5e7c3a436e8fc93baadc97b86294156660fd1022c1f93b2a9df19c092`  
		Last Modified: Fri, 01 Dec 2023 07:23:19 GMT  
		Size: 3.7 KB (3662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25725db729846ddeecbde5b23cf3f50a630732b27528ab4ea00146861c0c652`  
		Last Modified: Fri, 01 Dec 2023 07:23:24 GMT  
		Size: 120.2 MB (120176648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b58edfcda0eaacede3c3479eec06ea1e94e78e26656f43ac07ba44a166466e`  
		Last Modified: Fri, 01 Dec 2023 07:23:19 GMT  
		Size: 5.7 KB (5660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:a5c237bcece8e9b606a8b0c7294b3ee127239e9f95fa53c1a874fc1e9782144d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188065296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d29449c9c83de9b066b19f038a2c6a9743f64575fb284c49120eeb88c2ae50`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:37:11 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 05:37:34 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Fri, 01 Dec 2023 05:37:46 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 05:37:59 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 05:38:02 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 05:38:06 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 05:38:17 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 05:38:19 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 05:38:20 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 05:38:23 GMT
ENV BONITA_VERSION=9.0.0
# Fri, 01 Dec 2023 05:38:31 GMT
ENV BRANDING_VERSION=2023.2-u0
# Fri, 01 Dec 2023 05:38:38 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Fri, 01 Dec 2023 05:38:39 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 05:38:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 05:38:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 05:38:44 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 05:38:46 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Fri, 01 Dec 2023 05:39:10 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 05:39:24 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 05:39:26 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 05:39:27 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 05:39:29 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 05:39:30 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 05:39:30 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 05:39:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 05:39:37 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 05:39:39 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 05:39:40 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 05:39:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 05:39:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 05:39:44 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 05:39:45 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Fri, 01 Dec 2023 05:39:48 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 05:39:49 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 05:39:50 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 05:39:53 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1961607fe5674a8c1d805e44043c42bc4d67207e8faa4682b39b0c49b43310e0`  
		Last Modified: Fri, 01 Dec 2023 05:41:46 GMT  
		Size: 64.5 MB (64529445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d614eed5744f8547076db82ed976402325dba784ec4c2c56cd248e47d53f4ac7`  
		Last Modified: Fri, 01 Dec 2023 05:41:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f07fc2f3ef9e4b1ed2a727a7cee1b9cbbef7de8d3c65005435ef0e60b9cc643`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285d196f9f4d8fee5af9cc323fe3c0049ad86ad90736d5ee2137c2140a4e2667`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9473fbfd57624b832051d7be0d392ff859a5e86d692e7be88011b788829b206`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 3.7 KB (3666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ed5c1bc2b798e9f662cbf850403e06c4ae710ae6da02ed9a6f18057103c034`  
		Last Modified: Fri, 01 Dec 2023 05:41:41 GMT  
		Size: 120.2 MB (120176637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e548ee928063c5ebfbb873bb80b33c0c748cf199c09672584f7a2046f5c7b7d1`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 5.7 KB (5661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2023.2-u0`

```console
$ docker pull bonita@sha256:79ace3619e7ca496f76b98433d4ca2047128b714292078dc1272621b82f62d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2023.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:c2908f6f685ed1f4f19f56c9e93c76b77fcb8a7e0c644449909abc668413d280
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191362756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc511cde66b30fbc95e9d8ac98ed63de355bbfc78c577dc358f5da38bf27fb2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:29:56 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 06:30:00 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Fri, 01 Dec 2023 06:30:00 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 06:30:01 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 06:30:01 GMT
ENV BONITA_VERSION=9.0.0
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BRANDING_VERSION=2023.2-u0
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Fri, 01 Dec 2023 06:30:02 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 06:30:03 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 06:30:03 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Fri, 01 Dec 2023 06:30:08 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 06:30:08 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 06:30:08 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 06:30:09 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 06:30:09 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 06:30:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 06:30:09 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 06:30:09 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 06:30:09 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Fri, 01 Dec 2023 06:30:10 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 06:30:10 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 06:30:10 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 06:30:10 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8b9b9109619bd1c6b81bbc9ce4cecf24a7c2483fa9ecd2f813c0972cf018a0`  
		Last Modified: Fri, 01 Dec 2023 06:31:41 GMT  
		Size: 67.8 MB (67772846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076a1aa334a7b6eef088b4579bea958db5ad822017fe925ce57904a88cbee41d`  
		Last Modified: Fri, 01 Dec 2023 06:31:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d4d210bdf5ed96d7c4ee451e041b794cad6ce92ade9051714deeff815a4fa1`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0aeec3883498c38ebc9b066c4b119e783b7bd43cc90d5a104bf2abe034fa58`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e65d13ed7440987448e4ae294c6aa58f56eb639fc0f608bb1b18f1b6f17640`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee750d61171d80ab6d953bb21293f56e935aebe5e11fd103af20c860f98fd0f1`  
		Last Modified: Fri, 01 Dec 2023 06:31:38 GMT  
		Size: 120.2 MB (120176606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24a6648d8163c0174830c2f9f3af83ce399a9f2d702053a183d5a52bd63524c`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 5.7 KB (5657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:34c10898f477a7221a95893b57de3dcc23d4490708b50c5ff96cc632b7013d7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191218643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6765a28afb0cac1f9e3d96ac4cbf7909d9e495ecdd4597e1b33fe273b733fefc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:21:47 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 07:21:51 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Fri, 01 Dec 2023 07:21:52 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 07:21:53 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 07:21:53 GMT
ENV BONITA_VERSION=9.0.0
# Fri, 01 Dec 2023 07:21:53 GMT
ENV BRANDING_VERSION=2023.2-u0
# Fri, 01 Dec 2023 07:21:53 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Fri, 01 Dec 2023 07:21:53 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 07:21:54 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 07:21:54 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 07:21:54 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 07:21:54 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Fri, 01 Dec 2023 07:21:59 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 07:22:00 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 07:22:00 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 07:22:00 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 07:22:00 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 07:22:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 07:22:01 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 07:22:01 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Fri, 01 Dec 2023 07:22:01 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 07:22:01 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 07:22:01 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 07:22:01 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9d5c4d5cb627eed83e30a9f8cd45148519b03192374c37165c80843b69c944`  
		Last Modified: Fri, 01 Dec 2023 07:23:28 GMT  
		Size: 67.7 MB (67698077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7014c128521a3f66b5ecefcc308f824bc20824823772421ff1f33dfb925b8bec`  
		Last Modified: Fri, 01 Dec 2023 07:23:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efafcd70e05ac8cb6f234da4f4afb662b5e8a56e65f75a3fb2ef8d172ff9fe73`  
		Last Modified: Fri, 01 Dec 2023 07:23:18 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f0efdd3e80a7ce9b04f66c7b25197ef1fa5656cbde2701ddbe23e21f24f81`  
		Last Modified: Fri, 01 Dec 2023 07:23:19 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4b59d5e7c3a436e8fc93baadc97b86294156660fd1022c1f93b2a9df19c092`  
		Last Modified: Fri, 01 Dec 2023 07:23:19 GMT  
		Size: 3.7 KB (3662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25725db729846ddeecbde5b23cf3f50a630732b27528ab4ea00146861c0c652`  
		Last Modified: Fri, 01 Dec 2023 07:23:24 GMT  
		Size: 120.2 MB (120176648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b58edfcda0eaacede3c3479eec06ea1e94e78e26656f43ac07ba44a166466e`  
		Last Modified: Fri, 01 Dec 2023 07:23:19 GMT  
		Size: 5.7 KB (5660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:a5c237bcece8e9b606a8b0c7294b3ee127239e9f95fa53c1a874fc1e9782144d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188065296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d29449c9c83de9b066b19f038a2c6a9743f64575fb284c49120eeb88c2ae50`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:37:11 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 05:37:34 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Fri, 01 Dec 2023 05:37:46 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 05:37:59 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 05:38:02 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 05:38:06 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 05:38:17 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 05:38:19 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 05:38:20 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 05:38:23 GMT
ENV BONITA_VERSION=9.0.0
# Fri, 01 Dec 2023 05:38:31 GMT
ENV BRANDING_VERSION=2023.2-u0
# Fri, 01 Dec 2023 05:38:38 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Fri, 01 Dec 2023 05:38:39 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 05:38:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 05:38:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 05:38:44 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 05:38:46 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Fri, 01 Dec 2023 05:39:10 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 05:39:24 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 05:39:26 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 05:39:27 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 05:39:29 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 05:39:30 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 05:39:30 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 05:39:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 05:39:37 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 05:39:39 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 05:39:40 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 05:39:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 05:39:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 05:39:44 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 05:39:45 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Fri, 01 Dec 2023 05:39:48 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 05:39:49 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 05:39:50 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 05:39:53 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1961607fe5674a8c1d805e44043c42bc4d67207e8faa4682b39b0c49b43310e0`  
		Last Modified: Fri, 01 Dec 2023 05:41:46 GMT  
		Size: 64.5 MB (64529445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d614eed5744f8547076db82ed976402325dba784ec4c2c56cd248e47d53f4ac7`  
		Last Modified: Fri, 01 Dec 2023 05:41:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f07fc2f3ef9e4b1ed2a727a7cee1b9cbbef7de8d3c65005435ef0e60b9cc643`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285d196f9f4d8fee5af9cc323fe3c0049ad86ad90736d5ee2137c2140a4e2667`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9473fbfd57624b832051d7be0d392ff859a5e86d692e7be88011b788829b206`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 3.7 KB (3666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ed5c1bc2b798e9f662cbf850403e06c4ae710ae6da02ed9a6f18057103c034`  
		Last Modified: Fri, 01 Dec 2023 05:41:41 GMT  
		Size: 120.2 MB (120176637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e548ee928063c5ebfbb873bb80b33c0c748cf199c09672584f7a2046f5c7b7d1`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 5.7 KB (5661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14`

```console
$ docker pull bonita@sha256:d1b1430817862e6ec2c949a051a0bf7bb3e3ed8bb217b964f2c46b5e3bf36b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14` - linux; amd64

```console
$ docker pull bonita@sha256:0b39da2fce5692d9da1a30cd501131b6e38f2d8d7f4c454d567cc82254bbf15a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177053705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0258731632cbf3e4b1f4b3d21d34872a63e5ac8e9186f1e7f51a2b1c06bf5788`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:11 GMT
ADD file:aa1af71c6b66d2dddee4797236e3e526f70f904ab641cc0dd6b41445cfedf9b4 in / 
# Thu, 30 Nov 2023 23:23:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:29:01 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 06:29:05 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Dec 2023 06:29:05 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 06:29:06 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 06:29:06 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 06:29:06 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 06:29:06 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 06:29:07 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 06:29:07 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Dec 2023 06:29:07 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 06:29:08 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 06:29:08 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Fri, 01 Dec 2023 06:29:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 06:29:14 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 06:29:14 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 06:29:14 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 06:29:14 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 06:29:14 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 06:29:14 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 06:29:14 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 06:29:14 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 06:29:15 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 06:29:15 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 06:29:15 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 06:29:15 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 06:29:15 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 06:29:15 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 06:29:15 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 06:29:15 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 06:29:15 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d078792c4f9122259f14b539315bd92cbd9490ed73e08255a08689122b143108`  
		Last Modified: Thu, 30 Nov 2023 23:23:58 GMT  
		Size: 2.8 MB (2826431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720903041dfea054157f0f8e02d15889b59f92d15f9373669cd656f3da7773a2`  
		Last Modified: Fri, 01 Dec 2023 06:30:32 GMT  
		Size: 57.5 MB (57526462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8b1eade48114cc215530a5fd3a710d8fd96acf48c364a2a691960d59d8faea`  
		Last Modified: Fri, 01 Dec 2023 06:30:25 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ea7f05601ee30eed9e05274375dac2ea16463d74aeb50d58abba1ffdeddaf9`  
		Last Modified: Fri, 01 Dec 2023 06:30:23 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0815d21a20ea1c45842afcdde1de40d39337db7094e8f61a0e11ccf9c5a0a10d`  
		Last Modified: Fri, 01 Dec 2023 06:30:23 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8766f4cf6def8bec3f20e5f90c9da59325373efb39992b084ec0c7c3bf4f4f18`  
		Last Modified: Fri, 01 Dec 2023 06:30:23 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99052a5d3014117b87fecafd7b0d7cf27cbd3a34fe1d7d85d9fe737830707d94`  
		Last Modified: Fri, 01 Dec 2023 06:30:29 GMT  
		Size: 116.7 MB (116690799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b516060d37ff54116afdc197fc3150f36297f14f8448c709e9cbf458f37447cd`  
		Last Modified: Fri, 01 Dec 2023 06:30:23 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5b2d6e8f90985f1de8f8b28e2a782ba28fc48da05bc65485b3c117791b2f4662
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176271411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca911ae550fef027e875b85611f163a81c7e5df66e509418ea1c699963491e72`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:15 GMT
ADD file:3982c510455cc0ceea8cf8dd0b50b69588e35fd4f84522cb4000582c73781672 in / 
# Thu, 30 Nov 2023 23:11:15 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:20:55 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 07:21:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Dec 2023 07:21:03 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 07:21:03 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 07:21:03 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Dec 2023 07:21:04 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Dec 2023 07:21:04 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Dec 2023 07:21:04 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 07:21:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 07:21:04 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 07:21:04 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 07:21:04 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Fri, 01 Dec 2023 07:21:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 07:21:09 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 07:21:09 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 07:21:09 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 07:21:09 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 07:21:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 07:21:10 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 07:21:10 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 07:21:10 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 07:21:10 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 07:21:10 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 07:21:10 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8bc1ab4b84041d57f21a792410a00820f73fda7efe08bcd2ca6245349a40299d`  
		Last Modified: Thu, 30 Nov 2023 23:12:02 GMT  
		Size: 2.7 MB (2721527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5e6cbcb0fca87ea4c61fb0fc77a95a1b8c482b3257d7e52066502c605068d1`  
		Last Modified: Fri, 01 Dec 2023 07:22:22 GMT  
		Size: 56.8 MB (56849089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0faf7acb59acd13bf013b0078c5f3948b15b31f957f2b5497512f4b3c3b0ba18`  
		Last Modified: Fri, 01 Dec 2023 07:22:16 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef1bb09dff2e07150d1104f4210eed7c8fda7eedbd5b739bb2f0b47b6b6f2d0`  
		Last Modified: Fri, 01 Dec 2023 07:22:14 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41803d4b8416ee3140ef2796b457827220da427dc50cf8db98eb2b7f1d634807`  
		Last Modified: Fri, 01 Dec 2023 07:22:14 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4486bc124197eeea5df6efd4991ecc2fe969e4a50c8ee55370452d85b9f9c418`  
		Last Modified: Fri, 01 Dec 2023 07:22:14 GMT  
		Size: 3.0 KB (3029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc06e6c0fa652cfec6694f1edf2c1bba9471645fd3b10a8223416d08e94514bb`  
		Last Modified: Fri, 01 Dec 2023 07:22:19 GMT  
		Size: 116.7 MB (116690782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e43f009336775c04263616cecdb475be8ee1c617b50ae8fce9129ceaa9b56d8`  
		Last Modified: Fri, 01 Dec 2023 07:22:14 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; ppc64le

```console
$ docker pull bonita@sha256:068d06940e82702e726661c460e3be27f5d565a7b9f93576990762c035bf664e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172865596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c84db852a7ad8f0d11d7b6dd282f9d5457b0ee7e11adfa999c206549f46be8d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:36 GMT
ADD file:35af09f43b08c93abd4c6b8679d43e8ac40893bf5932c4c21f1bb037f53bb62c in / 
# Thu, 30 Nov 2023 23:19:41 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:28:31 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 05:28:55 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Dec 2023 05:28:59 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 05:29:01 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 05:29:07 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 05:29:12 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 05:29:15 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 05:29:17 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 05:29:24 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 05:29:30 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Dec 2023 05:29:33 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Dec 2023 05:29:34 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Dec 2023 05:29:35 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 05:29:37 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 05:29:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 05:29:49 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 05:29:52 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Fri, 01 Dec 2023 05:30:15 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 05:30:19 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 05:30:20 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 05:30:21 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 05:30:23 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 05:30:24 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 05:30:26 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 05:30:26 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 05:30:26 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 05:30:27 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 05:30:32 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 05:30:34 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 05:30:40 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 05:30:44 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 05:30:45 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 05:30:49 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 05:30:50 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 05:30:51 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:080a2fea3a772fa995cb0b07b4601e7cd57650fa4e8a50866da1de707946d7b3`  
		Last Modified: Thu, 30 Nov 2023 23:20:38 GMT  
		Size: 2.8 MB (2812474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7420ac528be0bd3985f1816f664fcf08a6b7c88d0d09e580515ca1153a86221a`  
		Last Modified: Fri, 01 Dec 2023 05:40:28 GMT  
		Size: 53.4 MB (53352308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eef1b0eab1321b515733639ecd9f305475419760c18cef29e353310cd577313`  
		Last Modified: Fri, 01 Dec 2023 05:40:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d529f71c424cdf78262a4162fcf4336300e28774ea5c4f62a575dfb33d1756`  
		Last Modified: Fri, 01 Dec 2023 05:40:17 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2d0175f87e6ba072091cd2711155ce23dc4db4473b0f2277e2ed297888b030`  
		Last Modified: Fri, 01 Dec 2023 05:40:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58211a662c2e1e63d65ed200a9e16f2442d20bc2edbedd458b612e4b8e421629`  
		Last Modified: Fri, 01 Dec 2023 05:40:17 GMT  
		Size: 3.0 KB (3036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed339e0ee12d30b9e48457389cfd9c9bc6f3e5b42b16b0c9be853eb4b2960688`  
		Last Modified: Fri, 01 Dec 2023 05:40:24 GMT  
		Size: 116.7 MB (116690791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534da3656bc472aaf3c3ab4f6b3dc316c7d886d7ceae90ed93e1b2455f609e14`  
		Last Modified: Fri, 01 Dec 2023 05:40:17 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14.0`

```console
$ docker pull bonita@sha256:d1b1430817862e6ec2c949a051a0bf7bb3e3ed8bb217b964f2c46b5e3bf36b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14.0` - linux; amd64

```console
$ docker pull bonita@sha256:0b39da2fce5692d9da1a30cd501131b6e38f2d8d7f4c454d567cc82254bbf15a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177053705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0258731632cbf3e4b1f4b3d21d34872a63e5ac8e9186f1e7f51a2b1c06bf5788`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:11 GMT
ADD file:aa1af71c6b66d2dddee4797236e3e526f70f904ab641cc0dd6b41445cfedf9b4 in / 
# Thu, 30 Nov 2023 23:23:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:29:01 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 06:29:05 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Dec 2023 06:29:05 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 06:29:06 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 06:29:06 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 06:29:06 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 06:29:06 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 06:29:07 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 06:29:07 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Dec 2023 06:29:07 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 06:29:07 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 06:29:08 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 06:29:08 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Fri, 01 Dec 2023 06:29:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 06:29:14 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 06:29:14 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 06:29:14 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 06:29:14 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 06:29:14 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 06:29:14 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 06:29:14 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 06:29:14 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 06:29:15 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 06:29:15 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 06:29:15 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 06:29:15 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 06:29:15 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 06:29:15 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 06:29:15 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 06:29:15 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 06:29:15 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d078792c4f9122259f14b539315bd92cbd9490ed73e08255a08689122b143108`  
		Last Modified: Thu, 30 Nov 2023 23:23:58 GMT  
		Size: 2.8 MB (2826431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720903041dfea054157f0f8e02d15889b59f92d15f9373669cd656f3da7773a2`  
		Last Modified: Fri, 01 Dec 2023 06:30:32 GMT  
		Size: 57.5 MB (57526462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8b1eade48114cc215530a5fd3a710d8fd96acf48c364a2a691960d59d8faea`  
		Last Modified: Fri, 01 Dec 2023 06:30:25 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ea7f05601ee30eed9e05274375dac2ea16463d74aeb50d58abba1ffdeddaf9`  
		Last Modified: Fri, 01 Dec 2023 06:30:23 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0815d21a20ea1c45842afcdde1de40d39337db7094e8f61a0e11ccf9c5a0a10d`  
		Last Modified: Fri, 01 Dec 2023 06:30:23 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8766f4cf6def8bec3f20e5f90c9da59325373efb39992b084ec0c7c3bf4f4f18`  
		Last Modified: Fri, 01 Dec 2023 06:30:23 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99052a5d3014117b87fecafd7b0d7cf27cbd3a34fe1d7d85d9fe737830707d94`  
		Last Modified: Fri, 01 Dec 2023 06:30:29 GMT  
		Size: 116.7 MB (116690799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b516060d37ff54116afdc197fc3150f36297f14f8448c709e9cbf458f37447cd`  
		Last Modified: Fri, 01 Dec 2023 06:30:23 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5b2d6e8f90985f1de8f8b28e2a782ba28fc48da05bc65485b3c117791b2f4662
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176271411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca911ae550fef027e875b85611f163a81c7e5df66e509418ea1c699963491e72`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:15 GMT
ADD file:3982c510455cc0ceea8cf8dd0b50b69588e35fd4f84522cb4000582c73781672 in / 
# Thu, 30 Nov 2023 23:11:15 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:20:55 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 07:21:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Dec 2023 07:21:03 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 07:21:03 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 07:21:03 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 07:21:03 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Dec 2023 07:21:04 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Dec 2023 07:21:04 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Dec 2023 07:21:04 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 07:21:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 07:21:04 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 07:21:04 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 07:21:04 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Fri, 01 Dec 2023 07:21:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 07:21:09 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 07:21:09 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 07:21:09 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 07:21:09 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 07:21:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 07:21:10 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 07:21:10 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 07:21:10 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 07:21:10 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 07:21:10 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 07:21:10 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 07:21:10 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8bc1ab4b84041d57f21a792410a00820f73fda7efe08bcd2ca6245349a40299d`  
		Last Modified: Thu, 30 Nov 2023 23:12:02 GMT  
		Size: 2.7 MB (2721527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5e6cbcb0fca87ea4c61fb0fc77a95a1b8c482b3257d7e52066502c605068d1`  
		Last Modified: Fri, 01 Dec 2023 07:22:22 GMT  
		Size: 56.8 MB (56849089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0faf7acb59acd13bf013b0078c5f3948b15b31f957f2b5497512f4b3c3b0ba18`  
		Last Modified: Fri, 01 Dec 2023 07:22:16 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef1bb09dff2e07150d1104f4210eed7c8fda7eedbd5b739bb2f0b47b6b6f2d0`  
		Last Modified: Fri, 01 Dec 2023 07:22:14 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41803d4b8416ee3140ef2796b457827220da427dc50cf8db98eb2b7f1d634807`  
		Last Modified: Fri, 01 Dec 2023 07:22:14 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4486bc124197eeea5df6efd4991ecc2fe969e4a50c8ee55370452d85b9f9c418`  
		Last Modified: Fri, 01 Dec 2023 07:22:14 GMT  
		Size: 3.0 KB (3029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc06e6c0fa652cfec6694f1edf2c1bba9471645fd3b10a8223416d08e94514bb`  
		Last Modified: Fri, 01 Dec 2023 07:22:19 GMT  
		Size: 116.7 MB (116690782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e43f009336775c04263616cecdb475be8ee1c617b50ae8fce9129ceaa9b56d8`  
		Last Modified: Fri, 01 Dec 2023 07:22:14 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:068d06940e82702e726661c460e3be27f5d565a7b9f93576990762c035bf664e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172865596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c84db852a7ad8f0d11d7b6dd282f9d5457b0ee7e11adfa999c206549f46be8d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:36 GMT
ADD file:35af09f43b08c93abd4c6b8679d43e8ac40893bf5932c4c21f1bb037f53bb62c in / 
# Thu, 30 Nov 2023 23:19:41 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:28:31 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 05:28:55 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Dec 2023 05:28:59 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 05:29:01 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 05:29:07 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 05:29:12 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 05:29:15 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 05:29:17 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 05:29:24 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 05:29:30 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Dec 2023 05:29:33 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Dec 2023 05:29:34 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Dec 2023 05:29:35 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 05:29:37 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 05:29:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Dec 2023 05:29:49 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 05:29:52 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Fri, 01 Dec 2023 05:30:15 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 05:30:19 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 05:30:20 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 05:30:21 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 05:30:23 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 05:30:24 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 05:30:26 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 05:30:26 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 05:30:26 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 05:30:27 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 05:30:32 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 05:30:34 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 05:30:40 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 05:30:44 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 05:30:45 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 05:30:49 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 05:30:50 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 05:30:51 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:080a2fea3a772fa995cb0b07b4601e7cd57650fa4e8a50866da1de707946d7b3`  
		Last Modified: Thu, 30 Nov 2023 23:20:38 GMT  
		Size: 2.8 MB (2812474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7420ac528be0bd3985f1816f664fcf08a6b7c88d0d09e580515ca1153a86221a`  
		Last Modified: Fri, 01 Dec 2023 05:40:28 GMT  
		Size: 53.4 MB (53352308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eef1b0eab1321b515733639ecd9f305475419760c18cef29e353310cd577313`  
		Last Modified: Fri, 01 Dec 2023 05:40:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d529f71c424cdf78262a4162fcf4336300e28774ea5c4f62a575dfb33d1756`  
		Last Modified: Fri, 01 Dec 2023 05:40:17 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2d0175f87e6ba072091cd2711155ce23dc4db4473b0f2277e2ed297888b030`  
		Last Modified: Fri, 01 Dec 2023 05:40:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58211a662c2e1e63d65ed200a9e16f2442d20bc2edbedd458b612e4b8e421629`  
		Last Modified: Fri, 01 Dec 2023 05:40:17 GMT  
		Size: 3.0 KB (3036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed339e0ee12d30b9e48457389cfd9c9bc6f3e5b42b16b0c9be853eb4b2960688`  
		Last Modified: Fri, 01 Dec 2023 05:40:24 GMT  
		Size: 116.7 MB (116690791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534da3656bc472aaf3c3ab4f6b3dc316c7d886d7ceae90ed93e1b2455f609e14`  
		Last Modified: Fri, 01 Dec 2023 05:40:17 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.15`

```console
$ docker pull bonita@sha256:c0c2f82754fe504249cbbcdf6da14d58e44b7d93c48e229d91195d1c3391f150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.15` - linux; amd64

```console
$ docker pull bonita@sha256:3f2a5f8cfecaeaf44d261a21a77bfa458a2483cdeec432f9eff23378b16e4a57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183640846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e2d2abc2adec54eeb1113166ba8069f9d1cdbd3a6389bc40beb0b9b13af299`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:05 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Thu, 30 Nov 2023 23:23:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:29:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 06:29:22 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 06:29:23 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 06:29:23 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 01 Dec 2023 06:29:24 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 06:29:25 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 06:29:25 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 01 Dec 2023 06:29:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 06:29:31 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 06:29:31 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 06:29:31 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 06:29:31 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 06:29:31 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 06:29:32 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 06:29:32 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 06:29:32 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 06:29:32 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 06:29:33 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 06:29:33 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a7de4dd1fa340a3596f9d87c144afbb221013d7aefe3b7bbee5e0f8c59b41a`  
		Last Modified: Fri, 01 Dec 2023 06:30:54 GMT  
		Size: 61.6 MB (61630058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c4a4f912a26d2f76e4ff02776754e420088c57ce9a2ca5a9b89b8eb620ee44`  
		Last Modified: Fri, 01 Dec 2023 06:30:47 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b79bf571108e3cb631de296157b86f89d6eed4a1eededa3644117f1d85ba78`  
		Last Modified: Fri, 01 Dec 2023 06:30:45 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db28c2c54c787fd6c58d30ad534265bbc1338c02d781d3cfda5c02388a9f8f8`  
		Last Modified: Fri, 01 Dec 2023 06:30:45 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3461a9fee92b21925964cc37dc6bf0a25c9a5c6f924c5cf4962ea1dce1987d7d`  
		Last Modified: Fri, 01 Dec 2023 06:30:45 GMT  
		Size: 3.0 KB (3044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658661c2e2e29e312ee825cee3b35b8d783db9381f0070354cb050f31ad995a1`  
		Last Modified: Fri, 01 Dec 2023 06:30:51 GMT  
		Size: 119.2 MB (119192973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bf11e4b849c7501942c46a5e836fab7ba2f3f2fee7281108ebd82fb495248d`  
		Last Modified: Fri, 01 Dec 2023 06:30:45 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:d47f702a4834ac9a23b879c41aed4849f1a139dcf5c39916efcbd23dea0154bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182784874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0626d39cdc1a9b4ab6f1d99851a09bdaf0da1a668b607118ed2cd62e8b37356e`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:11 GMT
ADD file:1efd26ad638f3c262f37eb81a32e3f026121dcd60479e91c42097bfc8329ed3b in / 
# Thu, 30 Nov 2023 23:11:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:21:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 07:21:19 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 07:21:21 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 07:21:21 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 01 Dec 2023 07:21:22 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 07:21:22 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 07:21:22 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 01 Dec 2023 07:21:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 07:21:27 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 07:21:27 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 07:21:27 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 07:21:27 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 07:21:28 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 07:21:28 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 07:21:28 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 07:21:28 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 07:21:28 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 07:21:28 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 07:21:28 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5362b5901f8a9898f2bcc8eb6c3e6990364aa058617afaae388bdb9f437d3d7e`  
		Last Modified: Thu, 30 Nov 2023 23:11:54 GMT  
		Size: 2.7 MB (2708293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfdfa4a3ddfa0317a5e137139992df18ed494662fe2cc4f5be0247ed5155238`  
		Last Modified: Fri, 01 Dec 2023 07:22:43 GMT  
		Size: 60.9 MB (60873558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29ea4642e8d305ab859fd91f1ce689f57e12ad7630c304d8d9f7ddbfc96c07a`  
		Last Modified: Fri, 01 Dec 2023 07:22:37 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454548b04a05907ccddbb4aa1f7d1f58a91fb1fbc23014dec45bf8277623a1eb`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb7828220892b0903efff7d253cd0beb56715c99199479a4ecc80e9a36ce54b`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8bb0f9bf23bab691b57f756f3c9998ed2474ce674492d761794256d6548fb5`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
		Size: 3.0 KB (3046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f855eea8850dd9cb6c6ed7df85416d77eefbf1f42794b129ec5993ed929668`  
		Last Modified: Fri, 01 Dec 2023 07:22:41 GMT  
		Size: 119.2 MB (119192991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc168c3b2cc1201a16844ebd5288631728bb808d3585998199bca718762b3dc9`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15` - linux; ppc64le

```console
$ docker pull bonita@sha256:b5827c5ffbcbae64d6821b4feacb0476e34467277b92b5414f80128caa651859
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179806702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb7a710960b5cab6c75e386f5a69e52630e3a5f6317a1a248548d630359a77b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:25 GMT
ADD file:41dd492ac8086a6a7ae54f70f208d397f81d19c9ada61f7e52b1f678c0e08ae3 in / 
# Thu, 30 Nov 2023 23:19:27 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:31:06 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 05:31:26 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 05:31:31 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 05:31:32 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 05:31:34 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 05:31:35 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 05:31:49 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 05:31:55 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 05:31:57 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 05:32:04 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 01 Dec 2023 05:32:08 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 01 Dec 2023 05:32:11 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 01 Dec 2023 05:32:13 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 05:32:14 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 05:32:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 05:32:32 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 05:32:33 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 01 Dec 2023 05:32:48 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 05:32:56 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 05:33:02 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 05:33:04 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 05:33:04 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 05:33:06 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 05:33:12 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 05:33:19 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 05:33:22 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 05:33:25 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 05:33:36 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 05:33:39 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 05:33:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 05:33:52 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 05:33:55 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 05:34:00 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 05:34:04 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 05:34:05 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ae6fb3870f7991147b39ddb2fee9e659464482f341bd584e2b45ba18fbe5b39d`  
		Last Modified: Thu, 30 Nov 2023 23:20:26 GMT  
		Size: 2.8 MB (2802949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a180d699c8c360717c7eba33d0346981db37ea03c89c0d483ecddafe62bb5066`  
		Last Modified: Fri, 01 Dec 2023 05:40:52 GMT  
		Size: 57.8 MB (57800737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4590040fa20c114ac9f1f795422716f99906b0cb674ffd52dc71368d562ef76e`  
		Last Modified: Fri, 01 Dec 2023 05:40:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ccd8ef1233df0bf4568230ebf74b871c8d1153960acee58e821367107ec68e`  
		Last Modified: Fri, 01 Dec 2023 05:40:42 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119ead57f8cdb954c992554a8622ef32e8f725f5d892211dac7014b418dbf6e8`  
		Last Modified: Fri, 01 Dec 2023 05:40:42 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5278384accac2af10c39fe2289ecb50e9edcf8411cb1d0ba83b6005f303a5a`  
		Last Modified: Fri, 01 Dec 2023 05:40:42 GMT  
		Size: 3.0 KB (3046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e62d2db76ebe310466af4838bedeb78892639f72eb679148a3e4b0955a917e`  
		Last Modified: Fri, 01 Dec 2023 05:40:49 GMT  
		Size: 119.2 MB (119192984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3415f15bcd4e066124af7d9f887e3c4c1814d4990976b5fa0ca155eff1d8aa`  
		Last Modified: Fri, 01 Dec 2023 05:40:42 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.15.0`

```console
$ docker pull bonita@sha256:c0c2f82754fe504249cbbcdf6da14d58e44b7d93c48e229d91195d1c3391f150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.15.0` - linux; amd64

```console
$ docker pull bonita@sha256:3f2a5f8cfecaeaf44d261a21a77bfa458a2483cdeec432f9eff23378b16e4a57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183640846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e2d2abc2adec54eeb1113166ba8069f9d1cdbd3a6389bc40beb0b9b13af299`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:05 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Thu, 30 Nov 2023 23:23:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:29:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 06:29:22 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 06:29:23 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 06:29:23 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 06:29:24 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 01 Dec 2023 06:29:24 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 06:29:24 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 06:29:25 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 06:29:25 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 01 Dec 2023 06:29:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 06:29:31 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 06:29:31 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 06:29:31 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 06:29:31 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 06:29:31 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 06:29:32 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 06:29:32 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 06:29:32 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 06:29:32 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 06:29:32 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 06:29:33 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 06:29:33 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a7de4dd1fa340a3596f9d87c144afbb221013d7aefe3b7bbee5e0f8c59b41a`  
		Last Modified: Fri, 01 Dec 2023 06:30:54 GMT  
		Size: 61.6 MB (61630058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c4a4f912a26d2f76e4ff02776754e420088c57ce9a2ca5a9b89b8eb620ee44`  
		Last Modified: Fri, 01 Dec 2023 06:30:47 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b79bf571108e3cb631de296157b86f89d6eed4a1eededa3644117f1d85ba78`  
		Last Modified: Fri, 01 Dec 2023 06:30:45 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db28c2c54c787fd6c58d30ad534265bbc1338c02d781d3cfda5c02388a9f8f8`  
		Last Modified: Fri, 01 Dec 2023 06:30:45 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3461a9fee92b21925964cc37dc6bf0a25c9a5c6f924c5cf4962ea1dce1987d7d`  
		Last Modified: Fri, 01 Dec 2023 06:30:45 GMT  
		Size: 3.0 KB (3044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658661c2e2e29e312ee825cee3b35b8d783db9381f0070354cb050f31ad995a1`  
		Last Modified: Fri, 01 Dec 2023 06:30:51 GMT  
		Size: 119.2 MB (119192973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bf11e4b849c7501942c46a5e836fab7ba2f3f2fee7281108ebd82fb495248d`  
		Last Modified: Fri, 01 Dec 2023 06:30:45 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:d47f702a4834ac9a23b879c41aed4849f1a139dcf5c39916efcbd23dea0154bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182784874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0626d39cdc1a9b4ab6f1d99851a09bdaf0da1a668b607118ed2cd62e8b37356e`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:11 GMT
ADD file:1efd26ad638f3c262f37eb81a32e3f026121dcd60479e91c42097bfc8329ed3b in / 
# Thu, 30 Nov 2023 23:11:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:21:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 07:21:19 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 07:21:21 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 07:21:21 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 07:21:21 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 01 Dec 2023 07:21:22 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 07:21:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 07:21:22 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 07:21:22 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 01 Dec 2023 07:21:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 07:21:27 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 07:21:27 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 07:21:27 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 07:21:27 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 07:21:28 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 07:21:28 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 07:21:28 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 07:21:28 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 07:21:28 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 07:21:28 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 07:21:28 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 07:21:28 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5362b5901f8a9898f2bcc8eb6c3e6990364aa058617afaae388bdb9f437d3d7e`  
		Last Modified: Thu, 30 Nov 2023 23:11:54 GMT  
		Size: 2.7 MB (2708293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfdfa4a3ddfa0317a5e137139992df18ed494662fe2cc4f5be0247ed5155238`  
		Last Modified: Fri, 01 Dec 2023 07:22:43 GMT  
		Size: 60.9 MB (60873558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29ea4642e8d305ab859fd91f1ce689f57e12ad7630c304d8d9f7ddbfc96c07a`  
		Last Modified: Fri, 01 Dec 2023 07:22:37 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454548b04a05907ccddbb4aa1f7d1f58a91fb1fbc23014dec45bf8277623a1eb`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb7828220892b0903efff7d253cd0beb56715c99199479a4ecc80e9a36ce54b`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8bb0f9bf23bab691b57f756f3c9998ed2474ce674492d761794256d6548fb5`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
		Size: 3.0 KB (3046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f855eea8850dd9cb6c6ed7df85416d77eefbf1f42794b129ec5993ed929668`  
		Last Modified: Fri, 01 Dec 2023 07:22:41 GMT  
		Size: 119.2 MB (119192991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc168c3b2cc1201a16844ebd5288631728bb808d3585998199bca718762b3dc9`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:b5827c5ffbcbae64d6821b4feacb0476e34467277b92b5414f80128caa651859
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179806702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb7a710960b5cab6c75e386f5a69e52630e3a5f6317a1a248548d630359a77b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:25 GMT
ADD file:41dd492ac8086a6a7ae54f70f208d397f81d19c9ada61f7e52b1f678c0e08ae3 in / 
# Thu, 30 Nov 2023 23:19:27 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:31:06 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 05:31:26 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 05:31:31 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 05:31:32 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 05:31:34 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 05:31:35 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 05:31:49 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 05:31:55 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 05:31:57 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 05:32:04 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 01 Dec 2023 05:32:08 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 01 Dec 2023 05:32:11 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 01 Dec 2023 05:32:13 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 05:32:14 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 05:32:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 01 Dec 2023 05:32:32 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 05:32:33 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 01 Dec 2023 05:32:48 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 05:32:56 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 05:33:02 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 05:33:04 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 05:33:04 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 05:33:06 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 05:33:12 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 05:33:19 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 05:33:22 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 05:33:25 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 05:33:36 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 05:33:39 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 05:33:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 05:33:52 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 05:33:55 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 05:34:00 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 05:34:04 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 05:34:05 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ae6fb3870f7991147b39ddb2fee9e659464482f341bd584e2b45ba18fbe5b39d`  
		Last Modified: Thu, 30 Nov 2023 23:20:26 GMT  
		Size: 2.8 MB (2802949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a180d699c8c360717c7eba33d0346981db37ea03c89c0d483ecddafe62bb5066`  
		Last Modified: Fri, 01 Dec 2023 05:40:52 GMT  
		Size: 57.8 MB (57800737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4590040fa20c114ac9f1f795422716f99906b0cb674ffd52dc71368d562ef76e`  
		Last Modified: Fri, 01 Dec 2023 05:40:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ccd8ef1233df0bf4568230ebf74b871c8d1153960acee58e821367107ec68e`  
		Last Modified: Fri, 01 Dec 2023 05:40:42 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119ead57f8cdb954c992554a8622ef32e8f725f5d892211dac7014b418dbf6e8`  
		Last Modified: Fri, 01 Dec 2023 05:40:42 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5278384accac2af10c39fe2289ecb50e9edcf8411cb1d0ba83b6005f303a5a`  
		Last Modified: Fri, 01 Dec 2023 05:40:42 GMT  
		Size: 3.0 KB (3046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e62d2db76ebe310466af4838bedeb78892639f72eb679148a3e4b0955a917e`  
		Last Modified: Fri, 01 Dec 2023 05:40:49 GMT  
		Size: 119.2 MB (119192984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3415f15bcd4e066124af7d9f887e3c4c1814d4990976b5fa0ca155eff1d8aa`  
		Last Modified: Fri, 01 Dec 2023 05:40:42 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:8.0`

```console
$ docker pull bonita@sha256:595f821ed1906bda1063d6102f3a9388bae83e74e82980ac1166aa8e304f179d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:8.0` - linux; amd64

```console
$ docker pull bonita@sha256:27684b4460a71b658929080fa6440da3414d6ff24344d9dc307fddb0a7e12ec6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183367603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31d2def8ee84ece08cf6db5d4b61eae62b97ce7d4734a4583d69d0ccab2c6825`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:29:35 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 06:29:39 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 06:29:40 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 06:29:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 06:29:41 GMT
ENV BONITA_VERSION=8.0.0
# Fri, 01 Dec 2023 06:29:41 GMT
ENV BRANDING_VERSION=2023.1-u0
# Fri, 01 Dec 2023 06:29:41 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Fri, 01 Dec 2023 06:29:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 06:29:42 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 06:29:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 06:29:42 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 06:29:42 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Fri, 01 Dec 2023 06:29:48 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 06:29:49 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 06:29:49 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 06:29:49 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 06:29:49 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 06:29:49 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 06:29:50 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 06:29:50 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Fri, 01 Dec 2023 06:29:50 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 06:29:50 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 06:29:50 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 06:29:50 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 06:29:50 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d74e11a0112260e7b840d15299041dd0568d302eec189bedd8abb935332ea1`  
		Last Modified: Fri, 01 Dec 2023 06:31:18 GMT  
		Size: 61.8 MB (61797112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42e036991f3a84d939c7c6d48a4ddb89d38194279b5f9ec881066175adcf2e6`  
		Last Modified: Fri, 01 Dec 2023 06:31:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c796a39d096f71a13c40ba1791426c302de88d76d500464883e8cd04d2985324`  
		Last Modified: Fri, 01 Dec 2023 06:31:08 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4baf4b33675b5d662a05df47b3de1f109d8a8dc3d95b632e91082817cac5d22d`  
		Last Modified: Fri, 01 Dec 2023 06:31:08 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658b5f03ae7a4659ee2fb15ea42334cfa233e34e22360c111a053fec4bb6c2ba`  
		Last Modified: Fri, 01 Dec 2023 06:31:08 GMT  
		Size: 3.5 KB (3475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2742b3e147382eda8c208f2c9ba80f96363f8d3b2149b8d97401bc37b69f453f`  
		Last Modified: Fri, 01 Dec 2023 06:31:14 GMT  
		Size: 118.2 MB (118180712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78dae36aa635a5196e661723c089b2c9d84297f0a6cd76fd01834ab319909958`  
		Last Modified: Fri, 01 Dec 2023 06:31:08 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:8.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:53363f2aa72cec59d9a702afc3fa426edd50ac4c3b6c59d39cd70410b6838fb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182518550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ea2fac76ce24aa06981d274ce5446591c9452afad8582bc135026e18ba2289`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:07 GMT
ADD file:e5c66967d6570e36da50c9d42dd8f8f55e6c6a65b92c79601ea9e750c076fa2a in / 
# Thu, 30 Nov 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:21:31 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 07:21:34 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 07:21:36 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 07:21:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BONITA_VERSION=8.0.0
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BRANDING_VERSION=2023.1-u0
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Fri, 01 Dec 2023 07:21:37 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 07:21:37 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 07:21:37 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Fri, 01 Dec 2023 07:21:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 07:21:42 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 07:21:42 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 07:21:42 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 07:21:43 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 07:21:43 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 07:21:43 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 07:21:43 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 07:21:43 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Fri, 01 Dec 2023 07:21:43 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 07:21:43 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 07:21:44 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 07:21:44 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 07:21:44 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b8180c93b172865af87a7c0e7e3c8bcb139e0d0c92e19c96467ff2cd4c8919ad`  
		Last Modified: Thu, 30 Nov 2023 23:11:45 GMT  
		Size: 3.3 MB (3258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17510e0ab09797198fef6127cabda527677df530cf6c16d613023485511b5f20`  
		Last Modified: Fri, 01 Dec 2023 07:23:06 GMT  
		Size: 61.1 MB (61069059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6794cf279bea6f7eb4a687b6d18cdafdfcb28a23cac1247613012b1f0a4e80d`  
		Last Modified: Fri, 01 Dec 2023 07:22:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319792810c396c636f3ec7a717a42cbb48763e227e423ebf0d4d93c1d975d4a6`  
		Last Modified: Fri, 01 Dec 2023 07:22:57 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeed99097524233839fe793aa9e2d839106de4b09a9a05bc9c300506db874ad`  
		Last Modified: Fri, 01 Dec 2023 07:22:57 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bebb77c53322de314d781c965f628915bccfd0daddf6c46db4ac7040c7c991`  
		Last Modified: Fri, 01 Dec 2023 07:22:57 GMT  
		Size: 3.5 KB (3477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d9df902eb4c460ed7f99e869f9f6aa757e44c78eb770a60f1686b927870446`  
		Last Modified: Fri, 01 Dec 2023 07:23:02 GMT  
		Size: 118.2 MB (118180680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36d68596a295c7cfbd8fbb7b60126065faa30cc2f19e1736e29acbf123d7e20`  
		Last Modified: Fri, 01 Dec 2023 07:22:57 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:8.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:2373cfe2822b0323615cd2d0aca47bba003ddf843d4a5cadfef38708a3baf190
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179562198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae2d8b1f7de69bfc6027007a22cfeb82ba701f811f42e984caee19feeb7babe`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:15 GMT
ADD file:e3eb0ea4f652282ad08228d0d146f33998b9e93641756d780ac0205aa828c070 in / 
# Thu, 30 Nov 2023 23:19:17 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:34:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 05:34:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 05:34:45 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 05:34:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 05:35:01 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 05:35:09 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 05:35:14 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 05:35:16 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 05:35:18 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 05:35:19 GMT
ENV BONITA_VERSION=8.0.0
# Fri, 01 Dec 2023 05:35:21 GMT
ENV BRANDING_VERSION=2023.1-u0
# Fri, 01 Dec 2023 05:35:26 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Fri, 01 Dec 2023 05:35:29 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 05:35:35 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 05:35:38 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 05:35:46 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 05:35:48 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Fri, 01 Dec 2023 05:36:05 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 05:36:14 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 05:36:15 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 05:36:18 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 05:36:23 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 05:36:33 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 05:36:37 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 05:36:39 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 05:36:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 05:36:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 05:36:42 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 05:36:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 05:36:47 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 05:36:52 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 05:36:55 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Fri, 01 Dec 2023 05:36:56 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 05:36:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 05:36:59 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 05:36:59 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 05:37:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c7d387f1f267ea360529df8d70b246f949e1afdb2317cdf84b028cda80a093d1`  
		Last Modified: Thu, 30 Nov 2023 23:20:17 GMT  
		Size: 3.4 MB (3391875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78644523bcfce42d84b446e010aee3442e2b970c87dbe17b0bf6def281c949a5`  
		Last Modified: Fri, 01 Dec 2023 05:41:18 GMT  
		Size: 58.0 MB (57979123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbf4876168f16d5cfe7e004dd600549c9882f62024084cf6025dd18976929e5`  
		Last Modified: Fri, 01 Dec 2023 05:41:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79a5b5a41bc29110bca4445e405d5d1769a3c1e7ef568b1e1da22571c19ab85`  
		Last Modified: Fri, 01 Dec 2023 05:41:07 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55fe42767d60b790259ab149f4d55f6aa4e364d5ba56466e288b83d22e5ff82`  
		Last Modified: Fri, 01 Dec 2023 05:41:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eca127dad012e2e68b066de5c368b4f2e8d0a5799a7ad531ebe5e3af9482bae`  
		Last Modified: Fri, 01 Dec 2023 05:41:07 GMT  
		Size: 3.5 KB (3481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9c3b7a7b97ce37611a9fa9d7286f04bc398cc48945419794a13cf9726eeb77`  
		Last Modified: Fri, 01 Dec 2023 05:41:14 GMT  
		Size: 118.2 MB (118180724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fba0861aef0e1fea57016a45d4cd36a81f1ac6a61982a379693920904ea8d1`  
		Last Modified: Fri, 01 Dec 2023 05:41:07 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:8.0.0`

```console
$ docker pull bonita@sha256:595f821ed1906bda1063d6102f3a9388bae83e74e82980ac1166aa8e304f179d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:8.0.0` - linux; amd64

```console
$ docker pull bonita@sha256:27684b4460a71b658929080fa6440da3414d6ff24344d9dc307fddb0a7e12ec6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183367603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31d2def8ee84ece08cf6db5d4b61eae62b97ce7d4734a4583d69d0ccab2c6825`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:29:35 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 06:29:39 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 06:29:40 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 06:29:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 06:29:41 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 06:29:41 GMT
ENV BONITA_VERSION=8.0.0
# Fri, 01 Dec 2023 06:29:41 GMT
ENV BRANDING_VERSION=2023.1-u0
# Fri, 01 Dec 2023 06:29:41 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Fri, 01 Dec 2023 06:29:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 06:29:42 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 06:29:42 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 06:29:42 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 06:29:42 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Fri, 01 Dec 2023 06:29:48 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 06:29:49 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 06:29:49 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 06:29:49 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 06:29:49 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 06:29:49 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 06:29:49 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 06:29:50 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 06:29:50 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Fri, 01 Dec 2023 06:29:50 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 06:29:50 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 06:29:50 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 06:29:50 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 06:29:50 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d74e11a0112260e7b840d15299041dd0568d302eec189bedd8abb935332ea1`  
		Last Modified: Fri, 01 Dec 2023 06:31:18 GMT  
		Size: 61.8 MB (61797112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42e036991f3a84d939c7c6d48a4ddb89d38194279b5f9ec881066175adcf2e6`  
		Last Modified: Fri, 01 Dec 2023 06:31:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c796a39d096f71a13c40ba1791426c302de88d76d500464883e8cd04d2985324`  
		Last Modified: Fri, 01 Dec 2023 06:31:08 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4baf4b33675b5d662a05df47b3de1f109d8a8dc3d95b632e91082817cac5d22d`  
		Last Modified: Fri, 01 Dec 2023 06:31:08 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658b5f03ae7a4659ee2fb15ea42334cfa233e34e22360c111a053fec4bb6c2ba`  
		Last Modified: Fri, 01 Dec 2023 06:31:08 GMT  
		Size: 3.5 KB (3475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2742b3e147382eda8c208f2c9ba80f96363f8d3b2149b8d97401bc37b69f453f`  
		Last Modified: Fri, 01 Dec 2023 06:31:14 GMT  
		Size: 118.2 MB (118180712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78dae36aa635a5196e661723c089b2c9d84297f0a6cd76fd01834ab319909958`  
		Last Modified: Fri, 01 Dec 2023 06:31:08 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:8.0.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:53363f2aa72cec59d9a702afc3fa426edd50ac4c3b6c59d39cd70410b6838fb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182518550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ea2fac76ce24aa06981d274ce5446591c9452afad8582bc135026e18ba2289`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:07 GMT
ADD file:e5c66967d6570e36da50c9d42dd8f8f55e6c6a65b92c79601ea9e750c076fa2a in / 
# Thu, 30 Nov 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:21:31 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 07:21:34 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 07:21:36 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 07:21:36 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 07:21:36 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BONITA_VERSION=8.0.0
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BRANDING_VERSION=2023.1-u0
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Fri, 01 Dec 2023 07:21:37 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 07:21:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 07:21:37 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 07:21:37 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Fri, 01 Dec 2023 07:21:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 07:21:42 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 07:21:42 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 07:21:42 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 07:21:43 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 07:21:43 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 07:21:43 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 07:21:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 07:21:43 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 07:21:43 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Fri, 01 Dec 2023 07:21:43 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 07:21:43 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 07:21:44 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 07:21:44 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 07:21:44 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b8180c93b172865af87a7c0e7e3c8bcb139e0d0c92e19c96467ff2cd4c8919ad`  
		Last Modified: Thu, 30 Nov 2023 23:11:45 GMT  
		Size: 3.3 MB (3258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17510e0ab09797198fef6127cabda527677df530cf6c16d613023485511b5f20`  
		Last Modified: Fri, 01 Dec 2023 07:23:06 GMT  
		Size: 61.1 MB (61069059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6794cf279bea6f7eb4a687b6d18cdafdfcb28a23cac1247613012b1f0a4e80d`  
		Last Modified: Fri, 01 Dec 2023 07:22:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319792810c396c636f3ec7a717a42cbb48763e227e423ebf0d4d93c1d975d4a6`  
		Last Modified: Fri, 01 Dec 2023 07:22:57 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeed99097524233839fe793aa9e2d839106de4b09a9a05bc9c300506db874ad`  
		Last Modified: Fri, 01 Dec 2023 07:22:57 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bebb77c53322de314d781c965f628915bccfd0daddf6c46db4ac7040c7c991`  
		Last Modified: Fri, 01 Dec 2023 07:22:57 GMT  
		Size: 3.5 KB (3477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d9df902eb4c460ed7f99e869f9f6aa757e44c78eb770a60f1686b927870446`  
		Last Modified: Fri, 01 Dec 2023 07:23:02 GMT  
		Size: 118.2 MB (118180680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36d68596a295c7cfbd8fbb7b60126065faa30cc2f19e1736e29acbf123d7e20`  
		Last Modified: Fri, 01 Dec 2023 07:22:57 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:8.0.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:2373cfe2822b0323615cd2d0aca47bba003ddf843d4a5cadfef38708a3baf190
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179562198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae2d8b1f7de69bfc6027007a22cfeb82ba701f811f42e984caee19feeb7babe`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:15 GMT
ADD file:e3eb0ea4f652282ad08228d0d146f33998b9e93641756d780ac0205aa828c070 in / 
# Thu, 30 Nov 2023 23:19:17 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:34:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 05:34:37 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 01 Dec 2023 05:34:45 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 05:34:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 05:35:01 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 05:35:09 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 05:35:14 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 05:35:16 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 05:35:18 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 05:35:19 GMT
ENV BONITA_VERSION=8.0.0
# Fri, 01 Dec 2023 05:35:21 GMT
ENV BRANDING_VERSION=2023.1-u0
# Fri, 01 Dec 2023 05:35:26 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Fri, 01 Dec 2023 05:35:29 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 05:35:35 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 05:35:38 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Fri, 01 Dec 2023 05:35:46 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 05:35:48 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Fri, 01 Dec 2023 05:36:05 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 05:36:14 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 05:36:15 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 05:36:18 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 05:36:23 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 05:36:33 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 05:36:37 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 05:36:39 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 05:36:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 05:36:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 05:36:42 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 05:36:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 05:36:47 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 05:36:52 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 05:36:55 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Fri, 01 Dec 2023 05:36:56 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Dec 2023 05:36:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 05:36:59 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 05:36:59 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 05:37:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c7d387f1f267ea360529df8d70b246f949e1afdb2317cdf84b028cda80a093d1`  
		Last Modified: Thu, 30 Nov 2023 23:20:17 GMT  
		Size: 3.4 MB (3391875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78644523bcfce42d84b446e010aee3442e2b970c87dbe17b0bf6def281c949a5`  
		Last Modified: Fri, 01 Dec 2023 05:41:18 GMT  
		Size: 58.0 MB (57979123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbf4876168f16d5cfe7e004dd600549c9882f62024084cf6025dd18976929e5`  
		Last Modified: Fri, 01 Dec 2023 05:41:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79a5b5a41bc29110bca4445e405d5d1769a3c1e7ef568b1e1da22571c19ab85`  
		Last Modified: Fri, 01 Dec 2023 05:41:07 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55fe42767d60b790259ab149f4d55f6aa4e364d5ba56466e288b83d22e5ff82`  
		Last Modified: Fri, 01 Dec 2023 05:41:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eca127dad012e2e68b066de5c368b4f2e8d0a5799a7ad531ebe5e3af9482bae`  
		Last Modified: Fri, 01 Dec 2023 05:41:07 GMT  
		Size: 3.5 KB (3481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9c3b7a7b97ce37611a9fa9d7286f04bc398cc48945419794a13cf9726eeb77`  
		Last Modified: Fri, 01 Dec 2023 05:41:14 GMT  
		Size: 118.2 MB (118180724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fba0861aef0e1fea57016a45d4cd36a81f1ac6a61982a379693920904ea8d1`  
		Last Modified: Fri, 01 Dec 2023 05:41:07 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:9.0`

```console
$ docker pull bonita@sha256:79ace3619e7ca496f76b98433d4ca2047128b714292078dc1272621b82f62d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:9.0` - linux; amd64

```console
$ docker pull bonita@sha256:c2908f6f685ed1f4f19f56c9e93c76b77fcb8a7e0c644449909abc668413d280
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191362756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc511cde66b30fbc95e9d8ac98ed63de355bbfc78c577dc358f5da38bf27fb2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:29:56 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 06:30:00 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Fri, 01 Dec 2023 06:30:00 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 06:30:01 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 06:30:01 GMT
ENV BONITA_VERSION=9.0.0
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BRANDING_VERSION=2023.2-u0
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Fri, 01 Dec 2023 06:30:02 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 06:30:03 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 06:30:03 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Fri, 01 Dec 2023 06:30:08 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 06:30:08 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 06:30:08 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 06:30:09 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 06:30:09 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 06:30:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 06:30:09 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 06:30:09 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 06:30:09 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Fri, 01 Dec 2023 06:30:10 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 06:30:10 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 06:30:10 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 06:30:10 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8b9b9109619bd1c6b81bbc9ce4cecf24a7c2483fa9ecd2f813c0972cf018a0`  
		Last Modified: Fri, 01 Dec 2023 06:31:41 GMT  
		Size: 67.8 MB (67772846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076a1aa334a7b6eef088b4579bea958db5ad822017fe925ce57904a88cbee41d`  
		Last Modified: Fri, 01 Dec 2023 06:31:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d4d210bdf5ed96d7c4ee451e041b794cad6ce92ade9051714deeff815a4fa1`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0aeec3883498c38ebc9b066c4b119e783b7bd43cc90d5a104bf2abe034fa58`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e65d13ed7440987448e4ae294c6aa58f56eb639fc0f608bb1b18f1b6f17640`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee750d61171d80ab6d953bb21293f56e935aebe5e11fd103af20c860f98fd0f1`  
		Last Modified: Fri, 01 Dec 2023 06:31:38 GMT  
		Size: 120.2 MB (120176606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24a6648d8163c0174830c2f9f3af83ce399a9f2d702053a183d5a52bd63524c`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 5.7 KB (5657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:9.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:34c10898f477a7221a95893b57de3dcc23d4490708b50c5ff96cc632b7013d7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191218643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6765a28afb0cac1f9e3d96ac4cbf7909d9e495ecdd4597e1b33fe273b733fefc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:21:47 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 07:21:51 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Fri, 01 Dec 2023 07:21:52 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 07:21:53 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 07:21:53 GMT
ENV BONITA_VERSION=9.0.0
# Fri, 01 Dec 2023 07:21:53 GMT
ENV BRANDING_VERSION=2023.2-u0
# Fri, 01 Dec 2023 07:21:53 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Fri, 01 Dec 2023 07:21:53 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 07:21:54 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 07:21:54 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 07:21:54 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 07:21:54 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Fri, 01 Dec 2023 07:21:59 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 07:22:00 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 07:22:00 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 07:22:00 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 07:22:00 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 07:22:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 07:22:01 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 07:22:01 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Fri, 01 Dec 2023 07:22:01 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 07:22:01 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 07:22:01 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 07:22:01 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9d5c4d5cb627eed83e30a9f8cd45148519b03192374c37165c80843b69c944`  
		Last Modified: Fri, 01 Dec 2023 07:23:28 GMT  
		Size: 67.7 MB (67698077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7014c128521a3f66b5ecefcc308f824bc20824823772421ff1f33dfb925b8bec`  
		Last Modified: Fri, 01 Dec 2023 07:23:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efafcd70e05ac8cb6f234da4f4afb662b5e8a56e65f75a3fb2ef8d172ff9fe73`  
		Last Modified: Fri, 01 Dec 2023 07:23:18 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f0efdd3e80a7ce9b04f66c7b25197ef1fa5656cbde2701ddbe23e21f24f81`  
		Last Modified: Fri, 01 Dec 2023 07:23:19 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4b59d5e7c3a436e8fc93baadc97b86294156660fd1022c1f93b2a9df19c092`  
		Last Modified: Fri, 01 Dec 2023 07:23:19 GMT  
		Size: 3.7 KB (3662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25725db729846ddeecbde5b23cf3f50a630732b27528ab4ea00146861c0c652`  
		Last Modified: Fri, 01 Dec 2023 07:23:24 GMT  
		Size: 120.2 MB (120176648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b58edfcda0eaacede3c3479eec06ea1e94e78e26656f43ac07ba44a166466e`  
		Last Modified: Fri, 01 Dec 2023 07:23:19 GMT  
		Size: 5.7 KB (5660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:9.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:a5c237bcece8e9b606a8b0c7294b3ee127239e9f95fa53c1a874fc1e9782144d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188065296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d29449c9c83de9b066b19f038a2c6a9743f64575fb284c49120eeb88c2ae50`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:37:11 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 05:37:34 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Fri, 01 Dec 2023 05:37:46 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 05:37:59 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 05:38:02 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 05:38:06 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 05:38:17 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 05:38:19 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 05:38:20 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 05:38:23 GMT
ENV BONITA_VERSION=9.0.0
# Fri, 01 Dec 2023 05:38:31 GMT
ENV BRANDING_VERSION=2023.2-u0
# Fri, 01 Dec 2023 05:38:38 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Fri, 01 Dec 2023 05:38:39 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 05:38:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 05:38:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 05:38:44 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 05:38:46 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Fri, 01 Dec 2023 05:39:10 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 05:39:24 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 05:39:26 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 05:39:27 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 05:39:29 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 05:39:30 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 05:39:30 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 05:39:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 05:39:37 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 05:39:39 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 05:39:40 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 05:39:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 05:39:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 05:39:44 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 05:39:45 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Fri, 01 Dec 2023 05:39:48 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 05:39:49 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 05:39:50 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 05:39:53 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1961607fe5674a8c1d805e44043c42bc4d67207e8faa4682b39b0c49b43310e0`  
		Last Modified: Fri, 01 Dec 2023 05:41:46 GMT  
		Size: 64.5 MB (64529445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d614eed5744f8547076db82ed976402325dba784ec4c2c56cd248e47d53f4ac7`  
		Last Modified: Fri, 01 Dec 2023 05:41:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f07fc2f3ef9e4b1ed2a727a7cee1b9cbbef7de8d3c65005435ef0e60b9cc643`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285d196f9f4d8fee5af9cc323fe3c0049ad86ad90736d5ee2137c2140a4e2667`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9473fbfd57624b832051d7be0d392ff859a5e86d692e7be88011b788829b206`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 3.7 KB (3666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ed5c1bc2b798e9f662cbf850403e06c4ae710ae6da02ed9a6f18057103c034`  
		Last Modified: Fri, 01 Dec 2023 05:41:41 GMT  
		Size: 120.2 MB (120176637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e548ee928063c5ebfbb873bb80b33c0c748cf199c09672584f7a2046f5c7b7d1`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 5.7 KB (5661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:9.0.0`

```console
$ docker pull bonita@sha256:79ace3619e7ca496f76b98433d4ca2047128b714292078dc1272621b82f62d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:9.0.0` - linux; amd64

```console
$ docker pull bonita@sha256:c2908f6f685ed1f4f19f56c9e93c76b77fcb8a7e0c644449909abc668413d280
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191362756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc511cde66b30fbc95e9d8ac98ed63de355bbfc78c577dc358f5da38bf27fb2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:29:56 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 06:30:00 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Fri, 01 Dec 2023 06:30:00 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 06:30:01 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 06:30:01 GMT
ENV BONITA_VERSION=9.0.0
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BRANDING_VERSION=2023.2-u0
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Fri, 01 Dec 2023 06:30:02 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 06:30:03 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 06:30:03 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Fri, 01 Dec 2023 06:30:08 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 06:30:08 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 06:30:08 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 06:30:09 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 06:30:09 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 06:30:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 06:30:09 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 06:30:09 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 06:30:09 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Fri, 01 Dec 2023 06:30:10 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 06:30:10 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 06:30:10 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 06:30:10 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8b9b9109619bd1c6b81bbc9ce4cecf24a7c2483fa9ecd2f813c0972cf018a0`  
		Last Modified: Fri, 01 Dec 2023 06:31:41 GMT  
		Size: 67.8 MB (67772846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076a1aa334a7b6eef088b4579bea958db5ad822017fe925ce57904a88cbee41d`  
		Last Modified: Fri, 01 Dec 2023 06:31:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d4d210bdf5ed96d7c4ee451e041b794cad6ce92ade9051714deeff815a4fa1`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0aeec3883498c38ebc9b066c4b119e783b7bd43cc90d5a104bf2abe034fa58`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e65d13ed7440987448e4ae294c6aa58f56eb639fc0f608bb1b18f1b6f17640`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee750d61171d80ab6d953bb21293f56e935aebe5e11fd103af20c860f98fd0f1`  
		Last Modified: Fri, 01 Dec 2023 06:31:38 GMT  
		Size: 120.2 MB (120176606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24a6648d8163c0174830c2f9f3af83ce399a9f2d702053a183d5a52bd63524c`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 5.7 KB (5657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:9.0.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:34c10898f477a7221a95893b57de3dcc23d4490708b50c5ff96cc632b7013d7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191218643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6765a28afb0cac1f9e3d96ac4cbf7909d9e495ecdd4597e1b33fe273b733fefc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:21:47 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 07:21:51 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Fri, 01 Dec 2023 07:21:52 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 07:21:53 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 07:21:53 GMT
ENV BONITA_VERSION=9.0.0
# Fri, 01 Dec 2023 07:21:53 GMT
ENV BRANDING_VERSION=2023.2-u0
# Fri, 01 Dec 2023 07:21:53 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Fri, 01 Dec 2023 07:21:53 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 07:21:54 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 07:21:54 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 07:21:54 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 07:21:54 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Fri, 01 Dec 2023 07:21:59 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 07:22:00 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 07:22:00 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 07:22:00 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 07:22:00 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 07:22:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 07:22:01 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 07:22:01 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Fri, 01 Dec 2023 07:22:01 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 07:22:01 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 07:22:01 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 07:22:01 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9d5c4d5cb627eed83e30a9f8cd45148519b03192374c37165c80843b69c944`  
		Last Modified: Fri, 01 Dec 2023 07:23:28 GMT  
		Size: 67.7 MB (67698077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7014c128521a3f66b5ecefcc308f824bc20824823772421ff1f33dfb925b8bec`  
		Last Modified: Fri, 01 Dec 2023 07:23:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efafcd70e05ac8cb6f234da4f4afb662b5e8a56e65f75a3fb2ef8d172ff9fe73`  
		Last Modified: Fri, 01 Dec 2023 07:23:18 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f0efdd3e80a7ce9b04f66c7b25197ef1fa5656cbde2701ddbe23e21f24f81`  
		Last Modified: Fri, 01 Dec 2023 07:23:19 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4b59d5e7c3a436e8fc93baadc97b86294156660fd1022c1f93b2a9df19c092`  
		Last Modified: Fri, 01 Dec 2023 07:23:19 GMT  
		Size: 3.7 KB (3662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25725db729846ddeecbde5b23cf3f50a630732b27528ab4ea00146861c0c652`  
		Last Modified: Fri, 01 Dec 2023 07:23:24 GMT  
		Size: 120.2 MB (120176648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b58edfcda0eaacede3c3479eec06ea1e94e78e26656f43ac07ba44a166466e`  
		Last Modified: Fri, 01 Dec 2023 07:23:19 GMT  
		Size: 5.7 KB (5660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:9.0.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:a5c237bcece8e9b606a8b0c7294b3ee127239e9f95fa53c1a874fc1e9782144d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188065296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d29449c9c83de9b066b19f038a2c6a9743f64575fb284c49120eeb88c2ae50`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:37:11 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 05:37:34 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Fri, 01 Dec 2023 05:37:46 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 05:37:59 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 05:38:02 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 05:38:06 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 05:38:17 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 05:38:19 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 05:38:20 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 05:38:23 GMT
ENV BONITA_VERSION=9.0.0
# Fri, 01 Dec 2023 05:38:31 GMT
ENV BRANDING_VERSION=2023.2-u0
# Fri, 01 Dec 2023 05:38:38 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Fri, 01 Dec 2023 05:38:39 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 05:38:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 05:38:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 05:38:44 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 05:38:46 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Fri, 01 Dec 2023 05:39:10 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 05:39:24 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 05:39:26 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 05:39:27 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 05:39:29 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 05:39:30 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 05:39:30 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 05:39:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 05:39:37 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 05:39:39 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 05:39:40 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 05:39:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 05:39:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 05:39:44 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 05:39:45 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Fri, 01 Dec 2023 05:39:48 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 05:39:49 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 05:39:50 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 05:39:53 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1961607fe5674a8c1d805e44043c42bc4d67207e8faa4682b39b0c49b43310e0`  
		Last Modified: Fri, 01 Dec 2023 05:41:46 GMT  
		Size: 64.5 MB (64529445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d614eed5744f8547076db82ed976402325dba784ec4c2c56cd248e47d53f4ac7`  
		Last Modified: Fri, 01 Dec 2023 05:41:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f07fc2f3ef9e4b1ed2a727a7cee1b9cbbef7de8d3c65005435ef0e60b9cc643`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285d196f9f4d8fee5af9cc323fe3c0049ad86ad90736d5ee2137c2140a4e2667`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9473fbfd57624b832051d7be0d392ff859a5e86d692e7be88011b788829b206`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 3.7 KB (3666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ed5c1bc2b798e9f662cbf850403e06c4ae710ae6da02ed9a6f18057103c034`  
		Last Modified: Fri, 01 Dec 2023 05:41:41 GMT  
		Size: 120.2 MB (120176637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e548ee928063c5ebfbb873bb80b33c0c748cf199c09672584f7a2046f5c7b7d1`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 5.7 KB (5661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:79ace3619e7ca496f76b98433d4ca2047128b714292078dc1272621b82f62d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:c2908f6f685ed1f4f19f56c9e93c76b77fcb8a7e0c644449909abc668413d280
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 MB (191362756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc511cde66b30fbc95e9d8ac98ed63de355bbfc78c577dc358f5da38bf27fb2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:29:56 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 06:30:00 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Fri, 01 Dec 2023 06:30:00 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 06:30:01 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 06:30:01 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 06:30:01 GMT
ENV BONITA_VERSION=9.0.0
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BRANDING_VERSION=2023.2-u0
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Fri, 01 Dec 2023 06:30:02 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 06:30:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 06:30:03 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 06:30:03 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Fri, 01 Dec 2023 06:30:08 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 06:30:08 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 06:30:08 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 06:30:09 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 06:30:09 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 06:30:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 06:30:09 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 06:30:09 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 06:30:09 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 06:30:09 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Fri, 01 Dec 2023 06:30:10 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 06:30:10 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 06:30:10 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 06:30:10 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8b9b9109619bd1c6b81bbc9ce4cecf24a7c2483fa9ecd2f813c0972cf018a0`  
		Last Modified: Fri, 01 Dec 2023 06:31:41 GMT  
		Size: 67.8 MB (67772846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076a1aa334a7b6eef088b4579bea958db5ad822017fe925ce57904a88cbee41d`  
		Last Modified: Fri, 01 Dec 2023 06:31:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d4d210bdf5ed96d7c4ee451e041b794cad6ce92ade9051714deeff815a4fa1`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0aeec3883498c38ebc9b066c4b119e783b7bd43cc90d5a104bf2abe034fa58`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e65d13ed7440987448e4ae294c6aa58f56eb639fc0f608bb1b18f1b6f17640`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 3.7 KB (3661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee750d61171d80ab6d953bb21293f56e935aebe5e11fd103af20c860f98fd0f1`  
		Last Modified: Fri, 01 Dec 2023 06:31:38 GMT  
		Size: 120.2 MB (120176606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24a6648d8163c0174830c2f9f3af83ce399a9f2d702053a183d5a52bd63524c`  
		Last Modified: Fri, 01 Dec 2023 06:31:31 GMT  
		Size: 5.7 KB (5657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:34c10898f477a7221a95893b57de3dcc23d4490708b50c5ff96cc632b7013d7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191218643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6765a28afb0cac1f9e3d96ac4cbf7909d9e495ecdd4597e1b33fe273b733fefc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:21:47 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 07:21:51 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Fri, 01 Dec 2023 07:21:52 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 07:21:53 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 07:21:53 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 07:21:53 GMT
ENV BONITA_VERSION=9.0.0
# Fri, 01 Dec 2023 07:21:53 GMT
ENV BRANDING_VERSION=2023.2-u0
# Fri, 01 Dec 2023 07:21:53 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Fri, 01 Dec 2023 07:21:53 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 07:21:54 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 07:21:54 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 07:21:54 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 07:21:54 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Fri, 01 Dec 2023 07:21:59 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 07:22:00 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 07:22:00 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 07:22:00 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 07:22:00 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 07:22:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 07:22:00 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 07:22:01 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 07:22:01 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Fri, 01 Dec 2023 07:22:01 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 07:22:01 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 07:22:01 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 07:22:01 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9d5c4d5cb627eed83e30a9f8cd45148519b03192374c37165c80843b69c944`  
		Last Modified: Fri, 01 Dec 2023 07:23:28 GMT  
		Size: 67.7 MB (67698077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7014c128521a3f66b5ecefcc308f824bc20824823772421ff1f33dfb925b8bec`  
		Last Modified: Fri, 01 Dec 2023 07:23:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efafcd70e05ac8cb6f234da4f4afb662b5e8a56e65f75a3fb2ef8d172ff9fe73`  
		Last Modified: Fri, 01 Dec 2023 07:23:18 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f0efdd3e80a7ce9b04f66c7b25197ef1fa5656cbde2701ddbe23e21f24f81`  
		Last Modified: Fri, 01 Dec 2023 07:23:19 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4b59d5e7c3a436e8fc93baadc97b86294156660fd1022c1f93b2a9df19c092`  
		Last Modified: Fri, 01 Dec 2023 07:23:19 GMT  
		Size: 3.7 KB (3662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25725db729846ddeecbde5b23cf3f50a630732b27528ab4ea00146861c0c652`  
		Last Modified: Fri, 01 Dec 2023 07:23:24 GMT  
		Size: 120.2 MB (120176648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b58edfcda0eaacede3c3479eec06ea1e94e78e26656f43ac07ba44a166466e`  
		Last Modified: Fri, 01 Dec 2023 07:23:19 GMT  
		Size: 5.7 KB (5660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:a5c237bcece8e9b606a8b0c7294b3ee127239e9f95fa53c1a874fc1e9782144d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.1 MB (188065296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d29449c9c83de9b066b19f038a2c6a9743f64575fb284c49120eeb88c2ae50`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:37:11 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Dec 2023 05:37:34 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg
# Fri, 01 Dec 2023 05:37:46 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Dec 2023 05:37:59 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Dec 2023 05:38:02 GMT
ARG BONITA_VERSION
# Fri, 01 Dec 2023 05:38:06 GMT
ARG BRANDING_VERSION
# Fri, 01 Dec 2023 05:38:17 GMT
ARG BONITA_SHA256
# Fri, 01 Dec 2023 05:38:19 GMT
ARG BASE_URL
# Fri, 01 Dec 2023 05:38:20 GMT
ARG BONITA_URL
# Fri, 01 Dec 2023 05:38:23 GMT
ENV BONITA_VERSION=9.0.0
# Fri, 01 Dec 2023 05:38:31 GMT
ENV BRANDING_VERSION=2023.2-u0
# Fri, 01 Dec 2023 05:38:38 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Fri, 01 Dec 2023 05:38:39 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 05:38:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Dec 2023 05:38:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Fri, 01 Dec 2023 05:38:44 GMT
RUN mkdir /opt/files
# Fri, 01 Dec 2023 05:38:46 GMT
COPY dir:6f895475e79bd870a1a9724f932a63f7aedb797824886234839cf6eaa2841312 in /opt/files 
# Fri, 01 Dec 2023 05:39:10 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Dec 2023 05:39:24 GMT
ENV HTTP_API=false
# Fri, 01 Dec 2023 05:39:26 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Dec 2023 05:39:27 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Dec 2023 05:39:29 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Dec 2023 05:39:30 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Dec 2023 05:39:30 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Dec 2023 05:39:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Dec 2023 05:39:37 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Dec 2023 05:39:39 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Dec 2023 05:39:40 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Dec 2023 05:39:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Dec 2023 05:39:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Dec 2023 05:39:44 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Dec 2023 05:39:45 GMT
COPY dir:521b895ad8a8708c79537daa0d77e6bec7578da53370df65b17697ee0035eee6 in /opt/templates 
# Fri, 01 Dec 2023 05:39:48 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 01 Dec 2023 05:39:49 GMT
EXPOSE 8080 9000
# Fri, 01 Dec 2023 05:39:50 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Dec 2023 05:39:53 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1961607fe5674a8c1d805e44043c42bc4d67207e8faa4682b39b0c49b43310e0`  
		Last Modified: Fri, 01 Dec 2023 05:41:46 GMT  
		Size: 64.5 MB (64529445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d614eed5744f8547076db82ed976402325dba784ec4c2c56cd248e47d53f4ac7`  
		Last Modified: Fri, 01 Dec 2023 05:41:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f07fc2f3ef9e4b1ed2a727a7cee1b9cbbef7de8d3c65005435ef0e60b9cc643`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285d196f9f4d8fee5af9cc323fe3c0049ad86ad90736d5ee2137c2140a4e2667`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9473fbfd57624b832051d7be0d392ff859a5e86d692e7be88011b788829b206`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 3.7 KB (3666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ed5c1bc2b798e9f662cbf850403e06c4ae710ae6da02ed9a6f18057103c034`  
		Last Modified: Fri, 01 Dec 2023 05:41:41 GMT  
		Size: 120.2 MB (120176637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e548ee928063c5ebfbb873bb80b33c0c748cf199c09672584f7a2046f5c7b7d1`  
		Last Modified: Fri, 01 Dec 2023 05:41:34 GMT  
		Size: 5.7 KB (5661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
