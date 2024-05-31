## `bonita:latest`

```console
$ docker pull bonita@sha256:3a9d88cb4d54684867374c0678e5f1f57d2980a0c4e85eeff73218a3174332cc
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
$ docker pull bonita@sha256:af2cb7430e8b5571bd958152fea93145c5c2255ad6d61651707a53e6f34a6b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191493413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9e910f067414221442bae5ee460987386b7ddafec2881c1429142350e92db5`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Thu, 16 Nov 2023 12:46:16 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1939637fb5155a60273f87945de2661e04a0a52dcc0c05278b87d189de23f65e`  
		Last Modified: Thu, 30 May 2024 20:56:17 GMT  
		Size: 67.9 MB (67906631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4b4524fe3cdda8f1152508d939ea79bb1ed82040b58b68afa8546f9a70cf4b`  
		Last Modified: Thu, 30 May 2024 20:56:16 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d093700972a77e8dad952ce3ebbe675e8c0f5e4495c135769288b725eea6b10`  
		Last Modified: Thu, 30 May 2024 20:56:16 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bee88caeaecf09e6e13d76086cade5f6702ec24cc0c0fe35b0107aeb245bb16`  
		Last Modified: Thu, 30 May 2024 20:56:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0419741fb22a6428dafec644a0d48b9b8bbe4290083d6fa0e30a311441ae25`  
		Last Modified: Thu, 30 May 2024 20:56:17 GMT  
		Size: 3.6 KB (3620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0042af743acf58281ab9462fb2e7e13991875cee35184c824564ed6824053dcc`  
		Last Modified: Thu, 30 May 2024 20:56:19 GMT  
		Size: 120.2 MB (120173518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b721a8666a5600e6e92e655e95837ea4447c786124180303c19a110b74db61ce`  
		Last Modified: Thu, 30 May 2024 20:56:17 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:latest` - unknown; unknown

```console
$ docker pull bonita@sha256:e72c00069a2890877e6e317c79dc3f467c3eaf81d4eebb0e2411abb86ba02f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1670807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae3c879f81f9d5da670d88e2b97e5bd32a42dfd6a3640b7bb67d7ab0e3dae8c`

```dockerfile
```

-	Layers:
	-	`sha256:1e655b58c49843ac878f758132b78343ea118a168c5c6038f559f7cf330a9295`  
		Last Modified: Thu, 30 May 2024 20:56:17 GMT  
		Size: 1.6 MB (1647840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75c1f26220831a99f7bfd06a7be2fb72878ee991a2a35c8a245ab0d6c7b078c6`  
		Last Modified: Thu, 30 May 2024 20:56:16 GMT  
		Size: 23.0 KB (22967 bytes)  
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
