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
$ docker pull bonita@sha256:1afdec31ca6a55879505a7cd66aae8e97652a46690231b394b39bed816bd57dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bonita:2022.1` - linux; amd64

```console
$ docker pull bonita@sha256:1a863c00f1d403b007e7e0e28df98cda855248cfef46b88688f571af87e27bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177052561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f166962921d07ad36985476b2b4a5c34d738646fdeee0241a97c58f4a80b44ea`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:59:18 GMT
ADD file:aa1af71c6b66d2dddee4797236e3e526f70f904ab641cc0dd6b41445cfedf9b4 in / 
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:59:18 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:59:18 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:59:18 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:59:18 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d078792c4f9122259f14b539315bd92cbd9490ed73e08255a08689122b143108`  
		Last Modified: Thu, 30 Nov 2023 23:23:58 GMT  
		Size: 2.8 MB (2826431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2850d502a838ba6c0b82d0b4418251ec5b73d7b6f34a41e068e1846a0d56ec15`  
		Last Modified: Thu, 30 May 2024 21:01:09 GMT  
		Size: 57.5 MB (57528345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0368b2e11d73d30a1719d88c08577a5769ad232b1a80e9e4953dbbafd5750527`  
		Last Modified: Thu, 30 May 2024 21:01:08 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1280aa1681af4413bf5897033d603717af6387c82a3590ebf3adfdc4e571de4`  
		Last Modified: Thu, 30 May 2024 21:01:08 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0133e2bf0ec8e0571228a78ce463d850ab1d1074984910bea0d19c00ed071a1`  
		Last Modified: Thu, 30 May 2024 21:01:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d916f80dafb2dca2d366c95c6373e977e74d52bef852742f9355e5b2f161ca`  
		Last Modified: Thu, 30 May 2024 21:01:09 GMT  
		Size: 3.0 KB (2992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a484f13af52fd6d101199d7112d1e44cd884b9fdc3f9b47aa48dd482bbfb78c`  
		Last Modified: Thu, 30 May 2024 21:01:11 GMT  
		Size: 116.7 MB (116687932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3b032ee0e7eafb05ffb6dcf308c04068996b47c7606bc8d075fe951fe10126`  
		Last Modified: Thu, 30 May 2024 21:01:09 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.1` - unknown; unknown

```console
$ docker pull bonita@sha256:e98f36524f181cc0c4f726eaf021c32b779d0774d1109312aa1d9215bbb5eba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.8 KB (621846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c21444c0a2122ba43fb28ed2a9881f7ecd6799fcea38c4c0dcf397eb249874b`

```dockerfile
```

-	Layers:
	-	`sha256:5e55962fd89e2c8bd1652c996fcc0bfe489da3135550cc6d770d0aca8c695061`  
		Last Modified: Thu, 30 May 2024 21:01:08 GMT  
		Size: 598.8 KB (598806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6670d5cd71b8a4ed15896b1392c2371b4beca3edcdeca22f270c89d50be22cb9`  
		Last Modified: Thu, 30 May 2024 21:01:08 GMT  
		Size: 23.0 KB (23040 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:b213041262a0970b880265347e6fce91d47e062bb45d3bf76295cf06b672de62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176270879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87186d8e14d4b205d9acd6f51a170db1460ed015a528507b8032876ff5fa1dfc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:59:18 GMT
ADD file:3982c510455cc0ceea8cf8dd0b50b69588e35fd4f84522cb4000582c73781672 in / 
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:59:18 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:59:18 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:59:18 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:59:18 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8bc1ab4b84041d57f21a792410a00820f73fda7efe08bcd2ca6245349a40299d`  
		Last Modified: Thu, 30 Nov 2023 23:12:02 GMT  
		Size: 2.7 MB (2721527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aef56ab86690ac9887c2884a0572f63ae54a4171beec97df76001874e1d938d`  
		Last Modified: Thu, 30 May 2024 22:45:20 GMT  
		Size: 56.9 MB (56851579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085dc8607af603cbda94196b45ddb7c0275334820c0246e04215e26e20802c4a`  
		Last Modified: Thu, 30 May 2024 22:45:17 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19fb80c67b80100fe22f7b08bfa74ad1b9070a32be301586ef2d727f9a50590`  
		Last Modified: Thu, 30 May 2024 22:45:17 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5b93a2662730914ae0ba7bf45f9a08fad198917faababcf5a1bd78f196288d`  
		Last Modified: Thu, 30 May 2024 22:45:18 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca20a4be91429ccf555ce1a52caf1c6f9444646d749449f6963c3a4c3970ee64`  
		Last Modified: Thu, 30 May 2024 22:45:18 GMT  
		Size: 3.0 KB (2988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f916901979ad5a2b355b3afb591759ef88100ad8fb9f2f9e4347222f6f9b14f`  
		Last Modified: Thu, 30 May 2024 22:45:25 GMT  
		Size: 116.7 MB (116687925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27675cdc16497debd66665daeef9344942b15c78e3cc3d401d93846094b91822`  
		Last Modified: Thu, 30 May 2024 22:45:19 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.1` - unknown; unknown

```console
$ docker pull bonita@sha256:df3af0ee9fe8ebfb9b344afb2eb0bd2c1aa19818cf817bd5b44cb9fd65e45b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.2 KB (621206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1630478d103b7072845192c91eb0d8a72bfd6fc7b4c6da3172e8efe5f5b00f54`

```dockerfile
```

-	Layers:
	-	`sha256:80866d2b60a761f8e0a20e282203cf2ad5758fe3978da1a72fd10aa29e60ad10`  
		Last Modified: Thu, 30 May 2024 22:45:18 GMT  
		Size: 597.9 KB (597866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef83d34f3540676c1ba9b5a0fe3100b746dd6ae139453adef199e02fd8aa5d8`  
		Last Modified: Thu, 30 May 2024 22:45:18 GMT  
		Size: 23.3 KB (23340 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:9e3a07a3365454dd742276176419251d2d96e5414f714174ee9b2a312c58881c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172866651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fe72c2160957b5c85293963318fd0681a8dc926bbec27139bbe023ef02e714`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:59:18 GMT
ADD file:35af09f43b08c93abd4c6b8679d43e8ac40893bf5932c4c21f1bb037f53bb62c in / 
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:59:18 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:59:18 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:59:18 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:59:18 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:080a2fea3a772fa995cb0b07b4601e7cd57650fa4e8a50866da1de707946d7b3`  
		Last Modified: Thu, 30 Nov 2023 23:20:38 GMT  
		Size: 2.8 MB (2812474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33c924802356b5e3d2e0d9d806dedfecf7cef7d8dd3eb869241e75b101f2026`  
		Last Modified: Thu, 30 May 2024 21:12:56 GMT  
		Size: 53.4 MB (53356415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69ddad3fc11d89779028d23f3fba05be63652828d1528069dff627ac678871e`  
		Last Modified: Thu, 30 May 2024 21:12:55 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aebbc847f70a92e9eb9252d917e3bd170ef1dbfcd47d9292fd2323e0e5c06d9`  
		Last Modified: Thu, 30 May 2024 21:12:54 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de5cd1d8cb72333a1d8ac61553b10fdd6f903de1fc544d3b767190b2fe248e9`  
		Last Modified: Thu, 30 May 2024 21:12:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee9ea34acfc5886a1ed11519581d81bd5bb1360a8e4dff3dd6bc4f7b66a4d84`  
		Last Modified: Thu, 30 May 2024 21:12:56 GMT  
		Size: 3.0 KB (2991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cc215ab03fbcf0b693cb48846ebc8b33ef364ae69fa3881b1291de2cc2dbf7`  
		Last Modified: Thu, 30 May 2024 21:12:59 GMT  
		Size: 116.7 MB (116687908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18674db949efb66ab61a5ce9b43debd5d86f25992b160b46e88c15076673739c`  
		Last Modified: Thu, 30 May 2024 21:12:57 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.1` - unknown; unknown

```console
$ docker pull bonita@sha256:eec4da703381341df05010a04afb3e20aa14300639b245b330b0af2577530f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.0 KB (618980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac67ac283fdf263f29b3332970fcd30cc8184646516ff533550b2748dcb3a58f`

```dockerfile
```

-	Layers:
	-	`sha256:711c8bf82b03025366753b692200e0b18dbb209a95ba1a3d64da63bdd53e5d42`  
		Last Modified: Thu, 30 May 2024 21:12:55 GMT  
		Size: 595.9 KB (595894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5c977c3112c94d455be931a33bf804f0e1ede48ef3e8a89e7d608fa137a88a8`  
		Last Modified: Thu, 30 May 2024 21:12:54 GMT  
		Size: 23.1 KB (23086 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2022.1-u0`

```console
$ docker pull bonita@sha256:1afdec31ca6a55879505a7cd66aae8e97652a46690231b394b39bed816bd57dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bonita:2022.1-u0` - linux; amd64

```console
$ docker pull bonita@sha256:1a863c00f1d403b007e7e0e28df98cda855248cfef46b88688f571af87e27bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177052561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f166962921d07ad36985476b2b4a5c34d738646fdeee0241a97c58f4a80b44ea`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:59:18 GMT
ADD file:aa1af71c6b66d2dddee4797236e3e526f70f904ab641cc0dd6b41445cfedf9b4 in / 
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:59:18 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:59:18 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:59:18 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:59:18 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d078792c4f9122259f14b539315bd92cbd9490ed73e08255a08689122b143108`  
		Last Modified: Thu, 30 Nov 2023 23:23:58 GMT  
		Size: 2.8 MB (2826431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2850d502a838ba6c0b82d0b4418251ec5b73d7b6f34a41e068e1846a0d56ec15`  
		Last Modified: Thu, 30 May 2024 21:01:09 GMT  
		Size: 57.5 MB (57528345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0368b2e11d73d30a1719d88c08577a5769ad232b1a80e9e4953dbbafd5750527`  
		Last Modified: Thu, 30 May 2024 21:01:08 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1280aa1681af4413bf5897033d603717af6387c82a3590ebf3adfdc4e571de4`  
		Last Modified: Thu, 30 May 2024 21:01:08 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0133e2bf0ec8e0571228a78ce463d850ab1d1074984910bea0d19c00ed071a1`  
		Last Modified: Thu, 30 May 2024 21:01:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d916f80dafb2dca2d366c95c6373e977e74d52bef852742f9355e5b2f161ca`  
		Last Modified: Thu, 30 May 2024 21:01:09 GMT  
		Size: 3.0 KB (2992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a484f13af52fd6d101199d7112d1e44cd884b9fdc3f9b47aa48dd482bbfb78c`  
		Last Modified: Thu, 30 May 2024 21:01:11 GMT  
		Size: 116.7 MB (116687932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3b032ee0e7eafb05ffb6dcf308c04068996b47c7606bc8d075fe951fe10126`  
		Last Modified: Thu, 30 May 2024 21:01:09 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.1-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:e98f36524f181cc0c4f726eaf021c32b779d0774d1109312aa1d9215bbb5eba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.8 KB (621846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c21444c0a2122ba43fb28ed2a9881f7ecd6799fcea38c4c0dcf397eb249874b`

```dockerfile
```

-	Layers:
	-	`sha256:5e55962fd89e2c8bd1652c996fcc0bfe489da3135550cc6d770d0aca8c695061`  
		Last Modified: Thu, 30 May 2024 21:01:08 GMT  
		Size: 598.8 KB (598806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6670d5cd71b8a4ed15896b1392c2371b4beca3edcdeca22f270c89d50be22cb9`  
		Last Modified: Thu, 30 May 2024 21:01:08 GMT  
		Size: 23.0 KB (23040 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:b213041262a0970b880265347e6fce91d47e062bb45d3bf76295cf06b672de62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176270879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87186d8e14d4b205d9acd6f51a170db1460ed015a528507b8032876ff5fa1dfc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:59:18 GMT
ADD file:3982c510455cc0ceea8cf8dd0b50b69588e35fd4f84522cb4000582c73781672 in / 
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:59:18 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:59:18 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:59:18 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:59:18 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8bc1ab4b84041d57f21a792410a00820f73fda7efe08bcd2ca6245349a40299d`  
		Last Modified: Thu, 30 Nov 2023 23:12:02 GMT  
		Size: 2.7 MB (2721527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aef56ab86690ac9887c2884a0572f63ae54a4171beec97df76001874e1d938d`  
		Last Modified: Thu, 30 May 2024 22:45:20 GMT  
		Size: 56.9 MB (56851579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085dc8607af603cbda94196b45ddb7c0275334820c0246e04215e26e20802c4a`  
		Last Modified: Thu, 30 May 2024 22:45:17 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19fb80c67b80100fe22f7b08bfa74ad1b9070a32be301586ef2d727f9a50590`  
		Last Modified: Thu, 30 May 2024 22:45:17 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5b93a2662730914ae0ba7bf45f9a08fad198917faababcf5a1bd78f196288d`  
		Last Modified: Thu, 30 May 2024 22:45:18 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca20a4be91429ccf555ce1a52caf1c6f9444646d749449f6963c3a4c3970ee64`  
		Last Modified: Thu, 30 May 2024 22:45:18 GMT  
		Size: 3.0 KB (2988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f916901979ad5a2b355b3afb591759ef88100ad8fb9f2f9e4347222f6f9b14f`  
		Last Modified: Thu, 30 May 2024 22:45:25 GMT  
		Size: 116.7 MB (116687925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27675cdc16497debd66665daeef9344942b15c78e3cc3d401d93846094b91822`  
		Last Modified: Thu, 30 May 2024 22:45:19 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.1-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:df3af0ee9fe8ebfb9b344afb2eb0bd2c1aa19818cf817bd5b44cb9fd65e45b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.2 KB (621206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1630478d103b7072845192c91eb0d8a72bfd6fc7b4c6da3172e8efe5f5b00f54`

```dockerfile
```

-	Layers:
	-	`sha256:80866d2b60a761f8e0a20e282203cf2ad5758fe3978da1a72fd10aa29e60ad10`  
		Last Modified: Thu, 30 May 2024 22:45:18 GMT  
		Size: 597.9 KB (597866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef83d34f3540676c1ba9b5a0fe3100b746dd6ae139453adef199e02fd8aa5d8`  
		Last Modified: Thu, 30 May 2024 22:45:18 GMT  
		Size: 23.3 KB (23340 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:9e3a07a3365454dd742276176419251d2d96e5414f714174ee9b2a312c58881c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172866651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fe72c2160957b5c85293963318fd0681a8dc926bbec27139bbe023ef02e714`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:59:18 GMT
ADD file:35af09f43b08c93abd4c6b8679d43e8ac40893bf5932c4c21f1bb037f53bb62c in / 
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:59:18 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:59:18 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:59:18 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:59:18 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:080a2fea3a772fa995cb0b07b4601e7cd57650fa4e8a50866da1de707946d7b3`  
		Last Modified: Thu, 30 Nov 2023 23:20:38 GMT  
		Size: 2.8 MB (2812474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33c924802356b5e3d2e0d9d806dedfecf7cef7d8dd3eb869241e75b101f2026`  
		Last Modified: Thu, 30 May 2024 21:12:56 GMT  
		Size: 53.4 MB (53356415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69ddad3fc11d89779028d23f3fba05be63652828d1528069dff627ac678871e`  
		Last Modified: Thu, 30 May 2024 21:12:55 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aebbc847f70a92e9eb9252d917e3bd170ef1dbfcd47d9292fd2323e0e5c06d9`  
		Last Modified: Thu, 30 May 2024 21:12:54 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de5cd1d8cb72333a1d8ac61553b10fdd6f903de1fc544d3b767190b2fe248e9`  
		Last Modified: Thu, 30 May 2024 21:12:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee9ea34acfc5886a1ed11519581d81bd5bb1360a8e4dff3dd6bc4f7b66a4d84`  
		Last Modified: Thu, 30 May 2024 21:12:56 GMT  
		Size: 3.0 KB (2991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cc215ab03fbcf0b693cb48846ebc8b33ef364ae69fa3881b1291de2cc2dbf7`  
		Last Modified: Thu, 30 May 2024 21:12:59 GMT  
		Size: 116.7 MB (116687908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18674db949efb66ab61a5ce9b43debd5d86f25992b160b46e88c15076673739c`  
		Last Modified: Thu, 30 May 2024 21:12:57 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.1-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:eec4da703381341df05010a04afb3e20aa14300639b245b330b0af2577530f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.0 KB (618980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac67ac283fdf263f29b3332970fcd30cc8184646516ff533550b2748dcb3a58f`

```dockerfile
```

-	Layers:
	-	`sha256:711c8bf82b03025366753b692200e0b18dbb209a95ba1a3d64da63bdd53e5d42`  
		Last Modified: Thu, 30 May 2024 21:12:55 GMT  
		Size: 595.9 KB (595894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5c977c3112c94d455be931a33bf804f0e1ede48ef3e8a89e7d608fa137a88a8`  
		Last Modified: Thu, 30 May 2024 21:12:54 GMT  
		Size: 23.1 KB (23086 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2022.2`

```console
$ docker pull bonita@sha256:5e79922cae414f2075d3cd98d4582d891a8c6eceab30b14b565d5e36434de45a
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
$ docker pull bonita@sha256:68b05aed88ef5c6c2afc65634b66599b99ef568801cac4ced905891add7ab0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183647748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4789c9604df70fa15d30e7f8ffbd9be70bc36cae45eb4caa2c8a236a49738ec`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:34:20 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:34:20 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_VERSION=7.15.0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BRANDING_VERSION=2022.2-u0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:34:20 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:34:20 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:34:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6702ed64834ed89f10c7ffaec872f8f5765de3235860148f12547cab2771c1d`  
		Last Modified: Thu, 30 May 2024 20:56:14 GMT  
		Size: 61.6 MB (61639298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b877c9ca382d7a2a9bbe48cb38590ee9b845354c1c027136defc025939a9b5c5`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b7a3b54e51d13fc173d43051341b1a99bb0466f758760291a70a21913c0e9e`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7180ba389779c576a63f8337f70c8ccb9f9183a29381261d6c5e0fdaa3f27a5e`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1100d2b7215d90ac2720b6761cbffcec112b9011c7524bb054209c6234ada209`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 3.0 KB (3003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99aae4a5291464a5844092748ad5630de4b9441dfc1ef3d25d70e745d3e3d99d`  
		Last Modified: Thu, 30 May 2024 20:56:16 GMT  
		Size: 119.2 MB (119190749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea18f123da6c9dbc056c9a79bfdedd5d26ca99a512689c87331e625d4b24029`  
		Last Modified: Thu, 30 May 2024 20:56:14 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2` - unknown; unknown

```console
$ docker pull bonita@sha256:ee97d17ff60c40ee97102546b7540ca7df7f77bbe4990efbd6f176951d56178a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.7 KB (843663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47502f3ae25dfae664f0abd59ace922765a6a96c65d0be5b336be50d7103cdb`

```dockerfile
```

-	Layers:
	-	`sha256:35fadb308cc14fac57123855c2bda2397f5ed1579951d69a202f2af4200c681e`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 820.6 KB (820644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1120c1721090eeac0d7a8648d52b033868d3ff5ac014cbc8c426441c1496e115`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 23.0 KB (23019 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:031eed17b81f05b9a751d4eb5de470c6f9816273bebd6968c254b1484c5d19f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182795104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27f5f7cfdb4d20f5bdefad7e5a798f6522bed0c90c2f14ee33430464441a4e5`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:34:20 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:34:20 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_VERSION=7.15.0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BRANDING_VERSION=2022.2-u0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:34:20 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:34:20 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:34:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9c413225ca7157a35f4580c54257db05570e292e99b9736cc3c4eef92890fc`  
		Last Modified: Thu, 30 May 2024 22:46:05 GMT  
		Size: 60.9 MB (60886274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8c5c2285121d4b0d57cf25e56d491dbd4a9028176e172d4d159ac57b2f8458`  
		Last Modified: Thu, 30 May 2024 22:46:02 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50994a35a8b227436180382bb0cafc50892b5bec29303b0564ea297b483b2848`  
		Last Modified: Thu, 30 May 2024 22:46:02 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fa5f03f6e8de9741cf728899e8639690cd97f1963245007e93020edf086350`  
		Last Modified: Thu, 30 May 2024 22:46:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e32a8d97e7f940e76e97b18729de5e3853b81f1e6e4d3fe72650de8f741bd2`  
		Last Modified: Thu, 30 May 2024 22:46:03 GMT  
		Size: 3.0 KB (3002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840c886a647e4761c865de41fdecf28aabdf392be2558d7588f4a132cf61caa3`  
		Last Modified: Thu, 30 May 2024 22:46:06 GMT  
		Size: 119.2 MB (119190681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c21e19f38f949440557d9eb970e85705fa9454b90b4444e4374a1a16a218797`  
		Last Modified: Thu, 30 May 2024 22:46:04 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2` - unknown; unknown

```console
$ docker pull bonita@sha256:b84756ab16037ed0d50238658f65923d8d825fbf955cbdd5a21ecd6ea48149c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.1 KB (843063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60471a4c0fc256e9b631b10770c84f34d1c797f6f5e75615e6b25006b4ed79f2`

```dockerfile
```

-	Layers:
	-	`sha256:90d6b129f43c5e6ff4cf07592e39064c69f522ee1ed1acfce8bf4b9f44e6c0f1`  
		Last Modified: Thu, 30 May 2024 22:46:03 GMT  
		Size: 819.7 KB (819744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d3c1ae4d6ad3bedbc5d25c34de1fb34bf1c682a64ed917713ee479f9de2232e`  
		Last Modified: Thu, 30 May 2024 22:46:02 GMT  
		Size: 23.3 KB (23319 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:9eb34c2150166972653b8dba12b89e9636dcc6da156b6929f0d7ab33d86ef655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179819681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b718d3559a26fb41d30f7cc907dba806e3f828e5b122d5c12860a18b4a15c2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:34:20 GMT
ADD file:cf4fecc20d85962cd46b6911d8ee82b9a3de2fa530bc58e998c2d544a888fdb9 in / 
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:34:20 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_VERSION=7.15.0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BRANDING_VERSION=2022.2-u0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:34:20 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:34:20 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:34:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:04646341bdb047ee1a3dd65db76069b9117954385033f5a340622fd170fa4b73`  
		Last Modified: Sat, 27 Jan 2024 00:28:46 GMT  
		Size: 2.8 MB (2802980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3169e99f3c3d30c82bce3b7fe8f4a643505e25691c0a3a8ea8daf01d4170a4b`  
		Last Modified: Thu, 30 May 2024 21:17:50 GMT  
		Size: 57.8 MB (57816142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a736beb4906376ce95524b776b66c7806e73f0558c594e28a931275f5efb1dfb`  
		Last Modified: Thu, 30 May 2024 21:17:47 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d7adbafe038499090091dd1243f6a053200f23d6e3db2243b369b9744c0009`  
		Last Modified: Thu, 30 May 2024 21:17:47 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4d5bde7cb90faccf971340b6ded0d3f8347c8c99b06593b9ac592ab80a53d3`  
		Last Modified: Thu, 30 May 2024 21:17:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c1c212f47019afda5d60f95f7ca3619dc58be9e73328321a4a07bf4af5e86c`  
		Last Modified: Thu, 30 May 2024 21:17:48 GMT  
		Size: 3.0 KB (3003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7556ecb8b489313ffd345e92e529dde59ae002a7f37cf50ac29e3f3882eb2e76`  
		Last Modified: Thu, 30 May 2024 21:17:52 GMT  
		Size: 119.2 MB (119190690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13dc87b637dcf22284ad9b9b1d17886ef0ea0a4c8e5dd743b1a325066c7c02e6`  
		Last Modified: Thu, 30 May 2024 21:17:48 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2` - unknown; unknown

```console
$ docker pull bonita@sha256:dbc429945850eeaea750e1080411ad264da2f86b7998a9be3a35b617c28cc4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8888a15d46bc3f610c29846bcdabbc10da3e2217d50b7559803a101b7eeb407`

```dockerfile
```

-	Layers:
	-	`sha256:69c6ec711a31ac4bae45f279d8816b71769961acbb70aec3f2c259938ee1be28`  
		Last Modified: Thu, 30 May 2024 21:17:48 GMT  
		Size: 817.7 KB (817723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e326df99f8c53edf340fc078fd1cd58591005a8f8a6509335db80fed3b38404`  
		Last Modified: Thu, 30 May 2024 21:17:47 GMT  
		Size: 23.1 KB (23065 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2022.2-u0`

```console
$ docker pull bonita@sha256:5e79922cae414f2075d3cd98d4582d891a8c6eceab30b14b565d5e36434de45a
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
$ docker pull bonita@sha256:68b05aed88ef5c6c2afc65634b66599b99ef568801cac4ced905891add7ab0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183647748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4789c9604df70fa15d30e7f8ffbd9be70bc36cae45eb4caa2c8a236a49738ec`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:34:20 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:34:20 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_VERSION=7.15.0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BRANDING_VERSION=2022.2-u0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:34:20 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:34:20 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:34:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6702ed64834ed89f10c7ffaec872f8f5765de3235860148f12547cab2771c1d`  
		Last Modified: Thu, 30 May 2024 20:56:14 GMT  
		Size: 61.6 MB (61639298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b877c9ca382d7a2a9bbe48cb38590ee9b845354c1c027136defc025939a9b5c5`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b7a3b54e51d13fc173d43051341b1a99bb0466f758760291a70a21913c0e9e`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7180ba389779c576a63f8337f70c8ccb9f9183a29381261d6c5e0fdaa3f27a5e`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1100d2b7215d90ac2720b6761cbffcec112b9011c7524bb054209c6234ada209`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 3.0 KB (3003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99aae4a5291464a5844092748ad5630de4b9441dfc1ef3d25d70e745d3e3d99d`  
		Last Modified: Thu, 30 May 2024 20:56:16 GMT  
		Size: 119.2 MB (119190749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea18f123da6c9dbc056c9a79bfdedd5d26ca99a512689c87331e625d4b24029`  
		Last Modified: Thu, 30 May 2024 20:56:14 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:ee97d17ff60c40ee97102546b7540ca7df7f77bbe4990efbd6f176951d56178a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.7 KB (843663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47502f3ae25dfae664f0abd59ace922765a6a96c65d0be5b336be50d7103cdb`

```dockerfile
```

-	Layers:
	-	`sha256:35fadb308cc14fac57123855c2bda2397f5ed1579951d69a202f2af4200c681e`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 820.6 KB (820644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1120c1721090eeac0d7a8648d52b033868d3ff5ac014cbc8c426441c1496e115`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 23.0 KB (23019 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:031eed17b81f05b9a751d4eb5de470c6f9816273bebd6968c254b1484c5d19f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182795104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27f5f7cfdb4d20f5bdefad7e5a798f6522bed0c90c2f14ee33430464441a4e5`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:34:20 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:34:20 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_VERSION=7.15.0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BRANDING_VERSION=2022.2-u0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:34:20 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:34:20 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:34:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9c413225ca7157a35f4580c54257db05570e292e99b9736cc3c4eef92890fc`  
		Last Modified: Thu, 30 May 2024 22:46:05 GMT  
		Size: 60.9 MB (60886274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8c5c2285121d4b0d57cf25e56d491dbd4a9028176e172d4d159ac57b2f8458`  
		Last Modified: Thu, 30 May 2024 22:46:02 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50994a35a8b227436180382bb0cafc50892b5bec29303b0564ea297b483b2848`  
		Last Modified: Thu, 30 May 2024 22:46:02 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fa5f03f6e8de9741cf728899e8639690cd97f1963245007e93020edf086350`  
		Last Modified: Thu, 30 May 2024 22:46:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e32a8d97e7f940e76e97b18729de5e3853b81f1e6e4d3fe72650de8f741bd2`  
		Last Modified: Thu, 30 May 2024 22:46:03 GMT  
		Size: 3.0 KB (3002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840c886a647e4761c865de41fdecf28aabdf392be2558d7588f4a132cf61caa3`  
		Last Modified: Thu, 30 May 2024 22:46:06 GMT  
		Size: 119.2 MB (119190681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c21e19f38f949440557d9eb970e85705fa9454b90b4444e4374a1a16a218797`  
		Last Modified: Thu, 30 May 2024 22:46:04 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:b84756ab16037ed0d50238658f65923d8d825fbf955cbdd5a21ecd6ea48149c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.1 KB (843063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60471a4c0fc256e9b631b10770c84f34d1c797f6f5e75615e6b25006b4ed79f2`

```dockerfile
```

-	Layers:
	-	`sha256:90d6b129f43c5e6ff4cf07592e39064c69f522ee1ed1acfce8bf4b9f44e6c0f1`  
		Last Modified: Thu, 30 May 2024 22:46:03 GMT  
		Size: 819.7 KB (819744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d3c1ae4d6ad3bedbc5d25c34de1fb34bf1c682a64ed917713ee479f9de2232e`  
		Last Modified: Thu, 30 May 2024 22:46:02 GMT  
		Size: 23.3 KB (23319 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:9eb34c2150166972653b8dba12b89e9636dcc6da156b6929f0d7ab33d86ef655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179819681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b718d3559a26fb41d30f7cc907dba806e3f828e5b122d5c12860a18b4a15c2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:34:20 GMT
ADD file:cf4fecc20d85962cd46b6911d8ee82b9a3de2fa530bc58e998c2d544a888fdb9 in / 
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:34:20 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_VERSION=7.15.0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BRANDING_VERSION=2022.2-u0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:34:20 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:34:20 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:34:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:04646341bdb047ee1a3dd65db76069b9117954385033f5a340622fd170fa4b73`  
		Last Modified: Sat, 27 Jan 2024 00:28:46 GMT  
		Size: 2.8 MB (2802980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3169e99f3c3d30c82bce3b7fe8f4a643505e25691c0a3a8ea8daf01d4170a4b`  
		Last Modified: Thu, 30 May 2024 21:17:50 GMT  
		Size: 57.8 MB (57816142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a736beb4906376ce95524b776b66c7806e73f0558c594e28a931275f5efb1dfb`  
		Last Modified: Thu, 30 May 2024 21:17:47 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d7adbafe038499090091dd1243f6a053200f23d6e3db2243b369b9744c0009`  
		Last Modified: Thu, 30 May 2024 21:17:47 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4d5bde7cb90faccf971340b6ded0d3f8347c8c99b06593b9ac592ab80a53d3`  
		Last Modified: Thu, 30 May 2024 21:17:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c1c212f47019afda5d60f95f7ca3619dc58be9e73328321a4a07bf4af5e86c`  
		Last Modified: Thu, 30 May 2024 21:17:48 GMT  
		Size: 3.0 KB (3003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7556ecb8b489313ffd345e92e529dde59ae002a7f37cf50ac29e3f3882eb2e76`  
		Last Modified: Thu, 30 May 2024 21:17:52 GMT  
		Size: 119.2 MB (119190690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13dc87b637dcf22284ad9b9b1d17886ef0ea0a4c8e5dd743b1a325066c7c02e6`  
		Last Modified: Thu, 30 May 2024 21:17:48 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:dbc429945850eeaea750e1080411ad264da2f86b7998a9be3a35b617c28cc4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8888a15d46bc3f610c29846bcdabbc10da3e2217d50b7559803a101b7eeb407`

```dockerfile
```

-	Layers:
	-	`sha256:69c6ec711a31ac4bae45f279d8816b71769961acbb70aec3f2c259938ee1be28`  
		Last Modified: Thu, 30 May 2024 21:17:48 GMT  
		Size: 817.7 KB (817723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e326df99f8c53edf340fc078fd1cd58591005a8f8a6509335db80fed3b38404`  
		Last Modified: Thu, 30 May 2024 21:17:47 GMT  
		Size: 23.1 KB (23065 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.1`

```console
$ docker pull bonita@sha256:05190016a00a01783ab68b77c073d142da324a4de5e344d5fc8eb4e08f4d725e
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
$ docker pull bonita@sha256:cce825ac7644fd7b1665c9e331fc403e5d672db18c62612531b9ddd108d8c853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183457895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59318a8026e721b80f30d0081d879bd5905694c47804b0223d6ab6adc7f9009d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:31:00 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_VERSION=8.0.0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BRANDING_VERSION=2023.1-u0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:31:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:31:00 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Wed, 15 Nov 2023 09:31:00 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
VOLUME [/opt/bonita/conf/logs]
# Wed, 15 Nov 2023 09:31:00 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:31:00 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fd34e6efb621be2c6a33a4342ed75b2eabf18c425e3493c52bc224ed2e5f22`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 61.9 MB (61879078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938ba79419d326f15d91444b8d7f502767a019c577bb86dcb1825168786920f`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d80844bd8d09281cd97dfa9eb3c27bfcc11f6d75075a34679079583f713a3e`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094db1411d9e829316fe3244a42b61e897ac4f7a74503b38e3986c182203a81b`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5047b989f83348dc2a430cfedfb4b39fd27c65e93611f89921d103816b60088b`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc5c9ac25523fc16256abc5c94d4823959b0fb7ede78e2514c61835ef69800c`  
		Last Modified: Thu, 20 Jun 2024 20:54:57 GMT  
		Size: 118.2 MB (118178555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0e97a0d4526f399153bec09432856e04a9e6f07ba3051fe5ff9b908d8d2d2e`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1` - unknown; unknown

```console
$ docker pull bonita@sha256:7c2344c3bae4f1e4fad5034af7021dc529c11ddfadda0278539309f7a4d7c178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.4 KB (842392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76956d38981f86cf8210758ea9841ecc56d034ae5158a05031be483fa88e9c8d`

```dockerfile
```

-	Layers:
	-	`sha256:c702bcf4221f8fbd6297dd327d5cf6ad93cbbb555b84e1d85100381929e7c2fe`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 819.2 KB (819154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98dd9bc4991f245e3dec118ab7c6f4fb16ff9d29c7cd70857a688b43033414d`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 23.2 KB (23238 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2a8211bccb6126e149ba5aeb200db20d2ad46c78a721de248324a5ce03b36b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182587785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90293c2b1ef2b511383052fc6a7c40178f20f0f1e36b2cb61fa3aa2e99d237b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:31:00 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_VERSION=8.0.0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BRANDING_VERSION=2023.1-u0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:31:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:31:00 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Wed, 15 Nov 2023 09:31:00 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
VOLUME [/opt/bonita/conf/logs]
# Wed, 15 Nov 2023 09:31:00 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:31:00 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e320cbe6007b5dedf0233709bc723fc4607d7fb5f829d82217ef543560aad7d`  
		Last Modified: Fri, 21 Jun 2024 04:35:26 GMT  
		Size: 61.1 MB (61126346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ea9fedde8038622b8526a5b85c441eee7841116bf26f844b83aaa1191e0dac`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b98ef9a238cf22e841ad204f987bc47c777ceaeba1d4085aedd9f1f64e81b17`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b318a41794c5371b6347de93c0154b7412554272fd77e255e6ee344059655c6c`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a09814e50f5970faaccaec563fc7ad8a8fa081730c3fb0c036330f547e625f`  
		Last Modified: Fri, 21 Jun 2024 04:35:25 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ca2992916fc11509c644e39aff85ead2ffa066d6e010b72cbddea7c3ed0e60`  
		Last Modified: Fri, 21 Jun 2024 04:35:28 GMT  
		Size: 118.2 MB (118178556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52030788e32622ddd3dc4030114c6f8b20e704b7e4a8fe4468316df704be26c0`  
		Last Modified: Fri, 21 Jun 2024 04:35:25 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1` - unknown; unknown

```console
$ docker pull bonita@sha256:18d57d0335b7cf4efc6b1d0c1a0c2185c513a3a83e4a12f0cb76c38da5f63407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.8 KB (841801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce984ed4e50cc3d40b698ae05ea0202fffe3a84696671fcec5de8b500d3e00cd`

```dockerfile
```

-	Layers:
	-	`sha256:fc37535d8ebd20459ee695a64294dc7772cac3b5c905412065ef14e4c7878594`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 818.3 KB (818263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44df43a6749e8edda5cffffe0330d940e84b12e602288fb07fd8904dcf351ba2`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 23.5 KB (23538 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:dcc8142308a098d4e62c718371c5392e8f71ac4c5cb59f62c7988b796c263aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179619841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8982389b6769fdac34527f358a750b30d6de4ce350d3f896d8daaf277a17bd94`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:80e24883ff1c790ff4b3d2b4488ea6cf7b9cbcf5432b00aba4c6043f5e4055c0 in / 
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:31:00 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_VERSION=8.0.0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BRANDING_VERSION=2023.1-u0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:31:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:31:00 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Wed, 15 Nov 2023 09:31:00 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
VOLUME [/opt/bonita/conf/logs]
# Wed, 15 Nov 2023 09:31:00 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:31:00 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f81397ca64cd321c51a90461a0c2f9fb32b00a52366a20f24075bb794eea71a2`  
		Last Modified: Thu, 20 Jun 2024 18:19:25 GMT  
		Size: 3.4 MB (3401809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210567cb03f3b32283f4642a983d2f70076991f82eae53e3c1a0275e8bf6baf6`  
		Last Modified: Fri, 21 Jun 2024 01:23:14 GMT  
		Size: 58.0 MB (58029183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1a7dd7c349b2370b225859ce8e0d63090bd54c459e7627279aff66761f42de`  
		Last Modified: Fri, 21 Jun 2024 01:23:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa42dbd8316045ef2401daa7e9b7366befa4482662398fc723f5a063acc97116`  
		Last Modified: Fri, 21 Jun 2024 01:23:12 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94a650ed84aae374b643fdca8f6b6df20ec8c7e4d11d6ff89180d8ed3170ce0`  
		Last Modified: Fri, 21 Jun 2024 01:23:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8155bde4dd4e7cdb6f5b917dd0f8709de6905c1226111f933e444813cb585ed`  
		Last Modified: Fri, 21 Jun 2024 01:23:13 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9045ca1a5493acc924cd5508a058b18ad545f9f83468b367a11e93fc312fe500`  
		Last Modified: Fri, 21 Jun 2024 01:23:17 GMT  
		Size: 118.2 MB (118178558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b9c66fc9f04f25705d2434b548de75fdf7874593d46be37ef6639764e04292`  
		Last Modified: Fri, 21 Jun 2024 01:23:14 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1` - unknown; unknown

```console
$ docker pull bonita@sha256:e3bc97e68aa0147911f67835df159b2c4f067c77ae148f4cf381a07e3f1f5e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **839.6 KB (839612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c1bfd4085a43aafadf4dd06235fe47ebd479506f52b88d151e05226d43d556`

```dockerfile
```

-	Layers:
	-	`sha256:cef32d66324a634f4c9389ee0eee40a7d6cb7b83c0d1ffa323c72dc3b0c98b1e`  
		Last Modified: Fri, 21 Jun 2024 01:23:12 GMT  
		Size: 816.3 KB (816328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b04a689ddae65938b13cd16d310a1e8b114fb7b33449e9905cbf0dc4cd462e17`  
		Last Modified: Fri, 21 Jun 2024 01:23:12 GMT  
		Size: 23.3 KB (23284 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.1-u0`

```console
$ docker pull bonita@sha256:05190016a00a01783ab68b77c073d142da324a4de5e344d5fc8eb4e08f4d725e
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
$ docker pull bonita@sha256:cce825ac7644fd7b1665c9e331fc403e5d672db18c62612531b9ddd108d8c853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183457895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59318a8026e721b80f30d0081d879bd5905694c47804b0223d6ab6adc7f9009d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:31:00 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_VERSION=8.0.0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BRANDING_VERSION=2023.1-u0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:31:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:31:00 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Wed, 15 Nov 2023 09:31:00 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
VOLUME [/opt/bonita/conf/logs]
# Wed, 15 Nov 2023 09:31:00 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:31:00 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fd34e6efb621be2c6a33a4342ed75b2eabf18c425e3493c52bc224ed2e5f22`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 61.9 MB (61879078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938ba79419d326f15d91444b8d7f502767a019c577bb86dcb1825168786920f`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d80844bd8d09281cd97dfa9eb3c27bfcc11f6d75075a34679079583f713a3e`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094db1411d9e829316fe3244a42b61e897ac4f7a74503b38e3986c182203a81b`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5047b989f83348dc2a430cfedfb4b39fd27c65e93611f89921d103816b60088b`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc5c9ac25523fc16256abc5c94d4823959b0fb7ede78e2514c61835ef69800c`  
		Last Modified: Thu, 20 Jun 2024 20:54:57 GMT  
		Size: 118.2 MB (118178555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0e97a0d4526f399153bec09432856e04a9e6f07ba3051fe5ff9b908d8d2d2e`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:7c2344c3bae4f1e4fad5034af7021dc529c11ddfadda0278539309f7a4d7c178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.4 KB (842392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76956d38981f86cf8210758ea9841ecc56d034ae5158a05031be483fa88e9c8d`

```dockerfile
```

-	Layers:
	-	`sha256:c702bcf4221f8fbd6297dd327d5cf6ad93cbbb555b84e1d85100381929e7c2fe`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 819.2 KB (819154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98dd9bc4991f245e3dec118ab7c6f4fb16ff9d29c7cd70857a688b43033414d`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 23.2 KB (23238 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2a8211bccb6126e149ba5aeb200db20d2ad46c78a721de248324a5ce03b36b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182587785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90293c2b1ef2b511383052fc6a7c40178f20f0f1e36b2cb61fa3aa2e99d237b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:31:00 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_VERSION=8.0.0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BRANDING_VERSION=2023.1-u0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:31:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:31:00 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Wed, 15 Nov 2023 09:31:00 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
VOLUME [/opt/bonita/conf/logs]
# Wed, 15 Nov 2023 09:31:00 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:31:00 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e320cbe6007b5dedf0233709bc723fc4607d7fb5f829d82217ef543560aad7d`  
		Last Modified: Fri, 21 Jun 2024 04:35:26 GMT  
		Size: 61.1 MB (61126346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ea9fedde8038622b8526a5b85c441eee7841116bf26f844b83aaa1191e0dac`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b98ef9a238cf22e841ad204f987bc47c777ceaeba1d4085aedd9f1f64e81b17`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b318a41794c5371b6347de93c0154b7412554272fd77e255e6ee344059655c6c`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a09814e50f5970faaccaec563fc7ad8a8fa081730c3fb0c036330f547e625f`  
		Last Modified: Fri, 21 Jun 2024 04:35:25 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ca2992916fc11509c644e39aff85ead2ffa066d6e010b72cbddea7c3ed0e60`  
		Last Modified: Fri, 21 Jun 2024 04:35:28 GMT  
		Size: 118.2 MB (118178556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52030788e32622ddd3dc4030114c6f8b20e704b7e4a8fe4468316df704be26c0`  
		Last Modified: Fri, 21 Jun 2024 04:35:25 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:18d57d0335b7cf4efc6b1d0c1a0c2185c513a3a83e4a12f0cb76c38da5f63407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.8 KB (841801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce984ed4e50cc3d40b698ae05ea0202fffe3a84696671fcec5de8b500d3e00cd`

```dockerfile
```

-	Layers:
	-	`sha256:fc37535d8ebd20459ee695a64294dc7772cac3b5c905412065ef14e4c7878594`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 818.3 KB (818263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44df43a6749e8edda5cffffe0330d940e84b12e602288fb07fd8904dcf351ba2`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 23.5 KB (23538 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:dcc8142308a098d4e62c718371c5392e8f71ac4c5cb59f62c7988b796c263aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179619841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8982389b6769fdac34527f358a750b30d6de4ce350d3f896d8daaf277a17bd94`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:80e24883ff1c790ff4b3d2b4488ea6cf7b9cbcf5432b00aba4c6043f5e4055c0 in / 
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:31:00 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_VERSION=8.0.0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BRANDING_VERSION=2023.1-u0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:31:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:31:00 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Wed, 15 Nov 2023 09:31:00 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
VOLUME [/opt/bonita/conf/logs]
# Wed, 15 Nov 2023 09:31:00 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:31:00 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f81397ca64cd321c51a90461a0c2f9fb32b00a52366a20f24075bb794eea71a2`  
		Last Modified: Thu, 20 Jun 2024 18:19:25 GMT  
		Size: 3.4 MB (3401809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210567cb03f3b32283f4642a983d2f70076991f82eae53e3c1a0275e8bf6baf6`  
		Last Modified: Fri, 21 Jun 2024 01:23:14 GMT  
		Size: 58.0 MB (58029183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1a7dd7c349b2370b225859ce8e0d63090bd54c459e7627279aff66761f42de`  
		Last Modified: Fri, 21 Jun 2024 01:23:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa42dbd8316045ef2401daa7e9b7366befa4482662398fc723f5a063acc97116`  
		Last Modified: Fri, 21 Jun 2024 01:23:12 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94a650ed84aae374b643fdca8f6b6df20ec8c7e4d11d6ff89180d8ed3170ce0`  
		Last Modified: Fri, 21 Jun 2024 01:23:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8155bde4dd4e7cdb6f5b917dd0f8709de6905c1226111f933e444813cb585ed`  
		Last Modified: Fri, 21 Jun 2024 01:23:13 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9045ca1a5493acc924cd5508a058b18ad545f9f83468b367a11e93fc312fe500`  
		Last Modified: Fri, 21 Jun 2024 01:23:17 GMT  
		Size: 118.2 MB (118178558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b9c66fc9f04f25705d2434b548de75fdf7874593d46be37ef6639764e04292`  
		Last Modified: Fri, 21 Jun 2024 01:23:14 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:e3bc97e68aa0147911f67835df159b2c4f067c77ae148f4cf381a07e3f1f5e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **839.6 KB (839612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c1bfd4085a43aafadf4dd06235fe47ebd479506f52b88d151e05226d43d556`

```dockerfile
```

-	Layers:
	-	`sha256:cef32d66324a634f4c9389ee0eee40a7d6cb7b83c0d1ffa323c72dc3b0c98b1e`  
		Last Modified: Fri, 21 Jun 2024 01:23:12 GMT  
		Size: 816.3 KB (816328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b04a689ddae65938b13cd16d310a1e8b114fb7b33449e9905cbf0dc4cd462e17`  
		Last Modified: Fri, 21 Jun 2024 01:23:12 GMT  
		Size: 23.3 KB (23284 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.2`

```console
$ docker pull bonita@sha256:f77cf6cf95850b802363581c2a390c83bdb3c06f391bf6f40ff683018e592454
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
$ docker pull bonita@sha256:cfafc89f4f8655735239ced8d569b71f05e4859d0a7f25930c1ca0afe1bca331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191504948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14632f7d69ca215136833045abccc81789c32547dd5369f5dff40ac86767bcb`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/bin/sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 16 Nov 2023 12:46:16 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BRANDING_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_SHA256
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BASE_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_VERSION=9.0.0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BRANDING_VERSION=2023.2-u0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
COPY files /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_PASSWORD=
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 16 Nov 2023 12:46:16 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 16 Nov 2023 12:46:16 GMT
COPY templates /opt/templates # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
VOLUME [/opt/bonita/conf/logs]
# Thu, 16 Nov 2023 12:46:16 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Thu, 16 Nov 2023 12:46:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edf3aff7655503316b5a3d27de022b8ac48b2fba2bad7cc769f68b5ab92cd8f`  
		Last Modified: Thu, 20 Jun 2024 20:54:58 GMT  
		Size: 67.9 MB (67906820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938ba79419d326f15d91444b8d7f502767a019c577bb86dcb1825168786920f`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02af2d7432ac7e3064a06cf121286bb620e72f6933e8dc6bd719d3d6d08361`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c57b81c81d5cd857c9e5f77738e6ad4a5d415808d06514cb3390c31b7d7e66`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161a6232ea5454614142c12d21f47f0b5878597927b9b2402d3ae2dc19ecf95f`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 3.6 KB (3621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6ee59c8134b30a102e94cf66b7431a76b72dc0a019455241530d62cfe55361`  
		Last Modified: Thu, 20 Jun 2024 20:54:59 GMT  
		Size: 120.2 MB (120173509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e705981acaa2e7c65f16d61c3d02dd1d7acd8b1506dc870e8320631e66873982`  
		Last Modified: Thu, 20 Jun 2024 20:54:56 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2` - unknown; unknown

```console
$ docker pull bonita@sha256:ea9cd92b1318d44bb5fb1f6d88cd9ec73ffaaaa8f13f72984e2a460f3614f0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1669914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dad4c1fab92b35923ad0afe16f88083372bd2ab1a7edeef888e125887aafe0b`

```dockerfile
```

-	Layers:
	-	`sha256:f1bf310b7bea83f154e65b01a2b7019ac30b889967679515ab390c236f9cecc7`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 1.6 MB (1646899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1087d9630f1315af984fc892fd8308edea8fdb8d5e5a6887964e5781a8ab036`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 23.0 KB (23015 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ad6960f37123c0538ed05bbe3f36d10998034edefbf98a09e68184ebba3d92da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191309040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ce96646115c63d60141c082ac915bd648341d67e1fd4aba7862ed1ec4053bc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/bin/sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 16 Nov 2023 12:46:16 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BRANDING_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_SHA256
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BASE_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_VERSION=9.0.0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BRANDING_VERSION=2023.2-u0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
COPY files /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_PASSWORD=
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 16 Nov 2023 12:46:16 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 16 Nov 2023 12:46:16 GMT
COPY templates /opt/templates # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
VOLUME [/opt/bonita/conf/logs]
# Thu, 16 Nov 2023 12:46:16 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Thu, 16 Nov 2023 12:46:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d66208e02de54624ca72d6357fe02b4ef5b57adfe46c10d4ada2b50c1994d`  
		Last Modified: Fri, 21 Jun 2024 04:36:10 GMT  
		Size: 67.8 MB (67786863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dc9c32d7820a287397c7e3461f8ddd6580a69519fc20812f3307736b3c59d6`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad67851d2ff9c33dd840e6fd8372fafd6ff597c963de7d59a57b9fd5736000ba`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd5e0cc73cb341c13e67803dd856f9a4f36dc573945d39ec56632de731ff65d`  
		Last Modified: Fri, 21 Jun 2024 04:36:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366b8f5db48cca3fdbcccb549e5245a72f44c7cd97879c5588b6792f05eadbeb`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 3.6 KB (3620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992af7ed68d9ece9daaf0acd2f30f07b95d6db872efca98b146bea5f67b306ab`  
		Last Modified: Fri, 21 Jun 2024 04:36:12 GMT  
		Size: 120.2 MB (120173507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0b72a4a51b8c7334db7df3c00cc380e94083cf809d6e9158bb2517c80c352a`  
		Last Modified: Fri, 21 Jun 2024 04:36:09 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2` - unknown; unknown

```console
$ docker pull bonita@sha256:9084bad2dd265d66e1f3a1da609691f425054b0b00123a837540e184d33cc91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1669376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861023f6c0a42f154b6918b930187e434f25df03ae60e6d4a5502c2a41a5aab9`

```dockerfile
```

-	Layers:
	-	`sha256:f02577bd4c6ef9093f4093b4d3c24215f954bc1216a65c30810586837de1a606`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 1.6 MB (1646048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3401512b9019aaa112d53dca527e4ed25c34cfc877826501089c484e3f71291`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:95d26a9359693148b468e0d6b21eb85502cbe57998f0de93fe9742c770e6789e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188177029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf400227ec7ef1a02fad802b358cc8cb1884f88eb05f91fc4ef97e288e79afe1`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:e0f257ed0b6b089b6a4fe2968065aa56ee04f7837fe7266dcd68be8d5242417b in / 
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/bin/sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 16 Nov 2023 12:46:16 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BRANDING_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_SHA256
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BASE_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_VERSION=9.0.0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BRANDING_VERSION=2023.2-u0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
COPY files /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_PASSWORD=
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 16 Nov 2023 12:46:16 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 16 Nov 2023 12:46:16 GMT
COPY templates /opt/templates # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
VOLUME [/opt/bonita/conf/logs]
# Thu, 16 Nov 2023 12:46:16 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Thu, 16 Nov 2023 12:46:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e3dd182a4c3296a9689fa043379c0a4ce2b865024ca7344a169d5d4759a52548`  
		Last Modified: Thu, 20 Jun 2024 18:19:16 GMT  
		Size: 3.4 MB (3357033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b8d6bcb67b4251182b5a25a8898185071bca1a3416e3ae7f82b63160702802`  
		Last Modified: Fri, 21 Jun 2024 01:24:39 GMT  
		Size: 64.6 MB (64635686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2401c0c0157a899c7f6efae6d42c1f7ea9ed7bfadb012acdc440bea1f01626e`  
		Last Modified: Fri, 21 Jun 2024 01:24:36 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8992554392ad6fe61a95d79803f89a21e9c1784aff1f68b7071d6eb54dcca8e`  
		Last Modified: Fri, 21 Jun 2024 01:24:36 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e2c509cae2e2c6c36cf5f8fede6096a705f1f5f23f44832961b0ff675f62b1`  
		Last Modified: Fri, 21 Jun 2024 01:24:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99dfd301f0a22b1867fe33b1226ede36e5363bcb0fc79b8ccf3375c5f64266`  
		Last Modified: Fri, 21 Jun 2024 01:24:37 GMT  
		Size: 3.6 KB (3620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cfd062320b3a5ed4871e2803459aecf4b65eb7966d8fbbda8a6a3c71ff2e65`  
		Last Modified: Fri, 21 Jun 2024 01:24:41 GMT  
		Size: 120.2 MB (120173588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9711be1a3b1cf19880d75f9dc5e1afc84eacd5356fe3b889e175c557b9356611`  
		Last Modified: Fri, 21 Jun 2024 01:24:38 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2` - unknown; unknown

```console
$ docker pull bonita@sha256:cefa5205449cf08d99e001d64fc0c62d8b2e7c7cc9d33b7d767c232add0bddde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1667134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1609a0e7e0f96392a4ca2db3afe595999baff2ca6a09f43a07dbd1763556919b`

```dockerfile
```

-	Layers:
	-	`sha256:493e414dd82430ed989337241ed1354b973cd5cd81a4b5dcea13387f6173e0ab`  
		Last Modified: Fri, 21 Jun 2024 01:24:37 GMT  
		Size: 1.6 MB (1644066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4dadb2e006eb3162ce0ac88bfce426857e8b63c3f0e81910373cd400bd5aa02`  
		Last Modified: Fri, 21 Jun 2024 01:24:36 GMT  
		Size: 23.1 KB (23068 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.2-u0`

```console
$ docker pull bonita@sha256:f77cf6cf95850b802363581c2a390c83bdb3c06f391bf6f40ff683018e592454
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
$ docker pull bonita@sha256:cfafc89f4f8655735239ced8d569b71f05e4859d0a7f25930c1ca0afe1bca331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191504948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14632f7d69ca215136833045abccc81789c32547dd5369f5dff40ac86767bcb`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/bin/sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 16 Nov 2023 12:46:16 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BRANDING_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_SHA256
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BASE_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_VERSION=9.0.0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BRANDING_VERSION=2023.2-u0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
COPY files /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_PASSWORD=
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 16 Nov 2023 12:46:16 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 16 Nov 2023 12:46:16 GMT
COPY templates /opt/templates # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
VOLUME [/opt/bonita/conf/logs]
# Thu, 16 Nov 2023 12:46:16 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Thu, 16 Nov 2023 12:46:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edf3aff7655503316b5a3d27de022b8ac48b2fba2bad7cc769f68b5ab92cd8f`  
		Last Modified: Thu, 20 Jun 2024 20:54:58 GMT  
		Size: 67.9 MB (67906820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938ba79419d326f15d91444b8d7f502767a019c577bb86dcb1825168786920f`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02af2d7432ac7e3064a06cf121286bb620e72f6933e8dc6bd719d3d6d08361`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c57b81c81d5cd857c9e5f77738e6ad4a5d415808d06514cb3390c31b7d7e66`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161a6232ea5454614142c12d21f47f0b5878597927b9b2402d3ae2dc19ecf95f`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 3.6 KB (3621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6ee59c8134b30a102e94cf66b7431a76b72dc0a019455241530d62cfe55361`  
		Last Modified: Thu, 20 Jun 2024 20:54:59 GMT  
		Size: 120.2 MB (120173509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e705981acaa2e7c65f16d61c3d02dd1d7acd8b1506dc870e8320631e66873982`  
		Last Modified: Thu, 20 Jun 2024 20:54:56 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:ea9cd92b1318d44bb5fb1f6d88cd9ec73ffaaaa8f13f72984e2a460f3614f0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1669914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dad4c1fab92b35923ad0afe16f88083372bd2ab1a7edeef888e125887aafe0b`

```dockerfile
```

-	Layers:
	-	`sha256:f1bf310b7bea83f154e65b01a2b7019ac30b889967679515ab390c236f9cecc7`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 1.6 MB (1646899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1087d9630f1315af984fc892fd8308edea8fdb8d5e5a6887964e5781a8ab036`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 23.0 KB (23015 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ad6960f37123c0538ed05bbe3f36d10998034edefbf98a09e68184ebba3d92da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191309040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ce96646115c63d60141c082ac915bd648341d67e1fd4aba7862ed1ec4053bc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/bin/sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 16 Nov 2023 12:46:16 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BRANDING_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_SHA256
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BASE_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_VERSION=9.0.0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BRANDING_VERSION=2023.2-u0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
COPY files /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_PASSWORD=
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 16 Nov 2023 12:46:16 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 16 Nov 2023 12:46:16 GMT
COPY templates /opt/templates # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
VOLUME [/opt/bonita/conf/logs]
# Thu, 16 Nov 2023 12:46:16 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Thu, 16 Nov 2023 12:46:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d66208e02de54624ca72d6357fe02b4ef5b57adfe46c10d4ada2b50c1994d`  
		Last Modified: Fri, 21 Jun 2024 04:36:10 GMT  
		Size: 67.8 MB (67786863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dc9c32d7820a287397c7e3461f8ddd6580a69519fc20812f3307736b3c59d6`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad67851d2ff9c33dd840e6fd8372fafd6ff597c963de7d59a57b9fd5736000ba`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd5e0cc73cb341c13e67803dd856f9a4f36dc573945d39ec56632de731ff65d`  
		Last Modified: Fri, 21 Jun 2024 04:36:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366b8f5db48cca3fdbcccb549e5245a72f44c7cd97879c5588b6792f05eadbeb`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 3.6 KB (3620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992af7ed68d9ece9daaf0acd2f30f07b95d6db872efca98b146bea5f67b306ab`  
		Last Modified: Fri, 21 Jun 2024 04:36:12 GMT  
		Size: 120.2 MB (120173507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0b72a4a51b8c7334db7df3c00cc380e94083cf809d6e9158bb2517c80c352a`  
		Last Modified: Fri, 21 Jun 2024 04:36:09 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:9084bad2dd265d66e1f3a1da609691f425054b0b00123a837540e184d33cc91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1669376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861023f6c0a42f154b6918b930187e434f25df03ae60e6d4a5502c2a41a5aab9`

```dockerfile
```

-	Layers:
	-	`sha256:f02577bd4c6ef9093f4093b4d3c24215f954bc1216a65c30810586837de1a606`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 1.6 MB (1646048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3401512b9019aaa112d53dca527e4ed25c34cfc877826501089c484e3f71291`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:95d26a9359693148b468e0d6b21eb85502cbe57998f0de93fe9742c770e6789e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188177029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf400227ec7ef1a02fad802b358cc8cb1884f88eb05f91fc4ef97e288e79afe1`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:e0f257ed0b6b089b6a4fe2968065aa56ee04f7837fe7266dcd68be8d5242417b in / 
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/bin/sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 16 Nov 2023 12:46:16 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BRANDING_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_SHA256
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BASE_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_VERSION=9.0.0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BRANDING_VERSION=2023.2-u0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
COPY files /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_PASSWORD=
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 16 Nov 2023 12:46:16 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 16 Nov 2023 12:46:16 GMT
COPY templates /opt/templates # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
VOLUME [/opt/bonita/conf/logs]
# Thu, 16 Nov 2023 12:46:16 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Thu, 16 Nov 2023 12:46:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e3dd182a4c3296a9689fa043379c0a4ce2b865024ca7344a169d5d4759a52548`  
		Last Modified: Thu, 20 Jun 2024 18:19:16 GMT  
		Size: 3.4 MB (3357033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b8d6bcb67b4251182b5a25a8898185071bca1a3416e3ae7f82b63160702802`  
		Last Modified: Fri, 21 Jun 2024 01:24:39 GMT  
		Size: 64.6 MB (64635686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2401c0c0157a899c7f6efae6d42c1f7ea9ed7bfadb012acdc440bea1f01626e`  
		Last Modified: Fri, 21 Jun 2024 01:24:36 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8992554392ad6fe61a95d79803f89a21e9c1784aff1f68b7071d6eb54dcca8e`  
		Last Modified: Fri, 21 Jun 2024 01:24:36 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e2c509cae2e2c6c36cf5f8fede6096a705f1f5f23f44832961b0ff675f62b1`  
		Last Modified: Fri, 21 Jun 2024 01:24:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99dfd301f0a22b1867fe33b1226ede36e5363bcb0fc79b8ccf3375c5f64266`  
		Last Modified: Fri, 21 Jun 2024 01:24:37 GMT  
		Size: 3.6 KB (3620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cfd062320b3a5ed4871e2803459aecf4b65eb7966d8fbbda8a6a3c71ff2e65`  
		Last Modified: Fri, 21 Jun 2024 01:24:41 GMT  
		Size: 120.2 MB (120173588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9711be1a3b1cf19880d75f9dc5e1afc84eacd5356fe3b889e175c557b9356611`  
		Last Modified: Fri, 21 Jun 2024 01:24:38 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:cefa5205449cf08d99e001d64fc0c62d8b2e7c7cc9d33b7d767c232add0bddde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1667134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1609a0e7e0f96392a4ca2db3afe595999baff2ca6a09f43a07dbd1763556919b`

```dockerfile
```

-	Layers:
	-	`sha256:493e414dd82430ed989337241ed1354b973cd5cd81a4b5dcea13387f6173e0ab`  
		Last Modified: Fri, 21 Jun 2024 01:24:37 GMT  
		Size: 1.6 MB (1644066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4dadb2e006eb3162ce0ac88bfce426857e8b63c3f0e81910373cd400bd5aa02`  
		Last Modified: Fri, 21 Jun 2024 01:24:36 GMT  
		Size: 23.1 KB (23068 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:7.14`

```console
$ docker pull bonita@sha256:1afdec31ca6a55879505a7cd66aae8e97652a46690231b394b39bed816bd57dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bonita:7.14` - linux; amd64

```console
$ docker pull bonita@sha256:1a863c00f1d403b007e7e0e28df98cda855248cfef46b88688f571af87e27bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177052561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f166962921d07ad36985476b2b4a5c34d738646fdeee0241a97c58f4a80b44ea`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:59:18 GMT
ADD file:aa1af71c6b66d2dddee4797236e3e526f70f904ab641cc0dd6b41445cfedf9b4 in / 
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:59:18 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:59:18 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:59:18 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:59:18 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d078792c4f9122259f14b539315bd92cbd9490ed73e08255a08689122b143108`  
		Last Modified: Thu, 30 Nov 2023 23:23:58 GMT  
		Size: 2.8 MB (2826431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2850d502a838ba6c0b82d0b4418251ec5b73d7b6f34a41e068e1846a0d56ec15`  
		Last Modified: Thu, 30 May 2024 21:01:09 GMT  
		Size: 57.5 MB (57528345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0368b2e11d73d30a1719d88c08577a5769ad232b1a80e9e4953dbbafd5750527`  
		Last Modified: Thu, 30 May 2024 21:01:08 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1280aa1681af4413bf5897033d603717af6387c82a3590ebf3adfdc4e571de4`  
		Last Modified: Thu, 30 May 2024 21:01:08 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0133e2bf0ec8e0571228a78ce463d850ab1d1074984910bea0d19c00ed071a1`  
		Last Modified: Thu, 30 May 2024 21:01:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d916f80dafb2dca2d366c95c6373e977e74d52bef852742f9355e5b2f161ca`  
		Last Modified: Thu, 30 May 2024 21:01:09 GMT  
		Size: 3.0 KB (2992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a484f13af52fd6d101199d7112d1e44cd884b9fdc3f9b47aa48dd482bbfb78c`  
		Last Modified: Thu, 30 May 2024 21:01:11 GMT  
		Size: 116.7 MB (116687932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3b032ee0e7eafb05ffb6dcf308c04068996b47c7606bc8d075fe951fe10126`  
		Last Modified: Thu, 30 May 2024 21:01:09 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.14` - unknown; unknown

```console
$ docker pull bonita@sha256:e98f36524f181cc0c4f726eaf021c32b779d0774d1109312aa1d9215bbb5eba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.8 KB (621846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c21444c0a2122ba43fb28ed2a9881f7ecd6799fcea38c4c0dcf397eb249874b`

```dockerfile
```

-	Layers:
	-	`sha256:5e55962fd89e2c8bd1652c996fcc0bfe489da3135550cc6d770d0aca8c695061`  
		Last Modified: Thu, 30 May 2024 21:01:08 GMT  
		Size: 598.8 KB (598806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6670d5cd71b8a4ed15896b1392c2371b4beca3edcdeca22f270c89d50be22cb9`  
		Last Modified: Thu, 30 May 2024 21:01:08 GMT  
		Size: 23.0 KB (23040 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.14` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:b213041262a0970b880265347e6fce91d47e062bb45d3bf76295cf06b672de62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176270879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87186d8e14d4b205d9acd6f51a170db1460ed015a528507b8032876ff5fa1dfc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:59:18 GMT
ADD file:3982c510455cc0ceea8cf8dd0b50b69588e35fd4f84522cb4000582c73781672 in / 
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:59:18 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:59:18 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:59:18 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:59:18 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8bc1ab4b84041d57f21a792410a00820f73fda7efe08bcd2ca6245349a40299d`  
		Last Modified: Thu, 30 Nov 2023 23:12:02 GMT  
		Size: 2.7 MB (2721527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aef56ab86690ac9887c2884a0572f63ae54a4171beec97df76001874e1d938d`  
		Last Modified: Thu, 30 May 2024 22:45:20 GMT  
		Size: 56.9 MB (56851579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085dc8607af603cbda94196b45ddb7c0275334820c0246e04215e26e20802c4a`  
		Last Modified: Thu, 30 May 2024 22:45:17 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19fb80c67b80100fe22f7b08bfa74ad1b9070a32be301586ef2d727f9a50590`  
		Last Modified: Thu, 30 May 2024 22:45:17 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5b93a2662730914ae0ba7bf45f9a08fad198917faababcf5a1bd78f196288d`  
		Last Modified: Thu, 30 May 2024 22:45:18 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca20a4be91429ccf555ce1a52caf1c6f9444646d749449f6963c3a4c3970ee64`  
		Last Modified: Thu, 30 May 2024 22:45:18 GMT  
		Size: 3.0 KB (2988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f916901979ad5a2b355b3afb591759ef88100ad8fb9f2f9e4347222f6f9b14f`  
		Last Modified: Thu, 30 May 2024 22:45:25 GMT  
		Size: 116.7 MB (116687925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27675cdc16497debd66665daeef9344942b15c78e3cc3d401d93846094b91822`  
		Last Modified: Thu, 30 May 2024 22:45:19 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.14` - unknown; unknown

```console
$ docker pull bonita@sha256:df3af0ee9fe8ebfb9b344afb2eb0bd2c1aa19818cf817bd5b44cb9fd65e45b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.2 KB (621206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1630478d103b7072845192c91eb0d8a72bfd6fc7b4c6da3172e8efe5f5b00f54`

```dockerfile
```

-	Layers:
	-	`sha256:80866d2b60a761f8e0a20e282203cf2ad5758fe3978da1a72fd10aa29e60ad10`  
		Last Modified: Thu, 30 May 2024 22:45:18 GMT  
		Size: 597.9 KB (597866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef83d34f3540676c1ba9b5a0fe3100b746dd6ae139453adef199e02fd8aa5d8`  
		Last Modified: Thu, 30 May 2024 22:45:18 GMT  
		Size: 23.3 KB (23340 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.14` - linux; ppc64le

```console
$ docker pull bonita@sha256:9e3a07a3365454dd742276176419251d2d96e5414f714174ee9b2a312c58881c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172866651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fe72c2160957b5c85293963318fd0681a8dc926bbec27139bbe023ef02e714`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:59:18 GMT
ADD file:35af09f43b08c93abd4c6b8679d43e8ac40893bf5932c4c21f1bb037f53bb62c in / 
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:59:18 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:59:18 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:59:18 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:59:18 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:080a2fea3a772fa995cb0b07b4601e7cd57650fa4e8a50866da1de707946d7b3`  
		Last Modified: Thu, 30 Nov 2023 23:20:38 GMT  
		Size: 2.8 MB (2812474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33c924802356b5e3d2e0d9d806dedfecf7cef7d8dd3eb869241e75b101f2026`  
		Last Modified: Thu, 30 May 2024 21:12:56 GMT  
		Size: 53.4 MB (53356415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69ddad3fc11d89779028d23f3fba05be63652828d1528069dff627ac678871e`  
		Last Modified: Thu, 30 May 2024 21:12:55 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aebbc847f70a92e9eb9252d917e3bd170ef1dbfcd47d9292fd2323e0e5c06d9`  
		Last Modified: Thu, 30 May 2024 21:12:54 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de5cd1d8cb72333a1d8ac61553b10fdd6f903de1fc544d3b767190b2fe248e9`  
		Last Modified: Thu, 30 May 2024 21:12:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee9ea34acfc5886a1ed11519581d81bd5bb1360a8e4dff3dd6bc4f7b66a4d84`  
		Last Modified: Thu, 30 May 2024 21:12:56 GMT  
		Size: 3.0 KB (2991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cc215ab03fbcf0b693cb48846ebc8b33ef364ae69fa3881b1291de2cc2dbf7`  
		Last Modified: Thu, 30 May 2024 21:12:59 GMT  
		Size: 116.7 MB (116687908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18674db949efb66ab61a5ce9b43debd5d86f25992b160b46e88c15076673739c`  
		Last Modified: Thu, 30 May 2024 21:12:57 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.14` - unknown; unknown

```console
$ docker pull bonita@sha256:eec4da703381341df05010a04afb3e20aa14300639b245b330b0af2577530f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.0 KB (618980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac67ac283fdf263f29b3332970fcd30cc8184646516ff533550b2748dcb3a58f`

```dockerfile
```

-	Layers:
	-	`sha256:711c8bf82b03025366753b692200e0b18dbb209a95ba1a3d64da63bdd53e5d42`  
		Last Modified: Thu, 30 May 2024 21:12:55 GMT  
		Size: 595.9 KB (595894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5c977c3112c94d455be931a33bf804f0e1ede48ef3e8a89e7d608fa137a88a8`  
		Last Modified: Thu, 30 May 2024 21:12:54 GMT  
		Size: 23.1 KB (23086 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:7.14.0`

```console
$ docker pull bonita@sha256:1afdec31ca6a55879505a7cd66aae8e97652a46690231b394b39bed816bd57dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bonita:7.14.0` - linux; amd64

```console
$ docker pull bonita@sha256:1a863c00f1d403b007e7e0e28df98cda855248cfef46b88688f571af87e27bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177052561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f166962921d07ad36985476b2b4a5c34d738646fdeee0241a97c58f4a80b44ea`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:59:18 GMT
ADD file:aa1af71c6b66d2dddee4797236e3e526f70f904ab641cc0dd6b41445cfedf9b4 in / 
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:59:18 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:59:18 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:59:18 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:59:18 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d078792c4f9122259f14b539315bd92cbd9490ed73e08255a08689122b143108`  
		Last Modified: Thu, 30 Nov 2023 23:23:58 GMT  
		Size: 2.8 MB (2826431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2850d502a838ba6c0b82d0b4418251ec5b73d7b6f34a41e068e1846a0d56ec15`  
		Last Modified: Thu, 30 May 2024 21:01:09 GMT  
		Size: 57.5 MB (57528345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0368b2e11d73d30a1719d88c08577a5769ad232b1a80e9e4953dbbafd5750527`  
		Last Modified: Thu, 30 May 2024 21:01:08 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1280aa1681af4413bf5897033d603717af6387c82a3590ebf3adfdc4e571de4`  
		Last Modified: Thu, 30 May 2024 21:01:08 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0133e2bf0ec8e0571228a78ce463d850ab1d1074984910bea0d19c00ed071a1`  
		Last Modified: Thu, 30 May 2024 21:01:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d916f80dafb2dca2d366c95c6373e977e74d52bef852742f9355e5b2f161ca`  
		Last Modified: Thu, 30 May 2024 21:01:09 GMT  
		Size: 3.0 KB (2992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a484f13af52fd6d101199d7112d1e44cd884b9fdc3f9b47aa48dd482bbfb78c`  
		Last Modified: Thu, 30 May 2024 21:01:11 GMT  
		Size: 116.7 MB (116687932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3b032ee0e7eafb05ffb6dcf308c04068996b47c7606bc8d075fe951fe10126`  
		Last Modified: Thu, 30 May 2024 21:01:09 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.14.0` - unknown; unknown

```console
$ docker pull bonita@sha256:e98f36524f181cc0c4f726eaf021c32b779d0774d1109312aa1d9215bbb5eba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.8 KB (621846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c21444c0a2122ba43fb28ed2a9881f7ecd6799fcea38c4c0dcf397eb249874b`

```dockerfile
```

-	Layers:
	-	`sha256:5e55962fd89e2c8bd1652c996fcc0bfe489da3135550cc6d770d0aca8c695061`  
		Last Modified: Thu, 30 May 2024 21:01:08 GMT  
		Size: 598.8 KB (598806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6670d5cd71b8a4ed15896b1392c2371b4beca3edcdeca22f270c89d50be22cb9`  
		Last Modified: Thu, 30 May 2024 21:01:08 GMT  
		Size: 23.0 KB (23040 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.14.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:b213041262a0970b880265347e6fce91d47e062bb45d3bf76295cf06b672de62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176270879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87186d8e14d4b205d9acd6f51a170db1460ed015a528507b8032876ff5fa1dfc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:59:18 GMT
ADD file:3982c510455cc0ceea8cf8dd0b50b69588e35fd4f84522cb4000582c73781672 in / 
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:59:18 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:59:18 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:59:18 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:59:18 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8bc1ab4b84041d57f21a792410a00820f73fda7efe08bcd2ca6245349a40299d`  
		Last Modified: Thu, 30 Nov 2023 23:12:02 GMT  
		Size: 2.7 MB (2721527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aef56ab86690ac9887c2884a0572f63ae54a4171beec97df76001874e1d938d`  
		Last Modified: Thu, 30 May 2024 22:45:20 GMT  
		Size: 56.9 MB (56851579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085dc8607af603cbda94196b45ddb7c0275334820c0246e04215e26e20802c4a`  
		Last Modified: Thu, 30 May 2024 22:45:17 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19fb80c67b80100fe22f7b08bfa74ad1b9070a32be301586ef2d727f9a50590`  
		Last Modified: Thu, 30 May 2024 22:45:17 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5b93a2662730914ae0ba7bf45f9a08fad198917faababcf5a1bd78f196288d`  
		Last Modified: Thu, 30 May 2024 22:45:18 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca20a4be91429ccf555ce1a52caf1c6f9444646d749449f6963c3a4c3970ee64`  
		Last Modified: Thu, 30 May 2024 22:45:18 GMT  
		Size: 3.0 KB (2988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f916901979ad5a2b355b3afb591759ef88100ad8fb9f2f9e4347222f6f9b14f`  
		Last Modified: Thu, 30 May 2024 22:45:25 GMT  
		Size: 116.7 MB (116687925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27675cdc16497debd66665daeef9344942b15c78e3cc3d401d93846094b91822`  
		Last Modified: Thu, 30 May 2024 22:45:19 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.14.0` - unknown; unknown

```console
$ docker pull bonita@sha256:df3af0ee9fe8ebfb9b344afb2eb0bd2c1aa19818cf817bd5b44cb9fd65e45b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.2 KB (621206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1630478d103b7072845192c91eb0d8a72bfd6fc7b4c6da3172e8efe5f5b00f54`

```dockerfile
```

-	Layers:
	-	`sha256:80866d2b60a761f8e0a20e282203cf2ad5758fe3978da1a72fd10aa29e60ad10`  
		Last Modified: Thu, 30 May 2024 22:45:18 GMT  
		Size: 597.9 KB (597866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef83d34f3540676c1ba9b5a0fe3100b746dd6ae139453adef199e02fd8aa5d8`  
		Last Modified: Thu, 30 May 2024 22:45:18 GMT  
		Size: 23.3 KB (23340 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.14.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:9e3a07a3365454dd742276176419251d2d96e5414f714174ee9b2a312c58881c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172866651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fe72c2160957b5c85293963318fd0681a8dc926bbec27139bbe023ef02e714`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:59:18 GMT
ADD file:35af09f43b08c93abd4c6b8679d43e8ac40893bf5932c4c21f1bb037f53bb62c in / 
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:59:18 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:59:18 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
# ARGS: BONITA_VERSION=7.14.0 BRANDING_VERSION=2022.1-u0 BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:59:18 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:59:18 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:59:18 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:59:18 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:59:18 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:59:18 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:59:18 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:59:18 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:080a2fea3a772fa995cb0b07b4601e7cd57650fa4e8a50866da1de707946d7b3`  
		Last Modified: Thu, 30 Nov 2023 23:20:38 GMT  
		Size: 2.8 MB (2812474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33c924802356b5e3d2e0d9d806dedfecf7cef7d8dd3eb869241e75b101f2026`  
		Last Modified: Thu, 30 May 2024 21:12:56 GMT  
		Size: 53.4 MB (53356415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69ddad3fc11d89779028d23f3fba05be63652828d1528069dff627ac678871e`  
		Last Modified: Thu, 30 May 2024 21:12:55 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aebbc847f70a92e9eb9252d917e3bd170ef1dbfcd47d9292fd2323e0e5c06d9`  
		Last Modified: Thu, 30 May 2024 21:12:54 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de5cd1d8cb72333a1d8ac61553b10fdd6f903de1fc544d3b767190b2fe248e9`  
		Last Modified: Thu, 30 May 2024 21:12:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee9ea34acfc5886a1ed11519581d81bd5bb1360a8e4dff3dd6bc4f7b66a4d84`  
		Last Modified: Thu, 30 May 2024 21:12:56 GMT  
		Size: 3.0 KB (2991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cc215ab03fbcf0b693cb48846ebc8b33ef364ae69fa3881b1291de2cc2dbf7`  
		Last Modified: Thu, 30 May 2024 21:12:59 GMT  
		Size: 116.7 MB (116687908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18674db949efb66ab61a5ce9b43debd5d86f25992b160b46e88c15076673739c`  
		Last Modified: Thu, 30 May 2024 21:12:57 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.14.0` - unknown; unknown

```console
$ docker pull bonita@sha256:eec4da703381341df05010a04afb3e20aa14300639b245b330b0af2577530f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.0 KB (618980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac67ac283fdf263f29b3332970fcd30cc8184646516ff533550b2748dcb3a58f`

```dockerfile
```

-	Layers:
	-	`sha256:711c8bf82b03025366753b692200e0b18dbb209a95ba1a3d64da63bdd53e5d42`  
		Last Modified: Thu, 30 May 2024 21:12:55 GMT  
		Size: 595.9 KB (595894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5c977c3112c94d455be931a33bf804f0e1ede48ef3e8a89e7d608fa137a88a8`  
		Last Modified: Thu, 30 May 2024 21:12:54 GMT  
		Size: 23.1 KB (23086 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:7.15`

```console
$ docker pull bonita@sha256:5e79922cae414f2075d3cd98d4582d891a8c6eceab30b14b565d5e36434de45a
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
$ docker pull bonita@sha256:68b05aed88ef5c6c2afc65634b66599b99ef568801cac4ced905891add7ab0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183647748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4789c9604df70fa15d30e7f8ffbd9be70bc36cae45eb4caa2c8a236a49738ec`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:34:20 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:34:20 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_VERSION=7.15.0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BRANDING_VERSION=2022.2-u0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:34:20 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:34:20 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:34:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6702ed64834ed89f10c7ffaec872f8f5765de3235860148f12547cab2771c1d`  
		Last Modified: Thu, 30 May 2024 20:56:14 GMT  
		Size: 61.6 MB (61639298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b877c9ca382d7a2a9bbe48cb38590ee9b845354c1c027136defc025939a9b5c5`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b7a3b54e51d13fc173d43051341b1a99bb0466f758760291a70a21913c0e9e`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7180ba389779c576a63f8337f70c8ccb9f9183a29381261d6c5e0fdaa3f27a5e`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1100d2b7215d90ac2720b6761cbffcec112b9011c7524bb054209c6234ada209`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 3.0 KB (3003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99aae4a5291464a5844092748ad5630de4b9441dfc1ef3d25d70e745d3e3d99d`  
		Last Modified: Thu, 30 May 2024 20:56:16 GMT  
		Size: 119.2 MB (119190749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea18f123da6c9dbc056c9a79bfdedd5d26ca99a512689c87331e625d4b24029`  
		Last Modified: Thu, 30 May 2024 20:56:14 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15` - unknown; unknown

```console
$ docker pull bonita@sha256:ee97d17ff60c40ee97102546b7540ca7df7f77bbe4990efbd6f176951d56178a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.7 KB (843663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47502f3ae25dfae664f0abd59ace922765a6a96c65d0be5b336be50d7103cdb`

```dockerfile
```

-	Layers:
	-	`sha256:35fadb308cc14fac57123855c2bda2397f5ed1579951d69a202f2af4200c681e`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 820.6 KB (820644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1120c1721090eeac0d7a8648d52b033868d3ff5ac014cbc8c426441c1496e115`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 23.0 KB (23019 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.15` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:031eed17b81f05b9a751d4eb5de470c6f9816273bebd6968c254b1484c5d19f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182795104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27f5f7cfdb4d20f5bdefad7e5a798f6522bed0c90c2f14ee33430464441a4e5`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:34:20 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:34:20 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_VERSION=7.15.0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BRANDING_VERSION=2022.2-u0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:34:20 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:34:20 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:34:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9c413225ca7157a35f4580c54257db05570e292e99b9736cc3c4eef92890fc`  
		Last Modified: Thu, 30 May 2024 22:46:05 GMT  
		Size: 60.9 MB (60886274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8c5c2285121d4b0d57cf25e56d491dbd4a9028176e172d4d159ac57b2f8458`  
		Last Modified: Thu, 30 May 2024 22:46:02 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50994a35a8b227436180382bb0cafc50892b5bec29303b0564ea297b483b2848`  
		Last Modified: Thu, 30 May 2024 22:46:02 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fa5f03f6e8de9741cf728899e8639690cd97f1963245007e93020edf086350`  
		Last Modified: Thu, 30 May 2024 22:46:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e32a8d97e7f940e76e97b18729de5e3853b81f1e6e4d3fe72650de8f741bd2`  
		Last Modified: Thu, 30 May 2024 22:46:03 GMT  
		Size: 3.0 KB (3002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840c886a647e4761c865de41fdecf28aabdf392be2558d7588f4a132cf61caa3`  
		Last Modified: Thu, 30 May 2024 22:46:06 GMT  
		Size: 119.2 MB (119190681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c21e19f38f949440557d9eb970e85705fa9454b90b4444e4374a1a16a218797`  
		Last Modified: Thu, 30 May 2024 22:46:04 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15` - unknown; unknown

```console
$ docker pull bonita@sha256:b84756ab16037ed0d50238658f65923d8d825fbf955cbdd5a21ecd6ea48149c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.1 KB (843063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60471a4c0fc256e9b631b10770c84f34d1c797f6f5e75615e6b25006b4ed79f2`

```dockerfile
```

-	Layers:
	-	`sha256:90d6b129f43c5e6ff4cf07592e39064c69f522ee1ed1acfce8bf4b9f44e6c0f1`  
		Last Modified: Thu, 30 May 2024 22:46:03 GMT  
		Size: 819.7 KB (819744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d3c1ae4d6ad3bedbc5d25c34de1fb34bf1c682a64ed917713ee479f9de2232e`  
		Last Modified: Thu, 30 May 2024 22:46:02 GMT  
		Size: 23.3 KB (23319 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.15` - linux; ppc64le

```console
$ docker pull bonita@sha256:9eb34c2150166972653b8dba12b89e9636dcc6da156b6929f0d7ab33d86ef655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179819681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b718d3559a26fb41d30f7cc907dba806e3f828e5b122d5c12860a18b4a15c2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:34:20 GMT
ADD file:cf4fecc20d85962cd46b6911d8ee82b9a3de2fa530bc58e998c2d544a888fdb9 in / 
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:34:20 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_VERSION=7.15.0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BRANDING_VERSION=2022.2-u0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:34:20 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:34:20 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:34:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:04646341bdb047ee1a3dd65db76069b9117954385033f5a340622fd170fa4b73`  
		Last Modified: Sat, 27 Jan 2024 00:28:46 GMT  
		Size: 2.8 MB (2802980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3169e99f3c3d30c82bce3b7fe8f4a643505e25691c0a3a8ea8daf01d4170a4b`  
		Last Modified: Thu, 30 May 2024 21:17:50 GMT  
		Size: 57.8 MB (57816142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a736beb4906376ce95524b776b66c7806e73f0558c594e28a931275f5efb1dfb`  
		Last Modified: Thu, 30 May 2024 21:17:47 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d7adbafe038499090091dd1243f6a053200f23d6e3db2243b369b9744c0009`  
		Last Modified: Thu, 30 May 2024 21:17:47 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4d5bde7cb90faccf971340b6ded0d3f8347c8c99b06593b9ac592ab80a53d3`  
		Last Modified: Thu, 30 May 2024 21:17:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c1c212f47019afda5d60f95f7ca3619dc58be9e73328321a4a07bf4af5e86c`  
		Last Modified: Thu, 30 May 2024 21:17:48 GMT  
		Size: 3.0 KB (3003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7556ecb8b489313ffd345e92e529dde59ae002a7f37cf50ac29e3f3882eb2e76`  
		Last Modified: Thu, 30 May 2024 21:17:52 GMT  
		Size: 119.2 MB (119190690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13dc87b637dcf22284ad9b9b1d17886ef0ea0a4c8e5dd743b1a325066c7c02e6`  
		Last Modified: Thu, 30 May 2024 21:17:48 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15` - unknown; unknown

```console
$ docker pull bonita@sha256:dbc429945850eeaea750e1080411ad264da2f86b7998a9be3a35b617c28cc4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8888a15d46bc3f610c29846bcdabbc10da3e2217d50b7559803a101b7eeb407`

```dockerfile
```

-	Layers:
	-	`sha256:69c6ec711a31ac4bae45f279d8816b71769961acbb70aec3f2c259938ee1be28`  
		Last Modified: Thu, 30 May 2024 21:17:48 GMT  
		Size: 817.7 KB (817723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e326df99f8c53edf340fc078fd1cd58591005a8f8a6509335db80fed3b38404`  
		Last Modified: Thu, 30 May 2024 21:17:47 GMT  
		Size: 23.1 KB (23065 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:7.15.0`

```console
$ docker pull bonita@sha256:5e79922cae414f2075d3cd98d4582d891a8c6eceab30b14b565d5e36434de45a
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
$ docker pull bonita@sha256:68b05aed88ef5c6c2afc65634b66599b99ef568801cac4ced905891add7ab0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183647748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4789c9604df70fa15d30e7f8ffbd9be70bc36cae45eb4caa2c8a236a49738ec`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:34:20 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:34:20 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_VERSION=7.15.0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BRANDING_VERSION=2022.2-u0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:34:20 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:34:20 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:34:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6702ed64834ed89f10c7ffaec872f8f5765de3235860148f12547cab2771c1d`  
		Last Modified: Thu, 30 May 2024 20:56:14 GMT  
		Size: 61.6 MB (61639298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b877c9ca382d7a2a9bbe48cb38590ee9b845354c1c027136defc025939a9b5c5`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b7a3b54e51d13fc173d43051341b1a99bb0466f758760291a70a21913c0e9e`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7180ba389779c576a63f8337f70c8ccb9f9183a29381261d6c5e0fdaa3f27a5e`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1100d2b7215d90ac2720b6761cbffcec112b9011c7524bb054209c6234ada209`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 3.0 KB (3003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99aae4a5291464a5844092748ad5630de4b9441dfc1ef3d25d70e745d3e3d99d`  
		Last Modified: Thu, 30 May 2024 20:56:16 GMT  
		Size: 119.2 MB (119190749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea18f123da6c9dbc056c9a79bfdedd5d26ca99a512689c87331e625d4b24029`  
		Last Modified: Thu, 30 May 2024 20:56:14 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15.0` - unknown; unknown

```console
$ docker pull bonita@sha256:ee97d17ff60c40ee97102546b7540ca7df7f77bbe4990efbd6f176951d56178a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.7 KB (843663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47502f3ae25dfae664f0abd59ace922765a6a96c65d0be5b336be50d7103cdb`

```dockerfile
```

-	Layers:
	-	`sha256:35fadb308cc14fac57123855c2bda2397f5ed1579951d69a202f2af4200c681e`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 820.6 KB (820644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1120c1721090eeac0d7a8648d52b033868d3ff5ac014cbc8c426441c1496e115`  
		Last Modified: Thu, 30 May 2024 20:56:13 GMT  
		Size: 23.0 KB (23019 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.15.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:031eed17b81f05b9a751d4eb5de470c6f9816273bebd6968c254b1484c5d19f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182795104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27f5f7cfdb4d20f5bdefad7e5a798f6522bed0c90c2f14ee33430464441a4e5`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:34:20 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:34:20 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_VERSION=7.15.0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BRANDING_VERSION=2022.2-u0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:34:20 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:34:20 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:34:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9c413225ca7157a35f4580c54257db05570e292e99b9736cc3c4eef92890fc`  
		Last Modified: Thu, 30 May 2024 22:46:05 GMT  
		Size: 60.9 MB (60886274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8c5c2285121d4b0d57cf25e56d491dbd4a9028176e172d4d159ac57b2f8458`  
		Last Modified: Thu, 30 May 2024 22:46:02 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50994a35a8b227436180382bb0cafc50892b5bec29303b0564ea297b483b2848`  
		Last Modified: Thu, 30 May 2024 22:46:02 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fa5f03f6e8de9741cf728899e8639690cd97f1963245007e93020edf086350`  
		Last Modified: Thu, 30 May 2024 22:46:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e32a8d97e7f940e76e97b18729de5e3853b81f1e6e4d3fe72650de8f741bd2`  
		Last Modified: Thu, 30 May 2024 22:46:03 GMT  
		Size: 3.0 KB (3002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840c886a647e4761c865de41fdecf28aabdf392be2558d7588f4a132cf61caa3`  
		Last Modified: Thu, 30 May 2024 22:46:06 GMT  
		Size: 119.2 MB (119190681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c21e19f38f949440557d9eb970e85705fa9454b90b4444e4374a1a16a218797`  
		Last Modified: Thu, 30 May 2024 22:46:04 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15.0` - unknown; unknown

```console
$ docker pull bonita@sha256:b84756ab16037ed0d50238658f65923d8d825fbf955cbdd5a21ecd6ea48149c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.1 KB (843063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60471a4c0fc256e9b631b10770c84f34d1c797f6f5e75615e6b25006b4ed79f2`

```dockerfile
```

-	Layers:
	-	`sha256:90d6b129f43c5e6ff4cf07592e39064c69f522ee1ed1acfce8bf4b9f44e6c0f1`  
		Last Modified: Thu, 30 May 2024 22:46:03 GMT  
		Size: 819.7 KB (819744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d3c1ae4d6ad3bedbc5d25c34de1fb34bf1c682a64ed917713ee479f9de2232e`  
		Last Modified: Thu, 30 May 2024 22:46:02 GMT  
		Size: 23.3 KB (23319 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.15.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:9eb34c2150166972653b8dba12b89e9636dcc6da156b6929f0d7ab33d86ef655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.8 MB (179819681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b718d3559a26fb41d30f7cc907dba806e3f828e5b122d5c12860a18b4a15c2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:34:20 GMT
ADD file:cf4fecc20d85962cd46b6911d8ee82b9a3de2fa530bc58e998c2d544a888fdb9 in / 
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:34:20 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_VERSION=7.15.0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BRANDING_VERSION=2022.2-u0
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:34:20 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:34:20 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:34:20 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:34:20 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:34:20 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:34:20 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:34:20 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:34:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:34:20 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:04646341bdb047ee1a3dd65db76069b9117954385033f5a340622fd170fa4b73`  
		Last Modified: Sat, 27 Jan 2024 00:28:46 GMT  
		Size: 2.8 MB (2802980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3169e99f3c3d30c82bce3b7fe8f4a643505e25691c0a3a8ea8daf01d4170a4b`  
		Last Modified: Thu, 30 May 2024 21:17:50 GMT  
		Size: 57.8 MB (57816142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a736beb4906376ce95524b776b66c7806e73f0558c594e28a931275f5efb1dfb`  
		Last Modified: Thu, 30 May 2024 21:17:47 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d7adbafe038499090091dd1243f6a053200f23d6e3db2243b369b9744c0009`  
		Last Modified: Thu, 30 May 2024 21:17:47 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4d5bde7cb90faccf971340b6ded0d3f8347c8c99b06593b9ac592ab80a53d3`  
		Last Modified: Thu, 30 May 2024 21:17:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c1c212f47019afda5d60f95f7ca3619dc58be9e73328321a4a07bf4af5e86c`  
		Last Modified: Thu, 30 May 2024 21:17:48 GMT  
		Size: 3.0 KB (3003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7556ecb8b489313ffd345e92e529dde59ae002a7f37cf50ac29e3f3882eb2e76`  
		Last Modified: Thu, 30 May 2024 21:17:52 GMT  
		Size: 119.2 MB (119190690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13dc87b637dcf22284ad9b9b1d17886ef0ea0a4c8e5dd743b1a325066c7c02e6`  
		Last Modified: Thu, 30 May 2024 21:17:48 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15.0` - unknown; unknown

```console
$ docker pull bonita@sha256:dbc429945850eeaea750e1080411ad264da2f86b7998a9be3a35b617c28cc4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8888a15d46bc3f610c29846bcdabbc10da3e2217d50b7559803a101b7eeb407`

```dockerfile
```

-	Layers:
	-	`sha256:69c6ec711a31ac4bae45f279d8816b71769961acbb70aec3f2c259938ee1be28`  
		Last Modified: Thu, 30 May 2024 21:17:48 GMT  
		Size: 817.7 KB (817723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e326df99f8c53edf340fc078fd1cd58591005a8f8a6509335db80fed3b38404`  
		Last Modified: Thu, 30 May 2024 21:17:47 GMT  
		Size: 23.1 KB (23065 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:8.0`

```console
$ docker pull bonita@sha256:05190016a00a01783ab68b77c073d142da324a4de5e344d5fc8eb4e08f4d725e
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
$ docker pull bonita@sha256:cce825ac7644fd7b1665c9e331fc403e5d672db18c62612531b9ddd108d8c853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183457895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59318a8026e721b80f30d0081d879bd5905694c47804b0223d6ab6adc7f9009d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:31:00 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_VERSION=8.0.0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BRANDING_VERSION=2023.1-u0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:31:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:31:00 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Wed, 15 Nov 2023 09:31:00 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
VOLUME [/opt/bonita/conf/logs]
# Wed, 15 Nov 2023 09:31:00 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:31:00 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fd34e6efb621be2c6a33a4342ed75b2eabf18c425e3493c52bc224ed2e5f22`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 61.9 MB (61879078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938ba79419d326f15d91444b8d7f502767a019c577bb86dcb1825168786920f`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d80844bd8d09281cd97dfa9eb3c27bfcc11f6d75075a34679079583f713a3e`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094db1411d9e829316fe3244a42b61e897ac4f7a74503b38e3986c182203a81b`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5047b989f83348dc2a430cfedfb4b39fd27c65e93611f89921d103816b60088b`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc5c9ac25523fc16256abc5c94d4823959b0fb7ede78e2514c61835ef69800c`  
		Last Modified: Thu, 20 Jun 2024 20:54:57 GMT  
		Size: 118.2 MB (118178555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0e97a0d4526f399153bec09432856e04a9e6f07ba3051fe5ff9b908d8d2d2e`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0` - unknown; unknown

```console
$ docker pull bonita@sha256:7c2344c3bae4f1e4fad5034af7021dc529c11ddfadda0278539309f7a4d7c178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.4 KB (842392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76956d38981f86cf8210758ea9841ecc56d034ae5158a05031be483fa88e9c8d`

```dockerfile
```

-	Layers:
	-	`sha256:c702bcf4221f8fbd6297dd327d5cf6ad93cbbb555b84e1d85100381929e7c2fe`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 819.2 KB (819154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98dd9bc4991f245e3dec118ab7c6f4fb16ff9d29c7cd70857a688b43033414d`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 23.2 KB (23238 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:8.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2a8211bccb6126e149ba5aeb200db20d2ad46c78a721de248324a5ce03b36b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182587785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90293c2b1ef2b511383052fc6a7c40178f20f0f1e36b2cb61fa3aa2e99d237b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:31:00 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_VERSION=8.0.0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BRANDING_VERSION=2023.1-u0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:31:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:31:00 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Wed, 15 Nov 2023 09:31:00 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
VOLUME [/opt/bonita/conf/logs]
# Wed, 15 Nov 2023 09:31:00 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:31:00 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e320cbe6007b5dedf0233709bc723fc4607d7fb5f829d82217ef543560aad7d`  
		Last Modified: Fri, 21 Jun 2024 04:35:26 GMT  
		Size: 61.1 MB (61126346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ea9fedde8038622b8526a5b85c441eee7841116bf26f844b83aaa1191e0dac`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b98ef9a238cf22e841ad204f987bc47c777ceaeba1d4085aedd9f1f64e81b17`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b318a41794c5371b6347de93c0154b7412554272fd77e255e6ee344059655c6c`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a09814e50f5970faaccaec563fc7ad8a8fa081730c3fb0c036330f547e625f`  
		Last Modified: Fri, 21 Jun 2024 04:35:25 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ca2992916fc11509c644e39aff85ead2ffa066d6e010b72cbddea7c3ed0e60`  
		Last Modified: Fri, 21 Jun 2024 04:35:28 GMT  
		Size: 118.2 MB (118178556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52030788e32622ddd3dc4030114c6f8b20e704b7e4a8fe4468316df704be26c0`  
		Last Modified: Fri, 21 Jun 2024 04:35:25 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0` - unknown; unknown

```console
$ docker pull bonita@sha256:18d57d0335b7cf4efc6b1d0c1a0c2185c513a3a83e4a12f0cb76c38da5f63407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.8 KB (841801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce984ed4e50cc3d40b698ae05ea0202fffe3a84696671fcec5de8b500d3e00cd`

```dockerfile
```

-	Layers:
	-	`sha256:fc37535d8ebd20459ee695a64294dc7772cac3b5c905412065ef14e4c7878594`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 818.3 KB (818263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44df43a6749e8edda5cffffe0330d940e84b12e602288fb07fd8904dcf351ba2`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 23.5 KB (23538 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:8.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:dcc8142308a098d4e62c718371c5392e8f71ac4c5cb59f62c7988b796c263aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179619841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8982389b6769fdac34527f358a750b30d6de4ce350d3f896d8daaf277a17bd94`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:80e24883ff1c790ff4b3d2b4488ea6cf7b9cbcf5432b00aba4c6043f5e4055c0 in / 
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:31:00 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_VERSION=8.0.0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BRANDING_VERSION=2023.1-u0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:31:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:31:00 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Wed, 15 Nov 2023 09:31:00 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
VOLUME [/opt/bonita/conf/logs]
# Wed, 15 Nov 2023 09:31:00 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:31:00 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f81397ca64cd321c51a90461a0c2f9fb32b00a52366a20f24075bb794eea71a2`  
		Last Modified: Thu, 20 Jun 2024 18:19:25 GMT  
		Size: 3.4 MB (3401809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210567cb03f3b32283f4642a983d2f70076991f82eae53e3c1a0275e8bf6baf6`  
		Last Modified: Fri, 21 Jun 2024 01:23:14 GMT  
		Size: 58.0 MB (58029183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1a7dd7c349b2370b225859ce8e0d63090bd54c459e7627279aff66761f42de`  
		Last Modified: Fri, 21 Jun 2024 01:23:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa42dbd8316045ef2401daa7e9b7366befa4482662398fc723f5a063acc97116`  
		Last Modified: Fri, 21 Jun 2024 01:23:12 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94a650ed84aae374b643fdca8f6b6df20ec8c7e4d11d6ff89180d8ed3170ce0`  
		Last Modified: Fri, 21 Jun 2024 01:23:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8155bde4dd4e7cdb6f5b917dd0f8709de6905c1226111f933e444813cb585ed`  
		Last Modified: Fri, 21 Jun 2024 01:23:13 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9045ca1a5493acc924cd5508a058b18ad545f9f83468b367a11e93fc312fe500`  
		Last Modified: Fri, 21 Jun 2024 01:23:17 GMT  
		Size: 118.2 MB (118178558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b9c66fc9f04f25705d2434b548de75fdf7874593d46be37ef6639764e04292`  
		Last Modified: Fri, 21 Jun 2024 01:23:14 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0` - unknown; unknown

```console
$ docker pull bonita@sha256:e3bc97e68aa0147911f67835df159b2c4f067c77ae148f4cf381a07e3f1f5e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **839.6 KB (839612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c1bfd4085a43aafadf4dd06235fe47ebd479506f52b88d151e05226d43d556`

```dockerfile
```

-	Layers:
	-	`sha256:cef32d66324a634f4c9389ee0eee40a7d6cb7b83c0d1ffa323c72dc3b0c98b1e`  
		Last Modified: Fri, 21 Jun 2024 01:23:12 GMT  
		Size: 816.3 KB (816328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b04a689ddae65938b13cd16d310a1e8b114fb7b33449e9905cbf0dc4cd462e17`  
		Last Modified: Fri, 21 Jun 2024 01:23:12 GMT  
		Size: 23.3 KB (23284 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:8.0.0`

```console
$ docker pull bonita@sha256:05190016a00a01783ab68b77c073d142da324a4de5e344d5fc8eb4e08f4d725e
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
$ docker pull bonita@sha256:cce825ac7644fd7b1665c9e331fc403e5d672db18c62612531b9ddd108d8c853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183457895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59318a8026e721b80f30d0081d879bd5905694c47804b0223d6ab6adc7f9009d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:31:00 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_VERSION=8.0.0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BRANDING_VERSION=2023.1-u0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:31:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:31:00 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Wed, 15 Nov 2023 09:31:00 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
VOLUME [/opt/bonita/conf/logs]
# Wed, 15 Nov 2023 09:31:00 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:31:00 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fd34e6efb621be2c6a33a4342ed75b2eabf18c425e3493c52bc224ed2e5f22`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 61.9 MB (61879078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938ba79419d326f15d91444b8d7f502767a019c577bb86dcb1825168786920f`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d80844bd8d09281cd97dfa9eb3c27bfcc11f6d75075a34679079583f713a3e`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094db1411d9e829316fe3244a42b61e897ac4f7a74503b38e3986c182203a81b`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5047b989f83348dc2a430cfedfb4b39fd27c65e93611f89921d103816b60088b`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc5c9ac25523fc16256abc5c94d4823959b0fb7ede78e2514c61835ef69800c`  
		Last Modified: Thu, 20 Jun 2024 20:54:57 GMT  
		Size: 118.2 MB (118178555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0e97a0d4526f399153bec09432856e04a9e6f07ba3051fe5ff9b908d8d2d2e`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:7c2344c3bae4f1e4fad5034af7021dc529c11ddfadda0278539309f7a4d7c178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.4 KB (842392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76956d38981f86cf8210758ea9841ecc56d034ae5158a05031be483fa88e9c8d`

```dockerfile
```

-	Layers:
	-	`sha256:c702bcf4221f8fbd6297dd327d5cf6ad93cbbb555b84e1d85100381929e7c2fe`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 819.2 KB (819154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98dd9bc4991f245e3dec118ab7c6f4fb16ff9d29c7cd70857a688b43033414d`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 23.2 KB (23238 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:8.0.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2a8211bccb6126e149ba5aeb200db20d2ad46c78a721de248324a5ce03b36b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182587785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90293c2b1ef2b511383052fc6a7c40178f20f0f1e36b2cb61fa3aa2e99d237b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:31:00 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_VERSION=8.0.0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BRANDING_VERSION=2023.1-u0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:31:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:31:00 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Wed, 15 Nov 2023 09:31:00 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
VOLUME [/opt/bonita/conf/logs]
# Wed, 15 Nov 2023 09:31:00 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:31:00 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e320cbe6007b5dedf0233709bc723fc4607d7fb5f829d82217ef543560aad7d`  
		Last Modified: Fri, 21 Jun 2024 04:35:26 GMT  
		Size: 61.1 MB (61126346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ea9fedde8038622b8526a5b85c441eee7841116bf26f844b83aaa1191e0dac`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b98ef9a238cf22e841ad204f987bc47c777ceaeba1d4085aedd9f1f64e81b17`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b318a41794c5371b6347de93c0154b7412554272fd77e255e6ee344059655c6c`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a09814e50f5970faaccaec563fc7ad8a8fa081730c3fb0c036330f547e625f`  
		Last Modified: Fri, 21 Jun 2024 04:35:25 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ca2992916fc11509c644e39aff85ead2ffa066d6e010b72cbddea7c3ed0e60`  
		Last Modified: Fri, 21 Jun 2024 04:35:28 GMT  
		Size: 118.2 MB (118178556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52030788e32622ddd3dc4030114c6f8b20e704b7e4a8fe4468316df704be26c0`  
		Last Modified: Fri, 21 Jun 2024 04:35:25 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:18d57d0335b7cf4efc6b1d0c1a0c2185c513a3a83e4a12f0cb76c38da5f63407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.8 KB (841801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce984ed4e50cc3d40b698ae05ea0202fffe3a84696671fcec5de8b500d3e00cd`

```dockerfile
```

-	Layers:
	-	`sha256:fc37535d8ebd20459ee695a64294dc7772cac3b5c905412065ef14e4c7878594`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 818.3 KB (818263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44df43a6749e8edda5cffffe0330d940e84b12e602288fb07fd8904dcf351ba2`  
		Last Modified: Fri, 21 Jun 2024 04:35:24 GMT  
		Size: 23.5 KB (23538 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:8.0.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:dcc8142308a098d4e62c718371c5392e8f71ac4c5cb59f62c7988b796c263aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179619841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8982389b6769fdac34527f358a750b30d6de4ce350d3f896d8daaf277a17bd94`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:80e24883ff1c790ff4b3d2b4488ea6cf7b9cbcf5432b00aba4c6043f5e4055c0 in / 
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/bin/sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 15 Nov 2023 09:31:00 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BRANDING_VERSION
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_SHA256
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BASE_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ARG BONITA_URL
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_VERSION=8.0.0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BRANDING_VERSION=2023.1-u0
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 15 Nov 2023 09:31:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
COPY files /opt/files # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_API_PASSWORD=
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 15 Nov 2023 09:31:00 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 15 Nov 2023 09:31:00 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 15 Nov 2023 09:31:00 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 15 Nov 2023 09:31:00 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 15 Nov 2023 09:31:00 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Wed, 15 Nov 2023 09:31:00 GMT
COPY templates /opt/templates # buildkit
# Wed, 15 Nov 2023 09:31:00 GMT
VOLUME [/opt/bonita/conf/logs]
# Wed, 15 Nov 2023 09:31:00 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Wed, 15 Nov 2023 09:31:00 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 15 Nov 2023 09:31:00 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f81397ca64cd321c51a90461a0c2f9fb32b00a52366a20f24075bb794eea71a2`  
		Last Modified: Thu, 20 Jun 2024 18:19:25 GMT  
		Size: 3.4 MB (3401809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210567cb03f3b32283f4642a983d2f70076991f82eae53e3c1a0275e8bf6baf6`  
		Last Modified: Fri, 21 Jun 2024 01:23:14 GMT  
		Size: 58.0 MB (58029183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1a7dd7c349b2370b225859ce8e0d63090bd54c459e7627279aff66761f42de`  
		Last Modified: Fri, 21 Jun 2024 01:23:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa42dbd8316045ef2401daa7e9b7366befa4482662398fc723f5a063acc97116`  
		Last Modified: Fri, 21 Jun 2024 01:23:12 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94a650ed84aae374b643fdca8f6b6df20ec8c7e4d11d6ff89180d8ed3170ce0`  
		Last Modified: Fri, 21 Jun 2024 01:23:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8155bde4dd4e7cdb6f5b917dd0f8709de6905c1226111f933e444813cb585ed`  
		Last Modified: Fri, 21 Jun 2024 01:23:13 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9045ca1a5493acc924cd5508a058b18ad545f9f83468b367a11e93fc312fe500`  
		Last Modified: Fri, 21 Jun 2024 01:23:17 GMT  
		Size: 118.2 MB (118178558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b9c66fc9f04f25705d2434b548de75fdf7874593d46be37ef6639764e04292`  
		Last Modified: Fri, 21 Jun 2024 01:23:14 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:e3bc97e68aa0147911f67835df159b2c4f067c77ae148f4cf381a07e3f1f5e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **839.6 KB (839612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c1bfd4085a43aafadf4dd06235fe47ebd479506f52b88d151e05226d43d556`

```dockerfile
```

-	Layers:
	-	`sha256:cef32d66324a634f4c9389ee0eee40a7d6cb7b83c0d1ffa323c72dc3b0c98b1e`  
		Last Modified: Fri, 21 Jun 2024 01:23:12 GMT  
		Size: 816.3 KB (816328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b04a689ddae65938b13cd16d310a1e8b114fb7b33449e9905cbf0dc4cd462e17`  
		Last Modified: Fri, 21 Jun 2024 01:23:12 GMT  
		Size: 23.3 KB (23284 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:9.0`

```console
$ docker pull bonita@sha256:f77cf6cf95850b802363581c2a390c83bdb3c06f391bf6f40ff683018e592454
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
$ docker pull bonita@sha256:cfafc89f4f8655735239ced8d569b71f05e4859d0a7f25930c1ca0afe1bca331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191504948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14632f7d69ca215136833045abccc81789c32547dd5369f5dff40ac86767bcb`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/bin/sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 16 Nov 2023 12:46:16 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BRANDING_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_SHA256
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BASE_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_VERSION=9.0.0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BRANDING_VERSION=2023.2-u0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
COPY files /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_PASSWORD=
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 16 Nov 2023 12:46:16 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 16 Nov 2023 12:46:16 GMT
COPY templates /opt/templates # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
VOLUME [/opt/bonita/conf/logs]
# Thu, 16 Nov 2023 12:46:16 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Thu, 16 Nov 2023 12:46:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edf3aff7655503316b5a3d27de022b8ac48b2fba2bad7cc769f68b5ab92cd8f`  
		Last Modified: Thu, 20 Jun 2024 20:54:58 GMT  
		Size: 67.9 MB (67906820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938ba79419d326f15d91444b8d7f502767a019c577bb86dcb1825168786920f`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02af2d7432ac7e3064a06cf121286bb620e72f6933e8dc6bd719d3d6d08361`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c57b81c81d5cd857c9e5f77738e6ad4a5d415808d06514cb3390c31b7d7e66`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161a6232ea5454614142c12d21f47f0b5878597927b9b2402d3ae2dc19ecf95f`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 3.6 KB (3621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6ee59c8134b30a102e94cf66b7431a76b72dc0a019455241530d62cfe55361`  
		Last Modified: Thu, 20 Jun 2024 20:54:59 GMT  
		Size: 120.2 MB (120173509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e705981acaa2e7c65f16d61c3d02dd1d7acd8b1506dc870e8320631e66873982`  
		Last Modified: Thu, 20 Jun 2024 20:54:56 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0` - unknown; unknown

```console
$ docker pull bonita@sha256:ea9cd92b1318d44bb5fb1f6d88cd9ec73ffaaaa8f13f72984e2a460f3614f0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1669914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dad4c1fab92b35923ad0afe16f88083372bd2ab1a7edeef888e125887aafe0b`

```dockerfile
```

-	Layers:
	-	`sha256:f1bf310b7bea83f154e65b01a2b7019ac30b889967679515ab390c236f9cecc7`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 1.6 MB (1646899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1087d9630f1315af984fc892fd8308edea8fdb8d5e5a6887964e5781a8ab036`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 23.0 KB (23015 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:9.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ad6960f37123c0538ed05bbe3f36d10998034edefbf98a09e68184ebba3d92da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191309040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ce96646115c63d60141c082ac915bd648341d67e1fd4aba7862ed1ec4053bc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/bin/sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 16 Nov 2023 12:46:16 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BRANDING_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_SHA256
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BASE_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_VERSION=9.0.0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BRANDING_VERSION=2023.2-u0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
COPY files /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_PASSWORD=
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 16 Nov 2023 12:46:16 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 16 Nov 2023 12:46:16 GMT
COPY templates /opt/templates # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
VOLUME [/opt/bonita/conf/logs]
# Thu, 16 Nov 2023 12:46:16 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Thu, 16 Nov 2023 12:46:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d66208e02de54624ca72d6357fe02b4ef5b57adfe46c10d4ada2b50c1994d`  
		Last Modified: Fri, 21 Jun 2024 04:36:10 GMT  
		Size: 67.8 MB (67786863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dc9c32d7820a287397c7e3461f8ddd6580a69519fc20812f3307736b3c59d6`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad67851d2ff9c33dd840e6fd8372fafd6ff597c963de7d59a57b9fd5736000ba`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd5e0cc73cb341c13e67803dd856f9a4f36dc573945d39ec56632de731ff65d`  
		Last Modified: Fri, 21 Jun 2024 04:36:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366b8f5db48cca3fdbcccb549e5245a72f44c7cd97879c5588b6792f05eadbeb`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 3.6 KB (3620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992af7ed68d9ece9daaf0acd2f30f07b95d6db872efca98b146bea5f67b306ab`  
		Last Modified: Fri, 21 Jun 2024 04:36:12 GMT  
		Size: 120.2 MB (120173507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0b72a4a51b8c7334db7df3c00cc380e94083cf809d6e9158bb2517c80c352a`  
		Last Modified: Fri, 21 Jun 2024 04:36:09 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0` - unknown; unknown

```console
$ docker pull bonita@sha256:9084bad2dd265d66e1f3a1da609691f425054b0b00123a837540e184d33cc91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1669376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861023f6c0a42f154b6918b930187e434f25df03ae60e6d4a5502c2a41a5aab9`

```dockerfile
```

-	Layers:
	-	`sha256:f02577bd4c6ef9093f4093b4d3c24215f954bc1216a65c30810586837de1a606`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 1.6 MB (1646048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3401512b9019aaa112d53dca527e4ed25c34cfc877826501089c484e3f71291`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:9.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:95d26a9359693148b468e0d6b21eb85502cbe57998f0de93fe9742c770e6789e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188177029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf400227ec7ef1a02fad802b358cc8cb1884f88eb05f91fc4ef97e288e79afe1`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:e0f257ed0b6b089b6a4fe2968065aa56ee04f7837fe7266dcd68be8d5242417b in / 
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/bin/sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 16 Nov 2023 12:46:16 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BRANDING_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_SHA256
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BASE_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_VERSION=9.0.0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BRANDING_VERSION=2023.2-u0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
COPY files /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_PASSWORD=
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 16 Nov 2023 12:46:16 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 16 Nov 2023 12:46:16 GMT
COPY templates /opt/templates # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
VOLUME [/opt/bonita/conf/logs]
# Thu, 16 Nov 2023 12:46:16 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Thu, 16 Nov 2023 12:46:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e3dd182a4c3296a9689fa043379c0a4ce2b865024ca7344a169d5d4759a52548`  
		Last Modified: Thu, 20 Jun 2024 18:19:16 GMT  
		Size: 3.4 MB (3357033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b8d6bcb67b4251182b5a25a8898185071bca1a3416e3ae7f82b63160702802`  
		Last Modified: Fri, 21 Jun 2024 01:24:39 GMT  
		Size: 64.6 MB (64635686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2401c0c0157a899c7f6efae6d42c1f7ea9ed7bfadb012acdc440bea1f01626e`  
		Last Modified: Fri, 21 Jun 2024 01:24:36 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8992554392ad6fe61a95d79803f89a21e9c1784aff1f68b7071d6eb54dcca8e`  
		Last Modified: Fri, 21 Jun 2024 01:24:36 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e2c509cae2e2c6c36cf5f8fede6096a705f1f5f23f44832961b0ff675f62b1`  
		Last Modified: Fri, 21 Jun 2024 01:24:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99dfd301f0a22b1867fe33b1226ede36e5363bcb0fc79b8ccf3375c5f64266`  
		Last Modified: Fri, 21 Jun 2024 01:24:37 GMT  
		Size: 3.6 KB (3620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cfd062320b3a5ed4871e2803459aecf4b65eb7966d8fbbda8a6a3c71ff2e65`  
		Last Modified: Fri, 21 Jun 2024 01:24:41 GMT  
		Size: 120.2 MB (120173588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9711be1a3b1cf19880d75f9dc5e1afc84eacd5356fe3b889e175c557b9356611`  
		Last Modified: Fri, 21 Jun 2024 01:24:38 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0` - unknown; unknown

```console
$ docker pull bonita@sha256:cefa5205449cf08d99e001d64fc0c62d8b2e7c7cc9d33b7d767c232add0bddde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1667134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1609a0e7e0f96392a4ca2db3afe595999baff2ca6a09f43a07dbd1763556919b`

```dockerfile
```

-	Layers:
	-	`sha256:493e414dd82430ed989337241ed1354b973cd5cd81a4b5dcea13387f6173e0ab`  
		Last Modified: Fri, 21 Jun 2024 01:24:37 GMT  
		Size: 1.6 MB (1644066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4dadb2e006eb3162ce0ac88bfce426857e8b63c3f0e81910373cd400bd5aa02`  
		Last Modified: Fri, 21 Jun 2024 01:24:36 GMT  
		Size: 23.1 KB (23068 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:9.0.0`

```console
$ docker pull bonita@sha256:f77cf6cf95850b802363581c2a390c83bdb3c06f391bf6f40ff683018e592454
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
$ docker pull bonita@sha256:cfafc89f4f8655735239ced8d569b71f05e4859d0a7f25930c1ca0afe1bca331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191504948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14632f7d69ca215136833045abccc81789c32547dd5369f5dff40ac86767bcb`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/bin/sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 16 Nov 2023 12:46:16 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BRANDING_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_SHA256
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BASE_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_VERSION=9.0.0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BRANDING_VERSION=2023.2-u0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
COPY files /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_PASSWORD=
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 16 Nov 2023 12:46:16 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 16 Nov 2023 12:46:16 GMT
COPY templates /opt/templates # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
VOLUME [/opt/bonita/conf/logs]
# Thu, 16 Nov 2023 12:46:16 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Thu, 16 Nov 2023 12:46:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edf3aff7655503316b5a3d27de022b8ac48b2fba2bad7cc769f68b5ab92cd8f`  
		Last Modified: Thu, 20 Jun 2024 20:54:58 GMT  
		Size: 67.9 MB (67906820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938ba79419d326f15d91444b8d7f502767a019c577bb86dcb1825168786920f`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02af2d7432ac7e3064a06cf121286bb620e72f6933e8dc6bd719d3d6d08361`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c57b81c81d5cd857c9e5f77738e6ad4a5d415808d06514cb3390c31b7d7e66`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161a6232ea5454614142c12d21f47f0b5878597927b9b2402d3ae2dc19ecf95f`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 3.6 KB (3621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6ee59c8134b30a102e94cf66b7431a76b72dc0a019455241530d62cfe55361`  
		Last Modified: Thu, 20 Jun 2024 20:54:59 GMT  
		Size: 120.2 MB (120173509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e705981acaa2e7c65f16d61c3d02dd1d7acd8b1506dc870e8320631e66873982`  
		Last Modified: Thu, 20 Jun 2024 20:54:56 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:ea9cd92b1318d44bb5fb1f6d88cd9ec73ffaaaa8f13f72984e2a460f3614f0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1669914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dad4c1fab92b35923ad0afe16f88083372bd2ab1a7edeef888e125887aafe0b`

```dockerfile
```

-	Layers:
	-	`sha256:f1bf310b7bea83f154e65b01a2b7019ac30b889967679515ab390c236f9cecc7`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 1.6 MB (1646899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1087d9630f1315af984fc892fd8308edea8fdb8d5e5a6887964e5781a8ab036`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 23.0 KB (23015 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:9.0.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ad6960f37123c0538ed05bbe3f36d10998034edefbf98a09e68184ebba3d92da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191309040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ce96646115c63d60141c082ac915bd648341d67e1fd4aba7862ed1ec4053bc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/bin/sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 16 Nov 2023 12:46:16 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BRANDING_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_SHA256
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BASE_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_VERSION=9.0.0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BRANDING_VERSION=2023.2-u0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
COPY files /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_PASSWORD=
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 16 Nov 2023 12:46:16 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 16 Nov 2023 12:46:16 GMT
COPY templates /opt/templates # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
VOLUME [/opt/bonita/conf/logs]
# Thu, 16 Nov 2023 12:46:16 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Thu, 16 Nov 2023 12:46:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d66208e02de54624ca72d6357fe02b4ef5b57adfe46c10d4ada2b50c1994d`  
		Last Modified: Fri, 21 Jun 2024 04:36:10 GMT  
		Size: 67.8 MB (67786863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dc9c32d7820a287397c7e3461f8ddd6580a69519fc20812f3307736b3c59d6`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad67851d2ff9c33dd840e6fd8372fafd6ff597c963de7d59a57b9fd5736000ba`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd5e0cc73cb341c13e67803dd856f9a4f36dc573945d39ec56632de731ff65d`  
		Last Modified: Fri, 21 Jun 2024 04:36:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366b8f5db48cca3fdbcccb549e5245a72f44c7cd97879c5588b6792f05eadbeb`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 3.6 KB (3620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992af7ed68d9ece9daaf0acd2f30f07b95d6db872efca98b146bea5f67b306ab`  
		Last Modified: Fri, 21 Jun 2024 04:36:12 GMT  
		Size: 120.2 MB (120173507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0b72a4a51b8c7334db7df3c00cc380e94083cf809d6e9158bb2517c80c352a`  
		Last Modified: Fri, 21 Jun 2024 04:36:09 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:9084bad2dd265d66e1f3a1da609691f425054b0b00123a837540e184d33cc91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1669376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861023f6c0a42f154b6918b930187e434f25df03ae60e6d4a5502c2a41a5aab9`

```dockerfile
```

-	Layers:
	-	`sha256:f02577bd4c6ef9093f4093b4d3c24215f954bc1216a65c30810586837de1a606`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 1.6 MB (1646048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3401512b9019aaa112d53dca527e4ed25c34cfc877826501089c484e3f71291`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:9.0.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:95d26a9359693148b468e0d6b21eb85502cbe57998f0de93fe9742c770e6789e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188177029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf400227ec7ef1a02fad802b358cc8cb1884f88eb05f91fc4ef97e288e79afe1`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:e0f257ed0b6b089b6a4fe2968065aa56ee04f7837fe7266dcd68be8d5242417b in / 
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/bin/sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 16 Nov 2023 12:46:16 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BRANDING_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_SHA256
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BASE_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_VERSION=9.0.0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BRANDING_VERSION=2023.2-u0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
COPY files /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_PASSWORD=
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 16 Nov 2023 12:46:16 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 16 Nov 2023 12:46:16 GMT
COPY templates /opt/templates # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
VOLUME [/opt/bonita/conf/logs]
# Thu, 16 Nov 2023 12:46:16 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Thu, 16 Nov 2023 12:46:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e3dd182a4c3296a9689fa043379c0a4ce2b865024ca7344a169d5d4759a52548`  
		Last Modified: Thu, 20 Jun 2024 18:19:16 GMT  
		Size: 3.4 MB (3357033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b8d6bcb67b4251182b5a25a8898185071bca1a3416e3ae7f82b63160702802`  
		Last Modified: Fri, 21 Jun 2024 01:24:39 GMT  
		Size: 64.6 MB (64635686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2401c0c0157a899c7f6efae6d42c1f7ea9ed7bfadb012acdc440bea1f01626e`  
		Last Modified: Fri, 21 Jun 2024 01:24:36 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8992554392ad6fe61a95d79803f89a21e9c1784aff1f68b7071d6eb54dcca8e`  
		Last Modified: Fri, 21 Jun 2024 01:24:36 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e2c509cae2e2c6c36cf5f8fede6096a705f1f5f23f44832961b0ff675f62b1`  
		Last Modified: Fri, 21 Jun 2024 01:24:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99dfd301f0a22b1867fe33b1226ede36e5363bcb0fc79b8ccf3375c5f64266`  
		Last Modified: Fri, 21 Jun 2024 01:24:37 GMT  
		Size: 3.6 KB (3620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cfd062320b3a5ed4871e2803459aecf4b65eb7966d8fbbda8a6a3c71ff2e65`  
		Last Modified: Fri, 21 Jun 2024 01:24:41 GMT  
		Size: 120.2 MB (120173588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9711be1a3b1cf19880d75f9dc5e1afc84eacd5356fe3b889e175c557b9356611`  
		Last Modified: Fri, 21 Jun 2024 01:24:38 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:cefa5205449cf08d99e001d64fc0c62d8b2e7c7cc9d33b7d767c232add0bddde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1667134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1609a0e7e0f96392a4ca2db3afe595999baff2ca6a09f43a07dbd1763556919b`

```dockerfile
```

-	Layers:
	-	`sha256:493e414dd82430ed989337241ed1354b973cd5cd81a4b5dcea13387f6173e0ab`  
		Last Modified: Fri, 21 Jun 2024 01:24:37 GMT  
		Size: 1.6 MB (1644066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4dadb2e006eb3162ce0ac88bfce426857e8b63c3f0e81910373cd400bd5aa02`  
		Last Modified: Fri, 21 Jun 2024 01:24:36 GMT  
		Size: 23.1 KB (23068 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:latest`

```console
$ docker pull bonita@sha256:f77cf6cf95850b802363581c2a390c83bdb3c06f391bf6f40ff683018e592454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:cfafc89f4f8655735239ced8d569b71f05e4859d0a7f25930c1ca0afe1bca331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191504948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14632f7d69ca215136833045abccc81789c32547dd5369f5dff40ac86767bcb`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/bin/sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 16 Nov 2023 12:46:16 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BRANDING_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_SHA256
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BASE_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_VERSION=9.0.0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BRANDING_VERSION=2023.2-u0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
COPY files /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_PASSWORD=
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 16 Nov 2023 12:46:16 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 16 Nov 2023 12:46:16 GMT
COPY templates /opt/templates # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
VOLUME [/opt/bonita/conf/logs]
# Thu, 16 Nov 2023 12:46:16 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Thu, 16 Nov 2023 12:46:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edf3aff7655503316b5a3d27de022b8ac48b2fba2bad7cc769f68b5ab92cd8f`  
		Last Modified: Thu, 20 Jun 2024 20:54:58 GMT  
		Size: 67.9 MB (67906820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938ba79419d326f15d91444b8d7f502767a019c577bb86dcb1825168786920f`  
		Last Modified: Thu, 20 Jun 2024 20:54:53 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd02af2d7432ac7e3064a06cf121286bb620e72f6933e8dc6bd719d3d6d08361`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c57b81c81d5cd857c9e5f77738e6ad4a5d415808d06514cb3390c31b7d7e66`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161a6232ea5454614142c12d21f47f0b5878597927b9b2402d3ae2dc19ecf95f`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 3.6 KB (3621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6ee59c8134b30a102e94cf66b7431a76b72dc0a019455241530d62cfe55361`  
		Last Modified: Thu, 20 Jun 2024 20:54:59 GMT  
		Size: 120.2 MB (120173509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e705981acaa2e7c65f16d61c3d02dd1d7acd8b1506dc870e8320631e66873982`  
		Last Modified: Thu, 20 Jun 2024 20:54:56 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:latest` - unknown; unknown

```console
$ docker pull bonita@sha256:ea9cd92b1318d44bb5fb1f6d88cd9ec73ffaaaa8f13f72984e2a460f3614f0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1669914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dad4c1fab92b35923ad0afe16f88083372bd2ab1a7edeef888e125887aafe0b`

```dockerfile
```

-	Layers:
	-	`sha256:f1bf310b7bea83f154e65b01a2b7019ac30b889967679515ab390c236f9cecc7`  
		Last Modified: Thu, 20 Jun 2024 20:54:55 GMT  
		Size: 1.6 MB (1646899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1087d9630f1315af984fc892fd8308edea8fdb8d5e5a6887964e5781a8ab036`  
		Last Modified: Thu, 20 Jun 2024 20:54:54 GMT  
		Size: 23.0 KB (23015 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ad6960f37123c0538ed05bbe3f36d10998034edefbf98a09e68184ebba3d92da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191309040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ce96646115c63d60141c082ac915bd648341d67e1fd4aba7862ed1ec4053bc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/bin/sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 16 Nov 2023 12:46:16 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BRANDING_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_SHA256
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BASE_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_VERSION=9.0.0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BRANDING_VERSION=2023.2-u0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
COPY files /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_PASSWORD=
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 16 Nov 2023 12:46:16 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 16 Nov 2023 12:46:16 GMT
COPY templates /opt/templates # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
VOLUME [/opt/bonita/conf/logs]
# Thu, 16 Nov 2023 12:46:16 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Thu, 16 Nov 2023 12:46:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d66208e02de54624ca72d6357fe02b4ef5b57adfe46c10d4ada2b50c1994d`  
		Last Modified: Fri, 21 Jun 2024 04:36:10 GMT  
		Size: 67.8 MB (67786863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dc9c32d7820a287397c7e3461f8ddd6580a69519fc20812f3307736b3c59d6`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad67851d2ff9c33dd840e6fd8372fafd6ff597c963de7d59a57b9fd5736000ba`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd5e0cc73cb341c13e67803dd856f9a4f36dc573945d39ec56632de731ff65d`  
		Last Modified: Fri, 21 Jun 2024 04:36:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366b8f5db48cca3fdbcccb549e5245a72f44c7cd97879c5588b6792f05eadbeb`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 3.6 KB (3620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992af7ed68d9ece9daaf0acd2f30f07b95d6db872efca98b146bea5f67b306ab`  
		Last Modified: Fri, 21 Jun 2024 04:36:12 GMT  
		Size: 120.2 MB (120173507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0b72a4a51b8c7334db7df3c00cc380e94083cf809d6e9158bb2517c80c352a`  
		Last Modified: Fri, 21 Jun 2024 04:36:09 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:latest` - unknown; unknown

```console
$ docker pull bonita@sha256:9084bad2dd265d66e1f3a1da609691f425054b0b00123a837540e184d33cc91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1669376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861023f6c0a42f154b6918b930187e434f25df03ae60e6d4a5502c2a41a5aab9`

```dockerfile
```

-	Layers:
	-	`sha256:f02577bd4c6ef9093f4093b4d3c24215f954bc1216a65c30810586837de1a606`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 1.6 MB (1646048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3401512b9019aaa112d53dca527e4ed25c34cfc877826501089c484e3f71291`  
		Last Modified: Fri, 21 Jun 2024 04:36:08 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:95d26a9359693148b468e0d6b21eb85502cbe57998f0de93fe9742c770e6789e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188177029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf400227ec7ef1a02fad802b358cc8cb1884f88eb05f91fc4ef97e288e79afe1`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:e0f257ed0b6b089b6a4fe2968065aa56ee04f7837fe7266dcd68be8d5242417b in / 
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/bin/sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 16 Nov 2023 12:46:16 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BRANDING_VERSION
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_SHA256
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BASE_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ARG BONITA_URL
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_VERSION=9.0.0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BRANDING_VERSION=2023.2-u0
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 16 Nov 2023 12:46:16 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
COPY files /opt/files # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_USERNAME=http-api
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_API_PASSWORD=
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_USERNAME=monitoring
# Thu, 16 Nov 2023 12:46:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Thu, 16 Nov 2023 12:46:16 GMT
ENV JMX_REMOTE_ACCESS=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Thu, 16 Nov 2023 12:46:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Thu, 16 Nov 2023 12:46:16 GMT
ENV HTTP_MAX_THREADS=20
# Thu, 16 Nov 2023 12:46:16 GMT
COPY templates /opt/templates # buildkit
# Thu, 16 Nov 2023 12:46:16 GMT
VOLUME [/opt/bonita/conf/logs]
# Thu, 16 Nov 2023 12:46:16 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Thu, 16 Nov 2023 12:46:16 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Thu, 16 Nov 2023 12:46:16 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e3dd182a4c3296a9689fa043379c0a4ce2b865024ca7344a169d5d4759a52548`  
		Last Modified: Thu, 20 Jun 2024 18:19:16 GMT  
		Size: 3.4 MB (3357033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b8d6bcb67b4251182b5a25a8898185071bca1a3416e3ae7f82b63160702802`  
		Last Modified: Fri, 21 Jun 2024 01:24:39 GMT  
		Size: 64.6 MB (64635686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2401c0c0157a899c7f6efae6d42c1f7ea9ed7bfadb012acdc440bea1f01626e`  
		Last Modified: Fri, 21 Jun 2024 01:24:36 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8992554392ad6fe61a95d79803f89a21e9c1784aff1f68b7071d6eb54dcca8e`  
		Last Modified: Fri, 21 Jun 2024 01:24:36 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e2c509cae2e2c6c36cf5f8fede6096a705f1f5f23f44832961b0ff675f62b1`  
		Last Modified: Fri, 21 Jun 2024 01:24:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c99dfd301f0a22b1867fe33b1226ede36e5363bcb0fc79b8ccf3375c5f64266`  
		Last Modified: Fri, 21 Jun 2024 01:24:37 GMT  
		Size: 3.6 KB (3620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cfd062320b3a5ed4871e2803459aecf4b65eb7966d8fbbda8a6a3c71ff2e65`  
		Last Modified: Fri, 21 Jun 2024 01:24:41 GMT  
		Size: 120.2 MB (120173588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9711be1a3b1cf19880d75f9dc5e1afc84eacd5356fe3b889e175c557b9356611`  
		Last Modified: Fri, 21 Jun 2024 01:24:38 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:latest` - unknown; unknown

```console
$ docker pull bonita@sha256:cefa5205449cf08d99e001d64fc0c62d8b2e7c7cc9d33b7d767c232add0bddde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1667134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1609a0e7e0f96392a4ca2db3afe595999baff2ca6a09f43a07dbd1763556919b`

```dockerfile
```

-	Layers:
	-	`sha256:493e414dd82430ed989337241ed1354b973cd5cd81a4b5dcea13387f6173e0ab`  
		Last Modified: Fri, 21 Jun 2024 01:24:37 GMT  
		Size: 1.6 MB (1644066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4dadb2e006eb3162ce0ac88bfce426857e8b63c3f0e81910373cd400bd5aa02`  
		Last Modified: Fri, 21 Jun 2024 01:24:36 GMT  
		Size: 23.1 KB (23068 bytes)  
		MIME: application/vnd.in-toto+json
