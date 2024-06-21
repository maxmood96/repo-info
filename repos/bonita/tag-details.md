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
$ docker pull bonita@sha256:29f543c3666b99a28017c80e97f1591a264db829239eadeefa31852b0e12c3ec
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
$ docker pull bonita@sha256:30079b8615151fd888c3abf7b9733190504977e0ab2630636b609728372bbdfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182573601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3d43a48e464b8894ebc9c932e63a38c089d6a08cafb112e73d546adf6b34cc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
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
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0502c1826d837d828ee506bf8f3f13428fe6205cd4a434a3588fda6d9b1a635e`  
		Last Modified: Thu, 30 May 2024 22:46:44 GMT  
		Size: 61.1 MB (61126449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78d0090e73117ea6b94074085b67fcf2a86507a09cd1f874f670453a6149809`  
		Last Modified: Thu, 30 May 2024 22:46:42 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1091f3c5b3e2b4dd0222543a3f1a1c571876df870b5221888e4ce89596db15af`  
		Last Modified: Thu, 30 May 2024 22:46:41 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d4290bf86de7a9efb4b8ce3b14a11e00efacf96515f85051f01cc8a84856a`  
		Last Modified: Thu, 30 May 2024 22:46:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60470cd7e3fe739380acb2e108dc5dee66b46532c7cd4e6c17cfca269521585`  
		Last Modified: Thu, 30 May 2024 22:46:43 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b2167dc14d94bd8cc91a151c662d03c66816144f75755f4ef2a483feffbfb3`  
		Last Modified: Thu, 30 May 2024 22:46:46 GMT  
		Size: 118.2 MB (118178575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1cb471eb013475d8411b75fd4b53a0bb04b0b19098f782986668b0832d7474`  
		Last Modified: Thu, 30 May 2024 22:46:43 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1` - unknown; unknown

```console
$ docker pull bonita@sha256:073ed1b15b8b3a429ee571774bf1906ddc4d1ed990a2eb01cb139941e9cdc44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6aceca2947fedefab474f4a3ae263df728a55d9c12daecc6ce09c0bd2a79b3a`

```dockerfile
```

-	Layers:
	-	`sha256:a8619873e6673cd6641103e16d130a1758bc6cea1a66a190eccce3c921b1d789`  
		Last Modified: Thu, 30 May 2024 22:46:42 GMT  
		Size: 819.2 KB (819232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4648bceb37b0d8e3cf1ecdfdb5445890552622873ce190aad1b3b1ae839080`  
		Last Modified: Thu, 30 May 2024 22:46:42 GMT  
		Size: 23.5 KB (23489 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:4c8690f24745794ba67cc276ccc8075fb47c829be4728f6570cf10dd0d33b307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179610318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13ec471c219b9d72f4473d771a0d6b8f1c92447fe0f7b98b570bd58545b1e09`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
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
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3555b0d2356ad5e27bb1167bec88a85252d0c80f688e1c8aab8b47cf2517d67d`  
		Last Modified: Thu, 30 May 2024 21:19:07 GMT  
		Size: 58.0 MB (58029322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05393a21a1f62ec4ec5c300b04c646aaafab1dfeb8059ed9768ffbe0ddac8069`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14baace67657acc4abcd9a81efb25927fc271bb8a5ee3fcd05030b735f982809`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919e82e7af965d43cec612645ef9a35e1b9b4e117d679487485fe668594f56f7`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab5c81aa774a9dcd37b5bc5147884779c3940fc6e15a21d2fc0adf4140a1029`  
		Last Modified: Thu, 30 May 2024 21:19:06 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cc4818f9afebf85690bf76ebe2b10890ba92ab25cfd99604103962b6c448a3`  
		Last Modified: Thu, 30 May 2024 21:19:11 GMT  
		Size: 118.2 MB (118178592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656497dcfb57ffb6c0244c47b46a6f239639898e097255e89f04ab593e789550`  
		Last Modified: Thu, 30 May 2024 21:19:07 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1` - unknown; unknown

```console
$ docker pull bonita@sha256:9a8c26e0e62a9ebe144d85d6a6dfccd316e6f14429e9cea37a9ad288f4b64fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.5 KB (840495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfccd9b7527cc03977ba497120ddc05a1dc78fff6bd53ba86f8cfcb84dc7e1e`

```dockerfile
```

-	Layers:
	-	`sha256:a7035582f39c0f59080e12e820dba0d7dda2e525e08b322b422a180fff42c163`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 817.3 KB (817260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad77c527c8f67713bb9ff7b0f4bd454e588268889bddad983200b276cc4b078a`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 23.2 KB (23235 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.1-u0`

```console
$ docker pull bonita@sha256:29f543c3666b99a28017c80e97f1591a264db829239eadeefa31852b0e12c3ec
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
$ docker pull bonita@sha256:30079b8615151fd888c3abf7b9733190504977e0ab2630636b609728372bbdfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182573601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3d43a48e464b8894ebc9c932e63a38c089d6a08cafb112e73d546adf6b34cc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
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
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0502c1826d837d828ee506bf8f3f13428fe6205cd4a434a3588fda6d9b1a635e`  
		Last Modified: Thu, 30 May 2024 22:46:44 GMT  
		Size: 61.1 MB (61126449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78d0090e73117ea6b94074085b67fcf2a86507a09cd1f874f670453a6149809`  
		Last Modified: Thu, 30 May 2024 22:46:42 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1091f3c5b3e2b4dd0222543a3f1a1c571876df870b5221888e4ce89596db15af`  
		Last Modified: Thu, 30 May 2024 22:46:41 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d4290bf86de7a9efb4b8ce3b14a11e00efacf96515f85051f01cc8a84856a`  
		Last Modified: Thu, 30 May 2024 22:46:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60470cd7e3fe739380acb2e108dc5dee66b46532c7cd4e6c17cfca269521585`  
		Last Modified: Thu, 30 May 2024 22:46:43 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b2167dc14d94bd8cc91a151c662d03c66816144f75755f4ef2a483feffbfb3`  
		Last Modified: Thu, 30 May 2024 22:46:46 GMT  
		Size: 118.2 MB (118178575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1cb471eb013475d8411b75fd4b53a0bb04b0b19098f782986668b0832d7474`  
		Last Modified: Thu, 30 May 2024 22:46:43 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:073ed1b15b8b3a429ee571774bf1906ddc4d1ed990a2eb01cb139941e9cdc44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6aceca2947fedefab474f4a3ae263df728a55d9c12daecc6ce09c0bd2a79b3a`

```dockerfile
```

-	Layers:
	-	`sha256:a8619873e6673cd6641103e16d130a1758bc6cea1a66a190eccce3c921b1d789`  
		Last Modified: Thu, 30 May 2024 22:46:42 GMT  
		Size: 819.2 KB (819232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4648bceb37b0d8e3cf1ecdfdb5445890552622873ce190aad1b3b1ae839080`  
		Last Modified: Thu, 30 May 2024 22:46:42 GMT  
		Size: 23.5 KB (23489 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:4c8690f24745794ba67cc276ccc8075fb47c829be4728f6570cf10dd0d33b307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179610318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13ec471c219b9d72f4473d771a0d6b8f1c92447fe0f7b98b570bd58545b1e09`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
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
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3555b0d2356ad5e27bb1167bec88a85252d0c80f688e1c8aab8b47cf2517d67d`  
		Last Modified: Thu, 30 May 2024 21:19:07 GMT  
		Size: 58.0 MB (58029322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05393a21a1f62ec4ec5c300b04c646aaafab1dfeb8059ed9768ffbe0ddac8069`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14baace67657acc4abcd9a81efb25927fc271bb8a5ee3fcd05030b735f982809`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919e82e7af965d43cec612645ef9a35e1b9b4e117d679487485fe668594f56f7`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab5c81aa774a9dcd37b5bc5147884779c3940fc6e15a21d2fc0adf4140a1029`  
		Last Modified: Thu, 30 May 2024 21:19:06 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cc4818f9afebf85690bf76ebe2b10890ba92ab25cfd99604103962b6c448a3`  
		Last Modified: Thu, 30 May 2024 21:19:11 GMT  
		Size: 118.2 MB (118178592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656497dcfb57ffb6c0244c47b46a6f239639898e097255e89f04ab593e789550`  
		Last Modified: Thu, 30 May 2024 21:19:07 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:9a8c26e0e62a9ebe144d85d6a6dfccd316e6f14429e9cea37a9ad288f4b64fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.5 KB (840495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfccd9b7527cc03977ba497120ddc05a1dc78fff6bd53ba86f8cfcb84dc7e1e`

```dockerfile
```

-	Layers:
	-	`sha256:a7035582f39c0f59080e12e820dba0d7dda2e525e08b322b422a180fff42c163`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 817.3 KB (817260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad77c527c8f67713bb9ff7b0f4bd454e588268889bddad983200b276cc4b078a`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 23.2 KB (23235 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.2`

```console
$ docker pull bonita@sha256:4655db3ee6308e3c00eb8f8c8e15fe494b7e7a2c98a5904b769be02129001c11
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
$ docker pull bonita@sha256:8885231f41ccefd4e873f2f807eeb2baced5708542e03085bb9388adccb6173e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191304430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d759f5d9811ac2bae2d1721abb082534cd145c928138cdd4a76b9b16f758d74c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf82cc3502f0dd9f68d96420f0dd34810219d98cee64d432da56905baf3d1ff`  
		Last Modified: Thu, 30 May 2024 22:47:28 GMT  
		Size: 67.8 MB (67786817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a8187e3a4e7ddc58b264bb94ac11f2d2328df254d766a89c0b3be4807e60bd`  
		Last Modified: Thu, 30 May 2024 22:47:25 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e96e75cf2398095e1a75dbf7bccf297438cfbc4531c11773890e153370e662`  
		Last Modified: Thu, 30 May 2024 22:47:25 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7157b7cbe66932baa94bc8bc980b51386093b171b56a2ed99979a9c111fdca34`  
		Last Modified: Thu, 30 May 2024 22:47:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c36c4c5b4ac2b281b949f1f1922d2231a54a94c38ff2b08847a866a40abf067`  
		Last Modified: Thu, 30 May 2024 22:47:26 GMT  
		Size: 3.6 KB (3619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d72f2303e5096aaa6f9553a85b544aea1399ec8a15560fab4adf4ad2190ca9`  
		Last Modified: Thu, 30 May 2024 22:47:31 GMT  
		Size: 120.2 MB (120173529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be3c7148b3af9ac779b55f1613f835ca7371df7b5579ad80f48f78ce0fbcbb5`  
		Last Modified: Thu, 30 May 2024 22:47:27 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2` - unknown; unknown

```console
$ docker pull bonita@sha256:971a7460c800fc1b94189e8d3f49b33e96fd8944c151d6014d88e42aba0bcdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1670227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ee0fafe5cd2c8df5dd3fbd33d5e9790c42c5ed70f43fb35976f70ccbbf9034`

```dockerfile
```

-	Layers:
	-	`sha256:301a1d875fe7faadd16c2a2938d74f9d98796674271747b221fcc9f66cf4c75d`  
		Last Modified: Thu, 30 May 2024 22:47:26 GMT  
		Size: 1.6 MB (1646948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4e8b89806b1e6fb4838e750e8ca8c7332f6e4b141f1e232b3ed368e938bb4e3`  
		Last Modified: Thu, 30 May 2024 22:47:25 GMT  
		Size: 23.3 KB (23279 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:3f6f725ab540006e337c624ddfed06bf4f4a73c4cbd08bc6103d6b3364dec5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188168435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0174cbd2be50fb8229b18c634fb905a0f548e80ba439e085edee62b554da1e21`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
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
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933ff233d80cafb23c8a39848655bb56717ee42eb569bd4ea086353663c213a7`  
		Last Modified: Thu, 30 May 2024 21:20:32 GMT  
		Size: 64.6 MB (64635683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e757faaf12567aef4eec6da6cec4ab7bbc3eb8678ce535cef291a7cbd4fa0d0`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c61f7cf0753303a85183089124599110f03375fb4d00490670ef83c39b2ed5`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128bee974bb009822e9dafc758aef7554a938b86c8db2c429df75efb161dd527`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4b4ae7263be86be00817b6013083ee78e2cf36ae577e016350c1fd09451125`  
		Last Modified: Thu, 30 May 2024 21:20:30 GMT  
		Size: 3.6 KB (3621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2964913bb9ac303033fe83ee911d05fc8e6d61aae73f331786f4b5ce031f7c11`  
		Last Modified: Thu, 30 May 2024 21:20:35 GMT  
		Size: 120.2 MB (120173541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4763f45736d51fa964cdfa12b10129215ea217754ee2561a67429b2b87f3c5d6`  
		Last Modified: Thu, 30 May 2024 21:20:31 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2` - unknown; unknown

```console
$ docker pull bonita@sha256:a6104abe671436f6654124942b1f13b0b7d3a8c1235aea503f5aad1872bf063f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1667972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05505caf88255fdfdcadd81b788a6db382832f5ce2ed1a895031fec025196435`

```dockerfile
```

-	Layers:
	-	`sha256:96044e0fcd1342720b92fd842763bfafb32139a892604eb783d4a1c6874bfd0e`  
		Last Modified: Thu, 30 May 2024 21:20:30 GMT  
		Size: 1.6 MB (1644953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4abb8d6fb0ef88498dd4cd039aeb116c435850adb9b6d2c1a10ec8913b4992a6`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 23.0 KB (23019 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.2-u0`

```console
$ docker pull bonita@sha256:4655db3ee6308e3c00eb8f8c8e15fe494b7e7a2c98a5904b769be02129001c11
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
$ docker pull bonita@sha256:8885231f41ccefd4e873f2f807eeb2baced5708542e03085bb9388adccb6173e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191304430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d759f5d9811ac2bae2d1721abb082534cd145c928138cdd4a76b9b16f758d74c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf82cc3502f0dd9f68d96420f0dd34810219d98cee64d432da56905baf3d1ff`  
		Last Modified: Thu, 30 May 2024 22:47:28 GMT  
		Size: 67.8 MB (67786817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a8187e3a4e7ddc58b264bb94ac11f2d2328df254d766a89c0b3be4807e60bd`  
		Last Modified: Thu, 30 May 2024 22:47:25 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e96e75cf2398095e1a75dbf7bccf297438cfbc4531c11773890e153370e662`  
		Last Modified: Thu, 30 May 2024 22:47:25 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7157b7cbe66932baa94bc8bc980b51386093b171b56a2ed99979a9c111fdca34`  
		Last Modified: Thu, 30 May 2024 22:47:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c36c4c5b4ac2b281b949f1f1922d2231a54a94c38ff2b08847a866a40abf067`  
		Last Modified: Thu, 30 May 2024 22:47:26 GMT  
		Size: 3.6 KB (3619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d72f2303e5096aaa6f9553a85b544aea1399ec8a15560fab4adf4ad2190ca9`  
		Last Modified: Thu, 30 May 2024 22:47:31 GMT  
		Size: 120.2 MB (120173529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be3c7148b3af9ac779b55f1613f835ca7371df7b5579ad80f48f78ce0fbcbb5`  
		Last Modified: Thu, 30 May 2024 22:47:27 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:971a7460c800fc1b94189e8d3f49b33e96fd8944c151d6014d88e42aba0bcdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1670227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ee0fafe5cd2c8df5dd3fbd33d5e9790c42c5ed70f43fb35976f70ccbbf9034`

```dockerfile
```

-	Layers:
	-	`sha256:301a1d875fe7faadd16c2a2938d74f9d98796674271747b221fcc9f66cf4c75d`  
		Last Modified: Thu, 30 May 2024 22:47:26 GMT  
		Size: 1.6 MB (1646948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4e8b89806b1e6fb4838e750e8ca8c7332f6e4b141f1e232b3ed368e938bb4e3`  
		Last Modified: Thu, 30 May 2024 22:47:25 GMT  
		Size: 23.3 KB (23279 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:3f6f725ab540006e337c624ddfed06bf4f4a73c4cbd08bc6103d6b3364dec5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188168435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0174cbd2be50fb8229b18c634fb905a0f548e80ba439e085edee62b554da1e21`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
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
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933ff233d80cafb23c8a39848655bb56717ee42eb569bd4ea086353663c213a7`  
		Last Modified: Thu, 30 May 2024 21:20:32 GMT  
		Size: 64.6 MB (64635683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e757faaf12567aef4eec6da6cec4ab7bbc3eb8678ce535cef291a7cbd4fa0d0`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c61f7cf0753303a85183089124599110f03375fb4d00490670ef83c39b2ed5`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128bee974bb009822e9dafc758aef7554a938b86c8db2c429df75efb161dd527`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4b4ae7263be86be00817b6013083ee78e2cf36ae577e016350c1fd09451125`  
		Last Modified: Thu, 30 May 2024 21:20:30 GMT  
		Size: 3.6 KB (3621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2964913bb9ac303033fe83ee911d05fc8e6d61aae73f331786f4b5ce031f7c11`  
		Last Modified: Thu, 30 May 2024 21:20:35 GMT  
		Size: 120.2 MB (120173541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4763f45736d51fa964cdfa12b10129215ea217754ee2561a67429b2b87f3c5d6`  
		Last Modified: Thu, 30 May 2024 21:20:31 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:a6104abe671436f6654124942b1f13b0b7d3a8c1235aea503f5aad1872bf063f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1667972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05505caf88255fdfdcadd81b788a6db382832f5ce2ed1a895031fec025196435`

```dockerfile
```

-	Layers:
	-	`sha256:96044e0fcd1342720b92fd842763bfafb32139a892604eb783d4a1c6874bfd0e`  
		Last Modified: Thu, 30 May 2024 21:20:30 GMT  
		Size: 1.6 MB (1644953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4abb8d6fb0ef88498dd4cd039aeb116c435850adb9b6d2c1a10ec8913b4992a6`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 23.0 KB (23019 bytes)  
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
$ docker pull bonita@sha256:29f543c3666b99a28017c80e97f1591a264db829239eadeefa31852b0e12c3ec
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
$ docker pull bonita@sha256:30079b8615151fd888c3abf7b9733190504977e0ab2630636b609728372bbdfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182573601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3d43a48e464b8894ebc9c932e63a38c089d6a08cafb112e73d546adf6b34cc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
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
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0502c1826d837d828ee506bf8f3f13428fe6205cd4a434a3588fda6d9b1a635e`  
		Last Modified: Thu, 30 May 2024 22:46:44 GMT  
		Size: 61.1 MB (61126449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78d0090e73117ea6b94074085b67fcf2a86507a09cd1f874f670453a6149809`  
		Last Modified: Thu, 30 May 2024 22:46:42 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1091f3c5b3e2b4dd0222543a3f1a1c571876df870b5221888e4ce89596db15af`  
		Last Modified: Thu, 30 May 2024 22:46:41 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d4290bf86de7a9efb4b8ce3b14a11e00efacf96515f85051f01cc8a84856a`  
		Last Modified: Thu, 30 May 2024 22:46:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60470cd7e3fe739380acb2e108dc5dee66b46532c7cd4e6c17cfca269521585`  
		Last Modified: Thu, 30 May 2024 22:46:43 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b2167dc14d94bd8cc91a151c662d03c66816144f75755f4ef2a483feffbfb3`  
		Last Modified: Thu, 30 May 2024 22:46:46 GMT  
		Size: 118.2 MB (118178575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1cb471eb013475d8411b75fd4b53a0bb04b0b19098f782986668b0832d7474`  
		Last Modified: Thu, 30 May 2024 22:46:43 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0` - unknown; unknown

```console
$ docker pull bonita@sha256:073ed1b15b8b3a429ee571774bf1906ddc4d1ed990a2eb01cb139941e9cdc44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6aceca2947fedefab474f4a3ae263df728a55d9c12daecc6ce09c0bd2a79b3a`

```dockerfile
```

-	Layers:
	-	`sha256:a8619873e6673cd6641103e16d130a1758bc6cea1a66a190eccce3c921b1d789`  
		Last Modified: Thu, 30 May 2024 22:46:42 GMT  
		Size: 819.2 KB (819232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4648bceb37b0d8e3cf1ecdfdb5445890552622873ce190aad1b3b1ae839080`  
		Last Modified: Thu, 30 May 2024 22:46:42 GMT  
		Size: 23.5 KB (23489 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:8.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:4c8690f24745794ba67cc276ccc8075fb47c829be4728f6570cf10dd0d33b307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179610318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13ec471c219b9d72f4473d771a0d6b8f1c92447fe0f7b98b570bd58545b1e09`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
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
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3555b0d2356ad5e27bb1167bec88a85252d0c80f688e1c8aab8b47cf2517d67d`  
		Last Modified: Thu, 30 May 2024 21:19:07 GMT  
		Size: 58.0 MB (58029322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05393a21a1f62ec4ec5c300b04c646aaafab1dfeb8059ed9768ffbe0ddac8069`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14baace67657acc4abcd9a81efb25927fc271bb8a5ee3fcd05030b735f982809`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919e82e7af965d43cec612645ef9a35e1b9b4e117d679487485fe668594f56f7`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab5c81aa774a9dcd37b5bc5147884779c3940fc6e15a21d2fc0adf4140a1029`  
		Last Modified: Thu, 30 May 2024 21:19:06 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cc4818f9afebf85690bf76ebe2b10890ba92ab25cfd99604103962b6c448a3`  
		Last Modified: Thu, 30 May 2024 21:19:11 GMT  
		Size: 118.2 MB (118178592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656497dcfb57ffb6c0244c47b46a6f239639898e097255e89f04ab593e789550`  
		Last Modified: Thu, 30 May 2024 21:19:07 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0` - unknown; unknown

```console
$ docker pull bonita@sha256:9a8c26e0e62a9ebe144d85d6a6dfccd316e6f14429e9cea37a9ad288f4b64fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.5 KB (840495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfccd9b7527cc03977ba497120ddc05a1dc78fff6bd53ba86f8cfcb84dc7e1e`

```dockerfile
```

-	Layers:
	-	`sha256:a7035582f39c0f59080e12e820dba0d7dda2e525e08b322b422a180fff42c163`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 817.3 KB (817260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad77c527c8f67713bb9ff7b0f4bd454e588268889bddad983200b276cc4b078a`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 23.2 KB (23235 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:8.0.0`

```console
$ docker pull bonita@sha256:29f543c3666b99a28017c80e97f1591a264db829239eadeefa31852b0e12c3ec
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
$ docker pull bonita@sha256:30079b8615151fd888c3abf7b9733190504977e0ab2630636b609728372bbdfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182573601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3d43a48e464b8894ebc9c932e63a38c089d6a08cafb112e73d546adf6b34cc`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
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
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0502c1826d837d828ee506bf8f3f13428fe6205cd4a434a3588fda6d9b1a635e`  
		Last Modified: Thu, 30 May 2024 22:46:44 GMT  
		Size: 61.1 MB (61126449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78d0090e73117ea6b94074085b67fcf2a86507a09cd1f874f670453a6149809`  
		Last Modified: Thu, 30 May 2024 22:46:42 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1091f3c5b3e2b4dd0222543a3f1a1c571876df870b5221888e4ce89596db15af`  
		Last Modified: Thu, 30 May 2024 22:46:41 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d4290bf86de7a9efb4b8ce3b14a11e00efacf96515f85051f01cc8a84856a`  
		Last Modified: Thu, 30 May 2024 22:46:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60470cd7e3fe739380acb2e108dc5dee66b46532c7cd4e6c17cfca269521585`  
		Last Modified: Thu, 30 May 2024 22:46:43 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b2167dc14d94bd8cc91a151c662d03c66816144f75755f4ef2a483feffbfb3`  
		Last Modified: Thu, 30 May 2024 22:46:46 GMT  
		Size: 118.2 MB (118178575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1cb471eb013475d8411b75fd4b53a0bb04b0b19098f782986668b0832d7474`  
		Last Modified: Thu, 30 May 2024 22:46:43 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:073ed1b15b8b3a429ee571774bf1906ddc4d1ed990a2eb01cb139941e9cdc44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6aceca2947fedefab474f4a3ae263df728a55d9c12daecc6ce09c0bd2a79b3a`

```dockerfile
```

-	Layers:
	-	`sha256:a8619873e6673cd6641103e16d130a1758bc6cea1a66a190eccce3c921b1d789`  
		Last Modified: Thu, 30 May 2024 22:46:42 GMT  
		Size: 819.2 KB (819232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe4648bceb37b0d8e3cf1ecdfdb5445890552622873ce190aad1b3b1ae839080`  
		Last Modified: Thu, 30 May 2024 22:46:42 GMT  
		Size: 23.5 KB (23489 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:8.0.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:4c8690f24745794ba67cc276ccc8075fb47c829be4728f6570cf10dd0d33b307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179610318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13ec471c219b9d72f4473d771a0d6b8f1c92447fe0f7b98b570bd58545b1e09`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 15 Nov 2023 09:31:00 GMT
ADD file:142556ae6fb4078ff8df7cd88ef4f1d91b27167561c6e93ceeee4d9a87677a22 in / 
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
	-	`sha256:c4bf8831607f5d219b98313740266d85a75f3b24c83a4db919b24cc51c6da633`  
		Last Modified: Sat, 27 Jan 2024 00:28:35 GMT  
		Size: 3.4 MB (3392106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3555b0d2356ad5e27bb1167bec88a85252d0c80f688e1c8aab8b47cf2517d67d`  
		Last Modified: Thu, 30 May 2024 21:19:07 GMT  
		Size: 58.0 MB (58029322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05393a21a1f62ec4ec5c300b04c646aaafab1dfeb8059ed9768ffbe0ddac8069`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14baace67657acc4abcd9a81efb25927fc271bb8a5ee3fcd05030b735f982809`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919e82e7af965d43cec612645ef9a35e1b9b4e117d679487485fe668594f56f7`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab5c81aa774a9dcd37b5bc5147884779c3940fc6e15a21d2fc0adf4140a1029`  
		Last Modified: Thu, 30 May 2024 21:19:06 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cc4818f9afebf85690bf76ebe2b10890ba92ab25cfd99604103962b6c448a3`  
		Last Modified: Thu, 30 May 2024 21:19:11 GMT  
		Size: 118.2 MB (118178592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656497dcfb57ffb6c0244c47b46a6f239639898e097255e89f04ab593e789550`  
		Last Modified: Thu, 30 May 2024 21:19:07 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:9a8c26e0e62a9ebe144d85d6a6dfccd316e6f14429e9cea37a9ad288f4b64fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.5 KB (840495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfccd9b7527cc03977ba497120ddc05a1dc78fff6bd53ba86f8cfcb84dc7e1e`

```dockerfile
```

-	Layers:
	-	`sha256:a7035582f39c0f59080e12e820dba0d7dda2e525e08b322b422a180fff42c163`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 817.3 KB (817260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad77c527c8f67713bb9ff7b0f4bd454e588268889bddad983200b276cc4b078a`  
		Last Modified: Thu, 30 May 2024 21:19:05 GMT  
		Size: 23.2 KB (23235 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:9.0`

```console
$ docker pull bonita@sha256:4655db3ee6308e3c00eb8f8c8e15fe494b7e7a2c98a5904b769be02129001c11
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
$ docker pull bonita@sha256:8885231f41ccefd4e873f2f807eeb2baced5708542e03085bb9388adccb6173e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191304430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d759f5d9811ac2bae2d1721abb082534cd145c928138cdd4a76b9b16f758d74c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf82cc3502f0dd9f68d96420f0dd34810219d98cee64d432da56905baf3d1ff`  
		Last Modified: Thu, 30 May 2024 22:47:28 GMT  
		Size: 67.8 MB (67786817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a8187e3a4e7ddc58b264bb94ac11f2d2328df254d766a89c0b3be4807e60bd`  
		Last Modified: Thu, 30 May 2024 22:47:25 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e96e75cf2398095e1a75dbf7bccf297438cfbc4531c11773890e153370e662`  
		Last Modified: Thu, 30 May 2024 22:47:25 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7157b7cbe66932baa94bc8bc980b51386093b171b56a2ed99979a9c111fdca34`  
		Last Modified: Thu, 30 May 2024 22:47:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c36c4c5b4ac2b281b949f1f1922d2231a54a94c38ff2b08847a866a40abf067`  
		Last Modified: Thu, 30 May 2024 22:47:26 GMT  
		Size: 3.6 KB (3619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d72f2303e5096aaa6f9553a85b544aea1399ec8a15560fab4adf4ad2190ca9`  
		Last Modified: Thu, 30 May 2024 22:47:31 GMT  
		Size: 120.2 MB (120173529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be3c7148b3af9ac779b55f1613f835ca7371df7b5579ad80f48f78ce0fbcbb5`  
		Last Modified: Thu, 30 May 2024 22:47:27 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0` - unknown; unknown

```console
$ docker pull bonita@sha256:971a7460c800fc1b94189e8d3f49b33e96fd8944c151d6014d88e42aba0bcdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1670227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ee0fafe5cd2c8df5dd3fbd33d5e9790c42c5ed70f43fb35976f70ccbbf9034`

```dockerfile
```

-	Layers:
	-	`sha256:301a1d875fe7faadd16c2a2938d74f9d98796674271747b221fcc9f66cf4c75d`  
		Last Modified: Thu, 30 May 2024 22:47:26 GMT  
		Size: 1.6 MB (1646948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4e8b89806b1e6fb4838e750e8ca8c7332f6e4b141f1e232b3ed368e938bb4e3`  
		Last Modified: Thu, 30 May 2024 22:47:25 GMT  
		Size: 23.3 KB (23279 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:9.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:3f6f725ab540006e337c624ddfed06bf4f4a73c4cbd08bc6103d6b3364dec5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188168435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0174cbd2be50fb8229b18c634fb905a0f548e80ba439e085edee62b554da1e21`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
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
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933ff233d80cafb23c8a39848655bb56717ee42eb569bd4ea086353663c213a7`  
		Last Modified: Thu, 30 May 2024 21:20:32 GMT  
		Size: 64.6 MB (64635683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e757faaf12567aef4eec6da6cec4ab7bbc3eb8678ce535cef291a7cbd4fa0d0`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c61f7cf0753303a85183089124599110f03375fb4d00490670ef83c39b2ed5`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128bee974bb009822e9dafc758aef7554a938b86c8db2c429df75efb161dd527`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4b4ae7263be86be00817b6013083ee78e2cf36ae577e016350c1fd09451125`  
		Last Modified: Thu, 30 May 2024 21:20:30 GMT  
		Size: 3.6 KB (3621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2964913bb9ac303033fe83ee911d05fc8e6d61aae73f331786f4b5ce031f7c11`  
		Last Modified: Thu, 30 May 2024 21:20:35 GMT  
		Size: 120.2 MB (120173541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4763f45736d51fa964cdfa12b10129215ea217754ee2561a67429b2b87f3c5d6`  
		Last Modified: Thu, 30 May 2024 21:20:31 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0` - unknown; unknown

```console
$ docker pull bonita@sha256:a6104abe671436f6654124942b1f13b0b7d3a8c1235aea503f5aad1872bf063f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1667972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05505caf88255fdfdcadd81b788a6db382832f5ce2ed1a895031fec025196435`

```dockerfile
```

-	Layers:
	-	`sha256:96044e0fcd1342720b92fd842763bfafb32139a892604eb783d4a1c6874bfd0e`  
		Last Modified: Thu, 30 May 2024 21:20:30 GMT  
		Size: 1.6 MB (1644953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4abb8d6fb0ef88498dd4cd039aeb116c435850adb9b6d2c1a10ec8913b4992a6`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 23.0 KB (23019 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:9.0.0`

```console
$ docker pull bonita@sha256:4655db3ee6308e3c00eb8f8c8e15fe494b7e7a2c98a5904b769be02129001c11
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
$ docker pull bonita@sha256:8885231f41ccefd4e873f2f807eeb2baced5708542e03085bb9388adccb6173e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191304430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d759f5d9811ac2bae2d1721abb082534cd145c928138cdd4a76b9b16f758d74c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf82cc3502f0dd9f68d96420f0dd34810219d98cee64d432da56905baf3d1ff`  
		Last Modified: Thu, 30 May 2024 22:47:28 GMT  
		Size: 67.8 MB (67786817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a8187e3a4e7ddc58b264bb94ac11f2d2328df254d766a89c0b3be4807e60bd`  
		Last Modified: Thu, 30 May 2024 22:47:25 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e96e75cf2398095e1a75dbf7bccf297438cfbc4531c11773890e153370e662`  
		Last Modified: Thu, 30 May 2024 22:47:25 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7157b7cbe66932baa94bc8bc980b51386093b171b56a2ed99979a9c111fdca34`  
		Last Modified: Thu, 30 May 2024 22:47:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c36c4c5b4ac2b281b949f1f1922d2231a54a94c38ff2b08847a866a40abf067`  
		Last Modified: Thu, 30 May 2024 22:47:26 GMT  
		Size: 3.6 KB (3619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d72f2303e5096aaa6f9553a85b544aea1399ec8a15560fab4adf4ad2190ca9`  
		Last Modified: Thu, 30 May 2024 22:47:31 GMT  
		Size: 120.2 MB (120173529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be3c7148b3af9ac779b55f1613f835ca7371df7b5579ad80f48f78ce0fbcbb5`  
		Last Modified: Thu, 30 May 2024 22:47:27 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:971a7460c800fc1b94189e8d3f49b33e96fd8944c151d6014d88e42aba0bcdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1670227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ee0fafe5cd2c8df5dd3fbd33d5e9790c42c5ed70f43fb35976f70ccbbf9034`

```dockerfile
```

-	Layers:
	-	`sha256:301a1d875fe7faadd16c2a2938d74f9d98796674271747b221fcc9f66cf4c75d`  
		Last Modified: Thu, 30 May 2024 22:47:26 GMT  
		Size: 1.6 MB (1646948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4e8b89806b1e6fb4838e750e8ca8c7332f6e4b141f1e232b3ed368e938bb4e3`  
		Last Modified: Thu, 30 May 2024 22:47:25 GMT  
		Size: 23.3 KB (23279 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:9.0.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:3f6f725ab540006e337c624ddfed06bf4f4a73c4cbd08bc6103d6b3364dec5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188168435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0174cbd2be50fb8229b18c634fb905a0f548e80ba439e085edee62b554da1e21`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
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
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933ff233d80cafb23c8a39848655bb56717ee42eb569bd4ea086353663c213a7`  
		Last Modified: Thu, 30 May 2024 21:20:32 GMT  
		Size: 64.6 MB (64635683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e757faaf12567aef4eec6da6cec4ab7bbc3eb8678ce535cef291a7cbd4fa0d0`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c61f7cf0753303a85183089124599110f03375fb4d00490670ef83c39b2ed5`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128bee974bb009822e9dafc758aef7554a938b86c8db2c429df75efb161dd527`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4b4ae7263be86be00817b6013083ee78e2cf36ae577e016350c1fd09451125`  
		Last Modified: Thu, 30 May 2024 21:20:30 GMT  
		Size: 3.6 KB (3621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2964913bb9ac303033fe83ee911d05fc8e6d61aae73f331786f4b5ce031f7c11`  
		Last Modified: Thu, 30 May 2024 21:20:35 GMT  
		Size: 120.2 MB (120173541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4763f45736d51fa964cdfa12b10129215ea217754ee2561a67429b2b87f3c5d6`  
		Last Modified: Thu, 30 May 2024 21:20:31 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:a6104abe671436f6654124942b1f13b0b7d3a8c1235aea503f5aad1872bf063f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1667972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05505caf88255fdfdcadd81b788a6db382832f5ce2ed1a895031fec025196435`

```dockerfile
```

-	Layers:
	-	`sha256:96044e0fcd1342720b92fd842763bfafb32139a892604eb783d4a1c6874bfd0e`  
		Last Modified: Thu, 30 May 2024 21:20:30 GMT  
		Size: 1.6 MB (1644953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4abb8d6fb0ef88498dd4cd039aeb116c435850adb9b6d2c1a10ec8913b4992a6`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 23.0 KB (23019 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:latest`

```console
$ docker pull bonita@sha256:4655db3ee6308e3c00eb8f8c8e15fe494b7e7a2c98a5904b769be02129001c11
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
$ docker pull bonita@sha256:8885231f41ccefd4e873f2f807eeb2baced5708542e03085bb9388adccb6173e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191304430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d759f5d9811ac2bae2d1721abb082534cd145c928138cdd4a76b9b16f758d74c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf82cc3502f0dd9f68d96420f0dd34810219d98cee64d432da56905baf3d1ff`  
		Last Modified: Thu, 30 May 2024 22:47:28 GMT  
		Size: 67.8 MB (67786817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a8187e3a4e7ddc58b264bb94ac11f2d2328df254d766a89c0b3be4807e60bd`  
		Last Modified: Thu, 30 May 2024 22:47:25 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e96e75cf2398095e1a75dbf7bccf297438cfbc4531c11773890e153370e662`  
		Last Modified: Thu, 30 May 2024 22:47:25 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7157b7cbe66932baa94bc8bc980b51386093b171b56a2ed99979a9c111fdca34`  
		Last Modified: Thu, 30 May 2024 22:47:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c36c4c5b4ac2b281b949f1f1922d2231a54a94c38ff2b08847a866a40abf067`  
		Last Modified: Thu, 30 May 2024 22:47:26 GMT  
		Size: 3.6 KB (3619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d72f2303e5096aaa6f9553a85b544aea1399ec8a15560fab4adf4ad2190ca9`  
		Last Modified: Thu, 30 May 2024 22:47:31 GMT  
		Size: 120.2 MB (120173529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be3c7148b3af9ac779b55f1613f835ca7371df7b5579ad80f48f78ce0fbcbb5`  
		Last Modified: Thu, 30 May 2024 22:47:27 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:latest` - unknown; unknown

```console
$ docker pull bonita@sha256:971a7460c800fc1b94189e8d3f49b33e96fd8944c151d6014d88e42aba0bcdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1670227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ee0fafe5cd2c8df5dd3fbd33d5e9790c42c5ed70f43fb35976f70ccbbf9034`

```dockerfile
```

-	Layers:
	-	`sha256:301a1d875fe7faadd16c2a2938d74f9d98796674271747b221fcc9f66cf4c75d`  
		Last Modified: Thu, 30 May 2024 22:47:26 GMT  
		Size: 1.6 MB (1646948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4e8b89806b1e6fb4838e750e8ca8c7332f6e4b141f1e232b3ed368e938bb4e3`  
		Last Modified: Thu, 30 May 2024 22:47:25 GMT  
		Size: 23.3 KB (23279 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:3f6f725ab540006e337c624ddfed06bf4f4a73c4cbd08bc6103d6b3364dec5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188168435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0174cbd2be50fb8229b18c634fb905a0f548e80ba439e085edee62b554da1e21`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
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
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933ff233d80cafb23c8a39848655bb56717ee42eb569bd4ea086353663c213a7`  
		Last Modified: Thu, 30 May 2024 21:20:32 GMT  
		Size: 64.6 MB (64635683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e757faaf12567aef4eec6da6cec4ab7bbc3eb8678ce535cef291a7cbd4fa0d0`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c61f7cf0753303a85183089124599110f03375fb4d00490670ef83c39b2ed5`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128bee974bb009822e9dafc758aef7554a938b86c8db2c429df75efb161dd527`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4b4ae7263be86be00817b6013083ee78e2cf36ae577e016350c1fd09451125`  
		Last Modified: Thu, 30 May 2024 21:20:30 GMT  
		Size: 3.6 KB (3621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2964913bb9ac303033fe83ee911d05fc8e6d61aae73f331786f4b5ce031f7c11`  
		Last Modified: Thu, 30 May 2024 21:20:35 GMT  
		Size: 120.2 MB (120173541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4763f45736d51fa964cdfa12b10129215ea217754ee2561a67429b2b87f3c5d6`  
		Last Modified: Thu, 30 May 2024 21:20:31 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:latest` - unknown; unknown

```console
$ docker pull bonita@sha256:a6104abe671436f6654124942b1f13b0b7d3a8c1235aea503f5aad1872bf063f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1667972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05505caf88255fdfdcadd81b788a6db382832f5ce2ed1a895031fec025196435`

```dockerfile
```

-	Layers:
	-	`sha256:96044e0fcd1342720b92fd842763bfafb32139a892604eb783d4a1c6874bfd0e`  
		Last Modified: Thu, 30 May 2024 21:20:30 GMT  
		Size: 1.6 MB (1644953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4abb8d6fb0ef88498dd4cd039aeb116c435850adb9b6d2c1a10ec8913b4992a6`  
		Last Modified: Thu, 30 May 2024 21:20:29 GMT  
		Size: 23.0 KB (23019 bytes)  
		MIME: application/vnd.in-toto+json
