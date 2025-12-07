## `bonita:latest`

```console
$ docker pull bonita@sha256:8d49dbbb8d3b84ab58c08a3e87eb00e83cca5bec1aba68c793b11cc25ca17563
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:b4dd4adc5f04f4b9342eb74569d4ad6ace0563dda417f3fa902ad7a1bb7082d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (195029081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb88ba891f1d087a1908a91261b3ef4559ae3a66c545052d32f9d94967d088f`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:59:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:36 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:59:36 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7f8c230ba505b418e4288e2b34758a6e4da32470944740e5ba0cfaae02271c22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='17aca4ecc1600f70ec88ea0f8bf3a06ba6806bdae8c96d03c07683c800f0d4e8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sat, 08 Nov 2025 17:59:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:40:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 08 Nov 2025 18:40:18 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach # buildkit
# Sat, 08 Nov 2025 18:40:18 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Sat, 08 Nov 2025 18:40:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S -G bonita -h /opt/bonita/ -s /sbin/nologin bonita # buildkit
# Sat, 08 Nov 2025 18:40:18 GMT
ARG BONITA_VERSION
# Sat, 08 Nov 2025 18:40:18 GMT
ARG BRANDING_VERSION
# Sat, 08 Nov 2025 18:40:18 GMT
ARG BONITA_SHA256
# Sat, 08 Nov 2025 18:40:18 GMT
ARG BASE_URL
# Sat, 08 Nov 2025 18:40:18 GMT
ARG BONITA_URL
# Sat, 08 Nov 2025 18:40:18 GMT
ENV BONITA_VERSION=10.3.0
# Sat, 08 Nov 2025 18:40:18 GMT
ENV BRANDING_VERSION=2025.1-u0
# Sat, 08 Nov 2025 18:40:18 GMT
ENV BONITA_SHA256=44c078fad0ffeec0afac2bf512040be16af4b722369039fe3daef1c091594637
# Sat, 08 Nov 2025 18:40:18 GMT
ENV ZIP_FILE=BonitaCommunity-2025.1-u0.zip
# Sat, 08 Nov 2025 18:40:18 GMT
ENV BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat
# Sat, 08 Nov 2025 18:40:18 GMT
ENV BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.3.0/bundle-tomcat-10.3.0.zip
# Sat, 08 Nov 2025 18:40:18 GMT
# ARGS: BONITA_VERSION=10.3.0 BRANDING_VERSION=2025.1-u0 BONITA_SHA256=44c078fad0ffeec0afac2bf512040be16af4b722369039fe3daef1c091594637 BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.3.0/bundle-tomcat-10.3.0.zip
RUN mkdir /opt/files # buildkit
# Sat, 08 Nov 2025 18:40:18 GMT
COPY files /opt/files # buildkit
# Sat, 08 Nov 2025 18:40:22 GMT
# ARGS: BONITA_VERSION=10.3.0 BRANDING_VERSION=2025.1-u0 BONITA_SHA256=44c078fad0ffeec0afac2bf512040be16af4b722369039fe3daef1c091594637 BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.3.0/bundle-tomcat-10.3.0.zip
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then       echo "File already present in /opt/files";     else       curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip       && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c -;     fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Sat, 08 Nov 2025 18:40:22 GMT
ENV HTTP_API=false
# Sat, 08 Nov 2025 18:40:22 GMT
ENV HTTP_API_USERNAME=http-api
# Sat, 08 Nov 2025 18:40:22 GMT
ENV HTTP_API_PASSWORD=
# Sat, 08 Nov 2025 18:40:22 GMT
ENV MONITORING_USERNAME=monitoring
# Sat, 08 Nov 2025 18:40:22 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Sat, 08 Nov 2025 18:40:22 GMT
ENV JMX_REMOTE_ACCESS=false
# Sat, 08 Nov 2025 18:40:22 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Sat, 08 Nov 2025 18:40:22 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Sat, 08 Nov 2025 18:40:22 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Sat, 08 Nov 2025 18:40:22 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Sat, 08 Nov 2025 18:40:22 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Sat, 08 Nov 2025 18:40:22 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Sat, 08 Nov 2025 18:40:22 GMT
ENV HTTP_MAX_THREADS=20
# Sat, 08 Nov 2025 18:40:22 GMT
COPY templates /opt/templates # buildkit
# Sat, 08 Nov 2025 18:40:22 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Sat, 08 Nov 2025 18:40:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh" "/opt/files/startup.sh"]
# Sat, 08 Nov 2025 18:40:22 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6625eac0c56afe980468268c82e58541814b3f353faae75b36aa85b733b9f6`  
		Last Modified: Sat, 08 Nov 2025 17:59:59 GMT  
		Size: 16.2 MB (16174571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a857bcc1a1505748a54fef25bb81f303468a26d3de127b6b0044b1ffde6275a`  
		Last Modified: Sat, 08 Nov 2025 18:00:03 GMT  
		Size: 53.2 MB (53169034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a75c308165465141d861c1b7f7ec799b18fc84d5d8b87396dc29c3aa4894ff`  
		Last Modified: Sat, 08 Nov 2025 17:59:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d1cf1d02f064d13d647e4816e26b17678a634769ec583b4eb29d5a68d415f7`  
		Last Modified: Sat, 08 Nov 2025 17:59:56 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c2cd3cf6daf2cde73c66d1921525d08278a3fbe222cf0d209c896d7b7fb095`  
		Last Modified: Sat, 08 Nov 2025 18:41:08 GMT  
		Size: 1.9 MB (1889200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7147ec54ee7a80ff31f7853a1748890f5bdb1069da2591c7e19745c00f0e9f`  
		Last Modified: Sat, 08 Nov 2025 18:41:08 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54403d7e4e63d8e87e7c3ed7650a10254a11796e06b5a087ca86e08259085c9`  
		Last Modified: Sat, 08 Nov 2025 18:41:08 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569cbebd07a0751223ecc2145595365ee00440b046a2fdb7772894308350ef1a`  
		Last Modified: Sat, 08 Nov 2025 18:41:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14621d7c249278b05815f4411941b709dc3104e4d6065b7c91813ed4e1eb177`  
		Last Modified: Sat, 08 Nov 2025 18:41:08 GMT  
		Size: 3.7 KB (3715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2846b2ef9babe9dc04605b285fba170e7ebcb2e0daa214a98b79f79aa4a7a6e`  
		Last Modified: Sat, 08 Nov 2025 18:41:17 GMT  
		Size: 120.1 MB (120140554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b75dede3efb7866b7b8659fc9c29aa34a6ebc1a084dd59f49226d95c550ca5`  
		Last Modified: Sat, 08 Nov 2025 18:41:08 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:latest` - unknown; unknown

```console
$ docker pull bonita@sha256:28b34fb582a4ab09c5b971976f9e5458fc1135f48fbad39b2d1df839d649480a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1320629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da158668979f1b6415167a59e1f050af305dbc87a82e5d3469d03c669b6d323`

```dockerfile
```

-	Layers:
	-	`sha256:46aa5efe204ba5beeca39870ff2645352836fb6089a536cf9cbd3df420f1fa06`  
		Last Modified: Sat, 08 Nov 2025 21:55:17 GMT  
		Size: 1.3 MB (1291472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d7d71037cd99c1d30e95dbb027852b9ed94033856c09f2a4d0aa284508e26bb`  
		Last Modified: Sat, 08 Nov 2025 21:55:18 GMT  
		Size: 29.2 KB (29157 bytes)  
		MIME: application/vnd.in-toto+json
