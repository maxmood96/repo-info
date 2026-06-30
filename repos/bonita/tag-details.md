<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `bonita`

-	[`bonita:11.1`](#bonita111)
-	[`bonita:11.1.0`](#bonita1110)
-	[`bonita:2026.2`](#bonita20262)
-	[`bonita:2026.2-u0`](#bonita20262-u0)
-	[`bonita:latest`](#bonitalatest)

## `bonita:11.1`

```console
$ docker pull bonita@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `bonita:11.1.0`

```console
$ docker pull bonita@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `bonita:2026.2`

```console
$ docker pull bonita@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `bonita:2026.2-u0`

```console
$ docker pull bonita@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `bonita:latest`

```console
$ docker pull bonita@sha256:29a9e05eb66391835a648083af17e013bdb06244f4ce923db4de8f7165ccc849
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:9705bf2773c1f423d544c0183a850f3446b7cab84a29c8e6bb4d3c7bec75f007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186489443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05778afa787814322865276a3954e772794c36d3d5f4ec79621e8ba49d9f3640`
-	Entrypoint: `["\/__cacert_entrypoint.sh","\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:56:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:56:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:56:31 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:56:31 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Mon, 22 Jun 2026 19:57:29 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='33399db5fb4f542df36a706d6642a3ba1fab3d247da707273a11ef29e39f0705';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='b75c9f0dd052adfd213f0c2c1cc0c8a6d4539a8de9f7947d2b8fc45d18289975';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 22 Jun 2026 19:57:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:57:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:57:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 20:24:14 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 22 Jun 2026 20:24:14 GMT
RUN apk add --no-cache tzdata curl unzip bash su-exec jattach # buildkit
# Mon, 22 Jun 2026 20:24:14 GMT
RUN mkdir /opt/custom-init.d/ # buildkit
# Mon, 22 Jun 2026 20:24:14 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S -G bonita -h /opt/bonita/ -s /sbin/nologin bonita # buildkit
# Mon, 22 Jun 2026 20:24:14 GMT
ARG BONITA_VERSION
# Mon, 22 Jun 2026 20:24:14 GMT
ARG BRANDING_VERSION
# Mon, 22 Jun 2026 20:24:14 GMT
ARG BONITA_SHA256
# Mon, 22 Jun 2026 20:24:14 GMT
ARG BASE_URL
# Mon, 22 Jun 2026 20:24:14 GMT
ARG BONITA_URL
# Mon, 22 Jun 2026 20:24:14 GMT
ARG PROGRADE_VERSION=1.1.1
# Mon, 22 Jun 2026 20:24:14 GMT
ARG PROGRADE_JAR_SHA1=300d7ee29d79cc0ad8aad8e7abe17588ad3d33c5
# Mon, 22 Jun 2026 20:24:14 GMT
ENV BONITA_VERSION=11.0.0
# Mon, 22 Jun 2026 20:24:14 GMT
ENV BRANDING_VERSION=2026.1-u0
# Mon, 22 Jun 2026 20:24:14 GMT
ENV BONITA_SHA256=a3a0c80b975b51e247c630a204170beb675f4a83139ff2d1c533c1b7db17a25b
# Mon, 22 Jun 2026 20:24:14 GMT
ENV ZIP_FILE=BonitaCommunity-2026.1-u0.zip
# Mon, 22 Jun 2026 20:24:14 GMT
ENV BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat
# Mon, 22 Jun 2026 20:24:14 GMT
ENV BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/11.0.0/bundle-tomcat-11.0.0.zip
# Mon, 22 Jun 2026 20:24:15 GMT
# ARGS: BONITA_VERSION=11.0.0 BRANDING_VERSION=2026.1-u0 BONITA_SHA256=a3a0c80b975b51e247c630a204170beb675f4a83139ff2d1c533c1b7db17a25b BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/11.0.0/bundle-tomcat-11.0.0.zip PROGRADE_VERSION=1.1.1 PROGRADE_JAR_SHA1=300d7ee29d79cc0ad8aad8e7abe17588ad3d33c5
RUN mkdir /opt/files # buildkit
# Mon, 22 Jun 2026 20:24:15 GMT
COPY files /opt/files # buildkit
# Mon, 22 Jun 2026 20:24:19 GMT
# ARGS: BONITA_VERSION=11.0.0 BRANDING_VERSION=2026.1-u0 BONITA_SHA256=a3a0c80b975b51e247c630a204170beb675f4a83139ff2d1c533c1b7db17a25b BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/11.0.0/bundle-tomcat-11.0.0.zip PROGRADE_VERSION=1.1.1 PROGRADE_JAR_SHA1=300d7ee29d79cc0ad8aad8e7abe17588ad3d33c5
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then       echo "File already present in /opt/files";     else       curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip       && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c -;     fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/conf/prograde   && mv /opt/files/prograde.policy /opt/bonita/conf/prograde/   && wget -nv -O pro-grade.jar https://repo1.maven.org/maven2/net/sourceforge/pro-grade/pro-grade/${PROGRADE_VERSION}/pro-grade-${PROGRADE_VERSION}.jar   && echo "${PROGRADE_JAR_SHA1}  pro-grade.jar" | sha1sum -c -   && mv pro-grade.jar /opt/bonita/server/lib/ext/pro-grade.jar   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup # buildkit
# Mon, 22 Jun 2026 20:24:19 GMT
ENV HTTP_API=false
# Mon, 22 Jun 2026 20:24:19 GMT
ENV HTTP_API_USERNAME=http-api
# Mon, 22 Jun 2026 20:24:19 GMT
ENV HTTP_API_PASSWORD=
# Mon, 22 Jun 2026 20:24:19 GMT
ENV MONITORING_USERNAME=monitoring
# Mon, 22 Jun 2026 20:24:19 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Mon, 22 Jun 2026 20:24:19 GMT
ENV JMX_REMOTE_ACCESS=false
# Mon, 22 Jun 2026 20:24:19 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Mon, 22 Jun 2026 20:24:19 GMT
ENV PRO_GRADE=true
# Mon, 22 Jun 2026 20:24:19 GMT
ENV PRO_GRADE_POLICY_PATH=/opt/bonita/conf/prograde
# Mon, 22 Jun 2026 20:24:19 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Mon, 22 Jun 2026 20:24:19 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Mon, 22 Jun 2026 20:24:19 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Mon, 22 Jun 2026 20:24:19 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Mon, 22 Jun 2026 20:24:19 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Mon, 22 Jun 2026 20:24:19 GMT
ENV HTTP_MAX_THREADS=20
# Mon, 22 Jun 2026 20:24:19 GMT
COPY templates /opt/templates # buildkit
# Mon, 22 Jun 2026 20:24:19 GMT
EXPOSE map[8080/tcp:{} 9000/tcp:{}]
# Mon, 22 Jun 2026 20:24:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh" "/opt/files/startup.sh"]
# Mon, 22 Jun 2026 20:24:19 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37871e84e40af454a54b03c545cfa7a05d360b1cf8bdc2b2faef8da08b487358`  
		Last Modified: Mon, 22 Jun 2026 19:56:45 GMT  
		Size: 16.8 MB (16815714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48bc301bba7c8d73bf2805c4290bb5114f91b9282b58db35a330e971859078c`  
		Last Modified: Mon, 22 Jun 2026 19:57:42 GMT  
		Size: 53.3 MB (53301851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfab6bf27dfce5f5d20f1f7581fde4dea20655dee7870bf82459720482da648`  
		Last Modified: Mon, 22 Jun 2026 19:57:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e04dda4cc8f30bcf6b1d841e785d39480726e5c43ef4a831590bee62f6096d`  
		Last Modified: Mon, 22 Jun 2026 19:57:40 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c97c701f173ccb02b150aeff3856ffac07e1a297e55383e2dfef4439171f7e7`  
		Last Modified: Mon, 22 Jun 2026 20:24:30 GMT  
		Size: 1.6 MB (1560725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f5954195cabf144a201b17f5e2f18cffada7fd4e2e9b248b3a49bcbea85aeb`  
		Last Modified: Mon, 22 Jun 2026 20:24:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2504f9b7ba8e15c8f984a74abee0dff07dfd32c60c6ff1682d8ec7ef1a14b94`  
		Last Modified: Mon, 22 Jun 2026 20:24:29 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b664a84877b1f36032019901eab3c8b50b8f26cd48d72731b95531360280ee91`  
		Last Modified: Mon, 22 Jun 2026 20:24:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ac1babae109212570d0aef5280cff263f83892db8938751ac7c9060558ecac`  
		Last Modified: Mon, 22 Jun 2026 20:24:31 GMT  
		Size: 4.9 KB (4924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aee428edf553411a32603f497ff3639a1cde6a7a0ec51eb26c9114534ed7b0`  
		Last Modified: Mon, 22 Jun 2026 20:24:34 GMT  
		Size: 111.0 MB (110952266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145f9d94503e0140325718d3e5579facdff56c2d46371557acfca0503e49a2ee`  
		Last Modified: Mon, 22 Jun 2026 20:24:31 GMT  
		Size: 6.0 KB (5952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bonita:latest` - unknown; unknown

```console
$ docker pull bonita@sha256:cc510c2469d8ab2ac6df77ff39304955e8a621494d6bd8a2cf42d1c5ba6eb3b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1235448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3ec399277a7ad4b46b0e52f749d944fc436441665c006a09a6eb6f47a8a6d6`

```dockerfile
```

-	Layers:
	-	`sha256:90f42c8c363842ecdde601da24ce3b4aeb6065fe9d99fcec560b2e40da55b33a`  
		Last Modified: Mon, 22 Jun 2026 20:24:29 GMT  
		Size: 1.2 MB (1204742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a40a43f6dc137701b01217585ec4170e7955c71861795d36818a77d8ae05d1a6`  
		Last Modified: Mon, 22 Jun 2026 20:24:29 GMT  
		Size: 30.7 KB (30706 bytes)  
		MIME: application/vnd.in-toto+json
