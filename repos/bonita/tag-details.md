<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `bonita`

-	[`bonita:2022.2`](#bonita20222)
-	[`bonita:2022.2-u0`](#bonita20222-u0)
-	[`bonita:2023.1`](#bonita20231)
-	[`bonita:2023.1-u0`](#bonita20231-u0)
-	[`bonita:2023.2`](#bonita20232)
-	[`bonita:2023.2-u0`](#bonita20232-u0)
-	[`bonita:7.15`](#bonita715)
-	[`bonita:7.15.0`](#bonita7150)
-	[`bonita:8.0`](#bonita80)
-	[`bonita:8.0.0`](#bonita800)
-	[`bonita:9.0`](#bonita90)
-	[`bonita:9.0.0`](#bonita900)
-	[`bonita:latest`](#bonitalatest)

## `bonita:2022.2`

```console
$ docker pull bonita@sha256:1c6a430928094bea86483958321eaa193d6d2ae63db01655ec5bc8814ccd4767
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
$ docker pull bonita@sha256:408e48996441391ffdd5b55248842416222d57110cfb8ce1b00cb0ab53ecbda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185539058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b596e7835378ff74882336593745a3fd6b65f517561fae7329d78c133aaf0b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e26d36434872ada6f212bf9c46fcee0c81376cbc455c4a373bb2dc878b9633`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 62.7 MB (62715912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d3c2310cb1029eeeb9a2c960cf4b96d7aa6fa2ff757b7d67d56528044ba383`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d272f1eaec9bda81395eb0d0af7d165db3cb97d0b6d409034ff9b816bdb7cd`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54f9c4205c383bc8148313c575377f20b383a7bef2ffc03ba4efedfde0828ce`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcadc120dc91b9dae7dbd4b5cb59bfdc5dc4043646cba759e07009b1c53198d`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 3.0 KB (2996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3156f69fba57e572e4bc26d14b1e751c11957a6d48260fd0f8c9046abc55c0dd`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 119.2 MB (119190675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61341086aead62bd41bd009b8b2247cc16aebecbcc1abe122959f5218d65b3c`  
		Last Modified: Mon, 22 Jul 2024 23:03:21 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2` - unknown; unknown

```console
$ docker pull bonita@sha256:f577a51518e1723fc441f4ff54649e12e91e2e6494f22c063b3985ed6901b67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **896.2 KB (896170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2d02d7dcd40a8440b8704c9a274e686aed6217b5f5fe2c21c5807fc877b6f2`

```dockerfile
```

-	Layers:
	-	`sha256:507d38c8211dc67faf13198b25c36e6b68b5ac1ad8d3d1a77fbdbb5dd50160b9`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 873.1 KB (873107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:820bacf2e755700862418681608ad660c541b211e6add38549ae3e5be8a89d45`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 23.1 KB (23063 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:a94dfcbd34bbf22ccddb13885c031196a1f42777fbeced23b2e1685b093f3427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185948693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2363d8729960e288ca2ad0146c4039fec58047648aeb2794941a88cf34c83c9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18a3131c341fa1d83f7e179e98ac72f1d0957f5ae99aa479b0bf4f3906e43e`  
		Last Modified: Tue, 23 Jul 2024 11:38:28 GMT  
		Size: 62.7 MB (62661473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a38e61750bc70d8a8687f015c32ff4caa6300d22f28b0f62fc4bc2fc3c876f`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d683c6aa3700af9f85bfccb37ab2e046f86dfad938a7cc9075fa11c730c80b6f`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ed0844ebdd1daee4cd96134d1d7a13dbb8ce41803adf8563c66f3977b69e5d`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54548f17b7cc1954972f4cb3ac364372de44aad7cbaa1724b482c93c6c6d93f`  
		Last Modified: Tue, 23 Jul 2024 11:38:27 GMT  
		Size: 3.0 KB (2995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bb75c815d1a199ec048c29bda8a6b530fa2e6686096a2304dbd9e72ef876c0`  
		Last Modified: Tue, 23 Jul 2024 11:38:30 GMT  
		Size: 119.2 MB (119190707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12c67a94de2d10fde21abe23af5776a48e19b95a4307513fc8dcdb7d3fb4bff`  
		Last Modified: Tue, 23 Jul 2024 11:38:27 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2` - unknown; unknown

```console
$ docker pull bonita@sha256:3aae030b860fa6538b6f2358be0160efcbaaa8c3727b4b4d248da378d6f85ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **895.5 KB (895525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac930e2b87335cfeca9d928d194ca285b18cec5ee1d8afc13939c061edc1ce7`

```dockerfile
```

-	Layers:
	-	`sha256:32331d13e18293e73b9255484762f2eb33d6cd839620df855bf8fd5869fd11a3`  
		Last Modified: Tue, 23 Jul 2024 11:38:27 GMT  
		Size: 872.2 KB (872162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28ffdd3a2677f8c3c58679d9740c4383e49a1c209433fd390306032bd4586278`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 23.4 KB (23363 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:9d0b6636bb12df79f37652872ebe94a7bf83dccd47c40082a4af3d60f250ec09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (181967625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeab47586cf3126573e558a7776ee7d7f0d0680c4afe40e8f9e2e486ef54b278`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f00defe5ad3922145736c51f873742d6339a6f7ce8f4eedcdd1322be46fcb9`  
		Last Modified: Tue, 23 Jul 2024 08:32:19 GMT  
		Size: 59.2 MB (59195818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec3dfaf5507de2b003060a953a25c7cf3bac4cddff4a2c509e10482d785eec5`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1895696360e6ddf12000c5e8f253b278e925b713b40229d01fb1e291b6fd26a7`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96b402cdb3108c7ea9d20fdc2fa786837f0b8753aea4ad22e262ddc5308a3f3`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d5a65e52d60b80dd56a2435a2b7a5b3aedaf0129bf7b4318cb6e867df84004`  
		Last Modified: Tue, 23 Jul 2024 08:32:18 GMT  
		Size: 3.0 KB (2995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf012b2af3f1e9767f4ad118224d6899f8604827004a977d8c001359782cc78`  
		Last Modified: Tue, 23 Jul 2024 08:32:21 GMT  
		Size: 119.2 MB (119190675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876e535d711745c23fbaf59abeaa2e56a54ccf724870c54a77a194cdbcfe5465`  
		Last Modified: Tue, 23 Jul 2024 08:32:18 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2` - unknown; unknown

```console
$ docker pull bonita@sha256:8b30a5ba15de9e8bfb176ba7476cbfb63d5c8f8f65132c4907f2419150bff36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **893.3 KB (893336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b02307df656a9829c8ae05af9c5c4b1cd4942adfc26b2e2a8f18093b3c7e5f`

```dockerfile
```

-	Layers:
	-	`sha256:5cb67e7a1fcb034eb8d89214aa2eed18affa4166a241ed233b1bff37909337a7`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 870.2 KB (870227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abf05205c44e6d5b64c43f4f9a07046e79ad5eaf3a16ff1496f90c46a1c32424`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 23.1 KB (23109 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2022.2-u0`

```console
$ docker pull bonita@sha256:1c6a430928094bea86483958321eaa193d6d2ae63db01655ec5bc8814ccd4767
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
$ docker pull bonita@sha256:408e48996441391ffdd5b55248842416222d57110cfb8ce1b00cb0ab53ecbda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185539058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b596e7835378ff74882336593745a3fd6b65f517561fae7329d78c133aaf0b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e26d36434872ada6f212bf9c46fcee0c81376cbc455c4a373bb2dc878b9633`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 62.7 MB (62715912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d3c2310cb1029eeeb9a2c960cf4b96d7aa6fa2ff757b7d67d56528044ba383`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d272f1eaec9bda81395eb0d0af7d165db3cb97d0b6d409034ff9b816bdb7cd`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54f9c4205c383bc8148313c575377f20b383a7bef2ffc03ba4efedfde0828ce`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcadc120dc91b9dae7dbd4b5cb59bfdc5dc4043646cba759e07009b1c53198d`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 3.0 KB (2996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3156f69fba57e572e4bc26d14b1e751c11957a6d48260fd0f8c9046abc55c0dd`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 119.2 MB (119190675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61341086aead62bd41bd009b8b2247cc16aebecbcc1abe122959f5218d65b3c`  
		Last Modified: Mon, 22 Jul 2024 23:03:21 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:f577a51518e1723fc441f4ff54649e12e91e2e6494f22c063b3985ed6901b67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **896.2 KB (896170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2d02d7dcd40a8440b8704c9a274e686aed6217b5f5fe2c21c5807fc877b6f2`

```dockerfile
```

-	Layers:
	-	`sha256:507d38c8211dc67faf13198b25c36e6b68b5ac1ad8d3d1a77fbdbb5dd50160b9`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 873.1 KB (873107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:820bacf2e755700862418681608ad660c541b211e6add38549ae3e5be8a89d45`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 23.1 KB (23063 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:a94dfcbd34bbf22ccddb13885c031196a1f42777fbeced23b2e1685b093f3427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185948693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2363d8729960e288ca2ad0146c4039fec58047648aeb2794941a88cf34c83c9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18a3131c341fa1d83f7e179e98ac72f1d0957f5ae99aa479b0bf4f3906e43e`  
		Last Modified: Tue, 23 Jul 2024 11:38:28 GMT  
		Size: 62.7 MB (62661473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a38e61750bc70d8a8687f015c32ff4caa6300d22f28b0f62fc4bc2fc3c876f`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d683c6aa3700af9f85bfccb37ab2e046f86dfad938a7cc9075fa11c730c80b6f`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ed0844ebdd1daee4cd96134d1d7a13dbb8ce41803adf8563c66f3977b69e5d`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54548f17b7cc1954972f4cb3ac364372de44aad7cbaa1724b482c93c6c6d93f`  
		Last Modified: Tue, 23 Jul 2024 11:38:27 GMT  
		Size: 3.0 KB (2995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bb75c815d1a199ec048c29bda8a6b530fa2e6686096a2304dbd9e72ef876c0`  
		Last Modified: Tue, 23 Jul 2024 11:38:30 GMT  
		Size: 119.2 MB (119190707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12c67a94de2d10fde21abe23af5776a48e19b95a4307513fc8dcdb7d3fb4bff`  
		Last Modified: Tue, 23 Jul 2024 11:38:27 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:3aae030b860fa6538b6f2358be0160efcbaaa8c3727b4b4d248da378d6f85ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **895.5 KB (895525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac930e2b87335cfeca9d928d194ca285b18cec5ee1d8afc13939c061edc1ce7`

```dockerfile
```

-	Layers:
	-	`sha256:32331d13e18293e73b9255484762f2eb33d6cd839620df855bf8fd5869fd11a3`  
		Last Modified: Tue, 23 Jul 2024 11:38:27 GMT  
		Size: 872.2 KB (872162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28ffdd3a2677f8c3c58679d9740c4383e49a1c209433fd390306032bd4586278`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 23.4 KB (23363 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2022.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:9d0b6636bb12df79f37652872ebe94a7bf83dccd47c40082a4af3d60f250ec09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (181967625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeab47586cf3126573e558a7776ee7d7f0d0680c4afe40e8f9e2e486ef54b278`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f00defe5ad3922145736c51f873742d6339a6f7ce8f4eedcdd1322be46fcb9`  
		Last Modified: Tue, 23 Jul 2024 08:32:19 GMT  
		Size: 59.2 MB (59195818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec3dfaf5507de2b003060a953a25c7cf3bac4cddff4a2c509e10482d785eec5`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1895696360e6ddf12000c5e8f253b278e925b713b40229d01fb1e291b6fd26a7`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96b402cdb3108c7ea9d20fdc2fa786837f0b8753aea4ad22e262ddc5308a3f3`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d5a65e52d60b80dd56a2435a2b7a5b3aedaf0129bf7b4318cb6e867df84004`  
		Last Modified: Tue, 23 Jul 2024 08:32:18 GMT  
		Size: 3.0 KB (2995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf012b2af3f1e9767f4ad118224d6899f8604827004a977d8c001359782cc78`  
		Last Modified: Tue, 23 Jul 2024 08:32:21 GMT  
		Size: 119.2 MB (119190675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876e535d711745c23fbaf59abeaa2e56a54ccf724870c54a77a194cdbcfe5465`  
		Last Modified: Tue, 23 Jul 2024 08:32:18 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2022.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:8b30a5ba15de9e8bfb176ba7476cbfb63d5c8f8f65132c4907f2419150bff36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **893.3 KB (893336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b02307df656a9829c8ae05af9c5c4b1cd4942adfc26b2e2a8f18093b3c7e5f`

```dockerfile
```

-	Layers:
	-	`sha256:5cb67e7a1fcb034eb8d89214aa2eed18affa4166a241ed233b1bff37909337a7`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 870.2 KB (870227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abf05205c44e6d5b64c43f4f9a07046e79ad5eaf3a16ff1496f90c46a1c32424`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 23.1 KB (23109 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.1`

```console
$ docker pull bonita@sha256:8078644ceba0aa4a65f75e9c06f14731d592d4e2ffb974e8e9d8abca430a250b
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
$ docker pull bonita@sha256:0019b22808973f0c45d6ac9c2d335ec76dd76d3e9942e1e8eb406824e0402c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.5 MB (184527335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdd35dbbf7c4aafd8a7f3aff39e05424cec2b34f9f48cf13301290ea53959c2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42290942e886a06996a836ea2292a2488e9e3716c3683069ba1976bd56bf227a`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 62.7 MB (62715850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928d4b6f81db120e1bfb0b2c8ce39a9b91e707bee7e5a1563d00c9bc261352db`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e60ba0b8f06398435b88b436dfb0d1a28454f18a606ff49e400d35dcdf416ab`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f4f2218b2e57a584476dd902b29f0ff3674e8ac530539822c987fab467516f`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb85986ab419810c818f6e06929b03bbb877a2db6a1cd28c43316cd5498c44be`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a464456c93c3c40875b976a7c942693ddeb5abd440c9e0d78da50923b2f273`  
		Last Modified: Mon, 22 Jul 2024 23:03:24 GMT  
		Size: 118.2 MB (118178579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bed3eca2b7e9ab46b44e13196fabe2c75139ba29944bd04fd0ac89755fbb58`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1` - unknown; unknown

```console
$ docker pull bonita@sha256:c1b2fc55fcc777c290a2a7d66749348351319eecf3b9efe8d129d298d2d832f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.8 KB (887808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fe2a3a43aff3bd6154dcd224f5637755559abd583b37fe31e1802b3ced1ea4`

```dockerfile
```

-	Layers:
	-	`sha256:39433bd14168438eb6cd96c0ecddb6772e0ba42840d9182fc39ca1e4992a22f3`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 864.6 KB (864575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b13180a591904a4a33dc60513ba87d3173cc1a8022844b7027b3ad7818b19c`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 23.2 KB (23233 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:dde48d521a614c62e8f3a9cd36c118e7ae0fa10554295960d909b79648450091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184936982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47aa4dc836dd4e88f3cc72105ff364652940fba92854dec18b38e7de678b23e4`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18a3131c341fa1d83f7e179e98ac72f1d0957f5ae99aa479b0bf4f3906e43e`  
		Last Modified: Tue, 23 Jul 2024 11:38:28 GMT  
		Size: 62.7 MB (62661473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a38e61750bc70d8a8687f015c32ff4caa6300d22f28b0f62fc4bc2fc3c876f`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d683c6aa3700af9f85bfccb37ab2e046f86dfad938a7cc9075fa11c730c80b6f`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9a51e6e8257ee06d7119b17534775990d1a56689b20987f890ae86b5069465`  
		Last Modified: Tue, 23 Jul 2024 11:53:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb4100fea5ca932d20603f5eb177c5290675f381063108cbe2cb026b532e1f4`  
		Last Modified: Tue, 23 Jul 2024 11:53:51 GMT  
		Size: 3.4 KB (3425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefac48f1b50071989b900abad7a4de0010196ddbd4b19e429386f4e1721cf26`  
		Last Modified: Tue, 23 Jul 2024 11:53:54 GMT  
		Size: 118.2 MB (118178568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc42237e6124a2dcd609eb0c1cf3ba44b8fa341c4e8392a00367a98f11a399d3`  
		Last Modified: Tue, 23 Jul 2024 11:53:52 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1` - unknown; unknown

```console
$ docker pull bonita@sha256:7b773a95359315d486af42d6f5312fcd86d1998edfe7d437bc844a46438dd99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.2 KB (887236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d5323eec75244a4e62483372cb9fbaa7874f8e64c5a21b1829c870297f7025`

```dockerfile
```

-	Layers:
	-	`sha256:c11b8db17f6c3bca1e8788d58c45dc68025db0e0fef2e4a1477f7e15e1c33db7`  
		Last Modified: Tue, 23 Jul 2024 11:53:51 GMT  
		Size: 863.7 KB (863703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:092a88428d5aa6ac8ec5dc4002caa259b4d0a39aa1cbc2c7ffc38e92d806417c`  
		Last Modified: Tue, 23 Jul 2024 11:53:51 GMT  
		Size: 23.5 KB (23533 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:28ef7e9de2cccb52730e908ab9bbc20436ebe0fffb02bd37d5da8f3ed39d7f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (180955943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9bebc082df2d622473e45e1019febc2fbf963da00dee3b45afd33b86440625`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f00defe5ad3922145736c51f873742d6339a6f7ce8f4eedcdd1322be46fcb9`  
		Last Modified: Tue, 23 Jul 2024 08:32:19 GMT  
		Size: 59.2 MB (59195818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec3dfaf5507de2b003060a953a25c7cf3bac4cddff4a2c509e10482d785eec5`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1895696360e6ddf12000c5e8f253b278e925b713b40229d01fb1e291b6fd26a7`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b276b80ff36bc4b4c6b8eaadd0c6b9f9e7f219803f305beb7962f8ba5f61898`  
		Last Modified: Tue, 23 Jul 2024 08:33:11 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0c6b8b52b8847e96d11e1da51fe5020e870e40f072e14ffc43b3e8af3d991b`  
		Last Modified: Tue, 23 Jul 2024 08:33:11 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2443f64f880182636863e185591c421f36345fd22fb46e9cf6bb4edeb2695b`  
		Last Modified: Tue, 23 Jul 2024 08:33:14 GMT  
		Size: 118.2 MB (118178560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6818e4316a633bf1417bc674dae9be1b37393df07737f2f446552e5d2007fecd`  
		Last Modified: Tue, 23 Jul 2024 08:33:11 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1` - unknown; unknown

```console
$ docker pull bonita@sha256:0715589c9c77f8c9805ce1563fac5c9aa39ceab6776ac90933d3dd34c847ad7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **885.0 KB (885015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eece2f575e84da1b37705ab8ec7d6de1e737f74e8163d32cc0c49bbcea592a9`

```dockerfile
```

-	Layers:
	-	`sha256:16eeeea6cdf5c679abfb68652dca764f2ab8533183bcd36153d656710c8944c6`  
		Last Modified: Tue, 23 Jul 2024 08:33:11 GMT  
		Size: 861.7 KB (861736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7f77ea80305832750b7eb7d27dfc6e449fc10c3e5cf7430d76f447d20c9de2`  
		Last Modified: Tue, 23 Jul 2024 08:33:10 GMT  
		Size: 23.3 KB (23279 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.1-u0`

```console
$ docker pull bonita@sha256:8078644ceba0aa4a65f75e9c06f14731d592d4e2ffb974e8e9d8abca430a250b
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
$ docker pull bonita@sha256:0019b22808973f0c45d6ac9c2d335ec76dd76d3e9942e1e8eb406824e0402c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.5 MB (184527335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdd35dbbf7c4aafd8a7f3aff39e05424cec2b34f9f48cf13301290ea53959c2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42290942e886a06996a836ea2292a2488e9e3716c3683069ba1976bd56bf227a`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 62.7 MB (62715850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928d4b6f81db120e1bfb0b2c8ce39a9b91e707bee7e5a1563d00c9bc261352db`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e60ba0b8f06398435b88b436dfb0d1a28454f18a606ff49e400d35dcdf416ab`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f4f2218b2e57a584476dd902b29f0ff3674e8ac530539822c987fab467516f`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb85986ab419810c818f6e06929b03bbb877a2db6a1cd28c43316cd5498c44be`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a464456c93c3c40875b976a7c942693ddeb5abd440c9e0d78da50923b2f273`  
		Last Modified: Mon, 22 Jul 2024 23:03:24 GMT  
		Size: 118.2 MB (118178579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bed3eca2b7e9ab46b44e13196fabe2c75139ba29944bd04fd0ac89755fbb58`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:c1b2fc55fcc777c290a2a7d66749348351319eecf3b9efe8d129d298d2d832f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.8 KB (887808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fe2a3a43aff3bd6154dcd224f5637755559abd583b37fe31e1802b3ced1ea4`

```dockerfile
```

-	Layers:
	-	`sha256:39433bd14168438eb6cd96c0ecddb6772e0ba42840d9182fc39ca1e4992a22f3`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 864.6 KB (864575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b13180a591904a4a33dc60513ba87d3173cc1a8022844b7027b3ad7818b19c`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 23.2 KB (23233 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:dde48d521a614c62e8f3a9cd36c118e7ae0fa10554295960d909b79648450091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184936982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47aa4dc836dd4e88f3cc72105ff364652940fba92854dec18b38e7de678b23e4`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18a3131c341fa1d83f7e179e98ac72f1d0957f5ae99aa479b0bf4f3906e43e`  
		Last Modified: Tue, 23 Jul 2024 11:38:28 GMT  
		Size: 62.7 MB (62661473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a38e61750bc70d8a8687f015c32ff4caa6300d22f28b0f62fc4bc2fc3c876f`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d683c6aa3700af9f85bfccb37ab2e046f86dfad938a7cc9075fa11c730c80b6f`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9a51e6e8257ee06d7119b17534775990d1a56689b20987f890ae86b5069465`  
		Last Modified: Tue, 23 Jul 2024 11:53:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb4100fea5ca932d20603f5eb177c5290675f381063108cbe2cb026b532e1f4`  
		Last Modified: Tue, 23 Jul 2024 11:53:51 GMT  
		Size: 3.4 KB (3425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefac48f1b50071989b900abad7a4de0010196ddbd4b19e429386f4e1721cf26`  
		Last Modified: Tue, 23 Jul 2024 11:53:54 GMT  
		Size: 118.2 MB (118178568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc42237e6124a2dcd609eb0c1cf3ba44b8fa341c4e8392a00367a98f11a399d3`  
		Last Modified: Tue, 23 Jul 2024 11:53:52 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:7b773a95359315d486af42d6f5312fcd86d1998edfe7d437bc844a46438dd99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.2 KB (887236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d5323eec75244a4e62483372cb9fbaa7874f8e64c5a21b1829c870297f7025`

```dockerfile
```

-	Layers:
	-	`sha256:c11b8db17f6c3bca1e8788d58c45dc68025db0e0fef2e4a1477f7e15e1c33db7`  
		Last Modified: Tue, 23 Jul 2024 11:53:51 GMT  
		Size: 863.7 KB (863703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:092a88428d5aa6ac8ec5dc4002caa259b4d0a39aa1cbc2c7ffc38e92d806417c`  
		Last Modified: Tue, 23 Jul 2024 11:53:51 GMT  
		Size: 23.5 KB (23533 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:28ef7e9de2cccb52730e908ab9bbc20436ebe0fffb02bd37d5da8f3ed39d7f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (180955943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9bebc082df2d622473e45e1019febc2fbf963da00dee3b45afd33b86440625`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f00defe5ad3922145736c51f873742d6339a6f7ce8f4eedcdd1322be46fcb9`  
		Last Modified: Tue, 23 Jul 2024 08:32:19 GMT  
		Size: 59.2 MB (59195818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec3dfaf5507de2b003060a953a25c7cf3bac4cddff4a2c509e10482d785eec5`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1895696360e6ddf12000c5e8f253b278e925b713b40229d01fb1e291b6fd26a7`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b276b80ff36bc4b4c6b8eaadd0c6b9f9e7f219803f305beb7962f8ba5f61898`  
		Last Modified: Tue, 23 Jul 2024 08:33:11 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0c6b8b52b8847e96d11e1da51fe5020e870e40f072e14ffc43b3e8af3d991b`  
		Last Modified: Tue, 23 Jul 2024 08:33:11 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2443f64f880182636863e185591c421f36345fd22fb46e9cf6bb4edeb2695b`  
		Last Modified: Tue, 23 Jul 2024 08:33:14 GMT  
		Size: 118.2 MB (118178560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6818e4316a633bf1417bc674dae9be1b37393df07737f2f446552e5d2007fecd`  
		Last Modified: Tue, 23 Jul 2024 08:33:11 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.1-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:0715589c9c77f8c9805ce1563fac5c9aa39ceab6776ac90933d3dd34c847ad7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **885.0 KB (885015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eece2f575e84da1b37705ab8ec7d6de1e737f74e8163d32cc0c49bbcea592a9`

```dockerfile
```

-	Layers:
	-	`sha256:16eeeea6cdf5c679abfb68652dca764f2ab8533183bcd36153d656710c8944c6`  
		Last Modified: Tue, 23 Jul 2024 08:33:11 GMT  
		Size: 861.7 KB (861736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7f77ea80305832750b7eb7d27dfc6e449fc10c3e5cf7430d76f447d20c9de2`  
		Last Modified: Tue, 23 Jul 2024 08:33:10 GMT  
		Size: 23.3 KB (23279 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.2`

```console
$ docker pull bonita@sha256:5a5453968d046efc29d0e7256da172fb45e1ba5400fa4e0f9946f62f256adff4
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
$ docker pull bonita@sha256:fb07515c82f066960b3b92f11bc4784fa86758b25611b46b48d4480ae6f2b7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192379686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb166874fbd87049328e914cef544f602684f4e2dc5857acf8f2ca7d0eebdc40`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595e01aa4eb60f98d294bf0ec435daabf12482951b82a734e6d8c388cd39ff79`  
		Last Modified: Mon, 22 Jul 2024 23:03:39 GMT  
		Size: 68.6 MB (68572848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ee2684decf767285f0aadba6014fe829a0e7abbbc3ba910f10a93d9c6c9aba`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2938d41a64655d7ec192c26f93ab16e8ac2871ec8f4f97aacfd6c4ad0068d0`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f9351cd9c3e6f9cd1cbd9c0d5be4024f89981700473011d280c392e2dacaea`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61139da512cde90a6b259c6438796bde5e165678b35384021b52ec9ce6a1e150`  
		Last Modified: Mon, 22 Jul 2024 23:03:38 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454fff921a6d3ec6dae173c4c7aebfa51a0c4bbdf6bafbea58759adff5e81a78`  
		Last Modified: Mon, 22 Jul 2024 23:03:42 GMT  
		Size: 120.2 MB (120173514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4eedbe26792d18178160e5dcde207ba967194bd349ffcd5d031dc9fe030886f`  
		Last Modified: Mon, 22 Jul 2024 23:03:38 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2` - unknown; unknown

```console
$ docker pull bonita@sha256:f81efc1e2ba132cb65e401d43c471348dcb3fd0d7786d2727e9d9e1bb433f8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1346716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f7aa2e6d1ce1736775a71d385813b5a3402daee13bc282c5cc51e0d43328bb`

```dockerfile
```

-	Layers:
	-	`sha256:07556575e076975a28eba36f80036245b77ecaa24aaf70c59945d736586b6b73`  
		Last Modified: Mon, 22 Jul 2024 23:03:38 GMT  
		Size: 1.3 MB (1323705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a769cbc044807e9a1273593b3f9965eded2e21c2307cbc71a4a0e1706449fb51`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 23.0 KB (23011 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2b9455a3dd2f581ae0589b061d171397d2cd36b58d1f4aeb4a3a3c416cfe07a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192798360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38b9db3fc9a76fca4e1d4cccd00e767e946fe5e6b43fe630e76744b4527f98d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bfb88f92130c70d4fa52b1899c69f532e3309325e1341fde1b7ce678ea419f`  
		Last Modified: Tue, 23 Jul 2024 11:56:00 GMT  
		Size: 68.5 MB (68527489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6159251b20b7872f263aaaabcb7d88ab76d15fdd9a8d308c08422c3d638c924`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6676aeef57ddb30577609ead8772b387507763efadd3b53daf96da53858366c1`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe859b0f70508e627ead785fd23f4b42d0ab2f86e1545b35689780780322346`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4442509c7fcc9fcd18aa44513795a6cb37434e5d5a0a6e2019956615e15a86ca`  
		Last Modified: Tue, 23 Jul 2024 11:55:58 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f383a3dba676f157f576b17e360db280bf4a350855431bb1c2787e379f15f9`  
		Last Modified: Tue, 23 Jul 2024 11:56:02 GMT  
		Size: 120.2 MB (120173507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f46cadf33f5acb346cf41bb1eb3de1e38291269afb40decae1939e319b36e1`  
		Last Modified: Tue, 23 Jul 2024 11:55:58 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2` - unknown; unknown

```console
$ docker pull bonita@sha256:42bc4c0bb298554e61aa476e29b21348df3b8db40f3e4eadd1b569adf2f711f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1346132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cb76f79c3c84039735c42024705c7f8056178f9bf88a8fac025332183a457a`

```dockerfile
```

-	Layers:
	-	`sha256:9180d571cd09e575ffb0af683371ba22e86ce51d62b128965b5ce6278af2b520`  
		Last Modified: Tue, 23 Jul 2024 11:55:58 GMT  
		Size: 1.3 MB (1322809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09e8af6a51ca6451cb53c68ed42c24a290cc6f12aa19ea36bb545f4ad2453bba`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:d81406a31ab5d80ed346312279dd71a3cc27b9706d80ea8b6c01238f0cfca82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189100475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e3148b64b8646e80f9f62ae5818c44bdc798ddfa47e1dafe826f2fe15b919d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251f343304d515f13e423d23fc7a0c26f78285f66eaad08626678a47be01dfbf`  
		Last Modified: Tue, 23 Jul 2024 08:34:22 GMT  
		Size: 65.3 MB (65344960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f816b7e6293d63faeefdcfd241c23a5adc2cd37c3c7940ba5960e994607c488`  
		Last Modified: Tue, 23 Jul 2024 08:34:19 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f722d7fcdc0a5fc8776c33f287ee14e2173ee76a55444d22fbb62c0cefbf14f`  
		Last Modified: Tue, 23 Jul 2024 08:34:20 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c22f671ec177720f0989457de7bb618b96c38e42e66e331244ce909178a699`  
		Last Modified: Tue, 23 Jul 2024 08:34:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa18d6e00a0374f9c83781bf6e45ad213594e13b52d2c26f9cd4a9f13f06d3f`  
		Last Modified: Tue, 23 Jul 2024 08:34:20 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df4fd0bbfc259dc847c31d3b3bd3a77874f9c0974831447d9888d6989b412f2`  
		Last Modified: Tue, 23 Jul 2024 08:34:24 GMT  
		Size: 120.2 MB (120173530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6848d09dfd0f6288674fb7ecadab78c01b5bb484e1f6c7c1034a1699320fcb`  
		Last Modified: Tue, 23 Jul 2024 08:34:21 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2` - unknown; unknown

```console
$ docker pull bonita@sha256:aa9a061ea8f904ed4f074ad1ba332a2aeb96df298200b4cbe64c80160d128027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1343849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db041c68bf817426e604e163cefc71bff5cc20d64b1b07ba3d9cc8f317c83a7`

```dockerfile
```

-	Layers:
	-	`sha256:8ca2880cb66fbc02f9bcc57cedbd0a4f77a9764c83ec3f34a51dd4d203bdd683`  
		Last Modified: Tue, 23 Jul 2024 08:34:20 GMT  
		Size: 1.3 MB (1320786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2df95bd07324a8822cba0d0d2a55a3d6bb200578fbf02c96c499bc2a9e752655`  
		Last Modified: Tue, 23 Jul 2024 08:34:19 GMT  
		Size: 23.1 KB (23063 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:2023.2-u0`

```console
$ docker pull bonita@sha256:5a5453968d046efc29d0e7256da172fb45e1ba5400fa4e0f9946f62f256adff4
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
$ docker pull bonita@sha256:fb07515c82f066960b3b92f11bc4784fa86758b25611b46b48d4480ae6f2b7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192379686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb166874fbd87049328e914cef544f602684f4e2dc5857acf8f2ca7d0eebdc40`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595e01aa4eb60f98d294bf0ec435daabf12482951b82a734e6d8c388cd39ff79`  
		Last Modified: Mon, 22 Jul 2024 23:03:39 GMT  
		Size: 68.6 MB (68572848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ee2684decf767285f0aadba6014fe829a0e7abbbc3ba910f10a93d9c6c9aba`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2938d41a64655d7ec192c26f93ab16e8ac2871ec8f4f97aacfd6c4ad0068d0`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f9351cd9c3e6f9cd1cbd9c0d5be4024f89981700473011d280c392e2dacaea`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61139da512cde90a6b259c6438796bde5e165678b35384021b52ec9ce6a1e150`  
		Last Modified: Mon, 22 Jul 2024 23:03:38 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454fff921a6d3ec6dae173c4c7aebfa51a0c4bbdf6bafbea58759adff5e81a78`  
		Last Modified: Mon, 22 Jul 2024 23:03:42 GMT  
		Size: 120.2 MB (120173514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4eedbe26792d18178160e5dcde207ba967194bd349ffcd5d031dc9fe030886f`  
		Last Modified: Mon, 22 Jul 2024 23:03:38 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:f81efc1e2ba132cb65e401d43c471348dcb3fd0d7786d2727e9d9e1bb433f8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1346716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f7aa2e6d1ce1736775a71d385813b5a3402daee13bc282c5cc51e0d43328bb`

```dockerfile
```

-	Layers:
	-	`sha256:07556575e076975a28eba36f80036245b77ecaa24aaf70c59945d736586b6b73`  
		Last Modified: Mon, 22 Jul 2024 23:03:38 GMT  
		Size: 1.3 MB (1323705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a769cbc044807e9a1273593b3f9965eded2e21c2307cbc71a4a0e1706449fb51`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 23.0 KB (23011 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2b9455a3dd2f581ae0589b061d171397d2cd36b58d1f4aeb4a3a3c416cfe07a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192798360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38b9db3fc9a76fca4e1d4cccd00e767e946fe5e6b43fe630e76744b4527f98d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bfb88f92130c70d4fa52b1899c69f532e3309325e1341fde1b7ce678ea419f`  
		Last Modified: Tue, 23 Jul 2024 11:56:00 GMT  
		Size: 68.5 MB (68527489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6159251b20b7872f263aaaabcb7d88ab76d15fdd9a8d308c08422c3d638c924`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6676aeef57ddb30577609ead8772b387507763efadd3b53daf96da53858366c1`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe859b0f70508e627ead785fd23f4b42d0ab2f86e1545b35689780780322346`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4442509c7fcc9fcd18aa44513795a6cb37434e5d5a0a6e2019956615e15a86ca`  
		Last Modified: Tue, 23 Jul 2024 11:55:58 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f383a3dba676f157f576b17e360db280bf4a350855431bb1c2787e379f15f9`  
		Last Modified: Tue, 23 Jul 2024 11:56:02 GMT  
		Size: 120.2 MB (120173507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f46cadf33f5acb346cf41bb1eb3de1e38291269afb40decae1939e319b36e1`  
		Last Modified: Tue, 23 Jul 2024 11:55:58 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:42bc4c0bb298554e61aa476e29b21348df3b8db40f3e4eadd1b569adf2f711f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1346132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cb76f79c3c84039735c42024705c7f8056178f9bf88a8fac025332183a457a`

```dockerfile
```

-	Layers:
	-	`sha256:9180d571cd09e575ffb0af683371ba22e86ce51d62b128965b5ce6278af2b520`  
		Last Modified: Tue, 23 Jul 2024 11:55:58 GMT  
		Size: 1.3 MB (1322809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09e8af6a51ca6451cb53c68ed42c24a290cc6f12aa19ea36bb545f4ad2453bba`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:2023.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:d81406a31ab5d80ed346312279dd71a3cc27b9706d80ea8b6c01238f0cfca82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189100475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e3148b64b8646e80f9f62ae5818c44bdc798ddfa47e1dafe826f2fe15b919d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251f343304d515f13e423d23fc7a0c26f78285f66eaad08626678a47be01dfbf`  
		Last Modified: Tue, 23 Jul 2024 08:34:22 GMT  
		Size: 65.3 MB (65344960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f816b7e6293d63faeefdcfd241c23a5adc2cd37c3c7940ba5960e994607c488`  
		Last Modified: Tue, 23 Jul 2024 08:34:19 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f722d7fcdc0a5fc8776c33f287ee14e2173ee76a55444d22fbb62c0cefbf14f`  
		Last Modified: Tue, 23 Jul 2024 08:34:20 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c22f671ec177720f0989457de7bb618b96c38e42e66e331244ce909178a699`  
		Last Modified: Tue, 23 Jul 2024 08:34:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa18d6e00a0374f9c83781bf6e45ad213594e13b52d2c26f9cd4a9f13f06d3f`  
		Last Modified: Tue, 23 Jul 2024 08:34:20 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df4fd0bbfc259dc847c31d3b3bd3a77874f9c0974831447d9888d6989b412f2`  
		Last Modified: Tue, 23 Jul 2024 08:34:24 GMT  
		Size: 120.2 MB (120173530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6848d09dfd0f6288674fb7ecadab78c01b5bb484e1f6c7c1034a1699320fcb`  
		Last Modified: Tue, 23 Jul 2024 08:34:21 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:2023.2-u0` - unknown; unknown

```console
$ docker pull bonita@sha256:aa9a061ea8f904ed4f074ad1ba332a2aeb96df298200b4cbe64c80160d128027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1343849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db041c68bf817426e604e163cefc71bff5cc20d64b1b07ba3d9cc8f317c83a7`

```dockerfile
```

-	Layers:
	-	`sha256:8ca2880cb66fbc02f9bcc57cedbd0a4f77a9764c83ec3f34a51dd4d203bdd683`  
		Last Modified: Tue, 23 Jul 2024 08:34:20 GMT  
		Size: 1.3 MB (1320786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2df95bd07324a8822cba0d0d2a55a3d6bb200578fbf02c96c499bc2a9e752655`  
		Last Modified: Tue, 23 Jul 2024 08:34:19 GMT  
		Size: 23.1 KB (23063 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:7.15`

```console
$ docker pull bonita@sha256:1c6a430928094bea86483958321eaa193d6d2ae63db01655ec5bc8814ccd4767
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
$ docker pull bonita@sha256:408e48996441391ffdd5b55248842416222d57110cfb8ce1b00cb0ab53ecbda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185539058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b596e7835378ff74882336593745a3fd6b65f517561fae7329d78c133aaf0b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e26d36434872ada6f212bf9c46fcee0c81376cbc455c4a373bb2dc878b9633`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 62.7 MB (62715912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d3c2310cb1029eeeb9a2c960cf4b96d7aa6fa2ff757b7d67d56528044ba383`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d272f1eaec9bda81395eb0d0af7d165db3cb97d0b6d409034ff9b816bdb7cd`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54f9c4205c383bc8148313c575377f20b383a7bef2ffc03ba4efedfde0828ce`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcadc120dc91b9dae7dbd4b5cb59bfdc5dc4043646cba759e07009b1c53198d`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 3.0 KB (2996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3156f69fba57e572e4bc26d14b1e751c11957a6d48260fd0f8c9046abc55c0dd`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 119.2 MB (119190675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61341086aead62bd41bd009b8b2247cc16aebecbcc1abe122959f5218d65b3c`  
		Last Modified: Mon, 22 Jul 2024 23:03:21 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15` - unknown; unknown

```console
$ docker pull bonita@sha256:f577a51518e1723fc441f4ff54649e12e91e2e6494f22c063b3985ed6901b67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **896.2 KB (896170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2d02d7dcd40a8440b8704c9a274e686aed6217b5f5fe2c21c5807fc877b6f2`

```dockerfile
```

-	Layers:
	-	`sha256:507d38c8211dc67faf13198b25c36e6b68b5ac1ad8d3d1a77fbdbb5dd50160b9`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 873.1 KB (873107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:820bacf2e755700862418681608ad660c541b211e6add38549ae3e5be8a89d45`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 23.1 KB (23063 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.15` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:a94dfcbd34bbf22ccddb13885c031196a1f42777fbeced23b2e1685b093f3427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185948693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2363d8729960e288ca2ad0146c4039fec58047648aeb2794941a88cf34c83c9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18a3131c341fa1d83f7e179e98ac72f1d0957f5ae99aa479b0bf4f3906e43e`  
		Last Modified: Tue, 23 Jul 2024 11:38:28 GMT  
		Size: 62.7 MB (62661473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a38e61750bc70d8a8687f015c32ff4caa6300d22f28b0f62fc4bc2fc3c876f`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d683c6aa3700af9f85bfccb37ab2e046f86dfad938a7cc9075fa11c730c80b6f`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ed0844ebdd1daee4cd96134d1d7a13dbb8ce41803adf8563c66f3977b69e5d`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54548f17b7cc1954972f4cb3ac364372de44aad7cbaa1724b482c93c6c6d93f`  
		Last Modified: Tue, 23 Jul 2024 11:38:27 GMT  
		Size: 3.0 KB (2995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bb75c815d1a199ec048c29bda8a6b530fa2e6686096a2304dbd9e72ef876c0`  
		Last Modified: Tue, 23 Jul 2024 11:38:30 GMT  
		Size: 119.2 MB (119190707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12c67a94de2d10fde21abe23af5776a48e19b95a4307513fc8dcdb7d3fb4bff`  
		Last Modified: Tue, 23 Jul 2024 11:38:27 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15` - unknown; unknown

```console
$ docker pull bonita@sha256:3aae030b860fa6538b6f2358be0160efcbaaa8c3727b4b4d248da378d6f85ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **895.5 KB (895525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac930e2b87335cfeca9d928d194ca285b18cec5ee1d8afc13939c061edc1ce7`

```dockerfile
```

-	Layers:
	-	`sha256:32331d13e18293e73b9255484762f2eb33d6cd839620df855bf8fd5869fd11a3`  
		Last Modified: Tue, 23 Jul 2024 11:38:27 GMT  
		Size: 872.2 KB (872162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28ffdd3a2677f8c3c58679d9740c4383e49a1c209433fd390306032bd4586278`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 23.4 KB (23363 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.15` - linux; ppc64le

```console
$ docker pull bonita@sha256:9d0b6636bb12df79f37652872ebe94a7bf83dccd47c40082a4af3d60f250ec09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (181967625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeab47586cf3126573e558a7776ee7d7f0d0680c4afe40e8f9e2e486ef54b278`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f00defe5ad3922145736c51f873742d6339a6f7ce8f4eedcdd1322be46fcb9`  
		Last Modified: Tue, 23 Jul 2024 08:32:19 GMT  
		Size: 59.2 MB (59195818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec3dfaf5507de2b003060a953a25c7cf3bac4cddff4a2c509e10482d785eec5`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1895696360e6ddf12000c5e8f253b278e925b713b40229d01fb1e291b6fd26a7`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96b402cdb3108c7ea9d20fdc2fa786837f0b8753aea4ad22e262ddc5308a3f3`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d5a65e52d60b80dd56a2435a2b7a5b3aedaf0129bf7b4318cb6e867df84004`  
		Last Modified: Tue, 23 Jul 2024 08:32:18 GMT  
		Size: 3.0 KB (2995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf012b2af3f1e9767f4ad118224d6899f8604827004a977d8c001359782cc78`  
		Last Modified: Tue, 23 Jul 2024 08:32:21 GMT  
		Size: 119.2 MB (119190675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876e535d711745c23fbaf59abeaa2e56a54ccf724870c54a77a194cdbcfe5465`  
		Last Modified: Tue, 23 Jul 2024 08:32:18 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15` - unknown; unknown

```console
$ docker pull bonita@sha256:8b30a5ba15de9e8bfb176ba7476cbfb63d5c8f8f65132c4907f2419150bff36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **893.3 KB (893336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b02307df656a9829c8ae05af9c5c4b1cd4942adfc26b2e2a8f18093b3c7e5f`

```dockerfile
```

-	Layers:
	-	`sha256:5cb67e7a1fcb034eb8d89214aa2eed18affa4166a241ed233b1bff37909337a7`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 870.2 KB (870227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abf05205c44e6d5b64c43f4f9a07046e79ad5eaf3a16ff1496f90c46a1c32424`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 23.1 KB (23109 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:7.15.0`

```console
$ docker pull bonita@sha256:1c6a430928094bea86483958321eaa193d6d2ae63db01655ec5bc8814ccd4767
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
$ docker pull bonita@sha256:408e48996441391ffdd5b55248842416222d57110cfb8ce1b00cb0ab53ecbda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185539058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b596e7835378ff74882336593745a3fd6b65f517561fae7329d78c133aaf0b`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e26d36434872ada6f212bf9c46fcee0c81376cbc455c4a373bb2dc878b9633`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 62.7 MB (62715912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d3c2310cb1029eeeb9a2c960cf4b96d7aa6fa2ff757b7d67d56528044ba383`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d272f1eaec9bda81395eb0d0af7d165db3cb97d0b6d409034ff9b816bdb7cd`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54f9c4205c383bc8148313c575377f20b383a7bef2ffc03ba4efedfde0828ce`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcadc120dc91b9dae7dbd4b5cb59bfdc5dc4043646cba759e07009b1c53198d`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 3.0 KB (2996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3156f69fba57e572e4bc26d14b1e751c11957a6d48260fd0f8c9046abc55c0dd`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 119.2 MB (119190675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61341086aead62bd41bd009b8b2247cc16aebecbcc1abe122959f5218d65b3c`  
		Last Modified: Mon, 22 Jul 2024 23:03:21 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15.0` - unknown; unknown

```console
$ docker pull bonita@sha256:f577a51518e1723fc441f4ff54649e12e91e2e6494f22c063b3985ed6901b67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **896.2 KB (896170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2d02d7dcd40a8440b8704c9a274e686aed6217b5f5fe2c21c5807fc877b6f2`

```dockerfile
```

-	Layers:
	-	`sha256:507d38c8211dc67faf13198b25c36e6b68b5ac1ad8d3d1a77fbdbb5dd50160b9`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 873.1 KB (873107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:820bacf2e755700862418681608ad660c541b211e6add38549ae3e5be8a89d45`  
		Last Modified: Mon, 22 Jul 2024 23:03:20 GMT  
		Size: 23.1 KB (23063 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.15.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:a94dfcbd34bbf22ccddb13885c031196a1f42777fbeced23b2e1685b093f3427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185948693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2363d8729960e288ca2ad0146c4039fec58047648aeb2794941a88cf34c83c9`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18a3131c341fa1d83f7e179e98ac72f1d0957f5ae99aa479b0bf4f3906e43e`  
		Last Modified: Tue, 23 Jul 2024 11:38:28 GMT  
		Size: 62.7 MB (62661473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a38e61750bc70d8a8687f015c32ff4caa6300d22f28b0f62fc4bc2fc3c876f`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d683c6aa3700af9f85bfccb37ab2e046f86dfad938a7cc9075fa11c730c80b6f`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ed0844ebdd1daee4cd96134d1d7a13dbb8ce41803adf8563c66f3977b69e5d`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54548f17b7cc1954972f4cb3ac364372de44aad7cbaa1724b482c93c6c6d93f`  
		Last Modified: Tue, 23 Jul 2024 11:38:27 GMT  
		Size: 3.0 KB (2995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bb75c815d1a199ec048c29bda8a6b530fa2e6686096a2304dbd9e72ef876c0`  
		Last Modified: Tue, 23 Jul 2024 11:38:30 GMT  
		Size: 119.2 MB (119190707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12c67a94de2d10fde21abe23af5776a48e19b95a4307513fc8dcdb7d3fb4bff`  
		Last Modified: Tue, 23 Jul 2024 11:38:27 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15.0` - unknown; unknown

```console
$ docker pull bonita@sha256:3aae030b860fa6538b6f2358be0160efcbaaa8c3727b4b4d248da378d6f85ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **895.5 KB (895525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac930e2b87335cfeca9d928d194ca285b18cec5ee1d8afc13939c061edc1ce7`

```dockerfile
```

-	Layers:
	-	`sha256:32331d13e18293e73b9255484762f2eb33d6cd839620df855bf8fd5869fd11a3`  
		Last Modified: Tue, 23 Jul 2024 11:38:27 GMT  
		Size: 872.2 KB (872162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28ffdd3a2677f8c3c58679d9740c4383e49a1c209433fd390306032bd4586278`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 23.4 KB (23363 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:7.15.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:9d0b6636bb12df79f37652872ebe94a7bf83dccd47c40082a4af3d60f250ec09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (181967625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeab47586cf3126573e558a7776ee7d7f0d0680c4afe40e8f9e2e486ef54b278`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:02:02 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:02:02 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_VERSION=7.15.0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BRANDING_VERSION=2022.2-u0
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ZIP_FILE=BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:02:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
# ARGS: BONITA_VERSION=7.15.0 BRANDING_VERSION=2022.2-u0 BONITA_SHA256=9e6d35b3763ccc091b4b4dec1697c96231552847d4329420e796727c946e37a6 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.2-u0/BonitaCommunity-2022.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:02:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:02:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:02:02 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:02:02 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:02:02 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:02:02 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:02:02 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:02:02 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f00defe5ad3922145736c51f873742d6339a6f7ce8f4eedcdd1322be46fcb9`  
		Last Modified: Tue, 23 Jul 2024 08:32:19 GMT  
		Size: 59.2 MB (59195818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec3dfaf5507de2b003060a953a25c7cf3bac4cddff4a2c509e10482d785eec5`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1895696360e6ddf12000c5e8f253b278e925b713b40229d01fb1e291b6fd26a7`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96b402cdb3108c7ea9d20fdc2fa786837f0b8753aea4ad22e262ddc5308a3f3`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d5a65e52d60b80dd56a2435a2b7a5b3aedaf0129bf7b4318cb6e867df84004`  
		Last Modified: Tue, 23 Jul 2024 08:32:18 GMT  
		Size: 3.0 KB (2995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf012b2af3f1e9767f4ad118224d6899f8604827004a977d8c001359782cc78`  
		Last Modified: Tue, 23 Jul 2024 08:32:21 GMT  
		Size: 119.2 MB (119190675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876e535d711745c23fbaf59abeaa2e56a54ccf724870c54a77a194cdbcfe5465`  
		Last Modified: Tue, 23 Jul 2024 08:32:18 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:7.15.0` - unknown; unknown

```console
$ docker pull bonita@sha256:8b30a5ba15de9e8bfb176ba7476cbfb63d5c8f8f65132c4907f2419150bff36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **893.3 KB (893336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b02307df656a9829c8ae05af9c5c4b1cd4942adfc26b2e2a8f18093b3c7e5f`

```dockerfile
```

-	Layers:
	-	`sha256:5cb67e7a1fcb034eb8d89214aa2eed18affa4166a241ed233b1bff37909337a7`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 870.2 KB (870227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abf05205c44e6d5b64c43f4f9a07046e79ad5eaf3a16ff1496f90c46a1c32424`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 23.1 KB (23109 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:8.0`

```console
$ docker pull bonita@sha256:8078644ceba0aa4a65f75e9c06f14731d592d4e2ffb974e8e9d8abca430a250b
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
$ docker pull bonita@sha256:0019b22808973f0c45d6ac9c2d335ec76dd76d3e9942e1e8eb406824e0402c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.5 MB (184527335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdd35dbbf7c4aafd8a7f3aff39e05424cec2b34f9f48cf13301290ea53959c2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42290942e886a06996a836ea2292a2488e9e3716c3683069ba1976bd56bf227a`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 62.7 MB (62715850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928d4b6f81db120e1bfb0b2c8ce39a9b91e707bee7e5a1563d00c9bc261352db`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e60ba0b8f06398435b88b436dfb0d1a28454f18a606ff49e400d35dcdf416ab`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f4f2218b2e57a584476dd902b29f0ff3674e8ac530539822c987fab467516f`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb85986ab419810c818f6e06929b03bbb877a2db6a1cd28c43316cd5498c44be`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a464456c93c3c40875b976a7c942693ddeb5abd440c9e0d78da50923b2f273`  
		Last Modified: Mon, 22 Jul 2024 23:03:24 GMT  
		Size: 118.2 MB (118178579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bed3eca2b7e9ab46b44e13196fabe2c75139ba29944bd04fd0ac89755fbb58`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0` - unknown; unknown

```console
$ docker pull bonita@sha256:c1b2fc55fcc777c290a2a7d66749348351319eecf3b9efe8d129d298d2d832f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.8 KB (887808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fe2a3a43aff3bd6154dcd224f5637755559abd583b37fe31e1802b3ced1ea4`

```dockerfile
```

-	Layers:
	-	`sha256:39433bd14168438eb6cd96c0ecddb6772e0ba42840d9182fc39ca1e4992a22f3`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 864.6 KB (864575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b13180a591904a4a33dc60513ba87d3173cc1a8022844b7027b3ad7818b19c`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 23.2 KB (23233 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:8.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:dde48d521a614c62e8f3a9cd36c118e7ae0fa10554295960d909b79648450091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184936982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47aa4dc836dd4e88f3cc72105ff364652940fba92854dec18b38e7de678b23e4`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18a3131c341fa1d83f7e179e98ac72f1d0957f5ae99aa479b0bf4f3906e43e`  
		Last Modified: Tue, 23 Jul 2024 11:38:28 GMT  
		Size: 62.7 MB (62661473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a38e61750bc70d8a8687f015c32ff4caa6300d22f28b0f62fc4bc2fc3c876f`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d683c6aa3700af9f85bfccb37ab2e046f86dfad938a7cc9075fa11c730c80b6f`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9a51e6e8257ee06d7119b17534775990d1a56689b20987f890ae86b5069465`  
		Last Modified: Tue, 23 Jul 2024 11:53:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb4100fea5ca932d20603f5eb177c5290675f381063108cbe2cb026b532e1f4`  
		Last Modified: Tue, 23 Jul 2024 11:53:51 GMT  
		Size: 3.4 KB (3425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefac48f1b50071989b900abad7a4de0010196ddbd4b19e429386f4e1721cf26`  
		Last Modified: Tue, 23 Jul 2024 11:53:54 GMT  
		Size: 118.2 MB (118178568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc42237e6124a2dcd609eb0c1cf3ba44b8fa341c4e8392a00367a98f11a399d3`  
		Last Modified: Tue, 23 Jul 2024 11:53:52 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0` - unknown; unknown

```console
$ docker pull bonita@sha256:7b773a95359315d486af42d6f5312fcd86d1998edfe7d437bc844a46438dd99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.2 KB (887236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d5323eec75244a4e62483372cb9fbaa7874f8e64c5a21b1829c870297f7025`

```dockerfile
```

-	Layers:
	-	`sha256:c11b8db17f6c3bca1e8788d58c45dc68025db0e0fef2e4a1477f7e15e1c33db7`  
		Last Modified: Tue, 23 Jul 2024 11:53:51 GMT  
		Size: 863.7 KB (863703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:092a88428d5aa6ac8ec5dc4002caa259b4d0a39aa1cbc2c7ffc38e92d806417c`  
		Last Modified: Tue, 23 Jul 2024 11:53:51 GMT  
		Size: 23.5 KB (23533 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:8.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:28ef7e9de2cccb52730e908ab9bbc20436ebe0fffb02bd37d5da8f3ed39d7f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (180955943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9bebc082df2d622473e45e1019febc2fbf963da00dee3b45afd33b86440625`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f00defe5ad3922145736c51f873742d6339a6f7ce8f4eedcdd1322be46fcb9`  
		Last Modified: Tue, 23 Jul 2024 08:32:19 GMT  
		Size: 59.2 MB (59195818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec3dfaf5507de2b003060a953a25c7cf3bac4cddff4a2c509e10482d785eec5`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1895696360e6ddf12000c5e8f253b278e925b713b40229d01fb1e291b6fd26a7`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b276b80ff36bc4b4c6b8eaadd0c6b9f9e7f219803f305beb7962f8ba5f61898`  
		Last Modified: Tue, 23 Jul 2024 08:33:11 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0c6b8b52b8847e96d11e1da51fe5020e870e40f072e14ffc43b3e8af3d991b`  
		Last Modified: Tue, 23 Jul 2024 08:33:11 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2443f64f880182636863e185591c421f36345fd22fb46e9cf6bb4edeb2695b`  
		Last Modified: Tue, 23 Jul 2024 08:33:14 GMT  
		Size: 118.2 MB (118178560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6818e4316a633bf1417bc674dae9be1b37393df07737f2f446552e5d2007fecd`  
		Last Modified: Tue, 23 Jul 2024 08:33:11 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0` - unknown; unknown

```console
$ docker pull bonita@sha256:0715589c9c77f8c9805ce1563fac5c9aa39ceab6776ac90933d3dd34c847ad7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **885.0 KB (885015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eece2f575e84da1b37705ab8ec7d6de1e737f74e8163d32cc0c49bbcea592a9`

```dockerfile
```

-	Layers:
	-	`sha256:16eeeea6cdf5c679abfb68652dca764f2ab8533183bcd36153d656710c8944c6`  
		Last Modified: Tue, 23 Jul 2024 08:33:11 GMT  
		Size: 861.7 KB (861736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7f77ea80305832750b7eb7d27dfc6e449fc10c3e5cf7430d76f447d20c9de2`  
		Last Modified: Tue, 23 Jul 2024 08:33:10 GMT  
		Size: 23.3 KB (23279 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:8.0.0`

```console
$ docker pull bonita@sha256:8078644ceba0aa4a65f75e9c06f14731d592d4e2ffb974e8e9d8abca430a250b
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
$ docker pull bonita@sha256:0019b22808973f0c45d6ac9c2d335ec76dd76d3e9942e1e8eb406824e0402c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.5 MB (184527335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdd35dbbf7c4aafd8a7f3aff39e05424cec2b34f9f48cf13301290ea53959c2`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42290942e886a06996a836ea2292a2488e9e3716c3683069ba1976bd56bf227a`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 62.7 MB (62715850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928d4b6f81db120e1bfb0b2c8ce39a9b91e707bee7e5a1563d00c9bc261352db`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e60ba0b8f06398435b88b436dfb0d1a28454f18a606ff49e400d35dcdf416ab`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f4f2218b2e57a584476dd902b29f0ff3674e8ac530539822c987fab467516f`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb85986ab419810c818f6e06929b03bbb877a2db6a1cd28c43316cd5498c44be`  
		Last Modified: Mon, 22 Jul 2024 23:03:23 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a464456c93c3c40875b976a7c942693ddeb5abd440c9e0d78da50923b2f273`  
		Last Modified: Mon, 22 Jul 2024 23:03:24 GMT  
		Size: 118.2 MB (118178579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bed3eca2b7e9ab46b44e13196fabe2c75139ba29944bd04fd0ac89755fbb58`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:c1b2fc55fcc777c290a2a7d66749348351319eecf3b9efe8d129d298d2d832f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.8 KB (887808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fe2a3a43aff3bd6154dcd224f5637755559abd583b37fe31e1802b3ced1ea4`

```dockerfile
```

-	Layers:
	-	`sha256:39433bd14168438eb6cd96c0ecddb6772e0ba42840d9182fc39ca1e4992a22f3`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 864.6 KB (864575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b13180a591904a4a33dc60513ba87d3173cc1a8022844b7027b3ad7818b19c`  
		Last Modified: Mon, 22 Jul 2024 23:03:22 GMT  
		Size: 23.2 KB (23233 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:8.0.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:dde48d521a614c62e8f3a9cd36c118e7ae0fa10554295960d909b79648450091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184936982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47aa4dc836dd4e88f3cc72105ff364652940fba92854dec18b38e7de678b23e4`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18a3131c341fa1d83f7e179e98ac72f1d0957f5ae99aa479b0bf4f3906e43e`  
		Last Modified: Tue, 23 Jul 2024 11:38:28 GMT  
		Size: 62.7 MB (62661473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a38e61750bc70d8a8687f015c32ff4caa6300d22f28b0f62fc4bc2fc3c876f`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d683c6aa3700af9f85bfccb37ab2e046f86dfad938a7cc9075fa11c730c80b6f`  
		Last Modified: Tue, 23 Jul 2024 11:38:26 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9a51e6e8257ee06d7119b17534775990d1a56689b20987f890ae86b5069465`  
		Last Modified: Tue, 23 Jul 2024 11:53:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb4100fea5ca932d20603f5eb177c5290675f381063108cbe2cb026b532e1f4`  
		Last Modified: Tue, 23 Jul 2024 11:53:51 GMT  
		Size: 3.4 KB (3425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefac48f1b50071989b900abad7a4de0010196ddbd4b19e429386f4e1721cf26`  
		Last Modified: Tue, 23 Jul 2024 11:53:54 GMT  
		Size: 118.2 MB (118178568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc42237e6124a2dcd609eb0c1cf3ba44b8fa341c4e8392a00367a98f11a399d3`  
		Last Modified: Tue, 23 Jul 2024 11:53:52 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:7b773a95359315d486af42d6f5312fcd86d1998edfe7d437bc844a46438dd99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **887.2 KB (887236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d5323eec75244a4e62483372cb9fbaa7874f8e64c5a21b1829c870297f7025`

```dockerfile
```

-	Layers:
	-	`sha256:c11b8db17f6c3bca1e8788d58c45dc68025db0e0fef2e4a1477f7e15e1c33db7`  
		Last Modified: Tue, 23 Jul 2024 11:53:51 GMT  
		Size: 863.7 KB (863703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:092a88428d5aa6ac8ec5dc4002caa259b4d0a39aa1cbc2c7ffc38e92d806417c`  
		Last Modified: Tue, 23 Jul 2024 11:53:51 GMT  
		Size: 23.5 KB (23533 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:8.0.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:28ef7e9de2cccb52730e908ab9bbc20436ebe0fffb02bd37d5da8f3ed39d7f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (180955943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9bebc082df2d622473e45e1019febc2fbf963da00dee3b45afd33b86440625`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:05:57 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:05:57 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_VERSION=8.0.0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BRANDING_VERSION=2023.1-u0
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ZIP_FILE=BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:05:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
# ARGS: BONITA_VERSION=8.0.0 BRANDING_VERSION=2023.1-u0 BONITA_SHA256=2141b33d5835a0205e6da06580f75f44fd79c798552d4d1c3b304e6fa1b69a60 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.1-u0/BonitaCommunity-2023.1-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:05:57 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:05:57 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:05:57 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:05:57 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:05:57 GMT
ENV INSTALL_PROVIDED_PAGES=false
# Mon, 08 Jul 2024 07:05:57 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:05:57 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:05:57 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:05:57 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:05:57 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f00defe5ad3922145736c51f873742d6339a6f7ce8f4eedcdd1322be46fcb9`  
		Last Modified: Tue, 23 Jul 2024 08:32:19 GMT  
		Size: 59.2 MB (59195818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec3dfaf5507de2b003060a953a25c7cf3bac4cddff4a2c509e10482d785eec5`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1895696360e6ddf12000c5e8f253b278e925b713b40229d01fb1e291b6fd26a7`  
		Last Modified: Tue, 23 Jul 2024 08:32:17 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b276b80ff36bc4b4c6b8eaadd0c6b9f9e7f219803f305beb7962f8ba5f61898`  
		Last Modified: Tue, 23 Jul 2024 08:33:11 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0c6b8b52b8847e96d11e1da51fe5020e870e40f072e14ffc43b3e8af3d991b`  
		Last Modified: Tue, 23 Jul 2024 08:33:11 GMT  
		Size: 3.4 KB (3429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2443f64f880182636863e185591c421f36345fd22fb46e9cf6bb4edeb2695b`  
		Last Modified: Tue, 23 Jul 2024 08:33:14 GMT  
		Size: 118.2 MB (118178560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6818e4316a633bf1417bc674dae9be1b37393df07737f2f446552e5d2007fecd`  
		Last Modified: Tue, 23 Jul 2024 08:33:11 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:8.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:0715589c9c77f8c9805ce1563fac5c9aa39ceab6776ac90933d3dd34c847ad7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **885.0 KB (885015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eece2f575e84da1b37705ab8ec7d6de1e737f74e8163d32cc0c49bbcea592a9`

```dockerfile
```

-	Layers:
	-	`sha256:16eeeea6cdf5c679abfb68652dca764f2ab8533183bcd36153d656710c8944c6`  
		Last Modified: Tue, 23 Jul 2024 08:33:11 GMT  
		Size: 861.7 KB (861736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7f77ea80305832750b7eb7d27dfc6e449fc10c3e5cf7430d76f447d20c9de2`  
		Last Modified: Tue, 23 Jul 2024 08:33:10 GMT  
		Size: 23.3 KB (23279 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:9.0`

```console
$ docker pull bonita@sha256:5a5453968d046efc29d0e7256da172fb45e1ba5400fa4e0f9946f62f256adff4
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
$ docker pull bonita@sha256:fb07515c82f066960b3b92f11bc4784fa86758b25611b46b48d4480ae6f2b7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192379686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb166874fbd87049328e914cef544f602684f4e2dc5857acf8f2ca7d0eebdc40`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595e01aa4eb60f98d294bf0ec435daabf12482951b82a734e6d8c388cd39ff79`  
		Last Modified: Mon, 22 Jul 2024 23:03:39 GMT  
		Size: 68.6 MB (68572848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ee2684decf767285f0aadba6014fe829a0e7abbbc3ba910f10a93d9c6c9aba`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2938d41a64655d7ec192c26f93ab16e8ac2871ec8f4f97aacfd6c4ad0068d0`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f9351cd9c3e6f9cd1cbd9c0d5be4024f89981700473011d280c392e2dacaea`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61139da512cde90a6b259c6438796bde5e165678b35384021b52ec9ce6a1e150`  
		Last Modified: Mon, 22 Jul 2024 23:03:38 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454fff921a6d3ec6dae173c4c7aebfa51a0c4bbdf6bafbea58759adff5e81a78`  
		Last Modified: Mon, 22 Jul 2024 23:03:42 GMT  
		Size: 120.2 MB (120173514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4eedbe26792d18178160e5dcde207ba967194bd349ffcd5d031dc9fe030886f`  
		Last Modified: Mon, 22 Jul 2024 23:03:38 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0` - unknown; unknown

```console
$ docker pull bonita@sha256:f81efc1e2ba132cb65e401d43c471348dcb3fd0d7786d2727e9d9e1bb433f8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1346716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f7aa2e6d1ce1736775a71d385813b5a3402daee13bc282c5cc51e0d43328bb`

```dockerfile
```

-	Layers:
	-	`sha256:07556575e076975a28eba36f80036245b77ecaa24aaf70c59945d736586b6b73`  
		Last Modified: Mon, 22 Jul 2024 23:03:38 GMT  
		Size: 1.3 MB (1323705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a769cbc044807e9a1273593b3f9965eded2e21c2307cbc71a4a0e1706449fb51`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 23.0 KB (23011 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:9.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2b9455a3dd2f581ae0589b061d171397d2cd36b58d1f4aeb4a3a3c416cfe07a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192798360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38b9db3fc9a76fca4e1d4cccd00e767e946fe5e6b43fe630e76744b4527f98d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bfb88f92130c70d4fa52b1899c69f532e3309325e1341fde1b7ce678ea419f`  
		Last Modified: Tue, 23 Jul 2024 11:56:00 GMT  
		Size: 68.5 MB (68527489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6159251b20b7872f263aaaabcb7d88ab76d15fdd9a8d308c08422c3d638c924`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6676aeef57ddb30577609ead8772b387507763efadd3b53daf96da53858366c1`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe859b0f70508e627ead785fd23f4b42d0ab2f86e1545b35689780780322346`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4442509c7fcc9fcd18aa44513795a6cb37434e5d5a0a6e2019956615e15a86ca`  
		Last Modified: Tue, 23 Jul 2024 11:55:58 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f383a3dba676f157f576b17e360db280bf4a350855431bb1c2787e379f15f9`  
		Last Modified: Tue, 23 Jul 2024 11:56:02 GMT  
		Size: 120.2 MB (120173507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f46cadf33f5acb346cf41bb1eb3de1e38291269afb40decae1939e319b36e1`  
		Last Modified: Tue, 23 Jul 2024 11:55:58 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0` - unknown; unknown

```console
$ docker pull bonita@sha256:42bc4c0bb298554e61aa476e29b21348df3b8db40f3e4eadd1b569adf2f711f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1346132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cb76f79c3c84039735c42024705c7f8056178f9bf88a8fac025332183a457a`

```dockerfile
```

-	Layers:
	-	`sha256:9180d571cd09e575ffb0af683371ba22e86ce51d62b128965b5ce6278af2b520`  
		Last Modified: Tue, 23 Jul 2024 11:55:58 GMT  
		Size: 1.3 MB (1322809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09e8af6a51ca6451cb53c68ed42c24a290cc6f12aa19ea36bb545f4ad2453bba`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:9.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:d81406a31ab5d80ed346312279dd71a3cc27b9706d80ea8b6c01238f0cfca82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189100475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e3148b64b8646e80f9f62ae5818c44bdc798ddfa47e1dafe826f2fe15b919d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251f343304d515f13e423d23fc7a0c26f78285f66eaad08626678a47be01dfbf`  
		Last Modified: Tue, 23 Jul 2024 08:34:22 GMT  
		Size: 65.3 MB (65344960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f816b7e6293d63faeefdcfd241c23a5adc2cd37c3c7940ba5960e994607c488`  
		Last Modified: Tue, 23 Jul 2024 08:34:19 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f722d7fcdc0a5fc8776c33f287ee14e2173ee76a55444d22fbb62c0cefbf14f`  
		Last Modified: Tue, 23 Jul 2024 08:34:20 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c22f671ec177720f0989457de7bb618b96c38e42e66e331244ce909178a699`  
		Last Modified: Tue, 23 Jul 2024 08:34:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa18d6e00a0374f9c83781bf6e45ad213594e13b52d2c26f9cd4a9f13f06d3f`  
		Last Modified: Tue, 23 Jul 2024 08:34:20 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df4fd0bbfc259dc847c31d3b3bd3a77874f9c0974831447d9888d6989b412f2`  
		Last Modified: Tue, 23 Jul 2024 08:34:24 GMT  
		Size: 120.2 MB (120173530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6848d09dfd0f6288674fb7ecadab78c01b5bb484e1f6c7c1034a1699320fcb`  
		Last Modified: Tue, 23 Jul 2024 08:34:21 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0` - unknown; unknown

```console
$ docker pull bonita@sha256:aa9a061ea8f904ed4f074ad1ba332a2aeb96df298200b4cbe64c80160d128027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1343849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db041c68bf817426e604e163cefc71bff5cc20d64b1b07ba3d9cc8f317c83a7`

```dockerfile
```

-	Layers:
	-	`sha256:8ca2880cb66fbc02f9bcc57cedbd0a4f77a9764c83ec3f34a51dd4d203bdd683`  
		Last Modified: Tue, 23 Jul 2024 08:34:20 GMT  
		Size: 1.3 MB (1320786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2df95bd07324a8822cba0d0d2a55a3d6bb200578fbf02c96c499bc2a9e752655`  
		Last Modified: Tue, 23 Jul 2024 08:34:19 GMT  
		Size: 23.1 KB (23063 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:9.0.0`

```console
$ docker pull bonita@sha256:5a5453968d046efc29d0e7256da172fb45e1ba5400fa4e0f9946f62f256adff4
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
$ docker pull bonita@sha256:fb07515c82f066960b3b92f11bc4784fa86758b25611b46b48d4480ae6f2b7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192379686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb166874fbd87049328e914cef544f602684f4e2dc5857acf8f2ca7d0eebdc40`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595e01aa4eb60f98d294bf0ec435daabf12482951b82a734e6d8c388cd39ff79`  
		Last Modified: Mon, 22 Jul 2024 23:03:39 GMT  
		Size: 68.6 MB (68572848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ee2684decf767285f0aadba6014fe829a0e7abbbc3ba910f10a93d9c6c9aba`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2938d41a64655d7ec192c26f93ab16e8ac2871ec8f4f97aacfd6c4ad0068d0`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f9351cd9c3e6f9cd1cbd9c0d5be4024f89981700473011d280c392e2dacaea`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61139da512cde90a6b259c6438796bde5e165678b35384021b52ec9ce6a1e150`  
		Last Modified: Mon, 22 Jul 2024 23:03:38 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454fff921a6d3ec6dae173c4c7aebfa51a0c4bbdf6bafbea58759adff5e81a78`  
		Last Modified: Mon, 22 Jul 2024 23:03:42 GMT  
		Size: 120.2 MB (120173514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4eedbe26792d18178160e5dcde207ba967194bd349ffcd5d031dc9fe030886f`  
		Last Modified: Mon, 22 Jul 2024 23:03:38 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:f81efc1e2ba132cb65e401d43c471348dcb3fd0d7786d2727e9d9e1bb433f8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1346716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f7aa2e6d1ce1736775a71d385813b5a3402daee13bc282c5cc51e0d43328bb`

```dockerfile
```

-	Layers:
	-	`sha256:07556575e076975a28eba36f80036245b77ecaa24aaf70c59945d736586b6b73`  
		Last Modified: Mon, 22 Jul 2024 23:03:38 GMT  
		Size: 1.3 MB (1323705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a769cbc044807e9a1273593b3f9965eded2e21c2307cbc71a4a0e1706449fb51`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 23.0 KB (23011 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:9.0.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2b9455a3dd2f581ae0589b061d171397d2cd36b58d1f4aeb4a3a3c416cfe07a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192798360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38b9db3fc9a76fca4e1d4cccd00e767e946fe5e6b43fe630e76744b4527f98d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bfb88f92130c70d4fa52b1899c69f532e3309325e1341fde1b7ce678ea419f`  
		Last Modified: Tue, 23 Jul 2024 11:56:00 GMT  
		Size: 68.5 MB (68527489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6159251b20b7872f263aaaabcb7d88ab76d15fdd9a8d308c08422c3d638c924`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6676aeef57ddb30577609ead8772b387507763efadd3b53daf96da53858366c1`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe859b0f70508e627ead785fd23f4b42d0ab2f86e1545b35689780780322346`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4442509c7fcc9fcd18aa44513795a6cb37434e5d5a0a6e2019956615e15a86ca`  
		Last Modified: Tue, 23 Jul 2024 11:55:58 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f383a3dba676f157f576b17e360db280bf4a350855431bb1c2787e379f15f9`  
		Last Modified: Tue, 23 Jul 2024 11:56:02 GMT  
		Size: 120.2 MB (120173507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f46cadf33f5acb346cf41bb1eb3de1e38291269afb40decae1939e319b36e1`  
		Last Modified: Tue, 23 Jul 2024 11:55:58 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:42bc4c0bb298554e61aa476e29b21348df3b8db40f3e4eadd1b569adf2f711f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1346132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cb76f79c3c84039735c42024705c7f8056178f9bf88a8fac025332183a457a`

```dockerfile
```

-	Layers:
	-	`sha256:9180d571cd09e575ffb0af683371ba22e86ce51d62b128965b5ce6278af2b520`  
		Last Modified: Tue, 23 Jul 2024 11:55:58 GMT  
		Size: 1.3 MB (1322809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09e8af6a51ca6451cb53c68ed42c24a290cc6f12aa19ea36bb545f4ad2453bba`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:9.0.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:d81406a31ab5d80ed346312279dd71a3cc27b9706d80ea8b6c01238f0cfca82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189100475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e3148b64b8646e80f9f62ae5818c44bdc798ddfa47e1dafe826f2fe15b919d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251f343304d515f13e423d23fc7a0c26f78285f66eaad08626678a47be01dfbf`  
		Last Modified: Tue, 23 Jul 2024 08:34:22 GMT  
		Size: 65.3 MB (65344960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f816b7e6293d63faeefdcfd241c23a5adc2cd37c3c7940ba5960e994607c488`  
		Last Modified: Tue, 23 Jul 2024 08:34:19 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f722d7fcdc0a5fc8776c33f287ee14e2173ee76a55444d22fbb62c0cefbf14f`  
		Last Modified: Tue, 23 Jul 2024 08:34:20 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c22f671ec177720f0989457de7bb618b96c38e42e66e331244ce909178a699`  
		Last Modified: Tue, 23 Jul 2024 08:34:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa18d6e00a0374f9c83781bf6e45ad213594e13b52d2c26f9cd4a9f13f06d3f`  
		Last Modified: Tue, 23 Jul 2024 08:34:20 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df4fd0bbfc259dc847c31d3b3bd3a77874f9c0974831447d9888d6989b412f2`  
		Last Modified: Tue, 23 Jul 2024 08:34:24 GMT  
		Size: 120.2 MB (120173530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6848d09dfd0f6288674fb7ecadab78c01b5bb484e1f6c7c1034a1699320fcb`  
		Last Modified: Tue, 23 Jul 2024 08:34:21 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:9.0.0` - unknown; unknown

```console
$ docker pull bonita@sha256:aa9a061ea8f904ed4f074ad1ba332a2aeb96df298200b4cbe64c80160d128027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1343849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db041c68bf817426e604e163cefc71bff5cc20d64b1b07ba3d9cc8f317c83a7`

```dockerfile
```

-	Layers:
	-	`sha256:8ca2880cb66fbc02f9bcc57cedbd0a4f77a9764c83ec3f34a51dd4d203bdd683`  
		Last Modified: Tue, 23 Jul 2024 08:34:20 GMT  
		Size: 1.3 MB (1320786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2df95bd07324a8822cba0d0d2a55a3d6bb200578fbf02c96c499bc2a9e752655`  
		Last Modified: Tue, 23 Jul 2024 08:34:19 GMT  
		Size: 23.1 KB (23063 bytes)  
		MIME: application/vnd.in-toto+json

## `bonita:latest`

```console
$ docker pull bonita@sha256:5a5453968d046efc29d0e7256da172fb45e1ba5400fa4e0f9946f62f256adff4
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
$ docker pull bonita@sha256:fb07515c82f066960b3b92f11bc4784fa86758b25611b46b48d4480ae6f2b7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192379686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb166874fbd87049328e914cef544f602684f4e2dc5857acf8f2ca7d0eebdc40`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595e01aa4eb60f98d294bf0ec435daabf12482951b82a734e6d8c388cd39ff79`  
		Last Modified: Mon, 22 Jul 2024 23:03:39 GMT  
		Size: 68.6 MB (68572848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ee2684decf767285f0aadba6014fe829a0e7abbbc3ba910f10a93d9c6c9aba`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2938d41a64655d7ec192c26f93ab16e8ac2871ec8f4f97aacfd6c4ad0068d0`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f9351cd9c3e6f9cd1cbd9c0d5be4024f89981700473011d280c392e2dacaea`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61139da512cde90a6b259c6438796bde5e165678b35384021b52ec9ce6a1e150`  
		Last Modified: Mon, 22 Jul 2024 23:03:38 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454fff921a6d3ec6dae173c4c7aebfa51a0c4bbdf6bafbea58759adff5e81a78`  
		Last Modified: Mon, 22 Jul 2024 23:03:42 GMT  
		Size: 120.2 MB (120173514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4eedbe26792d18178160e5dcde207ba967194bd349ffcd5d031dc9fe030886f`  
		Last Modified: Mon, 22 Jul 2024 23:03:38 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:latest` - unknown; unknown

```console
$ docker pull bonita@sha256:f81efc1e2ba132cb65e401d43c471348dcb3fd0d7786d2727e9d9e1bb433f8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1346716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f7aa2e6d1ce1736775a71d385813b5a3402daee13bc282c5cc51e0d43328bb`

```dockerfile
```

-	Layers:
	-	`sha256:07556575e076975a28eba36f80036245b77ecaa24aaf70c59945d736586b6b73`  
		Last Modified: Mon, 22 Jul 2024 23:03:38 GMT  
		Size: 1.3 MB (1323705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a769cbc044807e9a1273593b3f9965eded2e21c2307cbc71a4a0e1706449fb51`  
		Last Modified: Mon, 22 Jul 2024 23:03:37 GMT  
		Size: 23.0 KB (23011 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2b9455a3dd2f581ae0589b061d171397d2cd36b58d1f4aeb4a3a3c416cfe07a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192798360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38b9db3fc9a76fca4e1d4cccd00e767e946fe5e6b43fe630e76744b4527f98d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bfb88f92130c70d4fa52b1899c69f532e3309325e1341fde1b7ce678ea419f`  
		Last Modified: Tue, 23 Jul 2024 11:56:00 GMT  
		Size: 68.5 MB (68527489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6159251b20b7872f263aaaabcb7d88ab76d15fdd9a8d308c08422c3d638c924`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6676aeef57ddb30577609ead8772b387507763efadd3b53daf96da53858366c1`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe859b0f70508e627ead785fd23f4b42d0ab2f86e1545b35689780780322346`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4442509c7fcc9fcd18aa44513795a6cb37434e5d5a0a6e2019956615e15a86ca`  
		Last Modified: Tue, 23 Jul 2024 11:55:58 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f383a3dba676f157f576b17e360db280bf4a350855431bb1c2787e379f15f9`  
		Last Modified: Tue, 23 Jul 2024 11:56:02 GMT  
		Size: 120.2 MB (120173507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f46cadf33f5acb346cf41bb1eb3de1e38291269afb40decae1939e319b36e1`  
		Last Modified: Tue, 23 Jul 2024 11:55:58 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:latest` - unknown; unknown

```console
$ docker pull bonita@sha256:42bc4c0bb298554e61aa476e29b21348df3b8db40f3e4eadd1b569adf2f711f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1346132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cb76f79c3c84039735c42024705c7f8056178f9bf88a8fac025332183a457a`

```dockerfile
```

-	Layers:
	-	`sha256:9180d571cd09e575ffb0af683371ba22e86ce51d62b128965b5ce6278af2b520`  
		Last Modified: Tue, 23 Jul 2024 11:55:58 GMT  
		Size: 1.3 MB (1322809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09e8af6a51ca6451cb53c68ed42c24a290cc6f12aa19ea36bb545f4ad2453bba`  
		Last Modified: Tue, 23 Jul 2024 11:55:57 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.in-toto+json

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:d81406a31ab5d80ed346312279dd71a3cc27b9706d80ea8b6c01238f0cfca82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189100475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e3148b64b8646e80f9f62ae5818c44bdc798ddfa47e1dafe826f2fe15b919d`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 08 Jul 2024 07:08:41 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 08 Jul 2024 07:08:41 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach openjdk11-jre gnupg # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BRANDING_VERSION
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_SHA256
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BASE_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ARG BONITA_URL
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_VERSION=9.0.0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BRANDING_VERSION=2023.2-u0
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ZIP_FILE=BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 08 Jul 2024 07:08:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN mkdir /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
COPY files /opt/files # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
# ARGS: BONITA_VERSION=9.0.0 BRANDING_VERSION=2023.2-u0 BONITA_SHA256=c37be3ca64a07810609c97f75c47acb7fea2d29bafff181b447987514b53d140 BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2023.2-u0/BonitaCommunity-2023.2-u0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_API_PASSWORD=
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 08 Jul 2024 07:08:41 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 08 Jul 2024 07:08:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 08 Jul 2024 07:08:41 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 08 Jul 2024 07:08:41 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 08 Jul 2024 07:08:41 GMT
COPY templates /opt/templates # buildkit
# Mon, 08 Jul 2024 07:08:41 GMT
VOLUME [/opt/bonita/conf/logs]
# Mon, 08 Jul 2024 07:08:41 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 08 Jul 2024 07:08:41 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Mon, 08 Jul 2024 07:08:41 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251f343304d515f13e423d23fc7a0c26f78285f66eaad08626678a47be01dfbf`  
		Last Modified: Tue, 23 Jul 2024 08:34:22 GMT  
		Size: 65.3 MB (65344960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f816b7e6293d63faeefdcfd241c23a5adc2cd37c3c7940ba5960e994607c488`  
		Last Modified: Tue, 23 Jul 2024 08:34:19 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f722d7fcdc0a5fc8776c33f287ee14e2173ee76a55444d22fbb62c0cefbf14f`  
		Last Modified: Tue, 23 Jul 2024 08:34:20 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c22f671ec177720f0989457de7bb618b96c38e42e66e331244ce909178a699`  
		Last Modified: Tue, 23 Jul 2024 08:34:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa18d6e00a0374f9c83781bf6e45ad213594e13b52d2c26f9cd4a9f13f06d3f`  
		Last Modified: Tue, 23 Jul 2024 08:34:20 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df4fd0bbfc259dc847c31d3b3bd3a77874f9c0974831447d9888d6989b412f2`  
		Last Modified: Tue, 23 Jul 2024 08:34:24 GMT  
		Size: 120.2 MB (120173530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6848d09dfd0f6288674fb7ecadab78c01b5bb484e1f6c7c1034a1699320fcb`  
		Last Modified: Tue, 23 Jul 2024 08:34:21 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:latest` - unknown; unknown

```console
$ docker pull bonita@sha256:aa9a061ea8f904ed4f074ad1ba332a2aeb96df298200b4cbe64c80160d128027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1343849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db041c68bf817426e604e163cefc71bff5cc20d64b1b07ba3d9cc8f317c83a7`

```dockerfile
```

-	Layers:
	-	`sha256:8ca2880cb66fbc02f9bcc57cedbd0a4f77a9764c83ec3f34a51dd4d203bdd683`  
		Last Modified: Tue, 23 Jul 2024 08:34:20 GMT  
		Size: 1.3 MB (1320786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2df95bd07324a8822cba0d0d2a55a3d6bb200578fbf02c96c499bc2a9e752655`  
		Last Modified: Tue, 23 Jul 2024 08:34:19 GMT  
		Size: 23.1 KB (23063 bytes)  
		MIME: application/vnd.in-toto+json
