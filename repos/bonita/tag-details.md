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
$ docker pull bonita@sha256:247bdec3ade4c0393494d3f02c1c7390fac50a5622143450cee6cda0299e30a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.2` - linux; amd64

```console
$ docker pull bonita@sha256:b88ed7622e745bd94cd73920ee74f3e1743b444eb1ef78199028397cdbebfb11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183641859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba18c0093d544b17e4d54b43be6569be7b520b29fe8f7019ea175187aac41ba`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:47:19 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 00:47:24 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 00:47:25 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 00:47:25 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 27 Jan 2024 00:47:26 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 00:47:27 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 00:47:27 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 27 Jan 2024 00:47:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 00:47:33 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 00:47:34 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 00:47:34 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 00:47:34 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 00:47:34 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 00:47:35 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 00:47:35 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 00:47:35 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 00:47:35 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 00:47:35 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3227005c92c823e53fd986cab798cd7c0561f88af519d0992d08a1013b332511`  
		Last Modified: Sat, 27 Jan 2024 00:48:40 GMT  
		Size: 61.6 MB (61630982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b201a125d842b4ee71dd637756ba2042f9d85a846a2514c6d73caa11e9647f73`  
		Last Modified: Sat, 27 Jan 2024 00:48:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c6645cfdbcc82b5504b4ed4f9cafc2256cbc9a4a827bfa5904d4334a8af3f0`  
		Last Modified: Sat, 27 Jan 2024 00:48:30 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c923e825e97a38f99b954510958ab1ec615f2de325ba619c5aeac4012a64d192`  
		Last Modified: Sat, 27 Jan 2024 00:48:30 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b70561711c9950bfdb7dd20288a459e9b6d7c67318cc1fd3e5683f712b89348`  
		Last Modified: Sat, 27 Jan 2024 00:48:30 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaade8e0e4b5c3b19be581e4f34518200755f75f85621539c126a585df4b563`  
		Last Modified: Sat, 27 Jan 2024 00:48:36 GMT  
		Size: 119.2 MB (119193012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a666fa5fc4447d2587872bc8d27f85f584132656d0a978460263e24f66e5b1`  
		Last Modified: Sat, 27 Jan 2024 00:48:30 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:0863d13ea7215c9c64b4c17dc6ad65778d9d2d7cb5dfd51f6105f705f907b5e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182782593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5a545d83fc7b3e2844f42261f783778c13aabba4b1345b20105442c6ad542c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:41:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 03:41:45 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 03:41:46 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 03:41:46 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 03:41:46 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 03:41:46 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 03:41:47 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 03:41:47 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 03:41:47 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 27 Jan 2024 03:41:47 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 03:41:48 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 03:41:48 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 27 Jan 2024 03:41:53 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 03:41:54 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 03:41:54 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 03:41:54 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 03:41:54 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 03:41:54 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 03:41:55 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 03:41:55 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 03:41:55 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 03:41:55 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 03:41:55 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 03:41:55 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 03:41:55 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9aeed193214374cf5801901cd3e4e9498679fb9e8ecf8a47b9acf389047768`  
		Last Modified: Sat, 27 Jan 2024 03:42:54 GMT  
		Size: 60.9 MB (60871306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f88411f53f1dc00c4dc7b8a35e375866d43a89a4bc9e0d24546c8e09fd2e2d1`  
		Last Modified: Sat, 27 Jan 2024 03:42:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7263ce6925a7a781fcd60438f094cf48cc54c365cc25abf27ecd7fef127a4e`  
		Last Modified: Sat, 27 Jan 2024 03:42:45 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec74c9e2eba4c3e93f34b494cf5f31d4b284138b2e4e6049fcc2bcce4aea8e5f`  
		Last Modified: Sat, 27 Jan 2024 03:42:45 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f7b6d938bf851f6d6dc6b28af631c3ed3bfdcb6eab28a010ff107719d302e7`  
		Last Modified: Sat, 27 Jan 2024 03:42:45 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc7ce34a0b52aded05a48b83bea830ec9830d548e29aa0332da7b4fff19c00b`  
		Last Modified: Sat, 27 Jan 2024 03:42:50 GMT  
		Size: 119.2 MB (119192976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8068b432e4c4b1bea650b77c8a2ef9324d3e93ccbe82ea1c8d1d20894d4516`  
		Last Modified: Sat, 27 Jan 2024 03:42:45 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:95c820579813e786158590bc7881debb54487271074de98cec842ad7b69b4132
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179807340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b03cf2c9f6481c9d6f8696b945aa31abbf69cb75e5d84e35029f513a79d801`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:55 GMT
ADD file:cf4fecc20d85962cd46b6911d8ee82b9a3de2fa530bc58e998c2d544a888fdb9 in / 
# Sat, 27 Jan 2024 00:27:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:44:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 00:44:25 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 00:44:29 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 00:44:30 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 00:44:30 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 00:44:31 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 00:44:32 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 00:44:32 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 00:44:32 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 00:44:33 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 27 Jan 2024 00:44:33 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 27 Jan 2024 00:44:33 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 27 Jan 2024 00:44:34 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 00:44:34 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 00:44:35 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 00:44:37 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 00:44:37 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 27 Jan 2024 00:44:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 00:44:49 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 00:44:49 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 00:44:49 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 00:44:50 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 00:44:50 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 00:44:51 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 00:44:51 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 00:44:52 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 00:44:52 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 00:44:53 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 00:44:53 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 00:44:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 00:44:54 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 00:44:55 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 00:44:55 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 00:44:56 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 00:44:56 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:04646341bdb047ee1a3dd65db76069b9117954385033f5a340622fd170fa4b73`  
		Last Modified: Sat, 27 Jan 2024 00:28:46 GMT  
		Size: 2.8 MB (2802980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecedbdd44475442e30dd9f07b1201588cbc3deca7d5423bbab8d5fe5103c945`  
		Last Modified: Sat, 27 Jan 2024 00:47:09 GMT  
		Size: 57.8 MB (57801312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd822c1f511eef2eb11d5557a71dc5e70aa34a9a165f28a3aaefeade7c7d69d`  
		Last Modified: Sat, 27 Jan 2024 00:47:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b407ba46fcc4f09d729e6639a00276edd3635a0368f1b0c0c6237b7bb1244c7`  
		Last Modified: Sat, 27 Jan 2024 00:46:59 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1997d85ff2b05d7108927d8d4628124f8e433eed230cc11092576abb3f49e29`  
		Last Modified: Sat, 27 Jan 2024 00:46:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b3c45ddcb05889315e394439700449bd816dcfc65064798a3aa21b14018536`  
		Last Modified: Sat, 27 Jan 2024 00:46:59 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718a8cd102213b5f66a14ebb983c1adee17aec29b36df3bc170840238af01562`  
		Last Modified: Sat, 27 Jan 2024 00:47:05 GMT  
		Size: 119.2 MB (119193011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbe7966d79e73c569c6fd499370780726184844eaecbc8ecde962f74541c2b3`  
		Last Modified: Sat, 27 Jan 2024 00:46:59 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.2-u0`

```console
$ docker pull bonita@sha256:247bdec3ade4c0393494d3f02c1c7390fac50a5622143450cee6cda0299e30a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:b88ed7622e745bd94cd73920ee74f3e1743b444eb1ef78199028397cdbebfb11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183641859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba18c0093d544b17e4d54b43be6569be7b520b29fe8f7019ea175187aac41ba`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:47:19 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 00:47:24 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 00:47:25 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 00:47:25 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 27 Jan 2024 00:47:26 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 00:47:27 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 00:47:27 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 27 Jan 2024 00:47:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 00:47:33 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 00:47:34 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 00:47:34 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 00:47:34 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 00:47:34 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 00:47:35 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 00:47:35 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 00:47:35 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 00:47:35 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 00:47:35 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3227005c92c823e53fd986cab798cd7c0561f88af519d0992d08a1013b332511`  
		Last Modified: Sat, 27 Jan 2024 00:48:40 GMT  
		Size: 61.6 MB (61630982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b201a125d842b4ee71dd637756ba2042f9d85a846a2514c6d73caa11e9647f73`  
		Last Modified: Sat, 27 Jan 2024 00:48:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c6645cfdbcc82b5504b4ed4f9cafc2256cbc9a4a827bfa5904d4334a8af3f0`  
		Last Modified: Sat, 27 Jan 2024 00:48:30 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c923e825e97a38f99b954510958ab1ec615f2de325ba619c5aeac4012a64d192`  
		Last Modified: Sat, 27 Jan 2024 00:48:30 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b70561711c9950bfdb7dd20288a459e9b6d7c67318cc1fd3e5683f712b89348`  
		Last Modified: Sat, 27 Jan 2024 00:48:30 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaade8e0e4b5c3b19be581e4f34518200755f75f85621539c126a585df4b563`  
		Last Modified: Sat, 27 Jan 2024 00:48:36 GMT  
		Size: 119.2 MB (119193012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a666fa5fc4447d2587872bc8d27f85f584132656d0a978460263e24f66e5b1`  
		Last Modified: Sat, 27 Jan 2024 00:48:30 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:0863d13ea7215c9c64b4c17dc6ad65778d9d2d7cb5dfd51f6105f705f907b5e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182782593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5a545d83fc7b3e2844f42261f783778c13aabba4b1345b20105442c6ad542c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:41:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 03:41:45 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 03:41:46 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 03:41:46 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 03:41:46 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 03:41:46 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 03:41:47 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 03:41:47 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 03:41:47 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 27 Jan 2024 03:41:47 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 03:41:48 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 03:41:48 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 27 Jan 2024 03:41:53 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 03:41:54 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 03:41:54 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 03:41:54 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 03:41:54 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 03:41:54 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 03:41:55 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 03:41:55 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 03:41:55 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 03:41:55 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 03:41:55 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 03:41:55 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 03:41:55 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9aeed193214374cf5801901cd3e4e9498679fb9e8ecf8a47b9acf389047768`  
		Last Modified: Sat, 27 Jan 2024 03:42:54 GMT  
		Size: 60.9 MB (60871306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f88411f53f1dc00c4dc7b8a35e375866d43a89a4bc9e0d24546c8e09fd2e2d1`  
		Last Modified: Sat, 27 Jan 2024 03:42:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7263ce6925a7a781fcd60438f094cf48cc54c365cc25abf27ecd7fef127a4e`  
		Last Modified: Sat, 27 Jan 2024 03:42:45 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec74c9e2eba4c3e93f34b494cf5f31d4b284138b2e4e6049fcc2bcce4aea8e5f`  
		Last Modified: Sat, 27 Jan 2024 03:42:45 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f7b6d938bf851f6d6dc6b28af631c3ed3bfdcb6eab28a010ff107719d302e7`  
		Last Modified: Sat, 27 Jan 2024 03:42:45 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc7ce34a0b52aded05a48b83bea830ec9830d548e29aa0332da7b4fff19c00b`  
		Last Modified: Sat, 27 Jan 2024 03:42:50 GMT  
		Size: 119.2 MB (119192976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8068b432e4c4b1bea650b77c8a2ef9324d3e93ccbe82ea1c8d1d20894d4516`  
		Last Modified: Sat, 27 Jan 2024 03:42:45 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:95c820579813e786158590bc7881debb54487271074de98cec842ad7b69b4132
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179807340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b03cf2c9f6481c9d6f8696b945aa31abbf69cb75e5d84e35029f513a79d801`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:55 GMT
ADD file:cf4fecc20d85962cd46b6911d8ee82b9a3de2fa530bc58e998c2d544a888fdb9 in / 
# Sat, 27 Jan 2024 00:27:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:44:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 00:44:25 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 00:44:29 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 00:44:30 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 00:44:30 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 00:44:31 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 00:44:32 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 00:44:32 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 00:44:32 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 00:44:33 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 27 Jan 2024 00:44:33 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 27 Jan 2024 00:44:33 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 27 Jan 2024 00:44:34 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 00:44:34 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 00:44:35 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 00:44:37 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 00:44:37 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 27 Jan 2024 00:44:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 00:44:49 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 00:44:49 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 00:44:49 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 00:44:50 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 00:44:50 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 00:44:51 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 00:44:51 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 00:44:52 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 00:44:52 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 00:44:53 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 00:44:53 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 00:44:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 00:44:54 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 00:44:55 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 00:44:55 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 00:44:56 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 00:44:56 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:04646341bdb047ee1a3dd65db76069b9117954385033f5a340622fd170fa4b73`  
		Last Modified: Sat, 27 Jan 2024 00:28:46 GMT  
		Size: 2.8 MB (2802980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecedbdd44475442e30dd9f07b1201588cbc3deca7d5423bbab8d5fe5103c945`  
		Last Modified: Sat, 27 Jan 2024 00:47:09 GMT  
		Size: 57.8 MB (57801312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd822c1f511eef2eb11d5557a71dc5e70aa34a9a165f28a3aaefeade7c7d69d`  
		Last Modified: Sat, 27 Jan 2024 00:47:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b407ba46fcc4f09d729e6639a00276edd3635a0368f1b0c0c6237b7bb1244c7`  
		Last Modified: Sat, 27 Jan 2024 00:46:59 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1997d85ff2b05d7108927d8d4628124f8e433eed230cc11092576abb3f49e29`  
		Last Modified: Sat, 27 Jan 2024 00:46:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b3c45ddcb05889315e394439700449bd816dcfc65064798a3aa21b14018536`  
		Last Modified: Sat, 27 Jan 2024 00:46:59 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718a8cd102213b5f66a14ebb983c1adee17aec29b36df3bc170840238af01562`  
		Last Modified: Sat, 27 Jan 2024 00:47:05 GMT  
		Size: 119.2 MB (119193011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbe7966d79e73c569c6fd499370780726184844eaecbc8ecde962f74541c2b3`  
		Last Modified: Sat, 27 Jan 2024 00:46:59 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2023.1`

```console
$ docker pull bonita@sha256:0eb58c01fe865d15606e2e13b112e88918e0062c377397ee088f4c946c0bffe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2023.1` - linux; amd64

```console
$ docker pull bonita@sha256:148ce7a1b77477e51d494ca6eb2d0e72dd88beabc1af9cf6c1c9d8a50bd4f254
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183368755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed37b8369749a73bbd52a624ec28dd95ec0c38496b6a80b2fbbd7eaae5704d9a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:47:40 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 00:47:44 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 00:47:45 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 00:47:45 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 00:47:45 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 00:47:46 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 00:47:46 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 00:47:46 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 00:47:46 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 27 Jan 2024 00:47:46 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 00:47:47 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 00:47:47 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 27 Jan 2024 00:47:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 00:47:53 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 00:47:53 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 00:47:53 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 00:47:53 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 00:47:53 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 00:47:53 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 00:47:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 00:47:54 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 00:47:54 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 27 Jan 2024 00:47:54 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 00:47:54 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 27 Jan 2024 00:47:54 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 00:47:54 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 00:47:54 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1caad0f049bb37c74f8d0bfd5a4cd6260d83ecb09fbff87cf6cd869b950c9ed`  
		Last Modified: Sat, 27 Jan 2024 00:49:01 GMT  
		Size: 61.8 MB (61798192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7496f35111679745c1b3e57e3c121bf57d74a2f7bfd5a3a43e937dc3ed38c1`  
		Last Modified: Sat, 27 Jan 2024 00:48:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668f94ad6d84ec2445a677e6b29d1a81c199911fd1c91ea6839c80df8d2eaa5a`  
		Last Modified: Sat, 27 Jan 2024 00:48:52 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb2e089a63348da9cc541a2ba138dbf06dab87659d2def8f18c2b9c04a00f03`  
		Last Modified: Sat, 27 Jan 2024 00:48:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58d30dfcdc3e2a5e0610cd2861841ca25e0652eedd43122f20684e7f230f115`  
		Last Modified: Sat, 27 Jan 2024 00:48:52 GMT  
		Size: 3.5 KB (3474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453056aae58447fe970e8fde1f326fc129042a15aec770dbb065aa0ca7426fe5`  
		Last Modified: Sat, 27 Jan 2024 00:48:58 GMT  
		Size: 118.2 MB (118180700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ac8798d66ca73d5d44ea1ed8d58cd2dad81f630ce8b0d7a89464d4a85bb56e`  
		Last Modified: Sat, 27 Jan 2024 00:48:52 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:0973a31f7f849bded1d8ee329016f3c75ed3896ed7042b144c45f0233e16e360
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182518314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe0d62207dada883fef29220ebaa559b601cfa0cc2b6c1b9f21930dad4b2e1a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:41:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 03:42:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 03:42:03 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 03:42:04 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 03:42:04 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 27 Jan 2024 03:42:04 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 27 Jan 2024 03:42:04 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 27 Jan 2024 03:42:05 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 03:42:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 03:42:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 03:42:05 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 03:42:05 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 27 Jan 2024 03:42:10 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 03:42:10 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 03:42:10 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 03:42:10 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 03:42:10 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 03:42:10 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 03:42:11 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 03:42:11 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 03:42:11 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 27 Jan 2024 03:42:11 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 03:42:11 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 27 Jan 2024 03:42:11 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 03:42:12 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 03:42:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70ca11832c7ec17b887f0cbc179fd00e9eaaa19dc0890898781fe31c37d0721`  
		Last Modified: Sat, 27 Jan 2024 03:43:16 GMT  
		Size: 61.1 MB (61068901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f06f7ec9ba6e9194d968d839bc5a51c948ca47e7dd634cca3fc4f0c8418fa4`  
		Last Modified: Sat, 27 Jan 2024 03:43:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97055130a023b2d0f09833fca2b853541890035831c6dc69139ee2f5fe90922`  
		Last Modified: Sat, 27 Jan 2024 03:43:08 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ef971a4520af2c383da9c3105d2ebe61857c206f7d38fe20fe605ddec7f731`  
		Last Modified: Sat, 27 Jan 2024 03:43:08 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66435baaef09e74f1c298fe8ad1296edabe4314fb9fb2078037928d12550ccf`  
		Last Modified: Sat, 27 Jan 2024 03:43:08 GMT  
		Size: 3.5 KB (3476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be75eec397b88c12ce8e93f42760d1f810aa156f0bd82601b1e482e83c72a670`  
		Last Modified: Sat, 27 Jan 2024 03:43:13 GMT  
		Size: 118.2 MB (118180669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d20e5a926043f57d0891e83790824116707ee11255e76e51b02819c48dafc32`  
		Last Modified: Sat, 27 Jan 2024 03:43:08 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:8d287674970f1686ac28e73d5ac9f63a3c638998fa29ff4db7714a4474e46ec1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179570641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c715d50648e2b5c8e4c0a5e0701d94df828e5c4b7e125faa12abe94833af0cf3`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:48 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
# Sat, 27 Jan 2024 00:27:49 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:45:03 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 00:45:17 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 00:45:20 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 00:45:21 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 00:45:22 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 00:45:22 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 00:45:22 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 00:45:23 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 00:45:23 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 00:45:23 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 27 Jan 2024 00:45:24 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 27 Jan 2024 00:45:24 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 27 Jan 2024 00:45:25 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 00:45:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 00:45:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 00:45:27 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 00:45:28 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 27 Jan 2024 00:45:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 00:45:39 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 00:45:40 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 00:45:40 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 00:45:41 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 00:45:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 00:45:42 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 00:45:43 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 00:45:43 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 00:45:44 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 00:45:45 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 00:45:46 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 00:45:46 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 00:45:46 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 00:45:47 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 27 Jan 2024 00:45:47 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 00:45:48 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 27 Jan 2024 00:45:48 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 00:45:49 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 00:45:49 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7231d895a6fafeb2bc3ace13dd93264aacacd41260272c5078656f69557919`  
		Last Modified: Sat, 27 Jan 2024 00:47:34 GMT  
		Size: 58.0 MB (57987363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd72a35024358fd33f3712addc4aa20a7bf210b8fadbdd14a9aaa8253b0ac01`  
		Last Modified: Sat, 27 Jan 2024 00:47:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b639d9045501b3c64dfe5222baaadfd441f9a1c543d46bd02f5261b2f6996f`  
		Last Modified: Sat, 27 Jan 2024 00:47:24 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca334c2e0185403154f6c71d71c1c0d9267f89eca094c08ba805b69052ea8eb8`  
		Last Modified: Sat, 27 Jan 2024 00:47:24 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529d51e2dcead0661a1d0ca99d678fa843da912e7d7c70ac4c3120fc37e82cf1`  
		Last Modified: Sat, 27 Jan 2024 00:47:24 GMT  
		Size: 3.5 KB (3481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36857b1c0e242a3ad2250ed16714647036e33fd36f4b504dd5a4fd0b167a9b1d`  
		Last Modified: Sat, 27 Jan 2024 00:47:31 GMT  
		Size: 118.2 MB (118180710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea15b6bdefe7927d30456f39a7198cf92c63072b8a202934a495de7363d0f2ad`  
		Last Modified: Sat, 27 Jan 2024 00:47:24 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2023.1-u0`

```console
$ docker pull bonita@sha256:0eb58c01fe865d15606e2e13b112e88918e0062c377397ee088f4c946c0bffe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2023.1-u0` - linux; amd64

```console
$ docker pull bonita@sha256:148ce7a1b77477e51d494ca6eb2d0e72dd88beabc1af9cf6c1c9d8a50bd4f254
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183368755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed37b8369749a73bbd52a624ec28dd95ec0c38496b6a80b2fbbd7eaae5704d9a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:47:40 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 00:47:44 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 00:47:45 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 00:47:45 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 00:47:45 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 00:47:46 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 00:47:46 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 00:47:46 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 00:47:46 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 27 Jan 2024 00:47:46 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 00:47:47 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 00:47:47 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 27 Jan 2024 00:47:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 00:47:53 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 00:47:53 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 00:47:53 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 00:47:53 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 00:47:53 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 00:47:53 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 00:47:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 00:47:54 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 00:47:54 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 27 Jan 2024 00:47:54 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 00:47:54 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 27 Jan 2024 00:47:54 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 00:47:54 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 00:47:54 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1caad0f049bb37c74f8d0bfd5a4cd6260d83ecb09fbff87cf6cd869b950c9ed`  
		Last Modified: Sat, 27 Jan 2024 00:49:01 GMT  
		Size: 61.8 MB (61798192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7496f35111679745c1b3e57e3c121bf57d74a2f7bfd5a3a43e937dc3ed38c1`  
		Last Modified: Sat, 27 Jan 2024 00:48:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668f94ad6d84ec2445a677e6b29d1a81c199911fd1c91ea6839c80df8d2eaa5a`  
		Last Modified: Sat, 27 Jan 2024 00:48:52 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb2e089a63348da9cc541a2ba138dbf06dab87659d2def8f18c2b9c04a00f03`  
		Last Modified: Sat, 27 Jan 2024 00:48:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58d30dfcdc3e2a5e0610cd2861841ca25e0652eedd43122f20684e7f230f115`  
		Last Modified: Sat, 27 Jan 2024 00:48:52 GMT  
		Size: 3.5 KB (3474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453056aae58447fe970e8fde1f326fc129042a15aec770dbb065aa0ca7426fe5`  
		Last Modified: Sat, 27 Jan 2024 00:48:58 GMT  
		Size: 118.2 MB (118180700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ac8798d66ca73d5d44ea1ed8d58cd2dad81f630ce8b0d7a89464d4a85bb56e`  
		Last Modified: Sat, 27 Jan 2024 00:48:52 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:0973a31f7f849bded1d8ee329016f3c75ed3896ed7042b144c45f0233e16e360
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182518314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe0d62207dada883fef29220ebaa559b601cfa0cc2b6c1b9f21930dad4b2e1a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:41:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 03:42:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 03:42:03 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 03:42:04 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 03:42:04 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 27 Jan 2024 03:42:04 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 27 Jan 2024 03:42:04 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 27 Jan 2024 03:42:05 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 03:42:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 03:42:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 03:42:05 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 03:42:05 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 27 Jan 2024 03:42:10 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 03:42:10 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 03:42:10 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 03:42:10 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 03:42:10 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 03:42:10 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 03:42:11 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 03:42:11 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 03:42:11 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 27 Jan 2024 03:42:11 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 03:42:11 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 27 Jan 2024 03:42:11 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 03:42:12 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 03:42:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70ca11832c7ec17b887f0cbc179fd00e9eaaa19dc0890898781fe31c37d0721`  
		Last Modified: Sat, 27 Jan 2024 03:43:16 GMT  
		Size: 61.1 MB (61068901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f06f7ec9ba6e9194d968d839bc5a51c948ca47e7dd634cca3fc4f0c8418fa4`  
		Last Modified: Sat, 27 Jan 2024 03:43:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97055130a023b2d0f09833fca2b853541890035831c6dc69139ee2f5fe90922`  
		Last Modified: Sat, 27 Jan 2024 03:43:08 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ef971a4520af2c383da9c3105d2ebe61857c206f7d38fe20fe605ddec7f731`  
		Last Modified: Sat, 27 Jan 2024 03:43:08 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66435baaef09e74f1c298fe8ad1296edabe4314fb9fb2078037928d12550ccf`  
		Last Modified: Sat, 27 Jan 2024 03:43:08 GMT  
		Size: 3.5 KB (3476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be75eec397b88c12ce8e93f42760d1f810aa156f0bd82601b1e482e83c72a670`  
		Last Modified: Sat, 27 Jan 2024 03:43:13 GMT  
		Size: 118.2 MB (118180669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d20e5a926043f57d0891e83790824116707ee11255e76e51b02819c48dafc32`  
		Last Modified: Sat, 27 Jan 2024 03:43:08 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:8d287674970f1686ac28e73d5ac9f63a3c638998fa29ff4db7714a4474e46ec1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179570641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c715d50648e2b5c8e4c0a5e0701d94df828e5c4b7e125faa12abe94833af0cf3`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:48 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
# Sat, 27 Jan 2024 00:27:49 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:45:03 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 00:45:17 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 00:45:20 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 00:45:21 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 00:45:22 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 00:45:22 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 00:45:22 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 00:45:23 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 00:45:23 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 00:45:23 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 27 Jan 2024 00:45:24 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 27 Jan 2024 00:45:24 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 27 Jan 2024 00:45:25 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 00:45:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 00:45:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 00:45:27 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 00:45:28 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 27 Jan 2024 00:45:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 00:45:39 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 00:45:40 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 00:45:40 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 00:45:41 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 00:45:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 00:45:42 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 00:45:43 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 00:45:43 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 00:45:44 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 00:45:45 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 00:45:46 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 00:45:46 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 00:45:46 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 00:45:47 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 27 Jan 2024 00:45:47 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 00:45:48 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 27 Jan 2024 00:45:48 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 00:45:49 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 00:45:49 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7231d895a6fafeb2bc3ace13dd93264aacacd41260272c5078656f69557919`  
		Last Modified: Sat, 27 Jan 2024 00:47:34 GMT  
		Size: 58.0 MB (57987363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd72a35024358fd33f3712addc4aa20a7bf210b8fadbdd14a9aaa8253b0ac01`  
		Last Modified: Sat, 27 Jan 2024 00:47:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b639d9045501b3c64dfe5222baaadfd441f9a1c543d46bd02f5261b2f6996f`  
		Last Modified: Sat, 27 Jan 2024 00:47:24 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca334c2e0185403154f6c71d71c1c0d9267f89eca094c08ba805b69052ea8eb8`  
		Last Modified: Sat, 27 Jan 2024 00:47:24 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529d51e2dcead0661a1d0ca99d678fa843da912e7d7c70ac4c3120fc37e82cf1`  
		Last Modified: Sat, 27 Jan 2024 00:47:24 GMT  
		Size: 3.5 KB (3481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36857b1c0e242a3ad2250ed16714647036e33fd36f4b504dd5a4fd0b167a9b1d`  
		Last Modified: Sat, 27 Jan 2024 00:47:31 GMT  
		Size: 118.2 MB (118180710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea15b6bdefe7927d30456f39a7198cf92c63072b8a202934a495de7363d0f2ad`  
		Last Modified: Sat, 27 Jan 2024 00:47:24 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2023.2`

```console
$ docker pull bonita@sha256:0bedee63b0d734d177ce304454e3cee8ce837fea6c9abcc5c4e366c2ded7bb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2023.2` - linux; amd64

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

### `bonita:2023.2` - linux; arm64 variant v8

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

### `bonita:2023.2` - linux; ppc64le

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

## `bonita:2023.2-u0`

```console
$ docker pull bonita@sha256:0bedee63b0d734d177ce304454e3cee8ce837fea6c9abcc5c4e366c2ded7bb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2023.2-u0` - linux; amd64

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

### `bonita:2023.2-u0` - linux; arm64 variant v8

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

### `bonita:2023.2-u0` - linux; ppc64le

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
$ docker pull bonita@sha256:247bdec3ade4c0393494d3f02c1c7390fac50a5622143450cee6cda0299e30a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.15` - linux; amd64

```console
$ docker pull bonita@sha256:b88ed7622e745bd94cd73920ee74f3e1743b444eb1ef78199028397cdbebfb11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183641859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba18c0093d544b17e4d54b43be6569be7b520b29fe8f7019ea175187aac41ba`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:47:19 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 00:47:24 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 00:47:25 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 00:47:25 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 27 Jan 2024 00:47:26 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 00:47:27 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 00:47:27 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 27 Jan 2024 00:47:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 00:47:33 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 00:47:34 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 00:47:34 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 00:47:34 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 00:47:34 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 00:47:35 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 00:47:35 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 00:47:35 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 00:47:35 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 00:47:35 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3227005c92c823e53fd986cab798cd7c0561f88af519d0992d08a1013b332511`  
		Last Modified: Sat, 27 Jan 2024 00:48:40 GMT  
		Size: 61.6 MB (61630982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b201a125d842b4ee71dd637756ba2042f9d85a846a2514c6d73caa11e9647f73`  
		Last Modified: Sat, 27 Jan 2024 00:48:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c6645cfdbcc82b5504b4ed4f9cafc2256cbc9a4a827bfa5904d4334a8af3f0`  
		Last Modified: Sat, 27 Jan 2024 00:48:30 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c923e825e97a38f99b954510958ab1ec615f2de325ba619c5aeac4012a64d192`  
		Last Modified: Sat, 27 Jan 2024 00:48:30 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b70561711c9950bfdb7dd20288a459e9b6d7c67318cc1fd3e5683f712b89348`  
		Last Modified: Sat, 27 Jan 2024 00:48:30 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaade8e0e4b5c3b19be581e4f34518200755f75f85621539c126a585df4b563`  
		Last Modified: Sat, 27 Jan 2024 00:48:36 GMT  
		Size: 119.2 MB (119193012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a666fa5fc4447d2587872bc8d27f85f584132656d0a978460263e24f66e5b1`  
		Last Modified: Sat, 27 Jan 2024 00:48:30 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:0863d13ea7215c9c64b4c17dc6ad65778d9d2d7cb5dfd51f6105f705f907b5e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182782593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5a545d83fc7b3e2844f42261f783778c13aabba4b1345b20105442c6ad542c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:41:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 03:41:45 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 03:41:46 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 03:41:46 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 03:41:46 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 03:41:46 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 03:41:47 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 03:41:47 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 03:41:47 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 27 Jan 2024 03:41:47 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 03:41:48 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 03:41:48 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 27 Jan 2024 03:41:53 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 03:41:54 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 03:41:54 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 03:41:54 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 03:41:54 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 03:41:54 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 03:41:55 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 03:41:55 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 03:41:55 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 03:41:55 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 03:41:55 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 03:41:55 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 03:41:55 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9aeed193214374cf5801901cd3e4e9498679fb9e8ecf8a47b9acf389047768`  
		Last Modified: Sat, 27 Jan 2024 03:42:54 GMT  
		Size: 60.9 MB (60871306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f88411f53f1dc00c4dc7b8a35e375866d43a89a4bc9e0d24546c8e09fd2e2d1`  
		Last Modified: Sat, 27 Jan 2024 03:42:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7263ce6925a7a781fcd60438f094cf48cc54c365cc25abf27ecd7fef127a4e`  
		Last Modified: Sat, 27 Jan 2024 03:42:45 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec74c9e2eba4c3e93f34b494cf5f31d4b284138b2e4e6049fcc2bcce4aea8e5f`  
		Last Modified: Sat, 27 Jan 2024 03:42:45 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f7b6d938bf851f6d6dc6b28af631c3ed3bfdcb6eab28a010ff107719d302e7`  
		Last Modified: Sat, 27 Jan 2024 03:42:45 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc7ce34a0b52aded05a48b83bea830ec9830d548e29aa0332da7b4fff19c00b`  
		Last Modified: Sat, 27 Jan 2024 03:42:50 GMT  
		Size: 119.2 MB (119192976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8068b432e4c4b1bea650b77c8a2ef9324d3e93ccbe82ea1c8d1d20894d4516`  
		Last Modified: Sat, 27 Jan 2024 03:42:45 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15` - linux; ppc64le

```console
$ docker pull bonita@sha256:95c820579813e786158590bc7881debb54487271074de98cec842ad7b69b4132
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179807340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b03cf2c9f6481c9d6f8696b945aa31abbf69cb75e5d84e35029f513a79d801`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:55 GMT
ADD file:cf4fecc20d85962cd46b6911d8ee82b9a3de2fa530bc58e998c2d544a888fdb9 in / 
# Sat, 27 Jan 2024 00:27:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:44:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 00:44:25 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 00:44:29 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 00:44:30 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 00:44:30 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 00:44:31 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 00:44:32 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 00:44:32 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 00:44:32 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 00:44:33 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 27 Jan 2024 00:44:33 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 27 Jan 2024 00:44:33 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 27 Jan 2024 00:44:34 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 00:44:34 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 00:44:35 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 00:44:37 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 00:44:37 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 27 Jan 2024 00:44:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 00:44:49 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 00:44:49 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 00:44:49 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 00:44:50 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 00:44:50 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 00:44:51 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 00:44:51 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 00:44:52 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 00:44:52 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 00:44:53 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 00:44:53 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 00:44:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 00:44:54 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 00:44:55 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 00:44:55 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 00:44:56 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 00:44:56 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:04646341bdb047ee1a3dd65db76069b9117954385033f5a340622fd170fa4b73`  
		Last Modified: Sat, 27 Jan 2024 00:28:46 GMT  
		Size: 2.8 MB (2802980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecedbdd44475442e30dd9f07b1201588cbc3deca7d5423bbab8d5fe5103c945`  
		Last Modified: Sat, 27 Jan 2024 00:47:09 GMT  
		Size: 57.8 MB (57801312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd822c1f511eef2eb11d5557a71dc5e70aa34a9a165f28a3aaefeade7c7d69d`  
		Last Modified: Sat, 27 Jan 2024 00:47:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b407ba46fcc4f09d729e6639a00276edd3635a0368f1b0c0c6237b7bb1244c7`  
		Last Modified: Sat, 27 Jan 2024 00:46:59 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1997d85ff2b05d7108927d8d4628124f8e433eed230cc11092576abb3f49e29`  
		Last Modified: Sat, 27 Jan 2024 00:46:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b3c45ddcb05889315e394439700449bd816dcfc65064798a3aa21b14018536`  
		Last Modified: Sat, 27 Jan 2024 00:46:59 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718a8cd102213b5f66a14ebb983c1adee17aec29b36df3bc170840238af01562`  
		Last Modified: Sat, 27 Jan 2024 00:47:05 GMT  
		Size: 119.2 MB (119193011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbe7966d79e73c569c6fd499370780726184844eaecbc8ecde962f74541c2b3`  
		Last Modified: Sat, 27 Jan 2024 00:46:59 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.15.0`

```console
$ docker pull bonita@sha256:247bdec3ade4c0393494d3f02c1c7390fac50a5622143450cee6cda0299e30a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.15.0` - linux; amd64

```console
$ docker pull bonita@sha256:b88ed7622e745bd94cd73920ee74f3e1743b444eb1ef78199028397cdbebfb11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183641859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba18c0093d544b17e4d54b43be6569be7b520b29fe8f7019ea175187aac41ba`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:47:19 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 00:47:24 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 00:47:25 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 00:47:25 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 00:47:25 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 27 Jan 2024 00:47:26 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 00:47:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 00:47:27 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 00:47:27 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 27 Jan 2024 00:47:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 00:47:33 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 00:47:34 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 00:47:34 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 00:47:34 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 00:47:34 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 00:47:34 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 00:47:35 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 00:47:35 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 00:47:35 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 00:47:35 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 00:47:35 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3227005c92c823e53fd986cab798cd7c0561f88af519d0992d08a1013b332511`  
		Last Modified: Sat, 27 Jan 2024 00:48:40 GMT  
		Size: 61.6 MB (61630982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b201a125d842b4ee71dd637756ba2042f9d85a846a2514c6d73caa11e9647f73`  
		Last Modified: Sat, 27 Jan 2024 00:48:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c6645cfdbcc82b5504b4ed4f9cafc2256cbc9a4a827bfa5904d4334a8af3f0`  
		Last Modified: Sat, 27 Jan 2024 00:48:30 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c923e825e97a38f99b954510958ab1ec615f2de325ba619c5aeac4012a64d192`  
		Last Modified: Sat, 27 Jan 2024 00:48:30 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b70561711c9950bfdb7dd20288a459e9b6d7c67318cc1fd3e5683f712b89348`  
		Last Modified: Sat, 27 Jan 2024 00:48:30 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaade8e0e4b5c3b19be581e4f34518200755f75f85621539c126a585df4b563`  
		Last Modified: Sat, 27 Jan 2024 00:48:36 GMT  
		Size: 119.2 MB (119193012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a666fa5fc4447d2587872bc8d27f85f584132656d0a978460263e24f66e5b1`  
		Last Modified: Sat, 27 Jan 2024 00:48:30 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:0863d13ea7215c9c64b4c17dc6ad65778d9d2d7cb5dfd51f6105f705f907b5e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182782593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5a545d83fc7b3e2844f42261f783778c13aabba4b1345b20105442c6ad542c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:41:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 03:41:45 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 03:41:46 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 03:41:46 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 03:41:46 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 03:41:46 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 03:41:47 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 03:41:47 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 03:41:47 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 27 Jan 2024 03:41:47 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 03:41:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 03:41:48 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 03:41:48 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 27 Jan 2024 03:41:53 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 03:41:54 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 03:41:54 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 03:41:54 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 03:41:54 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 03:41:54 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 03:41:54 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 03:41:55 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 03:41:55 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 03:41:55 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 03:41:55 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 03:41:55 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 03:41:55 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 03:41:55 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9aeed193214374cf5801901cd3e4e9498679fb9e8ecf8a47b9acf389047768`  
		Last Modified: Sat, 27 Jan 2024 03:42:54 GMT  
		Size: 60.9 MB (60871306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f88411f53f1dc00c4dc7b8a35e375866d43a89a4bc9e0d24546c8e09fd2e2d1`  
		Last Modified: Sat, 27 Jan 2024 03:42:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7263ce6925a7a781fcd60438f094cf48cc54c365cc25abf27ecd7fef127a4e`  
		Last Modified: Sat, 27 Jan 2024 03:42:45 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec74c9e2eba4c3e93f34b494cf5f31d4b284138b2e4e6049fcc2bcce4aea8e5f`  
		Last Modified: Sat, 27 Jan 2024 03:42:45 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f7b6d938bf851f6d6dc6b28af631c3ed3bfdcb6eab28a010ff107719d302e7`  
		Last Modified: Sat, 27 Jan 2024 03:42:45 GMT  
		Size: 3.0 KB (3047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc7ce34a0b52aded05a48b83bea830ec9830d548e29aa0332da7b4fff19c00b`  
		Last Modified: Sat, 27 Jan 2024 03:42:50 GMT  
		Size: 119.2 MB (119192976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8068b432e4c4b1bea650b77c8a2ef9324d3e93ccbe82ea1c8d1d20894d4516`  
		Last Modified: Sat, 27 Jan 2024 03:42:45 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:95c820579813e786158590bc7881debb54487271074de98cec842ad7b69b4132
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179807340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b03cf2c9f6481c9d6f8696b945aa31abbf69cb75e5d84e35029f513a79d801`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:55 GMT
ADD file:cf4fecc20d85962cd46b6911d8ee82b9a3de2fa530bc58e998c2d544a888fdb9 in / 
# Sat, 27 Jan 2024 00:27:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:44:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 00:44:25 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 00:44:29 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 00:44:30 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 00:44:30 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 00:44:31 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 00:44:32 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 00:44:32 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 00:44:32 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 00:44:33 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 27 Jan 2024 00:44:33 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 27 Jan 2024 00:44:33 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 27 Jan 2024 00:44:34 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 00:44:34 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 00:44:35 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 27 Jan 2024 00:44:37 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 00:44:37 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 27 Jan 2024 00:44:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 00:44:49 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 00:44:49 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 00:44:49 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 00:44:50 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 00:44:50 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 00:44:51 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 00:44:51 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 00:44:52 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 00:44:52 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 00:44:53 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 00:44:53 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 00:44:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 00:44:54 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 00:44:55 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 00:44:55 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 00:44:56 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 00:44:56 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:04646341bdb047ee1a3dd65db76069b9117954385033f5a340622fd170fa4b73`  
		Last Modified: Sat, 27 Jan 2024 00:28:46 GMT  
		Size: 2.8 MB (2802980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecedbdd44475442e30dd9f07b1201588cbc3deca7d5423bbab8d5fe5103c945`  
		Last Modified: Sat, 27 Jan 2024 00:47:09 GMT  
		Size: 57.8 MB (57801312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd822c1f511eef2eb11d5557a71dc5e70aa34a9a165f28a3aaefeade7c7d69d`  
		Last Modified: Sat, 27 Jan 2024 00:47:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b407ba46fcc4f09d729e6639a00276edd3635a0368f1b0c0c6237b7bb1244c7`  
		Last Modified: Sat, 27 Jan 2024 00:46:59 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1997d85ff2b05d7108927d8d4628124f8e433eed230cc11092576abb3f49e29`  
		Last Modified: Sat, 27 Jan 2024 00:46:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b3c45ddcb05889315e394439700449bd816dcfc65064798a3aa21b14018536`  
		Last Modified: Sat, 27 Jan 2024 00:46:59 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718a8cd102213b5f66a14ebb983c1adee17aec29b36df3bc170840238af01562`  
		Last Modified: Sat, 27 Jan 2024 00:47:05 GMT  
		Size: 119.2 MB (119193011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbe7966d79e73c569c6fd499370780726184844eaecbc8ecde962f74541c2b3`  
		Last Modified: Sat, 27 Jan 2024 00:46:59 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:8.0`

```console
$ docker pull bonita@sha256:0eb58c01fe865d15606e2e13b112e88918e0062c377397ee088f4c946c0bffe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:8.0` - linux; amd64

```console
$ docker pull bonita@sha256:148ce7a1b77477e51d494ca6eb2d0e72dd88beabc1af9cf6c1c9d8a50bd4f254
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183368755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed37b8369749a73bbd52a624ec28dd95ec0c38496b6a80b2fbbd7eaae5704d9a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:47:40 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 00:47:44 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 00:47:45 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 00:47:45 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 00:47:45 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 00:47:46 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 00:47:46 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 00:47:46 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 00:47:46 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 27 Jan 2024 00:47:46 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 00:47:47 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 00:47:47 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 27 Jan 2024 00:47:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 00:47:53 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 00:47:53 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 00:47:53 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 00:47:53 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 00:47:53 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 00:47:53 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 00:47:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 00:47:54 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 00:47:54 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 27 Jan 2024 00:47:54 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 00:47:54 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 27 Jan 2024 00:47:54 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 00:47:54 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 00:47:54 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1caad0f049bb37c74f8d0bfd5a4cd6260d83ecb09fbff87cf6cd869b950c9ed`  
		Last Modified: Sat, 27 Jan 2024 00:49:01 GMT  
		Size: 61.8 MB (61798192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7496f35111679745c1b3e57e3c121bf57d74a2f7bfd5a3a43e937dc3ed38c1`  
		Last Modified: Sat, 27 Jan 2024 00:48:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668f94ad6d84ec2445a677e6b29d1a81c199911fd1c91ea6839c80df8d2eaa5a`  
		Last Modified: Sat, 27 Jan 2024 00:48:52 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb2e089a63348da9cc541a2ba138dbf06dab87659d2def8f18c2b9c04a00f03`  
		Last Modified: Sat, 27 Jan 2024 00:48:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58d30dfcdc3e2a5e0610cd2861841ca25e0652eedd43122f20684e7f230f115`  
		Last Modified: Sat, 27 Jan 2024 00:48:52 GMT  
		Size: 3.5 KB (3474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453056aae58447fe970e8fde1f326fc129042a15aec770dbb065aa0ca7426fe5`  
		Last Modified: Sat, 27 Jan 2024 00:48:58 GMT  
		Size: 118.2 MB (118180700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ac8798d66ca73d5d44ea1ed8d58cd2dad81f630ce8b0d7a89464d4a85bb56e`  
		Last Modified: Sat, 27 Jan 2024 00:48:52 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:8.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:0973a31f7f849bded1d8ee329016f3c75ed3896ed7042b144c45f0233e16e360
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182518314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe0d62207dada883fef29220ebaa559b601cfa0cc2b6c1b9f21930dad4b2e1a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:41:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 03:42:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 03:42:03 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 03:42:04 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 03:42:04 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 27 Jan 2024 03:42:04 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 27 Jan 2024 03:42:04 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 27 Jan 2024 03:42:05 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 03:42:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 03:42:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 03:42:05 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 03:42:05 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 27 Jan 2024 03:42:10 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 03:42:10 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 03:42:10 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 03:42:10 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 03:42:10 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 03:42:10 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 03:42:11 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 03:42:11 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 03:42:11 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 27 Jan 2024 03:42:11 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 03:42:11 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 27 Jan 2024 03:42:11 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 03:42:12 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 03:42:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70ca11832c7ec17b887f0cbc179fd00e9eaaa19dc0890898781fe31c37d0721`  
		Last Modified: Sat, 27 Jan 2024 03:43:16 GMT  
		Size: 61.1 MB (61068901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f06f7ec9ba6e9194d968d839bc5a51c948ca47e7dd634cca3fc4f0c8418fa4`  
		Last Modified: Sat, 27 Jan 2024 03:43:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97055130a023b2d0f09833fca2b853541890035831c6dc69139ee2f5fe90922`  
		Last Modified: Sat, 27 Jan 2024 03:43:08 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ef971a4520af2c383da9c3105d2ebe61857c206f7d38fe20fe605ddec7f731`  
		Last Modified: Sat, 27 Jan 2024 03:43:08 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66435baaef09e74f1c298fe8ad1296edabe4314fb9fb2078037928d12550ccf`  
		Last Modified: Sat, 27 Jan 2024 03:43:08 GMT  
		Size: 3.5 KB (3476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be75eec397b88c12ce8e93f42760d1f810aa156f0bd82601b1e482e83c72a670`  
		Last Modified: Sat, 27 Jan 2024 03:43:13 GMT  
		Size: 118.2 MB (118180669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d20e5a926043f57d0891e83790824116707ee11255e76e51b02819c48dafc32`  
		Last Modified: Sat, 27 Jan 2024 03:43:08 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:8.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:8d287674970f1686ac28e73d5ac9f63a3c638998fa29ff4db7714a4474e46ec1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179570641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c715d50648e2b5c8e4c0a5e0701d94df828e5c4b7e125faa12abe94833af0cf3`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:48 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
# Sat, 27 Jan 2024 00:27:49 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:45:03 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 00:45:17 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 00:45:20 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 00:45:21 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 00:45:22 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 00:45:22 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 00:45:22 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 00:45:23 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 00:45:23 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 00:45:23 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 27 Jan 2024 00:45:24 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 27 Jan 2024 00:45:24 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 27 Jan 2024 00:45:25 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 00:45:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 00:45:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 00:45:27 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 00:45:28 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 27 Jan 2024 00:45:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 00:45:39 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 00:45:40 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 00:45:40 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 00:45:41 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 00:45:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 00:45:42 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 00:45:43 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 00:45:43 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 00:45:44 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 00:45:45 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 00:45:46 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 00:45:46 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 00:45:46 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 00:45:47 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 27 Jan 2024 00:45:47 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 00:45:48 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 27 Jan 2024 00:45:48 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 00:45:49 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 00:45:49 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7231d895a6fafeb2bc3ace13dd93264aacacd41260272c5078656f69557919`  
		Last Modified: Sat, 27 Jan 2024 00:47:34 GMT  
		Size: 58.0 MB (57987363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd72a35024358fd33f3712addc4aa20a7bf210b8fadbdd14a9aaa8253b0ac01`  
		Last Modified: Sat, 27 Jan 2024 00:47:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b639d9045501b3c64dfe5222baaadfd441f9a1c543d46bd02f5261b2f6996f`  
		Last Modified: Sat, 27 Jan 2024 00:47:24 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca334c2e0185403154f6c71d71c1c0d9267f89eca094c08ba805b69052ea8eb8`  
		Last Modified: Sat, 27 Jan 2024 00:47:24 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529d51e2dcead0661a1d0ca99d678fa843da912e7d7c70ac4c3120fc37e82cf1`  
		Last Modified: Sat, 27 Jan 2024 00:47:24 GMT  
		Size: 3.5 KB (3481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36857b1c0e242a3ad2250ed16714647036e33fd36f4b504dd5a4fd0b167a9b1d`  
		Last Modified: Sat, 27 Jan 2024 00:47:31 GMT  
		Size: 118.2 MB (118180710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea15b6bdefe7927d30456f39a7198cf92c63072b8a202934a495de7363d0f2ad`  
		Last Modified: Sat, 27 Jan 2024 00:47:24 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:8.0.0`

```console
$ docker pull bonita@sha256:0eb58c01fe865d15606e2e13b112e88918e0062c377397ee088f4c946c0bffe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:8.0.0` - linux; amd64

```console
$ docker pull bonita@sha256:148ce7a1b77477e51d494ca6eb2d0e72dd88beabc1af9cf6c1c9d8a50bd4f254
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183368755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed37b8369749a73bbd52a624ec28dd95ec0c38496b6a80b2fbbd7eaae5704d9a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:47:40 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 00:47:44 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 00:47:45 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 00:47:45 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 00:47:45 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 00:47:46 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 00:47:46 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 00:47:46 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 00:47:46 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 27 Jan 2024 00:47:46 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 00:47:46 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 00:47:47 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 00:47:47 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 27 Jan 2024 00:47:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 00:47:53 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 00:47:53 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 00:47:53 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 00:47:53 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 00:47:53 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 00:47:53 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 00:47:53 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 00:47:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 00:47:54 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 00:47:54 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 27 Jan 2024 00:47:54 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 00:47:54 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 27 Jan 2024 00:47:54 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 00:47:54 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 00:47:54 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1caad0f049bb37c74f8d0bfd5a4cd6260d83ecb09fbff87cf6cd869b950c9ed`  
		Last Modified: Sat, 27 Jan 2024 00:49:01 GMT  
		Size: 61.8 MB (61798192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7496f35111679745c1b3e57e3c121bf57d74a2f7bfd5a3a43e937dc3ed38c1`  
		Last Modified: Sat, 27 Jan 2024 00:48:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668f94ad6d84ec2445a677e6b29d1a81c199911fd1c91ea6839c80df8d2eaa5a`  
		Last Modified: Sat, 27 Jan 2024 00:48:52 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb2e089a63348da9cc541a2ba138dbf06dab87659d2def8f18c2b9c04a00f03`  
		Last Modified: Sat, 27 Jan 2024 00:48:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58d30dfcdc3e2a5e0610cd2861841ca25e0652eedd43122f20684e7f230f115`  
		Last Modified: Sat, 27 Jan 2024 00:48:52 GMT  
		Size: 3.5 KB (3474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453056aae58447fe970e8fde1f326fc129042a15aec770dbb065aa0ca7426fe5`  
		Last Modified: Sat, 27 Jan 2024 00:48:58 GMT  
		Size: 118.2 MB (118180700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ac8798d66ca73d5d44ea1ed8d58cd2dad81f630ce8b0d7a89464d4a85bb56e`  
		Last Modified: Sat, 27 Jan 2024 00:48:52 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:8.0.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:0973a31f7f849bded1d8ee329016f3c75ed3896ed7042b144c45f0233e16e360
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182518314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe0d62207dada883fef29220ebaa559b601cfa0cc2b6c1b9f21930dad4b2e1a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:41:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 03:42:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 03:42:03 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 03:42:04 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 03:42:04 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 03:42:04 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 27 Jan 2024 03:42:04 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 27 Jan 2024 03:42:04 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 27 Jan 2024 03:42:05 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 03:42:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 03:42:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 03:42:05 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 03:42:05 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 27 Jan 2024 03:42:10 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 03:42:10 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 03:42:10 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 03:42:10 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 03:42:10 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 03:42:10 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 03:42:11 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 03:42:11 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 03:42:11 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 03:42:11 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 27 Jan 2024 03:42:11 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 03:42:11 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 27 Jan 2024 03:42:11 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 03:42:12 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 03:42:12 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70ca11832c7ec17b887f0cbc179fd00e9eaaa19dc0890898781fe31c37d0721`  
		Last Modified: Sat, 27 Jan 2024 03:43:16 GMT  
		Size: 61.1 MB (61068901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f06f7ec9ba6e9194d968d839bc5a51c948ca47e7dd634cca3fc4f0c8418fa4`  
		Last Modified: Sat, 27 Jan 2024 03:43:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97055130a023b2d0f09833fca2b853541890035831c6dc69139ee2f5fe90922`  
		Last Modified: Sat, 27 Jan 2024 03:43:08 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ef971a4520af2c383da9c3105d2ebe61857c206f7d38fe20fe605ddec7f731`  
		Last Modified: Sat, 27 Jan 2024 03:43:08 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66435baaef09e74f1c298fe8ad1296edabe4314fb9fb2078037928d12550ccf`  
		Last Modified: Sat, 27 Jan 2024 03:43:08 GMT  
		Size: 3.5 KB (3476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be75eec397b88c12ce8e93f42760d1f810aa156f0bd82601b1e482e83c72a670`  
		Last Modified: Sat, 27 Jan 2024 03:43:13 GMT  
		Size: 118.2 MB (118180669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d20e5a926043f57d0891e83790824116707ee11255e76e51b02819c48dafc32`  
		Last Modified: Sat, 27 Jan 2024 03:43:08 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:8.0.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:8d287674970f1686ac28e73d5ac9f63a3c638998fa29ff4db7714a4474e46ec1
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179570641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c715d50648e2b5c8e4c0a5e0701d94df828e5c4b7e125faa12abe94833af0cf3`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:48 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
# Sat, 27 Jan 2024 00:27:49 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:45:03 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 27 Jan 2024 00:45:17 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 27 Jan 2024 00:45:20 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 27 Jan 2024 00:45:21 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 27 Jan 2024 00:45:22 GMT
ARG BONITA_VERSION
# Sat, 27 Jan 2024 00:45:22 GMT
ARG BRANDING_VERSION
# Sat, 27 Jan 2024 00:45:22 GMT
ARG BONITA_SHA256
# Sat, 27 Jan 2024 00:45:23 GMT
ARG BASE_URL
# Sat, 27 Jan 2024 00:45:23 GMT
ARG BONITA_URL
# Sat, 27 Jan 2024 00:45:23 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 27 Jan 2024 00:45:24 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 27 Jan 2024 00:45:24 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 27 Jan 2024 00:45:25 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 00:45:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 27 Jan 2024 00:45:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 27 Jan 2024 00:45:27 GMT
RUN mkdir /opt/files
# Sat, 27 Jan 2024 00:45:28 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 27 Jan 2024 00:45:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 27 Jan 2024 00:45:39 GMT
ENV HTTP_API=false
# Sat, 27 Jan 2024 00:45:40 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 27 Jan 2024 00:45:40 GMT
ENV HTTP_API_PASSWORD=
# Sat, 27 Jan 2024 00:45:41 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 27 Jan 2024 00:45:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 27 Jan 2024 00:45:42 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 27 Jan 2024 00:45:43 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 27 Jan 2024 00:45:43 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 27 Jan 2024 00:45:44 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 27 Jan 2024 00:45:45 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 27 Jan 2024 00:45:46 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 27 Jan 2024 00:45:46 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 27 Jan 2024 00:45:46 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 27 Jan 2024 00:45:47 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 27 Jan 2024 00:45:47 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 27 Jan 2024 00:45:48 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 27 Jan 2024 00:45:48 GMT
EXPOSE 8080 9000
# Sat, 27 Jan 2024 00:45:49 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 27 Jan 2024 00:45:49 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7231d895a6fafeb2bc3ace13dd93264aacacd41260272c5078656f69557919`  
		Last Modified: Sat, 27 Jan 2024 00:47:34 GMT  
		Size: 58.0 MB (57987363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd72a35024358fd33f3712addc4aa20a7bf210b8fadbdd14a9aaa8253b0ac01`  
		Last Modified: Sat, 27 Jan 2024 00:47:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b639d9045501b3c64dfe5222baaadfd441f9a1c543d46bd02f5261b2f6996f`  
		Last Modified: Sat, 27 Jan 2024 00:47:24 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca334c2e0185403154f6c71d71c1c0d9267f89eca094c08ba805b69052ea8eb8`  
		Last Modified: Sat, 27 Jan 2024 00:47:24 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529d51e2dcead0661a1d0ca99d678fa843da912e7d7c70ac4c3120fc37e82cf1`  
		Last Modified: Sat, 27 Jan 2024 00:47:24 GMT  
		Size: 3.5 KB (3481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36857b1c0e242a3ad2250ed16714647036e33fd36f4b504dd5a4fd0b167a9b1d`  
		Last Modified: Sat, 27 Jan 2024 00:47:31 GMT  
		Size: 118.2 MB (118180710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea15b6bdefe7927d30456f39a7198cf92c63072b8a202934a495de7363d0f2ad`  
		Last Modified: Sat, 27 Jan 2024 00:47:24 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:9.0`

```console
$ docker pull bonita@sha256:0bedee63b0d734d177ce304454e3cee8ce837fea6c9abcc5c4e366c2ded7bb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:9.0` - linux; amd64

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

### `bonita:9.0` - linux; arm64 variant v8

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

### `bonita:9.0` - linux; ppc64le

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

## `bonita:9.0.0`

```console
$ docker pull bonita@sha256:0bedee63b0d734d177ce304454e3cee8ce837fea6c9abcc5c4e366c2ded7bb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:9.0.0` - linux; amd64

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

### `bonita:9.0.0` - linux; arm64 variant v8

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

### `bonita:9.0.0` - linux; ppc64le

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
