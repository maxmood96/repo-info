## `bonita:latest`

```console
$ docker pull bonita@sha256:1b28c73bbcde8ad017f3c5f5a0c06bc4edae15eb63135489125002fcf84a3fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:8ba7080a1dfe944cfa3aef310a80d85721b63bec01b8e828b4efa3720b6eb958
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180308041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9859da686fb4ba8fbb20e2bfab0b384a8efea93b24a5a7b1671330434e0a3a4a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:13:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 19 Jul 2022 23:13:19 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 19 Jul 2022 23:13:20 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 19 Jul 2022 23:13:21 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 19 Jul 2022 23:13:21 GMT
ARG BONITA_VERSION
# Tue, 19 Jul 2022 23:13:21 GMT
ARG BRANDING_VERSION
# Tue, 19 Jul 2022 23:13:21 GMT
ARG BONITA_SHA256
# Tue, 19 Jul 2022 23:13:21 GMT
ARG BASE_URL
# Tue, 19 Jul 2022 23:13:21 GMT
ARG BONITA_URL
# Tue, 19 Jul 2022 23:13:21 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 19 Jul 2022 23:13:21 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 19 Jul 2022 23:13:21 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 19 Jul 2022 23:13:21 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 19 Jul 2022 23:13:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 19 Jul 2022 23:13:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 19 Jul 2022 23:13:22 GMT
RUN mkdir /opt/files
# Tue, 19 Jul 2022 23:13:22 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 19 Jul 2022 23:13:30 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 19 Jul 2022 23:13:30 GMT
ENV HTTP_API=false
# Tue, 19 Jul 2022 23:13:30 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 19 Jul 2022 23:13:30 GMT
ENV HTTP_API_PASSWORD=
# Tue, 19 Jul 2022 23:13:30 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 19 Jul 2022 23:13:31 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 19 Jul 2022 23:13:31 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 19 Jul 2022 23:13:31 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 19 Jul 2022 23:13:31 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 19 Jul 2022 23:13:31 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 19 Jul 2022 23:13:31 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 19 Jul 2022 23:13:31 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 19 Jul 2022 23:13:31 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 19 Jul 2022 23:13:31 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 19 Jul 2022 23:13:31 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 19 Jul 2022 23:13:32 GMT
EXPOSE 8080 9000
# Tue, 19 Jul 2022 23:13:32 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 19 Jul 2022 23:13:32 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d6d302c572c7936a2c535df7e3665e4cea12109804d7db2e17c2350483f5c6`  
		Last Modified: Tue, 19 Jul 2022 23:14:04 GMT  
		Size: 60.8 MB (60792590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acef1e43a082930ac2a59ac750fcc44e89eee0d2ee2663ea15276a30a761c112`  
		Last Modified: Tue, 19 Jul 2022 23:13:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753d9cad27595f77612d22db5aff3bf2dd14371b997d3fd09692e97837874620`  
		Last Modified: Tue, 19 Jul 2022 23:13:53 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d59792a17a7735b2bbce017b4e9d56c1eb02cc888a64de33a280730e0c1acc4`  
		Last Modified: Tue, 19 Jul 2022 23:13:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a3b0241dac6de74f098fc124ba52ca8c4950e9b58a750f986190c73b50250b`  
		Last Modified: Tue, 19 Jul 2022 23:13:53 GMT  
		Size: 3.0 KB (3031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2f50a37fcc52dae6eaf265933b27d626a5e38dc2eca7b657a3062e4225083d`  
		Last Modified: Tue, 19 Jul 2022 23:14:00 GMT  
		Size: 116.7 MB (116690791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f1095e1b328bb6dfb64e3bc183b9c35afad21a80811146c52cabd8c1251db7`  
		Last Modified: Tue, 19 Jul 2022 23:13:53 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:b14e49b5ca541afa03c868b7617ac3f8bf2dca1217013940b3511bb53ac0fcfe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179532890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550d20a8d0a49aaa3f2a866b84e75f0470fc28aa3f2723eabb7f4b7762991f6d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 19 Jul 2022 22:39:42 GMT
ADD file:158791ae9b4fb18e208925ce1ac7396322e741030bcd9bcae7e320e83f517dfe in / 
# Tue, 19 Jul 2022 22:39:42 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:18:49 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 19 Jul 2022 23:18:53 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 19 Jul 2022 23:18:54 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 19 Jul 2022 23:18:55 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 19 Jul 2022 23:18:56 GMT
ARG BONITA_VERSION
# Tue, 19 Jul 2022 23:18:57 GMT
ARG BRANDING_VERSION
# Tue, 19 Jul 2022 23:18:58 GMT
ARG BONITA_SHA256
# Tue, 19 Jul 2022 23:18:59 GMT
ARG BASE_URL
# Tue, 19 Jul 2022 23:19:00 GMT
ARG BONITA_URL
# Tue, 19 Jul 2022 23:19:01 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 19 Jul 2022 23:19:02 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 19 Jul 2022 23:19:03 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 19 Jul 2022 23:19:04 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 19 Jul 2022 23:19:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 19 Jul 2022 23:19:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 19 Jul 2022 23:19:07 GMT
RUN mkdir /opt/files
# Tue, 19 Jul 2022 23:19:09 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 19 Jul 2022 23:19:20 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 19 Jul 2022 23:19:20 GMT
ENV HTTP_API=false
# Tue, 19 Jul 2022 23:19:21 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 19 Jul 2022 23:19:22 GMT
ENV HTTP_API_PASSWORD=
# Tue, 19 Jul 2022 23:19:23 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 19 Jul 2022 23:19:24 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 19 Jul 2022 23:19:25 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 19 Jul 2022 23:19:26 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 19 Jul 2022 23:19:27 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 19 Jul 2022 23:19:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 19 Jul 2022 23:19:29 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 19 Jul 2022 23:19:30 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 19 Jul 2022 23:19:31 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 19 Jul 2022 23:19:32 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 19 Jul 2022 23:19:34 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 19 Jul 2022 23:19:34 GMT
EXPOSE 8080 9000
# Tue, 19 Jul 2022 23:19:35 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 19 Jul 2022 23:19:36 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e0295fd11fe28fc9d5438734f4d9560cce203f9c2dc12b26e0cfd0c1c02548f7`  
		Last Modified: Tue, 19 Jul 2022 22:40:33 GMT  
		Size: 2.7 MB (2716890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a830a9157109fda713d4c8868452f009b89f5a0aa23e35b64a9fd8ffcbeb248e`  
		Last Modified: Tue, 19 Jul 2022 23:20:35 GMT  
		Size: 60.1 MB (60117412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a219e1f74381cab8fbf4b2158f0e0c8cccf2822e3693f1d8bd13ca27bec084`  
		Last Modified: Tue, 19 Jul 2022 23:20:27 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3153e8cd70c473bb49cd1568765d6399083f8655ace89dcb743660377256711`  
		Last Modified: Tue, 19 Jul 2022 23:20:25 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448fd19395d15f1dff4ee9d541ee4a4789a87a8902684e4abe9aec78f7c80696`  
		Last Modified: Tue, 19 Jul 2022 23:20:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932c91b8ca10c2ff283945c7998d94267040c160f86b043a84e8a794c4d09a3a`  
		Last Modified: Tue, 19 Jul 2022 23:20:25 GMT  
		Size: 3.0 KB (2999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a76d6481ad87c0f65cbd5bf6740c81fbcf6a2b23c530554ec66556c1515ef34`  
		Last Modified: Tue, 19 Jul 2022 23:20:34 GMT  
		Size: 116.7 MB (116688726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdff38d20f7bc060a65e11bf956a87d603ef22aeceda94be739ea3f0f13bd1c`  
		Last Modified: Tue, 19 Jul 2022 23:20:25 GMT  
		Size: 5.4 KB (5395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:6aa40b6458a0b5942abb0cae63ac5d6cd491c5cab4369d5d12de2ebfe3ff2d76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176132332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a0ae6c2630b8698141ad2b826af32382c0033d6e188becc025982a73e9327d8`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 19 Jul 2022 22:26:26 GMT
ADD file:fee9d1c50a43d2072ff528133302b3e4d565d1853e14a7d56be9f4532a330841 in / 
# Tue, 19 Jul 2022 22:26:28 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:19:52 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 19 Jul 2022 23:20:14 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 19 Jul 2022 23:20:29 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 19 Jul 2022 23:20:46 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 19 Jul 2022 23:20:52 GMT
ARG BONITA_VERSION
# Tue, 19 Jul 2022 23:20:59 GMT
ARG BRANDING_VERSION
# Tue, 19 Jul 2022 23:21:02 GMT
ARG BONITA_SHA256
# Tue, 19 Jul 2022 23:21:08 GMT
ARG BASE_URL
# Tue, 19 Jul 2022 23:21:14 GMT
ARG BONITA_URL
# Tue, 19 Jul 2022 23:21:20 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 19 Jul 2022 23:21:26 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 19 Jul 2022 23:21:30 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 19 Jul 2022 23:21:34 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 19 Jul 2022 23:21:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 19 Jul 2022 23:21:44 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 19 Jul 2022 23:21:53 GMT
RUN mkdir /opt/files
# Tue, 19 Jul 2022 23:21:54 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 19 Jul 2022 23:22:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 19 Jul 2022 23:22:25 GMT
ENV HTTP_API=false
# Tue, 19 Jul 2022 23:22:40 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 19 Jul 2022 23:23:01 GMT
ENV HTTP_API_PASSWORD=
# Tue, 19 Jul 2022 23:23:07 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 19 Jul 2022 23:23:15 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 19 Jul 2022 23:23:23 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 19 Jul 2022 23:23:27 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 19 Jul 2022 23:23:32 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 19 Jul 2022 23:23:35 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 19 Jul 2022 23:23:39 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 19 Jul 2022 23:23:42 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 19 Jul 2022 23:23:46 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 19 Jul 2022 23:23:49 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 19 Jul 2022 23:23:50 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 19 Jul 2022 23:23:52 GMT
EXPOSE 8080 9000
# Tue, 19 Jul 2022 23:23:56 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 19 Jul 2022 23:24:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a340aa0651fe455d7a9f4dba0b2b8048ef90ce173a72ac17cf04b9b6af34a2a9`  
		Last Modified: Tue, 19 Jul 2022 22:27:55 GMT  
		Size: 2.8 MB (2811642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0407fa4feb9b7977c80ec2b5ac36e8252a9701c33fb7200fd650a7670fb05bb`  
		Last Modified: Tue, 19 Jul 2022 23:25:13 GMT  
		Size: 56.6 MB (56619857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e50080ba130f5d06da1e2204114d6914f1e86616e352499efccf7b2f91d81f`  
		Last Modified: Tue, 19 Jul 2022 23:25:03 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b74ad31d688802cdd37f41c7f3272a5eb4fd9f2589c0bf3dba4924cc6b7b9eb`  
		Last Modified: Tue, 19 Jul 2022 23:24:59 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e6ab14b03fe37cba7903aa09f0f8d6eb76086d5e0d74230c8816361719fbf8`  
		Last Modified: Tue, 19 Jul 2022 23:25:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1665c44209121633da6010cf0aba1f64314d89fca03cd4c667bc331638f17874`  
		Last Modified: Tue, 19 Jul 2022 23:24:59 GMT  
		Size: 3.0 KB (3033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a94295fcd75be4c6ea68c3b2f076d012eec95766121579e8834a5da6806af73`  
		Last Modified: Tue, 19 Jul 2022 23:25:10 GMT  
		Size: 116.7 MB (116690811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe2d30730b3cd0901bb65ccabcf1d2e8455dbafb8af1caae6e59207dfc8103d`  
		Last Modified: Tue, 19 Jul 2022 23:24:59 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
