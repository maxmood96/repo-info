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
$ docker pull bonita@sha256:7592b8fc5b55c1ec917510f3f3253c2188336bb52c8423cff1c02ece11bbfe22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1` - linux; amd64

```console
$ docker pull bonita@sha256:614b3bf57bd53b58c41e9ae5fa4220fed0f668d1e2242e7d3a91d680acfa12e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177055922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012b0192b99d10145e149860626e2596412995a7937a5ba6977a110556756a94`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:11 GMT
ADD file:aa1af71c6b66d2dddee4797236e3e526f70f904ab641cc0dd6b41445cfedf9b4 in / 
# Thu, 30 Nov 2023 23:23:11 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:52:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 08:52:27 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 16 Mar 2024 08:52:28 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 08:52:29 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 08:52:29 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 16 Mar 2024 08:52:29 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 16 Mar 2024 08:52:29 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 16 Mar 2024 08:52:29 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 16 Mar 2024 08:52:29 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 08:52:30 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 16 Mar 2024 08:52:30 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 08:52:30 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Sat, 16 Mar 2024 08:52:35 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 08:52:35 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 08:52:36 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 08:52:36 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 08:52:36 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 08:52:36 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 08:52:36 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 08:52:37 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 08:52:37 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 08:52:37 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 08:52:37 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d078792c4f9122259f14b539315bd92cbd9490ed73e08255a08689122b143108`  
		Last Modified: Thu, 30 Nov 2023 23:23:58 GMT  
		Size: 2.8 MB (2826431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721052ed1dc84a3fb8eb82831c08d07a18f3c62b5daf18d0b22ae77a931589e4`  
		Last Modified: Sat, 16 Mar 2024 08:53:54 GMT  
		Size: 57.5 MB (57528627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa96d1361e205b329aa07490398c93cc1347da85a1e81c0fba2eea88a1c1de1`  
		Last Modified: Sat, 16 Mar 2024 08:53:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e67e799490441f506f5ee43b439203785a2036c8dc42215fb5d81c9c90b072b`  
		Last Modified: Sat, 16 Mar 2024 08:53:44 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75748435f57b474cb01258d59791e62e667f6c06f11a2feaa3e165bd746c8af2`  
		Last Modified: Sat, 16 Mar 2024 08:53:44 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c7cd28e3fef471a2b2786204e6ff452aedc10e6c54cd68bb781e092e6694f2`  
		Last Modified: Sat, 16 Mar 2024 08:53:44 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eddbe583e25ae21539c8679178336eb1bc81376303c3956b79a9cf0bd2f9c0b`  
		Last Modified: Sat, 16 Mar 2024 08:53:50 GMT  
		Size: 116.7 MB (116690850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0367de0b569c1dc942018aac9e4f575f5e400a5905023692f3f1c06dfdd4ba`  
		Last Modified: Sat, 16 Mar 2024 08:53:44 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:4cecd3e6736b520d11f91d41d41576aca058786b82455e22a77a8cacfea1c8e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176274521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3db678590a7e1f4434d412e23bc0aca607e84596e8110a716cf423b294e405`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:15 GMT
ADD file:3982c510455cc0ceea8cf8dd0b50b69588e35fd4f84522cb4000582c73781672 in / 
# Thu, 30 Nov 2023 23:11:15 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:02:04 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 03:02:07 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 16 Mar 2024 03:02:08 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 03:02:09 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 03:02:09 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 16 Mar 2024 03:02:09 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 16 Mar 2024 03:02:09 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 16 Mar 2024 03:02:10 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 16 Mar 2024 03:02:10 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 03:02:10 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 16 Mar 2024 03:02:10 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 03:02:10 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Sat, 16 Mar 2024 03:02:15 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 03:02:16 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 03:02:16 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 03:02:16 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 03:02:16 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 03:02:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 03:02:17 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 03:02:17 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 03:02:17 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 03:02:17 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 03:02:17 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 03:02:17 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8bc1ab4b84041d57f21a792410a00820f73fda7efe08bcd2ca6245349a40299d`  
		Last Modified: Thu, 30 Nov 2023 23:12:02 GMT  
		Size: 2.7 MB (2721527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f98ad3ac6297db92029c7b269d576cbcc363c7737d78d22f969ecd16dd28b7`  
		Last Modified: Sat, 16 Mar 2024 03:03:39 GMT  
		Size: 56.9 MB (56852201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cde48b71c6346eb41137992194341b2b73915f5a32bc08a0322e5a592687093`  
		Last Modified: Sat, 16 Mar 2024 03:03:33 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac11f8e718ce8403827c6ddb0e0037ae44a2aa68e711d8ab5e6284a7d26764d4`  
		Last Modified: Sat, 16 Mar 2024 03:03:31 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4d0afc9695afd8ee58c91a084b7f9197f659ba2cc3f8dbb82b9491e60256d2`  
		Last Modified: Sat, 16 Mar 2024 03:03:31 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4173ce5ddfd47b90b3e9b87ff89aa4bcca26eb8c61fe9e036de2e10898a2d9f`  
		Last Modified: Sat, 16 Mar 2024 03:03:31 GMT  
		Size: 3.0 KB (3030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e64d658467261890cdb35dcbe493e5998324ba0749685644dbea0a2e895f15`  
		Last Modified: Sat, 16 Mar 2024 03:03:36 GMT  
		Size: 116.7 MB (116690781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0671ecd06e564fc3480ededc35cc8cd240bcae4a96c27ea90a474618fc966c`  
		Last Modified: Sat, 16 Mar 2024 03:03:31 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:87dc261c266072e581c32e8905d47cb352b7e08eaaf70fb3cfd0e01a86fef793
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172870070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5163e25c3dd6ff50e76306219377706a2f1684270e443924fd3a15ecc2f30d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:36 GMT
ADD file:35af09f43b08c93abd4c6b8679d43e8ac40893bf5932c4c21f1bb037f53bb62c in / 
# Thu, 30 Nov 2023 23:19:41 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:57:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 15 Mar 2024 23:57:23 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 15 Mar 2024 23:57:26 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 15 Mar 2024 23:57:27 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 15 Mar 2024 23:57:27 GMT
ARG BONITA_VERSION
# Fri, 15 Mar 2024 23:57:27 GMT
ARG BRANDING_VERSION
# Fri, 15 Mar 2024 23:57:28 GMT
ARG BONITA_SHA256
# Fri, 15 Mar 2024 23:57:28 GMT
ARG BASE_URL
# Fri, 15 Mar 2024 23:57:28 GMT
ARG BONITA_URL
# Fri, 15 Mar 2024 23:57:29 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 15 Mar 2024 23:57:29 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 15 Mar 2024 23:57:29 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 15 Mar 2024 23:57:30 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 15 Mar 2024 23:57:30 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 15 Mar 2024 23:57:31 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 15 Mar 2024 23:57:32 GMT
RUN mkdir /opt/files
# Fri, 15 Mar 2024 23:57:32 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Fri, 15 Mar 2024 23:57:40 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 15 Mar 2024 23:57:42 GMT
ENV HTTP_API=false
# Fri, 15 Mar 2024 23:57:43 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 15 Mar 2024 23:57:43 GMT
ENV HTTP_API_PASSWORD=
# Fri, 15 Mar 2024 23:57:43 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 15 Mar 2024 23:57:43 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 15 Mar 2024 23:57:44 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 15 Mar 2024 23:57:44 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 15 Mar 2024 23:57:44 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 15 Mar 2024 23:57:45 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 15 Mar 2024 23:57:45 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 15 Mar 2024 23:57:46 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 15 Mar 2024 23:57:46 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 15 Mar 2024 23:57:47 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 15 Mar 2024 23:57:47 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 15 Mar 2024 23:57:47 GMT
EXPOSE 8080 9000
# Fri, 15 Mar 2024 23:57:48 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 15 Mar 2024 23:57:48 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:080a2fea3a772fa995cb0b07b4601e7cd57650fa4e8a50866da1de707946d7b3`  
		Last Modified: Thu, 30 Nov 2023 23:20:38 GMT  
		Size: 2.8 MB (2812474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0807b0c3db086f5586354387f13a35749209a7d8b79a5a54e69047df67d323ff`  
		Last Modified: Sat, 16 Mar 2024 00:00:35 GMT  
		Size: 53.4 MB (53356789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca87424184ccc9c707469061b00ce94627f03ef132bb62ba12f8eff075811407`  
		Last Modified: Sat, 16 Mar 2024 00:00:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e15e24b2e80b7692602f77d77fa8ed78831b65b2ea9b8435765ff0d347ff5d`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3f4cc5a4c9c00d82a333ab05169ddc07c5b55f0529af3df9c74a7d24ffc3df`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b8e7fc95d8ea3f1189422a42c5b3b6e5dd05e788f9c36d8b66850569bf3e1`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 3.0 KB (3029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb69de64d5944775cd968c77fee4b2c96ddb9a64b839bd97455b1e8ce60b30d`  
		Last Modified: Sat, 16 Mar 2024 00:00:32 GMT  
		Size: 116.7 MB (116690794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe2e0773c680d40f4cb25bf8670f4a162f89d77a8e1382b4931703314c8beba`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.1-u0`

```console
$ docker pull bonita@sha256:7592b8fc5b55c1ec917510f3f3253c2188336bb52c8423cff1c02ece11bbfe22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1-u0` - linux; amd64

```console
$ docker pull bonita@sha256:614b3bf57bd53b58c41e9ae5fa4220fed0f668d1e2242e7d3a91d680acfa12e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177055922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012b0192b99d10145e149860626e2596412995a7937a5ba6977a110556756a94`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:11 GMT
ADD file:aa1af71c6b66d2dddee4797236e3e526f70f904ab641cc0dd6b41445cfedf9b4 in / 
# Thu, 30 Nov 2023 23:23:11 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:52:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 08:52:27 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 16 Mar 2024 08:52:28 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 08:52:29 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 08:52:29 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 16 Mar 2024 08:52:29 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 16 Mar 2024 08:52:29 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 16 Mar 2024 08:52:29 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 16 Mar 2024 08:52:29 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 08:52:30 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 16 Mar 2024 08:52:30 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 08:52:30 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Sat, 16 Mar 2024 08:52:35 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 08:52:35 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 08:52:36 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 08:52:36 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 08:52:36 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 08:52:36 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 08:52:36 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 08:52:37 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 08:52:37 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 08:52:37 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 08:52:37 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d078792c4f9122259f14b539315bd92cbd9490ed73e08255a08689122b143108`  
		Last Modified: Thu, 30 Nov 2023 23:23:58 GMT  
		Size: 2.8 MB (2826431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721052ed1dc84a3fb8eb82831c08d07a18f3c62b5daf18d0b22ae77a931589e4`  
		Last Modified: Sat, 16 Mar 2024 08:53:54 GMT  
		Size: 57.5 MB (57528627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa96d1361e205b329aa07490398c93cc1347da85a1e81c0fba2eea88a1c1de1`  
		Last Modified: Sat, 16 Mar 2024 08:53:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e67e799490441f506f5ee43b439203785a2036c8dc42215fb5d81c9c90b072b`  
		Last Modified: Sat, 16 Mar 2024 08:53:44 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75748435f57b474cb01258d59791e62e667f6c06f11a2feaa3e165bd746c8af2`  
		Last Modified: Sat, 16 Mar 2024 08:53:44 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c7cd28e3fef471a2b2786204e6ff452aedc10e6c54cd68bb781e092e6694f2`  
		Last Modified: Sat, 16 Mar 2024 08:53:44 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eddbe583e25ae21539c8679178336eb1bc81376303c3956b79a9cf0bd2f9c0b`  
		Last Modified: Sat, 16 Mar 2024 08:53:50 GMT  
		Size: 116.7 MB (116690850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0367de0b569c1dc942018aac9e4f575f5e400a5905023692f3f1c06dfdd4ba`  
		Last Modified: Sat, 16 Mar 2024 08:53:44 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:4cecd3e6736b520d11f91d41d41576aca058786b82455e22a77a8cacfea1c8e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176274521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3db678590a7e1f4434d412e23bc0aca607e84596e8110a716cf423b294e405`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:15 GMT
ADD file:3982c510455cc0ceea8cf8dd0b50b69588e35fd4f84522cb4000582c73781672 in / 
# Thu, 30 Nov 2023 23:11:15 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:02:04 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 03:02:07 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 16 Mar 2024 03:02:08 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 03:02:09 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 03:02:09 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 16 Mar 2024 03:02:09 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 16 Mar 2024 03:02:09 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 16 Mar 2024 03:02:10 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 16 Mar 2024 03:02:10 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 03:02:10 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 16 Mar 2024 03:02:10 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 03:02:10 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Sat, 16 Mar 2024 03:02:15 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 03:02:16 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 03:02:16 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 03:02:16 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 03:02:16 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 03:02:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 03:02:17 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 03:02:17 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 03:02:17 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 03:02:17 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 03:02:17 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 03:02:17 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8bc1ab4b84041d57f21a792410a00820f73fda7efe08bcd2ca6245349a40299d`  
		Last Modified: Thu, 30 Nov 2023 23:12:02 GMT  
		Size: 2.7 MB (2721527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f98ad3ac6297db92029c7b269d576cbcc363c7737d78d22f969ecd16dd28b7`  
		Last Modified: Sat, 16 Mar 2024 03:03:39 GMT  
		Size: 56.9 MB (56852201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cde48b71c6346eb41137992194341b2b73915f5a32bc08a0322e5a592687093`  
		Last Modified: Sat, 16 Mar 2024 03:03:33 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac11f8e718ce8403827c6ddb0e0037ae44a2aa68e711d8ab5e6284a7d26764d4`  
		Last Modified: Sat, 16 Mar 2024 03:03:31 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4d0afc9695afd8ee58c91a084b7f9197f659ba2cc3f8dbb82b9491e60256d2`  
		Last Modified: Sat, 16 Mar 2024 03:03:31 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4173ce5ddfd47b90b3e9b87ff89aa4bcca26eb8c61fe9e036de2e10898a2d9f`  
		Last Modified: Sat, 16 Mar 2024 03:03:31 GMT  
		Size: 3.0 KB (3030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e64d658467261890cdb35dcbe493e5998324ba0749685644dbea0a2e895f15`  
		Last Modified: Sat, 16 Mar 2024 03:03:36 GMT  
		Size: 116.7 MB (116690781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0671ecd06e564fc3480ededc35cc8cd240bcae4a96c27ea90a474618fc966c`  
		Last Modified: Sat, 16 Mar 2024 03:03:31 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:87dc261c266072e581c32e8905d47cb352b7e08eaaf70fb3cfd0e01a86fef793
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172870070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5163e25c3dd6ff50e76306219377706a2f1684270e443924fd3a15ecc2f30d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:36 GMT
ADD file:35af09f43b08c93abd4c6b8679d43e8ac40893bf5932c4c21f1bb037f53bb62c in / 
# Thu, 30 Nov 2023 23:19:41 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:57:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 15 Mar 2024 23:57:23 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 15 Mar 2024 23:57:26 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 15 Mar 2024 23:57:27 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 15 Mar 2024 23:57:27 GMT
ARG BONITA_VERSION
# Fri, 15 Mar 2024 23:57:27 GMT
ARG BRANDING_VERSION
# Fri, 15 Mar 2024 23:57:28 GMT
ARG BONITA_SHA256
# Fri, 15 Mar 2024 23:57:28 GMT
ARG BASE_URL
# Fri, 15 Mar 2024 23:57:28 GMT
ARG BONITA_URL
# Fri, 15 Mar 2024 23:57:29 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 15 Mar 2024 23:57:29 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 15 Mar 2024 23:57:29 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 15 Mar 2024 23:57:30 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 15 Mar 2024 23:57:30 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 15 Mar 2024 23:57:31 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 15 Mar 2024 23:57:32 GMT
RUN mkdir /opt/files
# Fri, 15 Mar 2024 23:57:32 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Fri, 15 Mar 2024 23:57:40 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 15 Mar 2024 23:57:42 GMT
ENV HTTP_API=false
# Fri, 15 Mar 2024 23:57:43 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 15 Mar 2024 23:57:43 GMT
ENV HTTP_API_PASSWORD=
# Fri, 15 Mar 2024 23:57:43 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 15 Mar 2024 23:57:43 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 15 Mar 2024 23:57:44 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 15 Mar 2024 23:57:44 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 15 Mar 2024 23:57:44 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 15 Mar 2024 23:57:45 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 15 Mar 2024 23:57:45 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 15 Mar 2024 23:57:46 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 15 Mar 2024 23:57:46 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 15 Mar 2024 23:57:47 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 15 Mar 2024 23:57:47 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 15 Mar 2024 23:57:47 GMT
EXPOSE 8080 9000
# Fri, 15 Mar 2024 23:57:48 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 15 Mar 2024 23:57:48 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:080a2fea3a772fa995cb0b07b4601e7cd57650fa4e8a50866da1de707946d7b3`  
		Last Modified: Thu, 30 Nov 2023 23:20:38 GMT  
		Size: 2.8 MB (2812474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0807b0c3db086f5586354387f13a35749209a7d8b79a5a54e69047df67d323ff`  
		Last Modified: Sat, 16 Mar 2024 00:00:35 GMT  
		Size: 53.4 MB (53356789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca87424184ccc9c707469061b00ce94627f03ef132bb62ba12f8eff075811407`  
		Last Modified: Sat, 16 Mar 2024 00:00:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e15e24b2e80b7692602f77d77fa8ed78831b65b2ea9b8435765ff0d347ff5d`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3f4cc5a4c9c00d82a333ab05169ddc07c5b55f0529af3df9c74a7d24ffc3df`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b8e7fc95d8ea3f1189422a42c5b3b6e5dd05e788f9c36d8b66850569bf3e1`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 3.0 KB (3029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb69de64d5944775cd968c77fee4b2c96ddb9a64b839bd97455b1e8ce60b30d`  
		Last Modified: Sat, 16 Mar 2024 00:00:32 GMT  
		Size: 116.7 MB (116690794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe2e0773c680d40f4cb25bf8670f4a162f89d77a8e1382b4931703314c8beba`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.2`

```console
$ docker pull bonita@sha256:c2aed227c2879e90df69d37d7c7c7c3545af0b4386dbe27dd53439f747b4078d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.2` - linux; amd64

```console
$ docker pull bonita@sha256:a17d1ac91d78de7fe1eb5e900081c69e463dfaf1829cdb46ef9a1db44b2d6b80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183641885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6346a23ed3b2e4cdeec2654dc4e2be44273d1315ab385d325400c9b168798`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:52:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 08:52:45 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 16 Mar 2024 08:52:46 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 08:52:46 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 08:52:46 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 08:52:46 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 08:52:47 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 08:52:47 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 08:52:47 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 16 Mar 2024 08:52:47 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 16 Mar 2024 08:52:48 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 08:52:48 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 16 Mar 2024 08:52:53 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 08:52:53 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 08:52:53 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 08:52:53 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 08:52:53 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 08:52:54 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 08:52:54 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 08:52:54 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 08:52:54 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 08:52:54 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 08:52:54 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 08:52:54 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e2f30e0170fac06169f99093bfbbb7098e51c23decc518d1307594706f192d`  
		Last Modified: Sat, 16 Mar 2024 08:54:15 GMT  
		Size: 61.6 MB (61631016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fff655c8bc27318c185cf92814c29ea430168868c145c8d0c6c1fa896df558`  
		Last Modified: Sat, 16 Mar 2024 08:54:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c356553c484e84042fc82d0cc263dc3ccfd1b276bdec0c7bde8c9765737c10fd`  
		Last Modified: Sat, 16 Mar 2024 08:54:06 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8568a02a8b77cc1f23a9fedcf057c4b91c164fb03fa7a542bb01ddf0bdae06a`  
		Last Modified: Sat, 16 Mar 2024 08:54:06 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd3251fd5d4a5784c106c5ea9757b340c62762dabb3515ab3f87facc90b2e30`  
		Last Modified: Sat, 16 Mar 2024 08:54:06 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76bebd3b33b4c6592235394d093a66bf3031b35751983d6ec7ae0776dea936d`  
		Last Modified: Sat, 16 Mar 2024 08:54:11 GMT  
		Size: 119.2 MB (119192992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411ee5cf4fe043fdc36e8395e3a216204223d88c5629b7a5c732d28c4b1bc10a`  
		Last Modified: Sat, 16 Mar 2024 08:54:06 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:fbe9b805168ac54c9f9ca1bc974565b675cdcfdc89620c9a8e352934efac5108
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182782808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c1a014787ec3cc6b50a005939c7656540927a604687c1103254c2fe5eae4ad`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:02:21 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 03:02:26 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 16 Mar 2024 03:02:27 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 03:02:27 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 16 Mar 2024 03:02:28 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 16 Mar 2024 03:02:29 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 03:02:29 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 16 Mar 2024 03:02:34 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 03:02:35 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 03:02:35 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 03:02:35 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 03:02:35 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 03:02:35 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 03:02:35 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 03:02:36 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 03:02:36 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 03:02:36 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 03:02:36 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 03:02:36 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af8d8d6c53d7f614d66dbc83a68d4b91901dde18ec29fa4ac900148d9b56f13`  
		Last Modified: Sat, 16 Mar 2024 03:03:59 GMT  
		Size: 60.9 MB (60871527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2d2a008ac68258778d36996998a3c7aeef042e7621559ab04149773b47e12d`  
		Last Modified: Sat, 16 Mar 2024 03:03:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2a5777c86f1116d8f2d5037c763e9cc58f7be1834f9c993d4c9195b638e8f7`  
		Last Modified: Sat, 16 Mar 2024 03:03:51 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ac21a59a3da2f311c58e13e6984f0140a7d6e0ce3add666fd85e79b201269f`  
		Last Modified: Sat, 16 Mar 2024 03:03:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf9e382c19c6da30628695f95110bf20da93c501688f109f8a189ab87e79f61`  
		Last Modified: Sat, 16 Mar 2024 03:03:51 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29682f18d29221fee50a7e663b36ba1504c7d4424d71ac72e478cd549eac18e9`  
		Last Modified: Sat, 16 Mar 2024 03:03:56 GMT  
		Size: 119.2 MB (119192969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3943571ef8d271e5d9bf54a1f4575e3db9162fd74a09e65c2df5c8633c03b8`  
		Last Modified: Sat, 16 Mar 2024 03:03:51 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:0ce8ac817ee24e36974e87d8ea2bd020a595054cebb21d1a1c5ca15fec8ee3fe
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179807397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15048d1b99506c3b756e6e899f55667902aa3d70cd7a88a95aae0d0cbf57364a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:55 GMT
ADD file:cf4fecc20d85962cd46b6911d8ee82b9a3de2fa530bc58e998c2d544a888fdb9 in / 
# Sat, 27 Jan 2024 00:27:55 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:57:55 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 15 Mar 2024 23:58:06 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 15 Mar 2024 23:58:08 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 15 Mar 2024 23:58:09 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 15 Mar 2024 23:58:10 GMT
ARG BONITA_VERSION
# Fri, 15 Mar 2024 23:58:10 GMT
ARG BRANDING_VERSION
# Fri, 15 Mar 2024 23:58:11 GMT
ARG BONITA_SHA256
# Fri, 15 Mar 2024 23:58:11 GMT
ARG BASE_URL
# Fri, 15 Mar 2024 23:58:11 GMT
ARG BONITA_URL
# Fri, 15 Mar 2024 23:58:12 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 15 Mar 2024 23:58:12 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 15 Mar 2024 23:58:12 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 15 Mar 2024 23:58:13 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 15 Mar 2024 23:58:13 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 15 Mar 2024 23:58:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 15 Mar 2024 23:58:15 GMT
RUN mkdir /opt/files
# Fri, 15 Mar 2024 23:58:15 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 15 Mar 2024 23:58:24 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 15 Mar 2024 23:58:26 GMT
ENV HTTP_API=false
# Fri, 15 Mar 2024 23:58:26 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 15 Mar 2024 23:58:26 GMT
ENV HTTP_API_PASSWORD=
# Fri, 15 Mar 2024 23:58:27 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 15 Mar 2024 23:58:27 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 15 Mar 2024 23:58:27 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 15 Mar 2024 23:58:28 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 15 Mar 2024 23:58:28 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 15 Mar 2024 23:58:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 15 Mar 2024 23:58:29 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 15 Mar 2024 23:58:29 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 15 Mar 2024 23:58:30 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 15 Mar 2024 23:58:30 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 15 Mar 2024 23:58:30 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 15 Mar 2024 23:58:31 GMT
EXPOSE 8080 9000
# Fri, 15 Mar 2024 23:58:31 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 15 Mar 2024 23:58:31 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:04646341bdb047ee1a3dd65db76069b9117954385033f5a340622fd170fa4b73`  
		Last Modified: Sat, 27 Jan 2024 00:28:46 GMT  
		Size: 2.8 MB (2802980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c717590678abc6ba9f9b13ab93fd588ecf21bb546a88b89dd176f6301741c39f`  
		Last Modified: Sat, 16 Mar 2024 00:01:01 GMT  
		Size: 57.8 MB (57801404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a2af53c6ef53ec2919045eb31d183a4710a9697ee0a746f37c8cd8af032aa0`  
		Last Modified: Sat, 16 Mar 2024 00:00:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895228bf1c4c4fee002217f84c9aaf231f5c8d78966f57a2daab7d5d52d27180`  
		Last Modified: Sat, 16 Mar 2024 00:00:50 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea02e5282f5da095f8f9364d3db0df27a6df659161f7c39ad3b7fc6157f3896`  
		Last Modified: Sat, 16 Mar 2024 00:00:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274d2d383bc2f52e30690967ff49ce1b7ebb892d4a2566b9d50aad81baa78a34`  
		Last Modified: Sat, 16 Mar 2024 00:00:51 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af18bd400a6bcf4a409035d4013e7c5540badd73c7db72327a1eb1b68165b025`  
		Last Modified: Sat, 16 Mar 2024 00:00:58 GMT  
		Size: 119.2 MB (119192981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885e47b12d875fdd38cdc8c7f63608651009d61fa57e034e1fe45385ab6de95b`  
		Last Modified: Sat, 16 Mar 2024 00:00:51 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.2-u0`

```console
$ docker pull bonita@sha256:c2aed227c2879e90df69d37d7c7c7c3545af0b4386dbe27dd53439f747b4078d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:a17d1ac91d78de7fe1eb5e900081c69e463dfaf1829cdb46ef9a1db44b2d6b80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183641885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6346a23ed3b2e4cdeec2654dc4e2be44273d1315ab385d325400c9b168798`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:52:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 08:52:45 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 16 Mar 2024 08:52:46 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 08:52:46 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 08:52:46 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 08:52:46 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 08:52:47 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 08:52:47 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 08:52:47 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 16 Mar 2024 08:52:47 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 16 Mar 2024 08:52:48 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 08:52:48 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 16 Mar 2024 08:52:53 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 08:52:53 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 08:52:53 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 08:52:53 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 08:52:53 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 08:52:54 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 08:52:54 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 08:52:54 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 08:52:54 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 08:52:54 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 08:52:54 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 08:52:54 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e2f30e0170fac06169f99093bfbbb7098e51c23decc518d1307594706f192d`  
		Last Modified: Sat, 16 Mar 2024 08:54:15 GMT  
		Size: 61.6 MB (61631016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fff655c8bc27318c185cf92814c29ea430168868c145c8d0c6c1fa896df558`  
		Last Modified: Sat, 16 Mar 2024 08:54:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c356553c484e84042fc82d0cc263dc3ccfd1b276bdec0c7bde8c9765737c10fd`  
		Last Modified: Sat, 16 Mar 2024 08:54:06 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8568a02a8b77cc1f23a9fedcf057c4b91c164fb03fa7a542bb01ddf0bdae06a`  
		Last Modified: Sat, 16 Mar 2024 08:54:06 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd3251fd5d4a5784c106c5ea9757b340c62762dabb3515ab3f87facc90b2e30`  
		Last Modified: Sat, 16 Mar 2024 08:54:06 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76bebd3b33b4c6592235394d093a66bf3031b35751983d6ec7ae0776dea936d`  
		Last Modified: Sat, 16 Mar 2024 08:54:11 GMT  
		Size: 119.2 MB (119192992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411ee5cf4fe043fdc36e8395e3a216204223d88c5629b7a5c732d28c4b1bc10a`  
		Last Modified: Sat, 16 Mar 2024 08:54:06 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:fbe9b805168ac54c9f9ca1bc974565b675cdcfdc89620c9a8e352934efac5108
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182782808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c1a014787ec3cc6b50a005939c7656540927a604687c1103254c2fe5eae4ad`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:02:21 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 03:02:26 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 16 Mar 2024 03:02:27 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 03:02:27 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 16 Mar 2024 03:02:28 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 16 Mar 2024 03:02:29 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 03:02:29 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 16 Mar 2024 03:02:34 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 03:02:35 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 03:02:35 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 03:02:35 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 03:02:35 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 03:02:35 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 03:02:35 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 03:02:36 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 03:02:36 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 03:02:36 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 03:02:36 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 03:02:36 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af8d8d6c53d7f614d66dbc83a68d4b91901dde18ec29fa4ac900148d9b56f13`  
		Last Modified: Sat, 16 Mar 2024 03:03:59 GMT  
		Size: 60.9 MB (60871527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2d2a008ac68258778d36996998a3c7aeef042e7621559ab04149773b47e12d`  
		Last Modified: Sat, 16 Mar 2024 03:03:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2a5777c86f1116d8f2d5037c763e9cc58f7be1834f9c993d4c9195b638e8f7`  
		Last Modified: Sat, 16 Mar 2024 03:03:51 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ac21a59a3da2f311c58e13e6984f0140a7d6e0ce3add666fd85e79b201269f`  
		Last Modified: Sat, 16 Mar 2024 03:03:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf9e382c19c6da30628695f95110bf20da93c501688f109f8a189ab87e79f61`  
		Last Modified: Sat, 16 Mar 2024 03:03:51 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29682f18d29221fee50a7e663b36ba1504c7d4424d71ac72e478cd549eac18e9`  
		Last Modified: Sat, 16 Mar 2024 03:03:56 GMT  
		Size: 119.2 MB (119192969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3943571ef8d271e5d9bf54a1f4575e3db9162fd74a09e65c2df5c8633c03b8`  
		Last Modified: Sat, 16 Mar 2024 03:03:51 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:0ce8ac817ee24e36974e87d8ea2bd020a595054cebb21d1a1c5ca15fec8ee3fe
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179807397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15048d1b99506c3b756e6e899f55667902aa3d70cd7a88a95aae0d0cbf57364a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:55 GMT
ADD file:cf4fecc20d85962cd46b6911d8ee82b9a3de2fa530bc58e998c2d544a888fdb9 in / 
# Sat, 27 Jan 2024 00:27:55 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:57:55 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 15 Mar 2024 23:58:06 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 15 Mar 2024 23:58:08 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 15 Mar 2024 23:58:09 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 15 Mar 2024 23:58:10 GMT
ARG BONITA_VERSION
# Fri, 15 Mar 2024 23:58:10 GMT
ARG BRANDING_VERSION
# Fri, 15 Mar 2024 23:58:11 GMT
ARG BONITA_SHA256
# Fri, 15 Mar 2024 23:58:11 GMT
ARG BASE_URL
# Fri, 15 Mar 2024 23:58:11 GMT
ARG BONITA_URL
# Fri, 15 Mar 2024 23:58:12 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 15 Mar 2024 23:58:12 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 15 Mar 2024 23:58:12 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 15 Mar 2024 23:58:13 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 15 Mar 2024 23:58:13 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 15 Mar 2024 23:58:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 15 Mar 2024 23:58:15 GMT
RUN mkdir /opt/files
# Fri, 15 Mar 2024 23:58:15 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 15 Mar 2024 23:58:24 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 15 Mar 2024 23:58:26 GMT
ENV HTTP_API=false
# Fri, 15 Mar 2024 23:58:26 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 15 Mar 2024 23:58:26 GMT
ENV HTTP_API_PASSWORD=
# Fri, 15 Mar 2024 23:58:27 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 15 Mar 2024 23:58:27 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 15 Mar 2024 23:58:27 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 15 Mar 2024 23:58:28 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 15 Mar 2024 23:58:28 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 15 Mar 2024 23:58:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 15 Mar 2024 23:58:29 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 15 Mar 2024 23:58:29 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 15 Mar 2024 23:58:30 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 15 Mar 2024 23:58:30 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 15 Mar 2024 23:58:30 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 15 Mar 2024 23:58:31 GMT
EXPOSE 8080 9000
# Fri, 15 Mar 2024 23:58:31 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 15 Mar 2024 23:58:31 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:04646341bdb047ee1a3dd65db76069b9117954385033f5a340622fd170fa4b73`  
		Last Modified: Sat, 27 Jan 2024 00:28:46 GMT  
		Size: 2.8 MB (2802980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c717590678abc6ba9f9b13ab93fd588ecf21bb546a88b89dd176f6301741c39f`  
		Last Modified: Sat, 16 Mar 2024 00:01:01 GMT  
		Size: 57.8 MB (57801404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a2af53c6ef53ec2919045eb31d183a4710a9697ee0a746f37c8cd8af032aa0`  
		Last Modified: Sat, 16 Mar 2024 00:00:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895228bf1c4c4fee002217f84c9aaf231f5c8d78966f57a2daab7d5d52d27180`  
		Last Modified: Sat, 16 Mar 2024 00:00:50 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea02e5282f5da095f8f9364d3db0df27a6df659161f7c39ad3b7fc6157f3896`  
		Last Modified: Sat, 16 Mar 2024 00:00:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274d2d383bc2f52e30690967ff49ce1b7ebb892d4a2566b9d50aad81baa78a34`  
		Last Modified: Sat, 16 Mar 2024 00:00:51 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af18bd400a6bcf4a409035d4013e7c5540badd73c7db72327a1eb1b68165b025`  
		Last Modified: Sat, 16 Mar 2024 00:00:58 GMT  
		Size: 119.2 MB (119192981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885e47b12d875fdd38cdc8c7f63608651009d61fa57e034e1fe45385ab6de95b`  
		Last Modified: Sat, 16 Mar 2024 00:00:51 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2023.1`

```console
$ docker pull bonita@sha256:49fb74fc3b71f89f6d6e9797d164b1600abad1849a6028dd80bfd128061892f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2023.1` - linux; amd64

```console
$ docker pull bonita@sha256:c61e23c8804a29ca77e17220830059906ac2387c9c7a5a77fc237228705f7f2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183368861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d5a400c747eea94ef876f915427cee5dde2ff2518192d9b256a9284362111d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:52:58 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 08:53:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 16 Mar 2024 08:53:03 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 08:53:04 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 08:53:04 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 16 Mar 2024 08:53:04 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 16 Mar 2024 08:53:04 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 16 Mar 2024 08:53:05 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 16 Mar 2024 08:53:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 08:53:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 16 Mar 2024 08:53:05 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 08:53:05 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 16 Mar 2024 08:53:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 08:53:12 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 08:53:12 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 08:53:12 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 08:53:12 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 08:53:12 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 08:53:13 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 08:53:13 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 16 Mar 2024 08:53:13 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 08:53:13 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 16 Mar 2024 08:53:13 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 08:53:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 08:53:13 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd69f83dfb1af6156ab4a603d6adb5038a3de61d8f309815d8f71ff432d24d47`  
		Last Modified: Sat, 16 Mar 2024 08:54:37 GMT  
		Size: 61.8 MB (61798280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94aba78b855360f5e07023859c27c6506e8f329fa477a5127000ccae33f30201`  
		Last Modified: Sat, 16 Mar 2024 08:54:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b7103bb98a588a5b65a049c39d0bc58f591e89698cba680cd14f0ddfce1611`  
		Last Modified: Sat, 16 Mar 2024 08:54:27 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12969946da581ab79c1bd1f6fdc1c1b2c18a2ca3f1b92085c561cd6800ea1951`  
		Last Modified: Sat, 16 Mar 2024 08:54:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643dcbdefb131f742ad8a91eb18884649b7b3479c712bdea6b771a624e23d331`  
		Last Modified: Sat, 16 Mar 2024 08:54:27 GMT  
		Size: 3.5 KB (3479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca1495dd0222fa0452024c10ebb8999a7d67b681227ffba852ca7a38965b9b8`  
		Last Modified: Sat, 16 Mar 2024 08:54:33 GMT  
		Size: 118.2 MB (118180716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc08a431531cb196aae81bc59a46fe2aee90e8f57907cca39634d377a878233`  
		Last Modified: Sat, 16 Mar 2024 08:54:27 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2cf7a9e0dfec7e412366db745749a1882de313229dace54a1c0fa4d0238b207d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182518350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfe723e8e69c3692f902091e19028d21a854c8a561d8d56531186bd06e0742a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:02:40 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 03:02:46 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 16 Mar 2024 03:02:47 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 03:02:47 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 16 Mar 2024 03:02:48 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 16 Mar 2024 03:02:49 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 03:02:49 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 16 Mar 2024 03:02:55 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 03:02:56 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 03:02:56 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 03:02:56 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 03:02:56 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 03:02:56 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 03:02:56 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 03:02:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 16 Mar 2024 03:02:57 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 03:02:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 16 Mar 2024 03:02:57 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 03:02:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 03:02:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce75a0fccdb3c045fa082c0ced7f4fd9c2006c2330268952b760f12a2a35cc2`  
		Last Modified: Sat, 16 Mar 2024 03:04:19 GMT  
		Size: 61.1 MB (61068930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea23591cbb412dc67ab0bfad05949f7130f8cd6a1cefc6d37cebcd7f7b1c5b2`  
		Last Modified: Sat, 16 Mar 2024 03:04:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1a894c4d4faa07382633d71c68dd996729142c643773e2cf44864ffa432b8d`  
		Last Modified: Sat, 16 Mar 2024 03:04:11 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ee70d741bab4e322b44159fb2b328b8d0f46492e3dc6b002fe2e8e53c3d2a0`  
		Last Modified: Sat, 16 Mar 2024 03:04:10 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1256dfedfd6fbd6a595d7103aceab7d6962b0f7953070414a38572d90da7f6f6`  
		Last Modified: Sat, 16 Mar 2024 03:04:10 GMT  
		Size: 3.5 KB (3479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7afcf6e44eda62588204c309d1cbd6b29e94087bbe91daf29c0502245aa694`  
		Last Modified: Sat, 16 Mar 2024 03:04:15 GMT  
		Size: 118.2 MB (118180678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0103e0c0bb36f49efc6825fbe1d901ae5058087885ac6b11b842e16937e13e48`  
		Last Modified: Sat, 16 Mar 2024 03:04:11 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:af52de366938b25246c9b0cc840e8a08be35aa910856b42233081be537af1616
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179570657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b923c1405d914085ffe4f287be19baba2d93dcf48f442633c6c95d6c2f960f67`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:48 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
# Sat, 27 Jan 2024 00:27:49 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:58:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 15 Mar 2024 23:58:48 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 15 Mar 2024 23:58:51 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 15 Mar 2024 23:58:52 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 15 Mar 2024 23:58:52 GMT
ARG BONITA_VERSION
# Fri, 15 Mar 2024 23:58:53 GMT
ARG BRANDING_VERSION
# Fri, 15 Mar 2024 23:58:53 GMT
ARG BONITA_SHA256
# Fri, 15 Mar 2024 23:58:54 GMT
ARG BASE_URL
# Fri, 15 Mar 2024 23:58:54 GMT
ARG BONITA_URL
# Fri, 15 Mar 2024 23:58:54 GMT
ENV BONITA_VERSION=8.0.0
# Fri, 15 Mar 2024 23:58:55 GMT
ENV BRANDING_VERSION=2023.1-u0
# Fri, 15 Mar 2024 23:58:55 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Fri, 15 Mar 2024 23:58:56 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Fri, 15 Mar 2024 23:58:56 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 15 Mar 2024 23:58:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Fri, 15 Mar 2024 23:58:57 GMT
RUN mkdir /opt/files
# Fri, 15 Mar 2024 23:58:58 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Fri, 15 Mar 2024 23:59:07 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 15 Mar 2024 23:59:09 GMT
ENV HTTP_API=false
# Fri, 15 Mar 2024 23:59:09 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 15 Mar 2024 23:59:10 GMT
ENV HTTP_API_PASSWORD=
# Fri, 15 Mar 2024 23:59:10 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 15 Mar 2024 23:59:11 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 15 Mar 2024 23:59:11 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 15 Mar 2024 23:59:12 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 15 Mar 2024 23:59:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 15 Mar 2024 23:59:12 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 15 Mar 2024 23:59:13 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 15 Mar 2024 23:59:13 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 15 Mar 2024 23:59:14 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 15 Mar 2024 23:59:14 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 15 Mar 2024 23:59:15 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Fri, 15 Mar 2024 23:59:15 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 15 Mar 2024 23:59:15 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 15 Mar 2024 23:59:16 GMT
EXPOSE 8080 9000
# Fri, 15 Mar 2024 23:59:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 15 Mar 2024 23:59:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c0212967952fa7ddbc3dc401470abd092772f3da917bc2a5d92a4c19c5a235`  
		Last Modified: Sat, 16 Mar 2024 00:01:26 GMT  
		Size: 58.0 MB (57987381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecc94bb125d0bef7ff258cf75e8d9d7a6bce29b6cb1476b47ea61fcd5bf0f4a`  
		Last Modified: Sat, 16 Mar 2024 00:01:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c820ce1cbbd3221d267e7cc71ea8fc0da9c200f9172b9ea22c01549cfcb4051`  
		Last Modified: Sat, 16 Mar 2024 00:01:15 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a842fcb3410a5903a75519182004bd622d3f882e199f4187385cca90c855fcb`  
		Last Modified: Sat, 16 Mar 2024 00:01:16 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb00e368f8e725ba5330f672f1b6c237b8665cebc5d62b0cb31dd200446d641`  
		Last Modified: Sat, 16 Mar 2024 00:01:16 GMT  
		Size: 3.5 KB (3479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46652bb2301a0a5c735983f07b53553e8d9e4274acf1471c2dcfc8a6f3c38f20`  
		Last Modified: Sat, 16 Mar 2024 00:01:23 GMT  
		Size: 118.2 MB (118180704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a98a94d1a08a90ac94fa17e97526feca756d6b4e8e65d5164153382538246f`  
		Last Modified: Sat, 16 Mar 2024 00:01:15 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2023.1-u0`

```console
$ docker pull bonita@sha256:49fb74fc3b71f89f6d6e9797d164b1600abad1849a6028dd80bfd128061892f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2023.1-u0` - linux; amd64

```console
$ docker pull bonita@sha256:c61e23c8804a29ca77e17220830059906ac2387c9c7a5a77fc237228705f7f2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183368861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d5a400c747eea94ef876f915427cee5dde2ff2518192d9b256a9284362111d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:52:58 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 08:53:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 16 Mar 2024 08:53:03 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 08:53:04 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 08:53:04 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 16 Mar 2024 08:53:04 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 16 Mar 2024 08:53:04 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 16 Mar 2024 08:53:05 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 16 Mar 2024 08:53:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 08:53:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 16 Mar 2024 08:53:05 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 08:53:05 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 16 Mar 2024 08:53:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 08:53:12 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 08:53:12 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 08:53:12 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 08:53:12 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 08:53:12 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 08:53:13 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 08:53:13 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 16 Mar 2024 08:53:13 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 08:53:13 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 16 Mar 2024 08:53:13 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 08:53:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 08:53:13 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd69f83dfb1af6156ab4a603d6adb5038a3de61d8f309815d8f71ff432d24d47`  
		Last Modified: Sat, 16 Mar 2024 08:54:37 GMT  
		Size: 61.8 MB (61798280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94aba78b855360f5e07023859c27c6506e8f329fa477a5127000ccae33f30201`  
		Last Modified: Sat, 16 Mar 2024 08:54:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b7103bb98a588a5b65a049c39d0bc58f591e89698cba680cd14f0ddfce1611`  
		Last Modified: Sat, 16 Mar 2024 08:54:27 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12969946da581ab79c1bd1f6fdc1c1b2c18a2ca3f1b92085c561cd6800ea1951`  
		Last Modified: Sat, 16 Mar 2024 08:54:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643dcbdefb131f742ad8a91eb18884649b7b3479c712bdea6b771a624e23d331`  
		Last Modified: Sat, 16 Mar 2024 08:54:27 GMT  
		Size: 3.5 KB (3479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca1495dd0222fa0452024c10ebb8999a7d67b681227ffba852ca7a38965b9b8`  
		Last Modified: Sat, 16 Mar 2024 08:54:33 GMT  
		Size: 118.2 MB (118180716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc08a431531cb196aae81bc59a46fe2aee90e8f57907cca39634d377a878233`  
		Last Modified: Sat, 16 Mar 2024 08:54:27 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2cf7a9e0dfec7e412366db745749a1882de313229dace54a1c0fa4d0238b207d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182518350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfe723e8e69c3692f902091e19028d21a854c8a561d8d56531186bd06e0742a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:02:40 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 03:02:46 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 16 Mar 2024 03:02:47 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 03:02:47 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 16 Mar 2024 03:02:48 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 16 Mar 2024 03:02:49 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 03:02:49 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 16 Mar 2024 03:02:55 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 03:02:56 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 03:02:56 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 03:02:56 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 03:02:56 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 03:02:56 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 03:02:56 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 03:02:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 16 Mar 2024 03:02:57 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 03:02:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 16 Mar 2024 03:02:57 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 03:02:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 03:02:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce75a0fccdb3c045fa082c0ced7f4fd9c2006c2330268952b760f12a2a35cc2`  
		Last Modified: Sat, 16 Mar 2024 03:04:19 GMT  
		Size: 61.1 MB (61068930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea23591cbb412dc67ab0bfad05949f7130f8cd6a1cefc6d37cebcd7f7b1c5b2`  
		Last Modified: Sat, 16 Mar 2024 03:04:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1a894c4d4faa07382633d71c68dd996729142c643773e2cf44864ffa432b8d`  
		Last Modified: Sat, 16 Mar 2024 03:04:11 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ee70d741bab4e322b44159fb2b328b8d0f46492e3dc6b002fe2e8e53c3d2a0`  
		Last Modified: Sat, 16 Mar 2024 03:04:10 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1256dfedfd6fbd6a595d7103aceab7d6962b0f7953070414a38572d90da7f6f6`  
		Last Modified: Sat, 16 Mar 2024 03:04:10 GMT  
		Size: 3.5 KB (3479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7afcf6e44eda62588204c309d1cbd6b29e94087bbe91daf29c0502245aa694`  
		Last Modified: Sat, 16 Mar 2024 03:04:15 GMT  
		Size: 118.2 MB (118180678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0103e0c0bb36f49efc6825fbe1d901ae5058087885ac6b11b842e16937e13e48`  
		Last Modified: Sat, 16 Mar 2024 03:04:11 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2023.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:af52de366938b25246c9b0cc840e8a08be35aa910856b42233081be537af1616
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179570657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b923c1405d914085ffe4f287be19baba2d93dcf48f442633c6c95d6c2f960f67`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:48 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
# Sat, 27 Jan 2024 00:27:49 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:58:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 15 Mar 2024 23:58:48 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 15 Mar 2024 23:58:51 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 15 Mar 2024 23:58:52 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 15 Mar 2024 23:58:52 GMT
ARG BONITA_VERSION
# Fri, 15 Mar 2024 23:58:53 GMT
ARG BRANDING_VERSION
# Fri, 15 Mar 2024 23:58:53 GMT
ARG BONITA_SHA256
# Fri, 15 Mar 2024 23:58:54 GMT
ARG BASE_URL
# Fri, 15 Mar 2024 23:58:54 GMT
ARG BONITA_URL
# Fri, 15 Mar 2024 23:58:54 GMT
ENV BONITA_VERSION=8.0.0
# Fri, 15 Mar 2024 23:58:55 GMT
ENV BRANDING_VERSION=2023.1-u0
# Fri, 15 Mar 2024 23:58:55 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Fri, 15 Mar 2024 23:58:56 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Fri, 15 Mar 2024 23:58:56 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 15 Mar 2024 23:58:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Fri, 15 Mar 2024 23:58:57 GMT
RUN mkdir /opt/files
# Fri, 15 Mar 2024 23:58:58 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Fri, 15 Mar 2024 23:59:07 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 15 Mar 2024 23:59:09 GMT
ENV HTTP_API=false
# Fri, 15 Mar 2024 23:59:09 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 15 Mar 2024 23:59:10 GMT
ENV HTTP_API_PASSWORD=
# Fri, 15 Mar 2024 23:59:10 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 15 Mar 2024 23:59:11 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 15 Mar 2024 23:59:11 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 15 Mar 2024 23:59:12 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 15 Mar 2024 23:59:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 15 Mar 2024 23:59:12 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 15 Mar 2024 23:59:13 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 15 Mar 2024 23:59:13 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 15 Mar 2024 23:59:14 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 15 Mar 2024 23:59:14 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 15 Mar 2024 23:59:15 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Fri, 15 Mar 2024 23:59:15 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 15 Mar 2024 23:59:15 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 15 Mar 2024 23:59:16 GMT
EXPOSE 8080 9000
# Fri, 15 Mar 2024 23:59:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 15 Mar 2024 23:59:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c0212967952fa7ddbc3dc401470abd092772f3da917bc2a5d92a4c19c5a235`  
		Last Modified: Sat, 16 Mar 2024 00:01:26 GMT  
		Size: 58.0 MB (57987381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecc94bb125d0bef7ff258cf75e8d9d7a6bce29b6cb1476b47ea61fcd5bf0f4a`  
		Last Modified: Sat, 16 Mar 2024 00:01:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c820ce1cbbd3221d267e7cc71ea8fc0da9c200f9172b9ea22c01549cfcb4051`  
		Last Modified: Sat, 16 Mar 2024 00:01:15 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a842fcb3410a5903a75519182004bd622d3f882e199f4187385cca90c855fcb`  
		Last Modified: Sat, 16 Mar 2024 00:01:16 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb00e368f8e725ba5330f672f1b6c237b8665cebc5d62b0cb31dd200446d641`  
		Last Modified: Sat, 16 Mar 2024 00:01:16 GMT  
		Size: 3.5 KB (3479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46652bb2301a0a5c735983f07b53553e8d9e4274acf1471c2dcfc8a6f3c38f20`  
		Last Modified: Sat, 16 Mar 2024 00:01:23 GMT  
		Size: 118.2 MB (118180704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a98a94d1a08a90ac94fa17e97526feca756d6b4e8e65d5164153382538246f`  
		Last Modified: Sat, 16 Mar 2024 00:01:15 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2023.2`

```console
$ docker pull bonita@sha256:48fe1a388de4f57a67014c8ee26f65ca3a26b95c3c39a23069bc97dbae778d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2023.2` - linux; amd64

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

### `bonita:2023.2` - linux; arm64 variant v8

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

### `bonita:2023.2` - linux; ppc64le

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

## `bonita:2023.2-u0`

```console
$ docker pull bonita@sha256:48fe1a388de4f57a67014c8ee26f65ca3a26b95c3c39a23069bc97dbae778d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2023.2-u0` - linux; amd64

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

### `bonita:2023.2-u0` - linux; arm64 variant v8

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

### `bonita:2023.2-u0` - linux; ppc64le

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

## `bonita:7.14`

```console
$ docker pull bonita@sha256:7592b8fc5b55c1ec917510f3f3253c2188336bb52c8423cff1c02ece11bbfe22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14` - linux; amd64

```console
$ docker pull bonita@sha256:614b3bf57bd53b58c41e9ae5fa4220fed0f668d1e2242e7d3a91d680acfa12e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177055922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012b0192b99d10145e149860626e2596412995a7937a5ba6977a110556756a94`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:11 GMT
ADD file:aa1af71c6b66d2dddee4797236e3e526f70f904ab641cc0dd6b41445cfedf9b4 in / 
# Thu, 30 Nov 2023 23:23:11 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:52:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 08:52:27 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 16 Mar 2024 08:52:28 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 08:52:29 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 08:52:29 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 16 Mar 2024 08:52:29 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 16 Mar 2024 08:52:29 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 16 Mar 2024 08:52:29 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 16 Mar 2024 08:52:29 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 08:52:30 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 16 Mar 2024 08:52:30 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 08:52:30 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Sat, 16 Mar 2024 08:52:35 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 08:52:35 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 08:52:36 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 08:52:36 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 08:52:36 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 08:52:36 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 08:52:36 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 08:52:37 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 08:52:37 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 08:52:37 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 08:52:37 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d078792c4f9122259f14b539315bd92cbd9490ed73e08255a08689122b143108`  
		Last Modified: Thu, 30 Nov 2023 23:23:58 GMT  
		Size: 2.8 MB (2826431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721052ed1dc84a3fb8eb82831c08d07a18f3c62b5daf18d0b22ae77a931589e4`  
		Last Modified: Sat, 16 Mar 2024 08:53:54 GMT  
		Size: 57.5 MB (57528627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa96d1361e205b329aa07490398c93cc1347da85a1e81c0fba2eea88a1c1de1`  
		Last Modified: Sat, 16 Mar 2024 08:53:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e67e799490441f506f5ee43b439203785a2036c8dc42215fb5d81c9c90b072b`  
		Last Modified: Sat, 16 Mar 2024 08:53:44 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75748435f57b474cb01258d59791e62e667f6c06f11a2feaa3e165bd746c8af2`  
		Last Modified: Sat, 16 Mar 2024 08:53:44 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c7cd28e3fef471a2b2786204e6ff452aedc10e6c54cd68bb781e092e6694f2`  
		Last Modified: Sat, 16 Mar 2024 08:53:44 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eddbe583e25ae21539c8679178336eb1bc81376303c3956b79a9cf0bd2f9c0b`  
		Last Modified: Sat, 16 Mar 2024 08:53:50 GMT  
		Size: 116.7 MB (116690850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0367de0b569c1dc942018aac9e4f575f5e400a5905023692f3f1c06dfdd4ba`  
		Last Modified: Sat, 16 Mar 2024 08:53:44 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:4cecd3e6736b520d11f91d41d41576aca058786b82455e22a77a8cacfea1c8e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176274521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3db678590a7e1f4434d412e23bc0aca607e84596e8110a716cf423b294e405`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:15 GMT
ADD file:3982c510455cc0ceea8cf8dd0b50b69588e35fd4f84522cb4000582c73781672 in / 
# Thu, 30 Nov 2023 23:11:15 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:02:04 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 03:02:07 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 16 Mar 2024 03:02:08 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 03:02:09 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 03:02:09 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 16 Mar 2024 03:02:09 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 16 Mar 2024 03:02:09 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 16 Mar 2024 03:02:10 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 16 Mar 2024 03:02:10 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 03:02:10 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 16 Mar 2024 03:02:10 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 03:02:10 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Sat, 16 Mar 2024 03:02:15 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 03:02:16 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 03:02:16 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 03:02:16 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 03:02:16 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 03:02:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 03:02:17 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 03:02:17 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 03:02:17 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 03:02:17 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 03:02:17 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 03:02:17 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8bc1ab4b84041d57f21a792410a00820f73fda7efe08bcd2ca6245349a40299d`  
		Last Modified: Thu, 30 Nov 2023 23:12:02 GMT  
		Size: 2.7 MB (2721527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f98ad3ac6297db92029c7b269d576cbcc363c7737d78d22f969ecd16dd28b7`  
		Last Modified: Sat, 16 Mar 2024 03:03:39 GMT  
		Size: 56.9 MB (56852201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cde48b71c6346eb41137992194341b2b73915f5a32bc08a0322e5a592687093`  
		Last Modified: Sat, 16 Mar 2024 03:03:33 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac11f8e718ce8403827c6ddb0e0037ae44a2aa68e711d8ab5e6284a7d26764d4`  
		Last Modified: Sat, 16 Mar 2024 03:03:31 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4d0afc9695afd8ee58c91a084b7f9197f659ba2cc3f8dbb82b9491e60256d2`  
		Last Modified: Sat, 16 Mar 2024 03:03:31 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4173ce5ddfd47b90b3e9b87ff89aa4bcca26eb8c61fe9e036de2e10898a2d9f`  
		Last Modified: Sat, 16 Mar 2024 03:03:31 GMT  
		Size: 3.0 KB (3030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e64d658467261890cdb35dcbe493e5998324ba0749685644dbea0a2e895f15`  
		Last Modified: Sat, 16 Mar 2024 03:03:36 GMT  
		Size: 116.7 MB (116690781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0671ecd06e564fc3480ededc35cc8cd240bcae4a96c27ea90a474618fc966c`  
		Last Modified: Sat, 16 Mar 2024 03:03:31 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; ppc64le

```console
$ docker pull bonita@sha256:87dc261c266072e581c32e8905d47cb352b7e08eaaf70fb3cfd0e01a86fef793
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172870070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5163e25c3dd6ff50e76306219377706a2f1684270e443924fd3a15ecc2f30d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:36 GMT
ADD file:35af09f43b08c93abd4c6b8679d43e8ac40893bf5932c4c21f1bb037f53bb62c in / 
# Thu, 30 Nov 2023 23:19:41 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:57:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 15 Mar 2024 23:57:23 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 15 Mar 2024 23:57:26 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 15 Mar 2024 23:57:27 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 15 Mar 2024 23:57:27 GMT
ARG BONITA_VERSION
# Fri, 15 Mar 2024 23:57:27 GMT
ARG BRANDING_VERSION
# Fri, 15 Mar 2024 23:57:28 GMT
ARG BONITA_SHA256
# Fri, 15 Mar 2024 23:57:28 GMT
ARG BASE_URL
# Fri, 15 Mar 2024 23:57:28 GMT
ARG BONITA_URL
# Fri, 15 Mar 2024 23:57:29 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 15 Mar 2024 23:57:29 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 15 Mar 2024 23:57:29 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 15 Mar 2024 23:57:30 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 15 Mar 2024 23:57:30 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 15 Mar 2024 23:57:31 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 15 Mar 2024 23:57:32 GMT
RUN mkdir /opt/files
# Fri, 15 Mar 2024 23:57:32 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Fri, 15 Mar 2024 23:57:40 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 15 Mar 2024 23:57:42 GMT
ENV HTTP_API=false
# Fri, 15 Mar 2024 23:57:43 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 15 Mar 2024 23:57:43 GMT
ENV HTTP_API_PASSWORD=
# Fri, 15 Mar 2024 23:57:43 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 15 Mar 2024 23:57:43 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 15 Mar 2024 23:57:44 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 15 Mar 2024 23:57:44 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 15 Mar 2024 23:57:44 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 15 Mar 2024 23:57:45 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 15 Mar 2024 23:57:45 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 15 Mar 2024 23:57:46 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 15 Mar 2024 23:57:46 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 15 Mar 2024 23:57:47 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 15 Mar 2024 23:57:47 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 15 Mar 2024 23:57:47 GMT
EXPOSE 8080 9000
# Fri, 15 Mar 2024 23:57:48 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 15 Mar 2024 23:57:48 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:080a2fea3a772fa995cb0b07b4601e7cd57650fa4e8a50866da1de707946d7b3`  
		Last Modified: Thu, 30 Nov 2023 23:20:38 GMT  
		Size: 2.8 MB (2812474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0807b0c3db086f5586354387f13a35749209a7d8b79a5a54e69047df67d323ff`  
		Last Modified: Sat, 16 Mar 2024 00:00:35 GMT  
		Size: 53.4 MB (53356789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca87424184ccc9c707469061b00ce94627f03ef132bb62ba12f8eff075811407`  
		Last Modified: Sat, 16 Mar 2024 00:00:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e15e24b2e80b7692602f77d77fa8ed78831b65b2ea9b8435765ff0d347ff5d`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3f4cc5a4c9c00d82a333ab05169ddc07c5b55f0529af3df9c74a7d24ffc3df`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b8e7fc95d8ea3f1189422a42c5b3b6e5dd05e788f9c36d8b66850569bf3e1`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 3.0 KB (3029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb69de64d5944775cd968c77fee4b2c96ddb9a64b839bd97455b1e8ce60b30d`  
		Last Modified: Sat, 16 Mar 2024 00:00:32 GMT  
		Size: 116.7 MB (116690794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe2e0773c680d40f4cb25bf8670f4a162f89d77a8e1382b4931703314c8beba`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14.0`

```console
$ docker pull bonita@sha256:7592b8fc5b55c1ec917510f3f3253c2188336bb52c8423cff1c02ece11bbfe22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14.0` - linux; amd64

```console
$ docker pull bonita@sha256:614b3bf57bd53b58c41e9ae5fa4220fed0f668d1e2242e7d3a91d680acfa12e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177055922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012b0192b99d10145e149860626e2596412995a7937a5ba6977a110556756a94`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:11 GMT
ADD file:aa1af71c6b66d2dddee4797236e3e526f70f904ab641cc0dd6b41445cfedf9b4 in / 
# Thu, 30 Nov 2023 23:23:11 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:52:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 08:52:27 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 16 Mar 2024 08:52:28 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 08:52:29 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 08:52:29 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 08:52:29 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 16 Mar 2024 08:52:29 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 16 Mar 2024 08:52:29 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 16 Mar 2024 08:52:29 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 16 Mar 2024 08:52:29 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 08:52:30 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 16 Mar 2024 08:52:30 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 08:52:30 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Sat, 16 Mar 2024 08:52:35 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 08:52:35 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 08:52:36 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 08:52:36 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 08:52:36 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 08:52:36 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 08:52:36 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 08:52:36 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 08:52:37 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 08:52:37 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 08:52:37 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 08:52:37 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d078792c4f9122259f14b539315bd92cbd9490ed73e08255a08689122b143108`  
		Last Modified: Thu, 30 Nov 2023 23:23:58 GMT  
		Size: 2.8 MB (2826431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721052ed1dc84a3fb8eb82831c08d07a18f3c62b5daf18d0b22ae77a931589e4`  
		Last Modified: Sat, 16 Mar 2024 08:53:54 GMT  
		Size: 57.5 MB (57528627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa96d1361e205b329aa07490398c93cc1347da85a1e81c0fba2eea88a1c1de1`  
		Last Modified: Sat, 16 Mar 2024 08:53:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e67e799490441f506f5ee43b439203785a2036c8dc42215fb5d81c9c90b072b`  
		Last Modified: Sat, 16 Mar 2024 08:53:44 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75748435f57b474cb01258d59791e62e667f6c06f11a2feaa3e165bd746c8af2`  
		Last Modified: Sat, 16 Mar 2024 08:53:44 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c7cd28e3fef471a2b2786204e6ff452aedc10e6c54cd68bb781e092e6694f2`  
		Last Modified: Sat, 16 Mar 2024 08:53:44 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eddbe583e25ae21539c8679178336eb1bc81376303c3956b79a9cf0bd2f9c0b`  
		Last Modified: Sat, 16 Mar 2024 08:53:50 GMT  
		Size: 116.7 MB (116690850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0367de0b569c1dc942018aac9e4f575f5e400a5905023692f3f1c06dfdd4ba`  
		Last Modified: Sat, 16 Mar 2024 08:53:44 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:4cecd3e6736b520d11f91d41d41576aca058786b82455e22a77a8cacfea1c8e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176274521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3db678590a7e1f4434d412e23bc0aca607e84596e8110a716cf423b294e405`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:15 GMT
ADD file:3982c510455cc0ceea8cf8dd0b50b69588e35fd4f84522cb4000582c73781672 in / 
# Thu, 30 Nov 2023 23:11:15 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:02:04 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 03:02:07 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Sat, 16 Mar 2024 03:02:08 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 03:02:09 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 03:02:09 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 03:02:09 GMT
ENV BONITA_VERSION=7.14.0
# Sat, 16 Mar 2024 03:02:09 GMT
ENV BRANDING_VERSION=2022.1-u0
# Sat, 16 Mar 2024 03:02:09 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Sat, 16 Mar 2024 03:02:10 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Sat, 16 Mar 2024 03:02:10 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 03:02:10 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Sat, 16 Mar 2024 03:02:10 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 03:02:10 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Sat, 16 Mar 2024 03:02:15 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 03:02:16 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 03:02:16 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 03:02:16 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 03:02:16 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 03:02:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 03:02:17 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 03:02:17 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 03:02:17 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 03:02:17 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 03:02:17 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 03:02:17 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 03:02:17 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8bc1ab4b84041d57f21a792410a00820f73fda7efe08bcd2ca6245349a40299d`  
		Last Modified: Thu, 30 Nov 2023 23:12:02 GMT  
		Size: 2.7 MB (2721527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f98ad3ac6297db92029c7b269d576cbcc363c7737d78d22f969ecd16dd28b7`  
		Last Modified: Sat, 16 Mar 2024 03:03:39 GMT  
		Size: 56.9 MB (56852201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cde48b71c6346eb41137992194341b2b73915f5a32bc08a0322e5a592687093`  
		Last Modified: Sat, 16 Mar 2024 03:03:33 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac11f8e718ce8403827c6ddb0e0037ae44a2aa68e711d8ab5e6284a7d26764d4`  
		Last Modified: Sat, 16 Mar 2024 03:03:31 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4d0afc9695afd8ee58c91a084b7f9197f659ba2cc3f8dbb82b9491e60256d2`  
		Last Modified: Sat, 16 Mar 2024 03:03:31 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4173ce5ddfd47b90b3e9b87ff89aa4bcca26eb8c61fe9e036de2e10898a2d9f`  
		Last Modified: Sat, 16 Mar 2024 03:03:31 GMT  
		Size: 3.0 KB (3030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e64d658467261890cdb35dcbe493e5998324ba0749685644dbea0a2e895f15`  
		Last Modified: Sat, 16 Mar 2024 03:03:36 GMT  
		Size: 116.7 MB (116690781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0671ecd06e564fc3480ededc35cc8cd240bcae4a96c27ea90a474618fc966c`  
		Last Modified: Sat, 16 Mar 2024 03:03:31 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:87dc261c266072e581c32e8905d47cb352b7e08eaaf70fb3cfd0e01a86fef793
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172870070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5163e25c3dd6ff50e76306219377706a2f1684270e443924fd3a15ecc2f30d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:36 GMT
ADD file:35af09f43b08c93abd4c6b8679d43e8ac40893bf5932c4c21f1bb037f53bb62c in / 
# Thu, 30 Nov 2023 23:19:41 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:57:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 15 Mar 2024 23:57:23 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 15 Mar 2024 23:57:26 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 15 Mar 2024 23:57:27 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 15 Mar 2024 23:57:27 GMT
ARG BONITA_VERSION
# Fri, 15 Mar 2024 23:57:27 GMT
ARG BRANDING_VERSION
# Fri, 15 Mar 2024 23:57:28 GMT
ARG BONITA_SHA256
# Fri, 15 Mar 2024 23:57:28 GMT
ARG BASE_URL
# Fri, 15 Mar 2024 23:57:28 GMT
ARG BONITA_URL
# Fri, 15 Mar 2024 23:57:29 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 15 Mar 2024 23:57:29 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 15 Mar 2024 23:57:29 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 15 Mar 2024 23:57:30 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 15 Mar 2024 23:57:30 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 15 Mar 2024 23:57:31 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 15 Mar 2024 23:57:32 GMT
RUN mkdir /opt/files
# Fri, 15 Mar 2024 23:57:32 GMT
COPY dir:af2a57bc8d94b007ba0d0e7c139dfd9475d3c95e710ec521c0e4e68f19bce2ec in /opt/files 
# Fri, 15 Mar 2024 23:57:40 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 15 Mar 2024 23:57:42 GMT
ENV HTTP_API=false
# Fri, 15 Mar 2024 23:57:43 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 15 Mar 2024 23:57:43 GMT
ENV HTTP_API_PASSWORD=
# Fri, 15 Mar 2024 23:57:43 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 15 Mar 2024 23:57:43 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 15 Mar 2024 23:57:44 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 15 Mar 2024 23:57:44 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 15 Mar 2024 23:57:44 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 15 Mar 2024 23:57:45 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 15 Mar 2024 23:57:45 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 15 Mar 2024 23:57:46 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 15 Mar 2024 23:57:46 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 15 Mar 2024 23:57:47 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 15 Mar 2024 23:57:47 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 15 Mar 2024 23:57:47 GMT
EXPOSE 8080 9000
# Fri, 15 Mar 2024 23:57:48 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 15 Mar 2024 23:57:48 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:080a2fea3a772fa995cb0b07b4601e7cd57650fa4e8a50866da1de707946d7b3`  
		Last Modified: Thu, 30 Nov 2023 23:20:38 GMT  
		Size: 2.8 MB (2812474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0807b0c3db086f5586354387f13a35749209a7d8b79a5a54e69047df67d323ff`  
		Last Modified: Sat, 16 Mar 2024 00:00:35 GMT  
		Size: 53.4 MB (53356789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca87424184ccc9c707469061b00ce94627f03ef132bb62ba12f8eff075811407`  
		Last Modified: Sat, 16 Mar 2024 00:00:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e15e24b2e80b7692602f77d77fa8ed78831b65b2ea9b8435765ff0d347ff5d`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3f4cc5a4c9c00d82a333ab05169ddc07c5b55f0529af3df9c74a7d24ffc3df`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b8e7fc95d8ea3f1189422a42c5b3b6e5dd05e788f9c36d8b66850569bf3e1`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 3.0 KB (3029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb69de64d5944775cd968c77fee4b2c96ddb9a64b839bd97455b1e8ce60b30d`  
		Last Modified: Sat, 16 Mar 2024 00:00:32 GMT  
		Size: 116.7 MB (116690794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe2e0773c680d40f4cb25bf8670f4a162f89d77a8e1382b4931703314c8beba`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.15`

```console
$ docker pull bonita@sha256:c2aed227c2879e90df69d37d7c7c7c3545af0b4386dbe27dd53439f747b4078d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.15` - linux; amd64

```console
$ docker pull bonita@sha256:a17d1ac91d78de7fe1eb5e900081c69e463dfaf1829cdb46ef9a1db44b2d6b80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183641885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6346a23ed3b2e4cdeec2654dc4e2be44273d1315ab385d325400c9b168798`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:52:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 08:52:45 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 16 Mar 2024 08:52:46 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 08:52:46 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 08:52:46 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 08:52:46 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 08:52:47 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 08:52:47 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 08:52:47 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 16 Mar 2024 08:52:47 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 16 Mar 2024 08:52:48 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 08:52:48 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 16 Mar 2024 08:52:53 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 08:52:53 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 08:52:53 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 08:52:53 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 08:52:53 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 08:52:54 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 08:52:54 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 08:52:54 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 08:52:54 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 08:52:54 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 08:52:54 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 08:52:54 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e2f30e0170fac06169f99093bfbbb7098e51c23decc518d1307594706f192d`  
		Last Modified: Sat, 16 Mar 2024 08:54:15 GMT  
		Size: 61.6 MB (61631016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fff655c8bc27318c185cf92814c29ea430168868c145c8d0c6c1fa896df558`  
		Last Modified: Sat, 16 Mar 2024 08:54:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c356553c484e84042fc82d0cc263dc3ccfd1b276bdec0c7bde8c9765737c10fd`  
		Last Modified: Sat, 16 Mar 2024 08:54:06 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8568a02a8b77cc1f23a9fedcf057c4b91c164fb03fa7a542bb01ddf0bdae06a`  
		Last Modified: Sat, 16 Mar 2024 08:54:06 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd3251fd5d4a5784c106c5ea9757b340c62762dabb3515ab3f87facc90b2e30`  
		Last Modified: Sat, 16 Mar 2024 08:54:06 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76bebd3b33b4c6592235394d093a66bf3031b35751983d6ec7ae0776dea936d`  
		Last Modified: Sat, 16 Mar 2024 08:54:11 GMT  
		Size: 119.2 MB (119192992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411ee5cf4fe043fdc36e8395e3a216204223d88c5629b7a5c732d28c4b1bc10a`  
		Last Modified: Sat, 16 Mar 2024 08:54:06 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:fbe9b805168ac54c9f9ca1bc974565b675cdcfdc89620c9a8e352934efac5108
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182782808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c1a014787ec3cc6b50a005939c7656540927a604687c1103254c2fe5eae4ad`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:02:21 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 03:02:26 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 16 Mar 2024 03:02:27 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 03:02:27 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 16 Mar 2024 03:02:28 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 16 Mar 2024 03:02:29 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 03:02:29 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 16 Mar 2024 03:02:34 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 03:02:35 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 03:02:35 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 03:02:35 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 03:02:35 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 03:02:35 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 03:02:35 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 03:02:36 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 03:02:36 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 03:02:36 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 03:02:36 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 03:02:36 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af8d8d6c53d7f614d66dbc83a68d4b91901dde18ec29fa4ac900148d9b56f13`  
		Last Modified: Sat, 16 Mar 2024 03:03:59 GMT  
		Size: 60.9 MB (60871527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2d2a008ac68258778d36996998a3c7aeef042e7621559ab04149773b47e12d`  
		Last Modified: Sat, 16 Mar 2024 03:03:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2a5777c86f1116d8f2d5037c763e9cc58f7be1834f9c993d4c9195b638e8f7`  
		Last Modified: Sat, 16 Mar 2024 03:03:51 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ac21a59a3da2f311c58e13e6984f0140a7d6e0ce3add666fd85e79b201269f`  
		Last Modified: Sat, 16 Mar 2024 03:03:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf9e382c19c6da30628695f95110bf20da93c501688f109f8a189ab87e79f61`  
		Last Modified: Sat, 16 Mar 2024 03:03:51 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29682f18d29221fee50a7e663b36ba1504c7d4424d71ac72e478cd549eac18e9`  
		Last Modified: Sat, 16 Mar 2024 03:03:56 GMT  
		Size: 119.2 MB (119192969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3943571ef8d271e5d9bf54a1f4575e3db9162fd74a09e65c2df5c8633c03b8`  
		Last Modified: Sat, 16 Mar 2024 03:03:51 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15` - linux; ppc64le

```console
$ docker pull bonita@sha256:0ce8ac817ee24e36974e87d8ea2bd020a595054cebb21d1a1c5ca15fec8ee3fe
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179807397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15048d1b99506c3b756e6e899f55667902aa3d70cd7a88a95aae0d0cbf57364a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:55 GMT
ADD file:cf4fecc20d85962cd46b6911d8ee82b9a3de2fa530bc58e998c2d544a888fdb9 in / 
# Sat, 27 Jan 2024 00:27:55 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:57:55 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 15 Mar 2024 23:58:06 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 15 Mar 2024 23:58:08 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 15 Mar 2024 23:58:09 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 15 Mar 2024 23:58:10 GMT
ARG BONITA_VERSION
# Fri, 15 Mar 2024 23:58:10 GMT
ARG BRANDING_VERSION
# Fri, 15 Mar 2024 23:58:11 GMT
ARG BONITA_SHA256
# Fri, 15 Mar 2024 23:58:11 GMT
ARG BASE_URL
# Fri, 15 Mar 2024 23:58:11 GMT
ARG BONITA_URL
# Fri, 15 Mar 2024 23:58:12 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 15 Mar 2024 23:58:12 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 15 Mar 2024 23:58:12 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 15 Mar 2024 23:58:13 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 15 Mar 2024 23:58:13 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 15 Mar 2024 23:58:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 15 Mar 2024 23:58:15 GMT
RUN mkdir /opt/files
# Fri, 15 Mar 2024 23:58:15 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 15 Mar 2024 23:58:24 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 15 Mar 2024 23:58:26 GMT
ENV HTTP_API=false
# Fri, 15 Mar 2024 23:58:26 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 15 Mar 2024 23:58:26 GMT
ENV HTTP_API_PASSWORD=
# Fri, 15 Mar 2024 23:58:27 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 15 Mar 2024 23:58:27 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 15 Mar 2024 23:58:27 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 15 Mar 2024 23:58:28 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 15 Mar 2024 23:58:28 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 15 Mar 2024 23:58:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 15 Mar 2024 23:58:29 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 15 Mar 2024 23:58:29 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 15 Mar 2024 23:58:30 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 15 Mar 2024 23:58:30 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 15 Mar 2024 23:58:30 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 15 Mar 2024 23:58:31 GMT
EXPOSE 8080 9000
# Fri, 15 Mar 2024 23:58:31 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 15 Mar 2024 23:58:31 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:04646341bdb047ee1a3dd65db76069b9117954385033f5a340622fd170fa4b73`  
		Last Modified: Sat, 27 Jan 2024 00:28:46 GMT  
		Size: 2.8 MB (2802980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c717590678abc6ba9f9b13ab93fd588ecf21bb546a88b89dd176f6301741c39f`  
		Last Modified: Sat, 16 Mar 2024 00:01:01 GMT  
		Size: 57.8 MB (57801404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a2af53c6ef53ec2919045eb31d183a4710a9697ee0a746f37c8cd8af032aa0`  
		Last Modified: Sat, 16 Mar 2024 00:00:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895228bf1c4c4fee002217f84c9aaf231f5c8d78966f57a2daab7d5d52d27180`  
		Last Modified: Sat, 16 Mar 2024 00:00:50 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea02e5282f5da095f8f9364d3db0df27a6df659161f7c39ad3b7fc6157f3896`  
		Last Modified: Sat, 16 Mar 2024 00:00:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274d2d383bc2f52e30690967ff49ce1b7ebb892d4a2566b9d50aad81baa78a34`  
		Last Modified: Sat, 16 Mar 2024 00:00:51 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af18bd400a6bcf4a409035d4013e7c5540badd73c7db72327a1eb1b68165b025`  
		Last Modified: Sat, 16 Mar 2024 00:00:58 GMT  
		Size: 119.2 MB (119192981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885e47b12d875fdd38cdc8c7f63608651009d61fa57e034e1fe45385ab6de95b`  
		Last Modified: Sat, 16 Mar 2024 00:00:51 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.15.0`

```console
$ docker pull bonita@sha256:c2aed227c2879e90df69d37d7c7c7c3545af0b4386dbe27dd53439f747b4078d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.15.0` - linux; amd64

```console
$ docker pull bonita@sha256:a17d1ac91d78de7fe1eb5e900081c69e463dfaf1829cdb46ef9a1db44b2d6b80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183641885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6346a23ed3b2e4cdeec2654dc4e2be44273d1315ab385d325400c9b168798`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:52:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 08:52:45 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 16 Mar 2024 08:52:46 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 08:52:46 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 08:52:46 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 08:52:46 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 08:52:47 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 08:52:47 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 08:52:47 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 16 Mar 2024 08:52:47 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 08:52:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 16 Mar 2024 08:52:48 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 08:52:48 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 16 Mar 2024 08:52:53 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 08:52:53 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 08:52:53 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 08:52:53 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 08:52:53 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 08:52:54 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 08:52:54 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 08:52:54 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 08:52:54 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 08:52:54 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 08:52:54 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 08:52:54 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 08:52:54 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e2f30e0170fac06169f99093bfbbb7098e51c23decc518d1307594706f192d`  
		Last Modified: Sat, 16 Mar 2024 08:54:15 GMT  
		Size: 61.6 MB (61631016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fff655c8bc27318c185cf92814c29ea430168868c145c8d0c6c1fa896df558`  
		Last Modified: Sat, 16 Mar 2024 08:54:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c356553c484e84042fc82d0cc263dc3ccfd1b276bdec0c7bde8c9765737c10fd`  
		Last Modified: Sat, 16 Mar 2024 08:54:06 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8568a02a8b77cc1f23a9fedcf057c4b91c164fb03fa7a542bb01ddf0bdae06a`  
		Last Modified: Sat, 16 Mar 2024 08:54:06 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd3251fd5d4a5784c106c5ea9757b340c62762dabb3515ab3f87facc90b2e30`  
		Last Modified: Sat, 16 Mar 2024 08:54:06 GMT  
		Size: 3.0 KB (3049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76bebd3b33b4c6592235394d093a66bf3031b35751983d6ec7ae0776dea936d`  
		Last Modified: Sat, 16 Mar 2024 08:54:11 GMT  
		Size: 119.2 MB (119192992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411ee5cf4fe043fdc36e8395e3a216204223d88c5629b7a5c732d28c4b1bc10a`  
		Last Modified: Sat, 16 Mar 2024 08:54:06 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:fbe9b805168ac54c9f9ca1bc974565b675cdcfdc89620c9a8e352934efac5108
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182782808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c1a014787ec3cc6b50a005939c7656540927a604687c1103254c2fe5eae4ad`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:02:21 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 03:02:26 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 16 Mar 2024 03:02:27 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 03:02:27 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 03:02:28 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BONITA_VERSION=7.15.0
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BRANDING_VERSION=2022.2-u0
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Sat, 16 Mar 2024 03:02:28 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 03:02:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Sat, 16 Mar 2024 03:02:29 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 03:02:29 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Sat, 16 Mar 2024 03:02:34 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 03:02:35 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 03:02:35 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 03:02:35 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 03:02:35 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 03:02:35 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 03:02:35 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 03:02:36 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 03:02:36 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 03:02:36 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 03:02:36 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 03:02:36 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 03:02:36 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af8d8d6c53d7f614d66dbc83a68d4b91901dde18ec29fa4ac900148d9b56f13`  
		Last Modified: Sat, 16 Mar 2024 03:03:59 GMT  
		Size: 60.9 MB (60871527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2d2a008ac68258778d36996998a3c7aeef042e7621559ab04149773b47e12d`  
		Last Modified: Sat, 16 Mar 2024 03:03:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2a5777c86f1116d8f2d5037c763e9cc58f7be1834f9c993d4c9195b638e8f7`  
		Last Modified: Sat, 16 Mar 2024 03:03:51 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ac21a59a3da2f311c58e13e6984f0140a7d6e0ce3add666fd85e79b201269f`  
		Last Modified: Sat, 16 Mar 2024 03:03:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf9e382c19c6da30628695f95110bf20da93c501688f109f8a189ab87e79f61`  
		Last Modified: Sat, 16 Mar 2024 03:03:51 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29682f18d29221fee50a7e663b36ba1504c7d4424d71ac72e478cd549eac18e9`  
		Last Modified: Sat, 16 Mar 2024 03:03:56 GMT  
		Size: 119.2 MB (119192969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3943571ef8d271e5d9bf54a1f4575e3db9162fd74a09e65c2df5c8633c03b8`  
		Last Modified: Sat, 16 Mar 2024 03:03:51 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.15.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:0ce8ac817ee24e36974e87d8ea2bd020a595054cebb21d1a1c5ca15fec8ee3fe
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179807397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15048d1b99506c3b756e6e899f55667902aa3d70cd7a88a95aae0d0cbf57364a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:55 GMT
ADD file:cf4fecc20d85962cd46b6911d8ee82b9a3de2fa530bc58e998c2d544a888fdb9 in / 
# Sat, 27 Jan 2024 00:27:55 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:57:55 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 15 Mar 2024 23:58:06 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 15 Mar 2024 23:58:08 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 15 Mar 2024 23:58:09 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 15 Mar 2024 23:58:10 GMT
ARG BONITA_VERSION
# Fri, 15 Mar 2024 23:58:10 GMT
ARG BRANDING_VERSION
# Fri, 15 Mar 2024 23:58:11 GMT
ARG BONITA_SHA256
# Fri, 15 Mar 2024 23:58:11 GMT
ARG BASE_URL
# Fri, 15 Mar 2024 23:58:11 GMT
ARG BONITA_URL
# Fri, 15 Mar 2024 23:58:12 GMT
ENV BONITA_VERSION=7.15.0
# Fri, 15 Mar 2024 23:58:12 GMT
ENV BRANDING_VERSION=2022.2-u0
# Fri, 15 Mar 2024 23:58:12 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Fri, 15 Mar 2024 23:58:13 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Fri, 15 Mar 2024 23:58:13 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 15 Mar 2024 23:58:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Fri, 15 Mar 2024 23:58:15 GMT
RUN mkdir /opt/files
# Fri, 15 Mar 2024 23:58:15 GMT
COPY dir:2f998cb77cda0ed47e4d103dacbc15e680f0e173a75b624320e21173de664a22 in /opt/files 
# Fri, 15 Mar 2024 23:58:24 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 15 Mar 2024 23:58:26 GMT
ENV HTTP_API=false
# Fri, 15 Mar 2024 23:58:26 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 15 Mar 2024 23:58:26 GMT
ENV HTTP_API_PASSWORD=
# Fri, 15 Mar 2024 23:58:27 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 15 Mar 2024 23:58:27 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 15 Mar 2024 23:58:27 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 15 Mar 2024 23:58:28 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 15 Mar 2024 23:58:28 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 15 Mar 2024 23:58:28 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 15 Mar 2024 23:58:29 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 15 Mar 2024 23:58:29 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 15 Mar 2024 23:58:30 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 15 Mar 2024 23:58:30 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 15 Mar 2024 23:58:30 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 15 Mar 2024 23:58:31 GMT
EXPOSE 8080 9000
# Fri, 15 Mar 2024 23:58:31 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 15 Mar 2024 23:58:31 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:04646341bdb047ee1a3dd65db76069b9117954385033f5a340622fd170fa4b73`  
		Last Modified: Sat, 27 Jan 2024 00:28:46 GMT  
		Size: 2.8 MB (2802980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c717590678abc6ba9f9b13ab93fd588ecf21bb546a88b89dd176f6301741c39f`  
		Last Modified: Sat, 16 Mar 2024 00:01:01 GMT  
		Size: 57.8 MB (57801404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a2af53c6ef53ec2919045eb31d183a4710a9697ee0a746f37c8cd8af032aa0`  
		Last Modified: Sat, 16 Mar 2024 00:00:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895228bf1c4c4fee002217f84c9aaf231f5c8d78966f57a2daab7d5d52d27180`  
		Last Modified: Sat, 16 Mar 2024 00:00:50 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea02e5282f5da095f8f9364d3db0df27a6df659161f7c39ad3b7fc6157f3896`  
		Last Modified: Sat, 16 Mar 2024 00:00:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274d2d383bc2f52e30690967ff49ce1b7ebb892d4a2566b9d50aad81baa78a34`  
		Last Modified: Sat, 16 Mar 2024 00:00:51 GMT  
		Size: 3.0 KB (3045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af18bd400a6bcf4a409035d4013e7c5540badd73c7db72327a1eb1b68165b025`  
		Last Modified: Sat, 16 Mar 2024 00:00:58 GMT  
		Size: 119.2 MB (119192981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885e47b12d875fdd38cdc8c7f63608651009d61fa57e034e1fe45385ab6de95b`  
		Last Modified: Sat, 16 Mar 2024 00:00:51 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:8.0`

```console
$ docker pull bonita@sha256:49fb74fc3b71f89f6d6e9797d164b1600abad1849a6028dd80bfd128061892f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:8.0` - linux; amd64

```console
$ docker pull bonita@sha256:c61e23c8804a29ca77e17220830059906ac2387c9c7a5a77fc237228705f7f2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183368861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d5a400c747eea94ef876f915427cee5dde2ff2518192d9b256a9284362111d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:52:58 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 08:53:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 16 Mar 2024 08:53:03 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 08:53:04 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 08:53:04 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 16 Mar 2024 08:53:04 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 16 Mar 2024 08:53:04 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 16 Mar 2024 08:53:05 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 16 Mar 2024 08:53:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 08:53:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 16 Mar 2024 08:53:05 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 08:53:05 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 16 Mar 2024 08:53:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 08:53:12 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 08:53:12 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 08:53:12 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 08:53:12 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 08:53:12 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 08:53:13 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 08:53:13 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 16 Mar 2024 08:53:13 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 08:53:13 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 16 Mar 2024 08:53:13 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 08:53:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 08:53:13 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd69f83dfb1af6156ab4a603d6adb5038a3de61d8f309815d8f71ff432d24d47`  
		Last Modified: Sat, 16 Mar 2024 08:54:37 GMT  
		Size: 61.8 MB (61798280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94aba78b855360f5e07023859c27c6506e8f329fa477a5127000ccae33f30201`  
		Last Modified: Sat, 16 Mar 2024 08:54:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b7103bb98a588a5b65a049c39d0bc58f591e89698cba680cd14f0ddfce1611`  
		Last Modified: Sat, 16 Mar 2024 08:54:27 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12969946da581ab79c1bd1f6fdc1c1b2c18a2ca3f1b92085c561cd6800ea1951`  
		Last Modified: Sat, 16 Mar 2024 08:54:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643dcbdefb131f742ad8a91eb18884649b7b3479c712bdea6b771a624e23d331`  
		Last Modified: Sat, 16 Mar 2024 08:54:27 GMT  
		Size: 3.5 KB (3479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca1495dd0222fa0452024c10ebb8999a7d67b681227ffba852ca7a38965b9b8`  
		Last Modified: Sat, 16 Mar 2024 08:54:33 GMT  
		Size: 118.2 MB (118180716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc08a431531cb196aae81bc59a46fe2aee90e8f57907cca39634d377a878233`  
		Last Modified: Sat, 16 Mar 2024 08:54:27 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:8.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2cf7a9e0dfec7e412366db745749a1882de313229dace54a1c0fa4d0238b207d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182518350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfe723e8e69c3692f902091e19028d21a854c8a561d8d56531186bd06e0742a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:02:40 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 03:02:46 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 16 Mar 2024 03:02:47 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 03:02:47 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 16 Mar 2024 03:02:48 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 16 Mar 2024 03:02:49 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 03:02:49 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 16 Mar 2024 03:02:55 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 03:02:56 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 03:02:56 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 03:02:56 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 03:02:56 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 03:02:56 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 03:02:56 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 03:02:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 16 Mar 2024 03:02:57 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 03:02:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 16 Mar 2024 03:02:57 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 03:02:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 03:02:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce75a0fccdb3c045fa082c0ced7f4fd9c2006c2330268952b760f12a2a35cc2`  
		Last Modified: Sat, 16 Mar 2024 03:04:19 GMT  
		Size: 61.1 MB (61068930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea23591cbb412dc67ab0bfad05949f7130f8cd6a1cefc6d37cebcd7f7b1c5b2`  
		Last Modified: Sat, 16 Mar 2024 03:04:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1a894c4d4faa07382633d71c68dd996729142c643773e2cf44864ffa432b8d`  
		Last Modified: Sat, 16 Mar 2024 03:04:11 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ee70d741bab4e322b44159fb2b328b8d0f46492e3dc6b002fe2e8e53c3d2a0`  
		Last Modified: Sat, 16 Mar 2024 03:04:10 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1256dfedfd6fbd6a595d7103aceab7d6962b0f7953070414a38572d90da7f6f6`  
		Last Modified: Sat, 16 Mar 2024 03:04:10 GMT  
		Size: 3.5 KB (3479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7afcf6e44eda62588204c309d1cbd6b29e94087bbe91daf29c0502245aa694`  
		Last Modified: Sat, 16 Mar 2024 03:04:15 GMT  
		Size: 118.2 MB (118180678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0103e0c0bb36f49efc6825fbe1d901ae5058087885ac6b11b842e16937e13e48`  
		Last Modified: Sat, 16 Mar 2024 03:04:11 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:8.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:af52de366938b25246c9b0cc840e8a08be35aa910856b42233081be537af1616
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179570657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b923c1405d914085ffe4f287be19baba2d93dcf48f442633c6c95d6c2f960f67`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:48 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
# Sat, 27 Jan 2024 00:27:49 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:58:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 15 Mar 2024 23:58:48 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 15 Mar 2024 23:58:51 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 15 Mar 2024 23:58:52 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 15 Mar 2024 23:58:52 GMT
ARG BONITA_VERSION
# Fri, 15 Mar 2024 23:58:53 GMT
ARG BRANDING_VERSION
# Fri, 15 Mar 2024 23:58:53 GMT
ARG BONITA_SHA256
# Fri, 15 Mar 2024 23:58:54 GMT
ARG BASE_URL
# Fri, 15 Mar 2024 23:58:54 GMT
ARG BONITA_URL
# Fri, 15 Mar 2024 23:58:54 GMT
ENV BONITA_VERSION=8.0.0
# Fri, 15 Mar 2024 23:58:55 GMT
ENV BRANDING_VERSION=2023.1-u0
# Fri, 15 Mar 2024 23:58:55 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Fri, 15 Mar 2024 23:58:56 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Fri, 15 Mar 2024 23:58:56 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 15 Mar 2024 23:58:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Fri, 15 Mar 2024 23:58:57 GMT
RUN mkdir /opt/files
# Fri, 15 Mar 2024 23:58:58 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Fri, 15 Mar 2024 23:59:07 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 15 Mar 2024 23:59:09 GMT
ENV HTTP_API=false
# Fri, 15 Mar 2024 23:59:09 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 15 Mar 2024 23:59:10 GMT
ENV HTTP_API_PASSWORD=
# Fri, 15 Mar 2024 23:59:10 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 15 Mar 2024 23:59:11 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 15 Mar 2024 23:59:11 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 15 Mar 2024 23:59:12 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 15 Mar 2024 23:59:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 15 Mar 2024 23:59:12 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 15 Mar 2024 23:59:13 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 15 Mar 2024 23:59:13 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 15 Mar 2024 23:59:14 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 15 Mar 2024 23:59:14 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 15 Mar 2024 23:59:15 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Fri, 15 Mar 2024 23:59:15 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 15 Mar 2024 23:59:15 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 15 Mar 2024 23:59:16 GMT
EXPOSE 8080 9000
# Fri, 15 Mar 2024 23:59:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 15 Mar 2024 23:59:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c0212967952fa7ddbc3dc401470abd092772f3da917bc2a5d92a4c19c5a235`  
		Last Modified: Sat, 16 Mar 2024 00:01:26 GMT  
		Size: 58.0 MB (57987381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecc94bb125d0bef7ff258cf75e8d9d7a6bce29b6cb1476b47ea61fcd5bf0f4a`  
		Last Modified: Sat, 16 Mar 2024 00:01:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c820ce1cbbd3221d267e7cc71ea8fc0da9c200f9172b9ea22c01549cfcb4051`  
		Last Modified: Sat, 16 Mar 2024 00:01:15 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a842fcb3410a5903a75519182004bd622d3f882e199f4187385cca90c855fcb`  
		Last Modified: Sat, 16 Mar 2024 00:01:16 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb00e368f8e725ba5330f672f1b6c237b8665cebc5d62b0cb31dd200446d641`  
		Last Modified: Sat, 16 Mar 2024 00:01:16 GMT  
		Size: 3.5 KB (3479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46652bb2301a0a5c735983f07b53553e8d9e4274acf1471c2dcfc8a6f3c38f20`  
		Last Modified: Sat, 16 Mar 2024 00:01:23 GMT  
		Size: 118.2 MB (118180704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a98a94d1a08a90ac94fa17e97526feca756d6b4e8e65d5164153382538246f`  
		Last Modified: Sat, 16 Mar 2024 00:01:15 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:8.0.0`

```console
$ docker pull bonita@sha256:49fb74fc3b71f89f6d6e9797d164b1600abad1849a6028dd80bfd128061892f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:8.0.0` - linux; amd64

```console
$ docker pull bonita@sha256:c61e23c8804a29ca77e17220830059906ac2387c9c7a5a77fc237228705f7f2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183368861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d5a400c747eea94ef876f915427cee5dde2ff2518192d9b256a9284362111d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:52:58 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 08:53:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 16 Mar 2024 08:53:03 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 08:53:04 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 08:53:04 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 08:53:04 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 16 Mar 2024 08:53:04 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 16 Mar 2024 08:53:04 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 16 Mar 2024 08:53:05 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 16 Mar 2024 08:53:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 08:53:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 16 Mar 2024 08:53:05 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 08:53:05 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 16 Mar 2024 08:53:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 08:53:12 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 08:53:12 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 08:53:12 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 08:53:12 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 08:53:12 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 08:53:12 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 08:53:13 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 08:53:13 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 16 Mar 2024 08:53:13 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 08:53:13 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 16 Mar 2024 08:53:13 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 08:53:13 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 08:53:13 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd69f83dfb1af6156ab4a603d6adb5038a3de61d8f309815d8f71ff432d24d47`  
		Last Modified: Sat, 16 Mar 2024 08:54:37 GMT  
		Size: 61.8 MB (61798280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94aba78b855360f5e07023859c27c6506e8f329fa477a5127000ccae33f30201`  
		Last Modified: Sat, 16 Mar 2024 08:54:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b7103bb98a588a5b65a049c39d0bc58f591e89698cba680cd14f0ddfce1611`  
		Last Modified: Sat, 16 Mar 2024 08:54:27 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12969946da581ab79c1bd1f6fdc1c1b2c18a2ca3f1b92085c561cd6800ea1951`  
		Last Modified: Sat, 16 Mar 2024 08:54:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643dcbdefb131f742ad8a91eb18884649b7b3479c712bdea6b771a624e23d331`  
		Last Modified: Sat, 16 Mar 2024 08:54:27 GMT  
		Size: 3.5 KB (3479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca1495dd0222fa0452024c10ebb8999a7d67b681227ffba852ca7a38965b9b8`  
		Last Modified: Sat, 16 Mar 2024 08:54:33 GMT  
		Size: 118.2 MB (118180716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc08a431531cb196aae81bc59a46fe2aee90e8f57907cca39634d377a878233`  
		Last Modified: Sat, 16 Mar 2024 08:54:27 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:8.0.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2cf7a9e0dfec7e412366db745749a1882de313229dace54a1c0fa4d0238b207d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182518350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfe723e8e69c3692f902091e19028d21a854c8a561d8d56531186bd06e0742a`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Fri, 26 Jan 2024 23:45:00 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:02:40 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 16 Mar 2024 03:02:46 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Sat, 16 Mar 2024 03:02:47 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 16 Mar 2024 03:02:47 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BONITA_VERSION
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BRANDING_VERSION
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BONITA_SHA256
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BASE_URL
# Sat, 16 Mar 2024 03:02:48 GMT
ARG BONITA_URL
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BONITA_VERSION=8.0.0
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BRANDING_VERSION=2023.1-u0
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Sat, 16 Mar 2024 03:02:48 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 16 Mar 2024 03:02:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Sat, 16 Mar 2024 03:02:49 GMT
RUN mkdir /opt/files
# Sat, 16 Mar 2024 03:02:49 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Sat, 16 Mar 2024 03:02:55 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Sat, 16 Mar 2024 03:02:56 GMT
ENV HTTP_API=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 16 Mar 2024 03:02:56 GMT
ENV HTTP_API_PASSWORD=
# Sat, 16 Mar 2024 03:02:56 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 16 Mar 2024 03:02:56 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 16 Mar 2024 03:02:56 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 16 Mar 2024 03:02:56 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 16 Mar 2024 03:02:56 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 16 Mar 2024 03:02:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Sat, 16 Mar 2024 03:02:57 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Sat, 16 Mar 2024 03:02:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Sat, 16 Mar 2024 03:02:57 GMT
EXPOSE 8080 9000
# Sat, 16 Mar 2024 03:02:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Sat, 16 Mar 2024 03:02:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce75a0fccdb3c045fa082c0ced7f4fd9c2006c2330268952b760f12a2a35cc2`  
		Last Modified: Sat, 16 Mar 2024 03:04:19 GMT  
		Size: 61.1 MB (61068930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea23591cbb412dc67ab0bfad05949f7130f8cd6a1cefc6d37cebcd7f7b1c5b2`  
		Last Modified: Sat, 16 Mar 2024 03:04:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1a894c4d4faa07382633d71c68dd996729142c643773e2cf44864ffa432b8d`  
		Last Modified: Sat, 16 Mar 2024 03:04:11 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ee70d741bab4e322b44159fb2b328b8d0f46492e3dc6b002fe2e8e53c3d2a0`  
		Last Modified: Sat, 16 Mar 2024 03:04:10 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1256dfedfd6fbd6a595d7103aceab7d6962b0f7953070414a38572d90da7f6f6`  
		Last Modified: Sat, 16 Mar 2024 03:04:10 GMT  
		Size: 3.5 KB (3479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7afcf6e44eda62588204c309d1cbd6b29e94087bbe91daf29c0502245aa694`  
		Last Modified: Sat, 16 Mar 2024 03:04:15 GMT  
		Size: 118.2 MB (118180678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0103e0c0bb36f49efc6825fbe1d901ae5058087885ac6b11b842e16937e13e48`  
		Last Modified: Sat, 16 Mar 2024 03:04:11 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:8.0.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:af52de366938b25246c9b0cc840e8a08be35aa910856b42233081be537af1616
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179570657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b923c1405d914085ffe4f287be19baba2d93dcf48f442633c6c95d6c2f960f67`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:48 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
# Sat, 27 Jan 2024 00:27:49 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:58:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 15 Mar 2024 23:58:48 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre
# Fri, 15 Mar 2024 23:58:51 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 15 Mar 2024 23:58:52 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 15 Mar 2024 23:58:52 GMT
ARG BONITA_VERSION
# Fri, 15 Mar 2024 23:58:53 GMT
ARG BRANDING_VERSION
# Fri, 15 Mar 2024 23:58:53 GMT
ARG BONITA_SHA256
# Fri, 15 Mar 2024 23:58:54 GMT
ARG BASE_URL
# Fri, 15 Mar 2024 23:58:54 GMT
ARG BONITA_URL
# Fri, 15 Mar 2024 23:58:54 GMT
ENV BONITA_VERSION=8.0.0
# Fri, 15 Mar 2024 23:58:55 GMT
ENV BRANDING_VERSION=2023.1-u0
# Fri, 15 Mar 2024 23:58:55 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Fri, 15 Mar 2024 23:58:56 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Fri, 15 Mar 2024 23:58:56 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 15 Mar 2024 23:58:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Fri, 15 Mar 2024 23:58:57 GMT
RUN mkdir /opt/files
# Fri, 15 Mar 2024 23:58:58 GMT
COPY dir:4b7f2c51bcfd013e8daf18303cb247376a4033f376ea3bc007d00923c59e1fda in /opt/files 
# Fri, 15 Mar 2024 23:59:07 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 15 Mar 2024 23:59:09 GMT
ENV HTTP_API=false
# Fri, 15 Mar 2024 23:59:09 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 15 Mar 2024 23:59:10 GMT
ENV HTTP_API_PASSWORD=
# Fri, 15 Mar 2024 23:59:10 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 15 Mar 2024 23:59:11 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 15 Mar 2024 23:59:11 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 15 Mar 2024 23:59:12 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 15 Mar 2024 23:59:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 15 Mar 2024 23:59:12 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 15 Mar 2024 23:59:13 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 15 Mar 2024 23:59:13 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 15 Mar 2024 23:59:14 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 15 Mar 2024 23:59:14 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 15 Mar 2024 23:59:15 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Fri, 15 Mar 2024 23:59:15 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 15 Mar 2024 23:59:15 GMT
VOLUME [/opt/bonita/conf/logs]
# Fri, 15 Mar 2024 23:59:16 GMT
EXPOSE 8080 9000
# Fri, 15 Mar 2024 23:59:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 15 Mar 2024 23:59:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c0212967952fa7ddbc3dc401470abd092772f3da917bc2a5d92a4c19c5a235`  
		Last Modified: Sat, 16 Mar 2024 00:01:26 GMT  
		Size: 58.0 MB (57987381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecc94bb125d0bef7ff258cf75e8d9d7a6bce29b6cb1476b47ea61fcd5bf0f4a`  
		Last Modified: Sat, 16 Mar 2024 00:01:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c820ce1cbbd3221d267e7cc71ea8fc0da9c200f9172b9ea22c01549cfcb4051`  
		Last Modified: Sat, 16 Mar 2024 00:01:15 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a842fcb3410a5903a75519182004bd622d3f882e199f4187385cca90c855fcb`  
		Last Modified: Sat, 16 Mar 2024 00:01:16 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb00e368f8e725ba5330f672f1b6c237b8665cebc5d62b0cb31dd200446d641`  
		Last Modified: Sat, 16 Mar 2024 00:01:16 GMT  
		Size: 3.5 KB (3479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46652bb2301a0a5c735983f07b53553e8d9e4274acf1471c2dcfc8a6f3c38f20`  
		Last Modified: Sat, 16 Mar 2024 00:01:23 GMT  
		Size: 118.2 MB (118180704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a98a94d1a08a90ac94fa17e97526feca756d6b4e8e65d5164153382538246f`  
		Last Modified: Sat, 16 Mar 2024 00:01:15 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:9.0`

```console
$ docker pull bonita@sha256:48fe1a388de4f57a67014c8ee26f65ca3a26b95c3c39a23069bc97dbae778d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:9.0` - linux; amd64

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

### `bonita:9.0` - linux; arm64 variant v8

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

### `bonita:9.0` - linux; ppc64le

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

## `bonita:9.0.0`

```console
$ docker pull bonita@sha256:48fe1a388de4f57a67014c8ee26f65ca3a26b95c3c39a23069bc97dbae778d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:9.0.0` - linux; amd64

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

### `bonita:9.0.0` - linux; arm64 variant v8

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

### `bonita:9.0.0` - linux; ppc64le

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
