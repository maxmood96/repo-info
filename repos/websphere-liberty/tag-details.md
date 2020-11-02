<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `websphere-liberty`

-	[`websphere-liberty:20.0.0.11-full-java8-ibmjava`](#websphere-liberty200011-full-java8-ibmjava)
-	[`websphere-liberty:20.0.0.11-kernel-java8-ibmjava`](#websphere-liberty200011-kernel-java8-ibmjava)
-	[`websphere-liberty:20.0.0.6-full-java8-ibmjava`](#websphere-liberty20006-full-java8-ibmjava)
-	[`websphere-liberty:20.0.0.6-kernel-java8-ibmjava`](#websphere-liberty20006-kernel-java8-ibmjava)
-	[`websphere-liberty:20.0.0.9-full-java8-ibmjava`](#websphere-liberty20009-full-java8-ibmjava)
-	[`websphere-liberty:20.0.0.9-kernel-java8-ibmjava`](#websphere-liberty20009-kernel-java8-ibmjava)
-	[`websphere-liberty:beta`](#websphere-libertybeta)
-	[`websphere-liberty:full`](#websphere-libertyfull)
-	[`websphere-liberty:kernel`](#websphere-libertykernel)
-	[`websphere-liberty:latest`](#websphere-libertylatest)

## `websphere-liberty:20.0.0.11-full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:18eda83455b37361d5b8185db35b036b0741e2d6321edc3f320f76f99a2005bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; s390x

### `websphere-liberty:20.0.0.11-full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:f2d3484947b5ef3eba60da5da7a2933ee1603dde6ca0866231816b49e35ec8ac
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.3 MB (410339605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a7ae09af3a625913020bd0bbd31fc3a99a3f07ceaa24017811dc94fcc95556`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:44:45 GMT
ADD file:0a8ec4fb62616b6605197e20e0a7b511dc5b03d4af0e04c929dfd9fb457d2065 in / 
# Fri, 25 Sep 2020 22:44:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:44:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:44:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:44:48 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:01:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 25 Sep 2020 23:01:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:44:39 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:46:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:46:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 01:09:20 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 01:09:21 GMT
ARG OPENJ9_SCC=true
# Mon, 02 Nov 2020 21:43:28 GMT
ARG EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033
# Mon, 02 Nov 2020 21:43:28 GMT
ARG NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285
# Mon, 02 Nov 2020 21:43:29 GMT
ARG NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4
# Mon, 02 Nov 2020 21:43:29 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.11 org.opencontainers.image.revision=cl201120201014-1215 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Mon, 02 Nov 2020 21:43:29 GMT
ENV LIBERTY_VERSION=20.0.0_11
# Mon, 02 Nov 2020 21:43:29 GMT
ARG LIBERTY_URL
# Mon, 02 Nov 2020 21:43:30 GMT
ARG DOWNLOAD_OPTIONS=
# Mon, 02 Nov 2020 21:43:47 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Mon, 02 Nov 2020 21:43:49 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Nov 2020 21:43:50 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.11 BuildLabel=cl201120201014-1215
# Mon, 02 Nov 2020 21:43:50 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Mon, 02 Nov 2020 21:43:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 02 Nov 2020 21:43:53 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Mon, 02 Nov 2020 21:43:54 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Mon, 02 Nov 2020 21:43:55 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Mon, 02 Nov 2020 21:44:05 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Mon, 02 Nov 2020 21:44:05 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Mon, 02 Nov 2020 21:44:06 GMT
USER 1001
# Mon, 02 Nov 2020 21:44:06 GMT
EXPOSE 9080 9443
# Mon, 02 Nov 2020 21:44:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Mon, 02 Nov 2020 21:44:07 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Mon, 02 Nov 2020 21:44:17 GMT
ARG VERBOSE=false
# Mon, 02 Nov 2020 21:44:17 GMT
ARG REPOSITORIES_PROPERTIES=
# Mon, 02 Nov 2020 21:47:46 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Mon, 02 Nov 2020 21:47:55 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Mon, 02 Nov 2020 21:48:28 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:dd2de95b9a1c45e92bcc791d469201229b58d68187c99de6b08b00a13fa33393`  
		Last Modified: Fri, 25 Sep 2020 22:45:52 GMT  
		Size: 25.4 MB (25371975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38a48ef4dfab2bd639d381d11b3390b6bf8860b2ef3356e9bb55f7cb8c775f9`  
		Last Modified: Fri, 25 Sep 2020 22:45:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eced51184728468b347a6e3f143c356cd174c4a54be3cc10ec5aeddb402765fd`  
		Last Modified: Fri, 25 Sep 2020 22:45:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba234a37a5b5e77c8926746b575c905aa5fec2800099d1b330e0b05ecae699e5`  
		Last Modified: Fri, 25 Sep 2020 23:06:23 GMT  
		Size: 2.7 MB (2672151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74bce2b49bfe4913da5bc9719137a9c8d8fe4ae973dfa550b069adb24de7048`  
		Last Modified: Wed, 30 Sep 2020 00:49:52 GMT  
		Size: 127.5 MB (127515953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08d08612c2861209c25e0388fa03a8f4fe3ddbdf39967f0b4f056365f68c0af`  
		Last Modified: Mon, 02 Nov 2020 21:49:16 GMT  
		Size: 27.8 MB (27750974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed39a525cf22a2bdb1fdf34f9d4af2c54f005fa2143d82dd168392e278d8960a`  
		Last Modified: Mon, 02 Nov 2020 21:49:12 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb8c80357fb12d31581890c1f844deba6fe1345e6ee8daf3204f09c1fa90e59`  
		Last Modified: Mon, 02 Nov 2020 21:49:13 GMT  
		Size: 9.4 KB (9397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec7cfc60cd4170ce48119f317a2ec7bff04d5f2e6eb85c47727eecbd9e3b4e8`  
		Last Modified: Mon, 02 Nov 2020 21:49:12 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e5f963669923f98efcd98c1454d5009eef887d9db09246b36281cd08b4755a`  
		Last Modified: Mon, 02 Nov 2020 21:49:13 GMT  
		Size: 10.4 KB (10380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ffb399aa2d3f3f5521e2ddd71ae1c4508bfcca25d8f9a107209a33101f5ad9`  
		Last Modified: Mon, 02 Nov 2020 21:49:13 GMT  
		Size: 5.7 MB (5740146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbb629819ee5a33b88dc1adba9cd8ab0cf15177ed5b3318c952eef818455fc2`  
		Last Modified: Mon, 02 Nov 2020 21:49:32 GMT  
		Size: 200.1 MB (200106867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d43599856aa54a17ca17d3530ffe68e52b5e63287dd373396868e64b88b91cb`  
		Last Modified: Mon, 02 Nov 2020 21:49:23 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed812a4d484b2133a7ab73d780f1a18896b568aeca2cc5ed26315882dfbb9751`  
		Last Modified: Mon, 02 Nov 2020 21:49:26 GMT  
		Size: 21.2 MB (21158808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:20.0.0.11-kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:c89c58478048762f147705cf88f8284a7707777c490a464cba36ba4e4ca53688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; s390x

### `websphere-liberty:20.0.0.11-kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:3b8c9f2857caa79ed8def6c26f462034476188e45d64aadbe4e804f3d8b49ecf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189072982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb40c977e0c23dca8f1107e576710f68870ec733c0a10f2b8f633217d856824f`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:44:45 GMT
ADD file:0a8ec4fb62616b6605197e20e0a7b511dc5b03d4af0e04c929dfd9fb457d2065 in / 
# Fri, 25 Sep 2020 22:44:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:44:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:44:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:44:48 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:01:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 25 Sep 2020 23:01:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:44:39 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:46:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:46:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 01:09:20 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 01:09:21 GMT
ARG OPENJ9_SCC=true
# Mon, 02 Nov 2020 21:43:28 GMT
ARG EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033
# Mon, 02 Nov 2020 21:43:28 GMT
ARG NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285
# Mon, 02 Nov 2020 21:43:29 GMT
ARG NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4
# Mon, 02 Nov 2020 21:43:29 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.11 org.opencontainers.image.revision=cl201120201014-1215 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Mon, 02 Nov 2020 21:43:29 GMT
ENV LIBERTY_VERSION=20.0.0_11
# Mon, 02 Nov 2020 21:43:29 GMT
ARG LIBERTY_URL
# Mon, 02 Nov 2020 21:43:30 GMT
ARG DOWNLOAD_OPTIONS=
# Mon, 02 Nov 2020 21:43:47 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Mon, 02 Nov 2020 21:43:49 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Nov 2020 21:43:50 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.11 BuildLabel=cl201120201014-1215
# Mon, 02 Nov 2020 21:43:50 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Mon, 02 Nov 2020 21:43:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 02 Nov 2020 21:43:53 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Mon, 02 Nov 2020 21:43:54 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Mon, 02 Nov 2020 21:43:55 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Mon, 02 Nov 2020 21:44:05 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Mon, 02 Nov 2020 21:44:05 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Mon, 02 Nov 2020 21:44:06 GMT
USER 1001
# Mon, 02 Nov 2020 21:44:06 GMT
EXPOSE 9080 9443
# Mon, 02 Nov 2020 21:44:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Mon, 02 Nov 2020 21:44:07 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:dd2de95b9a1c45e92bcc791d469201229b58d68187c99de6b08b00a13fa33393`  
		Last Modified: Fri, 25 Sep 2020 22:45:52 GMT  
		Size: 25.4 MB (25371975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38a48ef4dfab2bd639d381d11b3390b6bf8860b2ef3356e9bb55f7cb8c775f9`  
		Last Modified: Fri, 25 Sep 2020 22:45:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eced51184728468b347a6e3f143c356cd174c4a54be3cc10ec5aeddb402765fd`  
		Last Modified: Fri, 25 Sep 2020 22:45:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba234a37a5b5e77c8926746b575c905aa5fec2800099d1b330e0b05ecae699e5`  
		Last Modified: Fri, 25 Sep 2020 23:06:23 GMT  
		Size: 2.7 MB (2672151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74bce2b49bfe4913da5bc9719137a9c8d8fe4ae973dfa550b069adb24de7048`  
		Last Modified: Wed, 30 Sep 2020 00:49:52 GMT  
		Size: 127.5 MB (127515953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08d08612c2861209c25e0388fa03a8f4fe3ddbdf39967f0b4f056365f68c0af`  
		Last Modified: Mon, 02 Nov 2020 21:49:16 GMT  
		Size: 27.8 MB (27750974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed39a525cf22a2bdb1fdf34f9d4af2c54f005fa2143d82dd168392e278d8960a`  
		Last Modified: Mon, 02 Nov 2020 21:49:12 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb8c80357fb12d31581890c1f844deba6fe1345e6ee8daf3204f09c1fa90e59`  
		Last Modified: Mon, 02 Nov 2020 21:49:13 GMT  
		Size: 9.4 KB (9397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec7cfc60cd4170ce48119f317a2ec7bff04d5f2e6eb85c47727eecbd9e3b4e8`  
		Last Modified: Mon, 02 Nov 2020 21:49:12 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e5f963669923f98efcd98c1454d5009eef887d9db09246b36281cd08b4755a`  
		Last Modified: Mon, 02 Nov 2020 21:49:13 GMT  
		Size: 10.4 KB (10380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ffb399aa2d3f3f5521e2ddd71ae1c4508bfcca25d8f9a107209a33101f5ad9`  
		Last Modified: Mon, 02 Nov 2020 21:49:13 GMT  
		Size: 5.7 MB (5740146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:20.0.0.6-full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:57fc2ac9b00c23f89fe3e3c9208cc6183bbd93d7425849436df7f2aa56144021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:20.0.0.6-full-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:512448a0ef7dbb67da775172fbab0f46ececb183e1c1649578663568bdab95ba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.9 MB (395880782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd885d0c7c9c7d40f4c3314b899fe92ff38a3525a923d9eed23b5dd5c6782fd`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 00:39:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 26 Sep 2020 00:39:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:21:19 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:22:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 00:47:06 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 00:47:07 GMT
ARG OPENJ9_SCC=true
# Wed, 30 Sep 2020 00:52:00 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.6 org.opencontainers.image.revision=cl200620200528-0414 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 30 Sep 2020 00:52:01 GMT
ENV LIBERTY_VERSION=20.0.0_06
# Wed, 30 Sep 2020 00:52:01 GMT
ARG LIBERTY_URL
# Wed, 30 Sep 2020 00:52:01 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 30 Sep 2020 00:52:10 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:52:10 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Sep 2020 00:52:10 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.6 BuildLabel=cl200620200528-0414
# Wed, 30 Sep 2020 00:52:10 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 30 Sep 2020 00:52:12 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 02:08:20 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Thu, 22 Oct 2020 02:08:20 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Oct 2020 02:08:20 GMT
COPY dir:f50ec19c0b3217fa3d6d42c3ce4a254879f817de03e99e13f96ba6b66fb6862e in /licenses/ 
# Thu, 22 Oct 2020 02:08:21 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 02:08:33 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Oct 2020 02:08:33 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Thu, 22 Oct 2020 02:08:33 GMT
USER 1001
# Thu, 22 Oct 2020 02:08:33 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 02:08:34 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Oct 2020 02:08:34 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Oct 2020 02:08:38 GMT
ARG VERBOSE=false
# Thu, 22 Oct 2020 02:08:38 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Oct 2020 02:11:36 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Thu, 22 Oct 2020 02:11:36 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Oct 2020 02:12:22 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e87f30ee71d2ba7a1d467dc205703e1443af14fdd58777f796dd35311cc49dc`  
		Last Modified: Sat, 26 Sep 2020 00:44:29 GMT  
		Size: 3.0 MB (2958234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6197f6576703d3211fafc6a64b9bf241bbed280c07aa2aabcc272d0dea695d0`  
		Last Modified: Wed, 30 Sep 2020 00:26:15 GMT  
		Size: 130.3 MB (130288845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8633dd0670be7c95d6883fc2ab61a19469165f71ca8a28f59c7970c4c0043e5`  
		Last Modified: Wed, 30 Sep 2020 00:57:22 GMT  
		Size: 13.8 MB (13765739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404edd26a18a2b7bc87f66a93d9cbd69490b98d52e43088a14be3c1ef8bf4f35`  
		Last Modified: Wed, 30 Sep 2020 00:57:21 GMT  
		Size: 646.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290882eae5c67f046b2c4362101aaf3104c04e01dab687ce5ade5b759ebb5199`  
		Last Modified: Thu, 22 Oct 2020 02:14:29 GMT  
		Size: 9.4 KB (9362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea85acab5c36f76f551fa588112c3c49e2a5e09d7d726c4ddf11e88fa9da2a94`  
		Last Modified: Thu, 22 Oct 2020 02:14:29 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a224fc253bed1371bf62e8328f968a0b649f67686974b8d27ae5b8add7c6136a`  
		Last Modified: Thu, 22 Oct 2020 02:14:29 GMT  
		Size: 57.2 KB (57206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b42f5a504e724b3c535eae231e089658b3610712570a32a929118f975aee08e`  
		Last Modified: Thu, 22 Oct 2020 02:14:29 GMT  
		Size: 10.3 KB (10270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4276015eccaa10ddc6a0bf1a4e7d81c3c1c8660da2112e6682a9869478d834a`  
		Last Modified: Thu, 22 Oct 2020 02:14:30 GMT  
		Size: 5.6 MB (5596087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2c57453406d82f4470ff4a01d8bf7dfb10611842f3f073f807fdc55fb8518e`  
		Last Modified: Thu, 22 Oct 2020 02:14:51 GMT  
		Size: 194.6 MB (194644393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad6b6522d4173fe64e9c92458d36e4e9751b139b92af81ae8518df044ff76c7`  
		Last Modified: Thu, 22 Oct 2020 02:14:35 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c872b9a611c220f41ecf53c7b1acf88b283ddcf651350b2af91ae992bf01c3`  
		Last Modified: Thu, 22 Oct 2020 02:14:39 GMT  
		Size: 21.8 MB (21846171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.6-full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:bc4c4cc01953580c8050ae7c27a674658e9344f9ddab1be6013ff12db7051076
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.0 MB (395002135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c5bf889d6a9382cfaec9b03b8a745a40c62e026db15091a5da5a062c4f565b`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 04:38:06 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 26 Sep 2020 04:38:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:21:11 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:22:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 00:55:46 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 00:55:50 GMT
ARG OPENJ9_SCC=true
# Wed, 30 Sep 2020 01:06:38 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.6 org.opencontainers.image.revision=cl200620200528-0414 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 30 Sep 2020 01:06:40 GMT
ENV LIBERTY_VERSION=20.0.0_06
# Wed, 30 Sep 2020 01:06:45 GMT
ARG LIBERTY_URL
# Wed, 30 Sep 2020 01:06:50 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 30 Sep 2020 01:07:50 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 01:07:58 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Sep 2020 01:08:01 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.6 BuildLabel=cl200620200528-0414
# Wed, 30 Sep 2020 01:08:05 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 30 Sep 2020 01:08:21 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 11:47:15 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Thu, 22 Oct 2020 11:47:17 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Oct 2020 11:47:18 GMT
COPY dir:f50ec19c0b3217fa3d6d42c3ce4a254879f817de03e99e13f96ba6b66fb6862e in /licenses/ 
# Thu, 22 Oct 2020 11:47:31 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 11:47:55 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Oct 2020 11:47:59 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Thu, 22 Oct 2020 11:48:02 GMT
USER 1001
# Thu, 22 Oct 2020 11:48:06 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 11:48:09 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Oct 2020 11:48:13 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Oct 2020 11:48:30 GMT
ARG VERBOSE=false
# Thu, 22 Oct 2020 11:48:32 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Oct 2020 11:54:05 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Thu, 22 Oct 2020 11:54:11 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Oct 2020 11:55:48 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405e3c1dd428ca3ff035da6469a7c6c36d02c92adb80d285656f61f8dd866b1`  
		Last Modified: Sat, 26 Sep 2020 04:43:33 GMT  
		Size: 3.1 MB (3075371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3df9e8e9238216b0bc889f73468bb1724d9dd627858e018235ae9634916c005`  
		Last Modified: Wed, 30 Sep 2020 00:28:00 GMT  
		Size: 129.8 MB (129833821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2378d4c09af6c09df41dd03ea9c83dd69a222bce129fc2624c0be575e71911`  
		Last Modified: Wed, 30 Sep 2020 01:25:38 GMT  
		Size: 13.8 MB (13765463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a240772517c6b242b85e8a3231e2574348ea2220896299d065906e4434b657a`  
		Last Modified: Wed, 30 Sep 2020 01:25:20 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6939a55908e765ebbb6174f1b0d9b698d434ad3d58eaa1927a265327a579658`  
		Last Modified: Thu, 22 Oct 2020 12:04:24 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79b0f7d4bc3ecc249ea8bacc1a97b5a3642eb6d702356e03ef73d0f059c2a4f`  
		Last Modified: Thu, 22 Oct 2020 12:04:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379b8bc1a27ce89d84424906b0f4238463699811157f5de8d2dab0d10bb59e4a`  
		Last Modified: Thu, 22 Oct 2020 12:04:25 GMT  
		Size: 57.2 KB (57205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f88d625f374044230482590cd5cb33506b63f8dc5560eb8593f99f9982f9dc`  
		Last Modified: Thu, 22 Oct 2020 12:04:24 GMT  
		Size: 10.4 KB (10390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30410bad077657c9c0e3b2e59e5bfcc179f313bf52511ecc2267115eecbce69`  
		Last Modified: Thu, 22 Oct 2020 12:04:29 GMT  
		Size: 5.2 MB (5169922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d671f54b6c7d2f98eb8ac14347174040007a3995e389e3680652c1c2c61bbe8`  
		Last Modified: Thu, 22 Oct 2020 12:07:13 GMT  
		Size: 194.2 MB (194225806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a946b5663391f6728a6e367fe7108572a5b87e997acae61d798fd9a469d72d7f`  
		Last Modified: Thu, 22 Oct 2020 12:04:42 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc6ae56d38c11e926047e0849f59fbaad173eda468ffcf2ea170fcbe751162c`  
		Last Modified: Thu, 22 Oct 2020 12:04:55 GMT  
		Size: 18.4 MB (18443298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.6-full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:cc4087d63591f22a3e458434c31f62d1ce6b79f20e0541d57c4468e3106dc124
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.4 MB (391438031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdfb8a24f5b861822bfa69c197e2cbe9963fa75a67451d01bc2bfefcccfb8a28`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:44:45 GMT
ADD file:0a8ec4fb62616b6605197e20e0a7b511dc5b03d4af0e04c929dfd9fb457d2065 in / 
# Fri, 25 Sep 2020 22:44:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:44:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:44:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:44:48 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:01:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 25 Sep 2020 23:01:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:44:39 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:46:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:46:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 01:09:20 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 01:09:21 GMT
ARG OPENJ9_SCC=true
# Wed, 30 Sep 2020 01:15:39 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.6 org.opencontainers.image.revision=cl200620200528-0414 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 30 Sep 2020 01:15:39 GMT
ENV LIBERTY_VERSION=20.0.0_06
# Wed, 30 Sep 2020 01:15:40 GMT
ARG LIBERTY_URL
# Wed, 30 Sep 2020 01:15:41 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 30 Sep 2020 01:15:56 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 01:15:58 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Sep 2020 01:15:59 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.6 BuildLabel=cl200620200528-0414
# Wed, 30 Sep 2020 01:16:00 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 30 Sep 2020 01:16:02 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 02:19:17 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Thu, 22 Oct 2020 02:19:18 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Oct 2020 02:19:18 GMT
COPY dir:f50ec19c0b3217fa3d6d42c3ce4a254879f817de03e99e13f96ba6b66fb6862e in /licenses/ 
# Thu, 22 Oct 2020 02:19:20 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 02:19:31 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Oct 2020 02:19:32 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Thu, 22 Oct 2020 02:19:32 GMT
USER 1001
# Thu, 22 Oct 2020 02:19:33 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 02:19:33 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Oct 2020 02:19:34 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Oct 2020 02:19:38 GMT
ARG VERBOSE=false
# Thu, 22 Oct 2020 02:19:39 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Oct 2020 02:22:54 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Thu, 22 Oct 2020 02:23:03 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Oct 2020 02:23:36 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:dd2de95b9a1c45e92bcc791d469201229b58d68187c99de6b08b00a13fa33393`  
		Last Modified: Fri, 25 Sep 2020 22:45:52 GMT  
		Size: 25.4 MB (25371975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38a48ef4dfab2bd639d381d11b3390b6bf8860b2ef3356e9bb55f7cb8c775f9`  
		Last Modified: Fri, 25 Sep 2020 22:45:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eced51184728468b347a6e3f143c356cd174c4a54be3cc10ec5aeddb402765fd`  
		Last Modified: Fri, 25 Sep 2020 22:45:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba234a37a5b5e77c8926746b575c905aa5fec2800099d1b330e0b05ecae699e5`  
		Last Modified: Fri, 25 Sep 2020 23:06:23 GMT  
		Size: 2.7 MB (2672151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74bce2b49bfe4913da5bc9719137a9c8d8fe4ae973dfa550b069adb24de7048`  
		Last Modified: Wed, 30 Sep 2020 00:49:52 GMT  
		Size: 127.5 MB (127515953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db90a8134ecac4b7768f6837726f00fbad04ce25cf442acc4a3b5b9e05331b4`  
		Last Modified: Wed, 30 Sep 2020 01:23:15 GMT  
		Size: 13.8 MB (13764873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b9d7f1eca87c52fb79c465f3f007f805fc2cfe5a10c7d5b478f8f891f86c7f`  
		Last Modified: Wed, 30 Sep 2020 01:23:13 GMT  
		Size: 690.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0303a641db3b2780627126ef5f20879201a7923bc616595a37fc3639cf1c1e5e`  
		Last Modified: Thu, 22 Oct 2020 02:25:23 GMT  
		Size: 9.4 KB (9390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59e441115d72eb13172be67f6a24b56aed0f64ec222241d0ce644ee6657c8c1`  
		Last Modified: Thu, 22 Oct 2020 02:25:21 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfd42d67b60fa152833fa27994e5cb346683a653ae2ec8afaff249c3a128d18`  
		Last Modified: Thu, 22 Oct 2020 02:25:22 GMT  
		Size: 57.2 KB (57206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea2bbf21fa3e8036e08ab1a7bf00bbeae0bd14c61279aa778efe2e727da1e84`  
		Last Modified: Thu, 22 Oct 2020 02:25:21 GMT  
		Size: 10.4 KB (10375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3086f22f95dbd68134f24ee96362341b5478814a7e58db7fd244e503f4189e0b`  
		Last Modified: Thu, 22 Oct 2020 02:25:22 GMT  
		Size: 5.8 MB (5795659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe06d3cc816f6a095e83a393eb458518fcffc2cad534aeec897a8a0351349be`  
		Last Modified: Thu, 22 Oct 2020 02:25:39 GMT  
		Size: 194.9 MB (194850608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67aa5a5fd82d9d808de3857fdff38159128abd4a2d52e4cf5aa0c3cddc79699c`  
		Last Modified: Thu, 22 Oct 2020 02:25:29 GMT  
		Size: 952.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0b713c15a2156cdbaf67e30e164a925fa2fa554bc6a7914e27891d4cdee283`  
		Last Modified: Thu, 22 Oct 2020 02:25:31 GMT  
		Size: 21.4 MB (21386888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:20.0.0.6-kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:8708ac68dbb08e457e6fc38353fd5991be3b102e045f7a630998c31a80049244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:20.0.0.6-kernel-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:e2bf7b0d79936ccca502a359bce46af4da2a93a52e7c0b34fdd4bdfbf4aedbfd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179389264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f27f021fac135dc559b3550945c7a9383b502a369e7e53ecc3752951186e34`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 00:39:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 26 Sep 2020 00:39:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:21:19 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:22:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 00:47:06 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 00:47:07 GMT
ARG OPENJ9_SCC=true
# Wed, 30 Sep 2020 00:52:00 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.6 org.opencontainers.image.revision=cl200620200528-0414 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 30 Sep 2020 00:52:01 GMT
ENV LIBERTY_VERSION=20.0.0_06
# Wed, 30 Sep 2020 00:52:01 GMT
ARG LIBERTY_URL
# Wed, 30 Sep 2020 00:52:01 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 30 Sep 2020 00:52:10 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:52:10 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Sep 2020 00:52:10 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.6 BuildLabel=cl200620200528-0414
# Wed, 30 Sep 2020 00:52:10 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 30 Sep 2020 00:52:12 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 02:08:20 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Thu, 22 Oct 2020 02:08:20 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Oct 2020 02:08:20 GMT
COPY dir:f50ec19c0b3217fa3d6d42c3ce4a254879f817de03e99e13f96ba6b66fb6862e in /licenses/ 
# Thu, 22 Oct 2020 02:08:21 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 02:08:33 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Oct 2020 02:08:33 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Thu, 22 Oct 2020 02:08:33 GMT
USER 1001
# Thu, 22 Oct 2020 02:08:33 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 02:08:34 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Oct 2020 02:08:34 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e87f30ee71d2ba7a1d467dc205703e1443af14fdd58777f796dd35311cc49dc`  
		Last Modified: Sat, 26 Sep 2020 00:44:29 GMT  
		Size: 3.0 MB (2958234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6197f6576703d3211fafc6a64b9bf241bbed280c07aa2aabcc272d0dea695d0`  
		Last Modified: Wed, 30 Sep 2020 00:26:15 GMT  
		Size: 130.3 MB (130288845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8633dd0670be7c95d6883fc2ab61a19469165f71ca8a28f59c7970c4c0043e5`  
		Last Modified: Wed, 30 Sep 2020 00:57:22 GMT  
		Size: 13.8 MB (13765739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404edd26a18a2b7bc87f66a93d9cbd69490b98d52e43088a14be3c1ef8bf4f35`  
		Last Modified: Wed, 30 Sep 2020 00:57:21 GMT  
		Size: 646.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290882eae5c67f046b2c4362101aaf3104c04e01dab687ce5ade5b759ebb5199`  
		Last Modified: Thu, 22 Oct 2020 02:14:29 GMT  
		Size: 9.4 KB (9362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea85acab5c36f76f551fa588112c3c49e2a5e09d7d726c4ddf11e88fa9da2a94`  
		Last Modified: Thu, 22 Oct 2020 02:14:29 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a224fc253bed1371bf62e8328f968a0b649f67686974b8d27ae5b8add7c6136a`  
		Last Modified: Thu, 22 Oct 2020 02:14:29 GMT  
		Size: 57.2 KB (57206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b42f5a504e724b3c535eae231e089658b3610712570a32a929118f975aee08e`  
		Last Modified: Thu, 22 Oct 2020 02:14:29 GMT  
		Size: 10.3 KB (10270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4276015eccaa10ddc6a0bf1a4e7d81c3c1c8660da2112e6682a9869478d834a`  
		Last Modified: Thu, 22 Oct 2020 02:14:30 GMT  
		Size: 5.6 MB (5596087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.6-kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:bbdb8b69636746d8dc0d5cec13473eb6e8e6e0a3b1d8d847910fe55038fb9cb8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.3 MB (182332075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397ead32ef13f7a48ab4180077fafabbfa232675f2de51a589faf8ae4639318`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 04:38:06 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 26 Sep 2020 04:38:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:21:11 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:22:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 00:55:46 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 00:55:50 GMT
ARG OPENJ9_SCC=true
# Wed, 30 Sep 2020 01:06:38 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.6 org.opencontainers.image.revision=cl200620200528-0414 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 30 Sep 2020 01:06:40 GMT
ENV LIBERTY_VERSION=20.0.0_06
# Wed, 30 Sep 2020 01:06:45 GMT
ARG LIBERTY_URL
# Wed, 30 Sep 2020 01:06:50 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 30 Sep 2020 01:07:50 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 01:07:58 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Sep 2020 01:08:01 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.6 BuildLabel=cl200620200528-0414
# Wed, 30 Sep 2020 01:08:05 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 30 Sep 2020 01:08:21 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 11:47:15 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Thu, 22 Oct 2020 11:47:17 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Oct 2020 11:47:18 GMT
COPY dir:f50ec19c0b3217fa3d6d42c3ce4a254879f817de03e99e13f96ba6b66fb6862e in /licenses/ 
# Thu, 22 Oct 2020 11:47:31 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 11:47:55 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Oct 2020 11:47:59 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Thu, 22 Oct 2020 11:48:02 GMT
USER 1001
# Thu, 22 Oct 2020 11:48:06 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 11:48:09 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Oct 2020 11:48:13 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405e3c1dd428ca3ff035da6469a7c6c36d02c92adb80d285656f61f8dd866b1`  
		Last Modified: Sat, 26 Sep 2020 04:43:33 GMT  
		Size: 3.1 MB (3075371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3df9e8e9238216b0bc889f73468bb1724d9dd627858e018235ae9634916c005`  
		Last Modified: Wed, 30 Sep 2020 00:28:00 GMT  
		Size: 129.8 MB (129833821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2378d4c09af6c09df41dd03ea9c83dd69a222bce129fc2624c0be575e71911`  
		Last Modified: Wed, 30 Sep 2020 01:25:38 GMT  
		Size: 13.8 MB (13765463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a240772517c6b242b85e8a3231e2574348ea2220896299d065906e4434b657a`  
		Last Modified: Wed, 30 Sep 2020 01:25:20 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6939a55908e765ebbb6174f1b0d9b698d434ad3d58eaa1927a265327a579658`  
		Last Modified: Thu, 22 Oct 2020 12:04:24 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79b0f7d4bc3ecc249ea8bacc1a97b5a3642eb6d702356e03ef73d0f059c2a4f`  
		Last Modified: Thu, 22 Oct 2020 12:04:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379b8bc1a27ce89d84424906b0f4238463699811157f5de8d2dab0d10bb59e4a`  
		Last Modified: Thu, 22 Oct 2020 12:04:25 GMT  
		Size: 57.2 KB (57205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f88d625f374044230482590cd5cb33506b63f8dc5560eb8593f99f9982f9dc`  
		Last Modified: Thu, 22 Oct 2020 12:04:24 GMT  
		Size: 10.4 KB (10390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30410bad077657c9c0e3b2e59e5bfcc179f313bf52511ecc2267115eecbce69`  
		Last Modified: Thu, 22 Oct 2020 12:04:29 GMT  
		Size: 5.2 MB (5169922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.6-kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:77fb922c5eed6aafd276f74b9b42b92cf5ed057faff9e632e8086946ad5decd5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175199583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07305e10540846a248f45c93b692c763a9516023efe0c449ad3ef87e4c4772a2`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:44:45 GMT
ADD file:0a8ec4fb62616b6605197e20e0a7b511dc5b03d4af0e04c929dfd9fb457d2065 in / 
# Fri, 25 Sep 2020 22:44:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:44:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:44:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:44:48 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:01:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 25 Sep 2020 23:01:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:44:39 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:46:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:46:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 01:09:20 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 01:09:21 GMT
ARG OPENJ9_SCC=true
# Wed, 30 Sep 2020 01:15:39 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.6 org.opencontainers.image.revision=cl200620200528-0414 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 30 Sep 2020 01:15:39 GMT
ENV LIBERTY_VERSION=20.0.0_06
# Wed, 30 Sep 2020 01:15:40 GMT
ARG LIBERTY_URL
# Wed, 30 Sep 2020 01:15:41 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 30 Sep 2020 01:15:56 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 01:15:58 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Sep 2020 01:15:59 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.6 BuildLabel=cl200620200528-0414
# Wed, 30 Sep 2020 01:16:00 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 30 Sep 2020 01:16:02 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 02:19:17 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Thu, 22 Oct 2020 02:19:18 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Oct 2020 02:19:18 GMT
COPY dir:f50ec19c0b3217fa3d6d42c3ce4a254879f817de03e99e13f96ba6b66fb6862e in /licenses/ 
# Thu, 22 Oct 2020 02:19:20 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 02:19:31 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Oct 2020 02:19:32 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Thu, 22 Oct 2020 02:19:32 GMT
USER 1001
# Thu, 22 Oct 2020 02:19:33 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 02:19:33 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Oct 2020 02:19:34 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:dd2de95b9a1c45e92bcc791d469201229b58d68187c99de6b08b00a13fa33393`  
		Last Modified: Fri, 25 Sep 2020 22:45:52 GMT  
		Size: 25.4 MB (25371975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38a48ef4dfab2bd639d381d11b3390b6bf8860b2ef3356e9bb55f7cb8c775f9`  
		Last Modified: Fri, 25 Sep 2020 22:45:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eced51184728468b347a6e3f143c356cd174c4a54be3cc10ec5aeddb402765fd`  
		Last Modified: Fri, 25 Sep 2020 22:45:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba234a37a5b5e77c8926746b575c905aa5fec2800099d1b330e0b05ecae699e5`  
		Last Modified: Fri, 25 Sep 2020 23:06:23 GMT  
		Size: 2.7 MB (2672151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74bce2b49bfe4913da5bc9719137a9c8d8fe4ae973dfa550b069adb24de7048`  
		Last Modified: Wed, 30 Sep 2020 00:49:52 GMT  
		Size: 127.5 MB (127515953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db90a8134ecac4b7768f6837726f00fbad04ce25cf442acc4a3b5b9e05331b4`  
		Last Modified: Wed, 30 Sep 2020 01:23:15 GMT  
		Size: 13.8 MB (13764873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b9d7f1eca87c52fb79c465f3f007f805fc2cfe5a10c7d5b478f8f891f86c7f`  
		Last Modified: Wed, 30 Sep 2020 01:23:13 GMT  
		Size: 690.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0303a641db3b2780627126ef5f20879201a7923bc616595a37fc3639cf1c1e5e`  
		Last Modified: Thu, 22 Oct 2020 02:25:23 GMT  
		Size: 9.4 KB (9390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59e441115d72eb13172be67f6a24b56aed0f64ec222241d0ce644ee6657c8c1`  
		Last Modified: Thu, 22 Oct 2020 02:25:21 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfd42d67b60fa152833fa27994e5cb346683a653ae2ec8afaff249c3a128d18`  
		Last Modified: Thu, 22 Oct 2020 02:25:22 GMT  
		Size: 57.2 KB (57206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea2bbf21fa3e8036e08ab1a7bf00bbeae0bd14c61279aa778efe2e727da1e84`  
		Last Modified: Thu, 22 Oct 2020 02:25:21 GMT  
		Size: 10.4 KB (10375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3086f22f95dbd68134f24ee96362341b5478814a7e58db7fd244e503f4189e0b`  
		Last Modified: Thu, 22 Oct 2020 02:25:22 GMT  
		Size: 5.8 MB (5795659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:20.0.0.9-full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:4787f290c854145639b87e9717434b3a9e4c42d0ea5820e85700cceacb5a970e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:20.0.0.9-full-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:cca5d95434dcd91ee2f583c651fa8b1003a915e1cf19f29b53f7a0a676b7892d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.3 MB (396316741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbb930dd79b441811d802994a6c9aea9f5b82b5bb1e7de1ab30e3d1db5ce09c`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 00:39:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 26 Sep 2020 00:39:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:21:19 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:22:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 00:47:06 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 00:47:07 GMT
ARG OPENJ9_SCC=true
# Wed, 30 Sep 2020 00:47:07 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.9 org.opencontainers.image.revision=cl200920200820-0913 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 30 Sep 2020 00:47:07 GMT
ENV LIBERTY_VERSION=20.0.0_09
# Wed, 30 Sep 2020 00:47:07 GMT
ARG LIBERTY_URL
# Wed, 30 Sep 2020 00:47:07 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 30 Sep 2020 00:47:16 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:47:17 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Sep 2020 00:47:17 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.9 BuildLabel=cl200920200820-0913
# Wed, 30 Sep 2020 00:47:17 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 30 Sep 2020 00:47:18 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 02:03:53 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Thu, 22 Oct 2020 02:03:53 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Oct 2020 02:03:53 GMT
COPY dir:224d4e71546da3cefb07cf2f1979378ff1c8b135f955554198d7206b463e22c9 in /licenses/ 
# Thu, 22 Oct 2020 02:03:54 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 02:04:08 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Oct 2020 02:04:08 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Thu, 22 Oct 2020 02:04:08 GMT
USER 1001
# Thu, 22 Oct 2020 02:04:08 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 02:04:08 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Oct 2020 02:04:09 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Oct 2020 02:04:14 GMT
ARG VERBOSE=false
# Thu, 22 Oct 2020 02:04:15 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Oct 2020 02:07:19 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Thu, 22 Oct 2020 02:07:19 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Oct 2020 02:08:04 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e87f30ee71d2ba7a1d467dc205703e1443af14fdd58777f796dd35311cc49dc`  
		Last Modified: Sat, 26 Sep 2020 00:44:29 GMT  
		Size: 3.0 MB (2958234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6197f6576703d3211fafc6a64b9bf241bbed280c07aa2aabcc272d0dea695d0`  
		Last Modified: Wed, 30 Sep 2020 00:26:15 GMT  
		Size: 130.3 MB (130288845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2415d740245909d7c1610813c241d6347bdd7b2ab18ace3718338c4027db88`  
		Last Modified: Wed, 30 Sep 2020 00:56:53 GMT  
		Size: 13.8 MB (13792053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4356a6353a8e85e0d9c0f7ae314951b652807102377ff0a7c3469fbcd5421021`  
		Last Modified: Wed, 30 Sep 2020 00:56:52 GMT  
		Size: 651.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf11b2700628fad2c7560024f7a40964132c8ebeaf1c6769172d2125bb90c8bc`  
		Last Modified: Thu, 22 Oct 2020 02:14:02 GMT  
		Size: 9.4 KB (9363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c12adfb03508aeba6b71f8f2f643cade9325c37c18da1c211ed34328e9992bc`  
		Last Modified: Thu, 22 Oct 2020 02:14:02 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90daf153b136a26de3e58bd72ce04fd45900414261291c662b2fb0b63ef5a325`  
		Last Modified: Thu, 22 Oct 2020 02:14:02 GMT  
		Size: 58.8 KB (58771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f99546e7f4dcde1bb25bcbbc06a31381806864c3ff82c97354a885c69b8114d`  
		Last Modified: Thu, 22 Oct 2020 02:14:02 GMT  
		Size: 10.3 KB (10274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398af486048dd2b2eb73f6648a43b4cc8482ec1ece9506b52dbee8dd9b89e06b`  
		Last Modified: Thu, 22 Oct 2020 02:14:02 GMT  
		Size: 5.7 MB (5722974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce686166dba21faa67b9dc27f0df5c24efa096f58b802bbbb382af8f271acc1`  
		Last Modified: Thu, 22 Oct 2020 02:14:23 GMT  
		Size: 195.3 MB (195265674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abcc36e7ff5430262a672d91b25e2a1fb8358098e9a242e6801ebf82f8a66d96`  
		Last Modified: Thu, 22 Oct 2020 02:14:07 GMT  
		Size: 952.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d027d2c39bda094d6c9a28a3e57b13ad9321fe93ec77cf9435a591b171d24adc`  
		Last Modified: Thu, 22 Oct 2020 02:14:10 GMT  
		Size: 21.5 MB (21506075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.9-full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:a03afb76b80bcf6137e31e50b5f8ad6b300b68c53e3500f6e9f6ff34da1504fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.6 MB (395646663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e27c3626b8f9ae1db731e5ef8e2068fed3dd8914c6a2ed1b3af848159160a6`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 04:38:06 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 26 Sep 2020 04:38:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:21:11 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:22:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 00:55:46 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 00:55:50 GMT
ARG OPENJ9_SCC=true
# Wed, 30 Sep 2020 00:55:53 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.9 org.opencontainers.image.revision=cl200920200820-0913 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 30 Sep 2020 00:55:57 GMT
ENV LIBERTY_VERSION=20.0.0_09
# Wed, 30 Sep 2020 00:56:01 GMT
ARG LIBERTY_URL
# Wed, 30 Sep 2020 00:56:03 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 30 Sep 2020 00:56:45 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:56:50 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Sep 2020 00:56:58 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.9 BuildLabel=cl200920200820-0913
# Wed, 30 Sep 2020 00:57:01 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 30 Sep 2020 00:57:20 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 11:38:26 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Thu, 22 Oct 2020 11:38:28 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Oct 2020 11:38:30 GMT
COPY dir:224d4e71546da3cefb07cf2f1979378ff1c8b135f955554198d7206b463e22c9 in /licenses/ 
# Thu, 22 Oct 2020 11:38:44 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 11:39:19 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Oct 2020 11:39:25 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Thu, 22 Oct 2020 11:39:28 GMT
USER 1001
# Thu, 22 Oct 2020 11:39:33 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 11:39:40 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Oct 2020 11:39:45 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Oct 2020 11:40:08 GMT
ARG VERBOSE=false
# Thu, 22 Oct 2020 11:40:11 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Oct 2020 11:45:12 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Thu, 22 Oct 2020 11:45:20 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Oct 2020 11:46:49 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405e3c1dd428ca3ff035da6469a7c6c36d02c92adb80d285656f61f8dd866b1`  
		Last Modified: Sat, 26 Sep 2020 04:43:33 GMT  
		Size: 3.1 MB (3075371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3df9e8e9238216b0bc889f73468bb1724d9dd627858e018235ae9634916c005`  
		Last Modified: Wed, 30 Sep 2020 00:28:00 GMT  
		Size: 129.8 MB (129833821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823515bdeca4437818119da5fce43579cc792159f149acf684a45b934386c7eb`  
		Last Modified: Wed, 30 Sep 2020 01:21:08 GMT  
		Size: 13.8 MB (13791813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40d62c5a6f4337c9074d5c4e64744bbe97a3966170165f0feb89023346cfb88`  
		Last Modified: Wed, 30 Sep 2020 01:20:48 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408dcf507268d03c81ececf4a0748770d2540a3d1be27af5ae25b17c573ca308`  
		Last Modified: Thu, 22 Oct 2020 12:02:05 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9b9a5f6eb6784e32fe343bd1fe7ab6cbef43c72e700bd6024356677acff5b5`  
		Last Modified: Thu, 22 Oct 2020 12:02:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea2f98f0ab9c7cadd2a1fe4827e6452de324a147093843fae5aa1b762b85965`  
		Last Modified: Thu, 22 Oct 2020 12:02:05 GMT  
		Size: 58.8 KB (58774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55ae68185ab77ffb005f8a4e8c104cb7286d296b5a138919eb7bb6fbf6fc0a5`  
		Last Modified: Thu, 22 Oct 2020 12:02:05 GMT  
		Size: 10.4 KB (10385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020f88916cded0b689a35ec92a0d25bc7671d88123e3067ed05e380fd4aa656`  
		Last Modified: Thu, 22 Oct 2020 12:02:10 GMT  
		Size: 5.2 MB (5207702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ac7833235ae2115efd0e714c3535a9bfcfc330cd94677d3c46b861f1c2cfe3`  
		Last Modified: Thu, 22 Oct 2020 12:04:08 GMT  
		Size: 194.8 MB (194764277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3140b5acf68e5ca72fdf0a237de6bd6ac1383be7881428f65e0ef7677a5c3497`  
		Last Modified: Thu, 22 Oct 2020 12:02:22 GMT  
		Size: 954.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7da337d4d385e2ecc5d88955c60b0aead21b3b2f46f5baa180db16019bdf49`  
		Last Modified: Thu, 22 Oct 2020 12:02:34 GMT  
		Size: 18.5 MB (18483660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.9-full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:9758e449bf26b4f37f076437245cc088d8a116b4fe45b815c6a0354a0971f15a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.3 MB (392292985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7980369f261e96ea562d1db2c335435a53faced54aa25e797fb0b8ccca6c8c75`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:44:45 GMT
ADD file:0a8ec4fb62616b6605197e20e0a7b511dc5b03d4af0e04c929dfd9fb457d2065 in / 
# Fri, 25 Sep 2020 22:44:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:44:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:44:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:44:48 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:01:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 25 Sep 2020 23:01:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:44:39 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:46:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:46:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 01:09:20 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 01:09:21 GMT
ARG OPENJ9_SCC=true
# Wed, 30 Sep 2020 01:09:21 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.9 org.opencontainers.image.revision=cl200920200820-0913 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 30 Sep 2020 01:09:22 GMT
ENV LIBERTY_VERSION=20.0.0_09
# Wed, 30 Sep 2020 01:09:23 GMT
ARG LIBERTY_URL
# Wed, 30 Sep 2020 01:09:23 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 30 Sep 2020 01:09:37 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 01:09:39 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Sep 2020 01:09:39 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.9 BuildLabel=cl200920200820-0913
# Wed, 30 Sep 2020 01:09:40 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 30 Sep 2020 01:09:42 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 02:14:04 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Thu, 22 Oct 2020 02:14:04 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Oct 2020 02:14:04 GMT
COPY dir:224d4e71546da3cefb07cf2f1979378ff1c8b135f955554198d7206b463e22c9 in /licenses/ 
# Thu, 22 Oct 2020 02:14:06 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 02:14:17 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Oct 2020 02:14:18 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Thu, 22 Oct 2020 02:14:19 GMT
USER 1001
# Thu, 22 Oct 2020 02:14:19 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 02:14:20 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Oct 2020 02:14:20 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Oct 2020 02:14:25 GMT
ARG VERBOSE=false
# Thu, 22 Oct 2020 02:14:25 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Oct 2020 02:18:16 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Thu, 22 Oct 2020 02:18:25 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Oct 2020 02:19:00 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:dd2de95b9a1c45e92bcc791d469201229b58d68187c99de6b08b00a13fa33393`  
		Last Modified: Fri, 25 Sep 2020 22:45:52 GMT  
		Size: 25.4 MB (25371975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38a48ef4dfab2bd639d381d11b3390b6bf8860b2ef3356e9bb55f7cb8c775f9`  
		Last Modified: Fri, 25 Sep 2020 22:45:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eced51184728468b347a6e3f143c356cd174c4a54be3cc10ec5aeddb402765fd`  
		Last Modified: Fri, 25 Sep 2020 22:45:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba234a37a5b5e77c8926746b575c905aa5fec2800099d1b330e0b05ecae699e5`  
		Last Modified: Fri, 25 Sep 2020 23:06:23 GMT  
		Size: 2.7 MB (2672151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74bce2b49bfe4913da5bc9719137a9c8d8fe4ae973dfa550b069adb24de7048`  
		Last Modified: Wed, 30 Sep 2020 00:49:52 GMT  
		Size: 127.5 MB (127515953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77715da17b219d1c6e5695be8472cb6cd06180077f6f40724b79bf306cf97ce1`  
		Last Modified: Wed, 30 Sep 2020 01:22:43 GMT  
		Size: 13.8 MB (13791205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4aaa48bce574f69fcf6a8bb0f15d6282874aebd87c36fad85be727b1f373429`  
		Last Modified: Wed, 30 Sep 2020 01:22:23 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87c5e1eca5131b91ae9908e974a65e104db6cb5b09573261afd6771953fdade`  
		Last Modified: Thu, 22 Oct 2020 02:24:59 GMT  
		Size: 9.4 KB (9391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89f26fefbc1d652c7cfc9b158c941f44d9ed0d723d6975a1d43b29cfe6e078b`  
		Last Modified: Thu, 22 Oct 2020 02:24:59 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed03a39ae34ac6bc0dc918c06c07143ce0c95827d88bc0845472dd87ef7bf36`  
		Last Modified: Thu, 22 Oct 2020 02:24:59 GMT  
		Size: 58.8 KB (58772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad36e143a9d0fa2a5dcf5ba008f5300ce84bc9ccf01c0c2c0f5d3d4893e5868a`  
		Last Modified: Thu, 22 Oct 2020 02:24:59 GMT  
		Size: 10.4 KB (10378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717919d7ae883353ec4de17453a3f2a77bc928b9eec103d7d31cd290d69874bb`  
		Last Modified: Thu, 22 Oct 2020 02:24:59 GMT  
		Size: 5.8 MB (5781973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4371ac353376263a3a42fe9a3a95f689ef57adab536de1e754d6b497888550`  
		Last Modified: Thu, 22 Oct 2020 02:25:15 GMT  
		Size: 195.3 MB (195341166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d988f1f3faa3b9270688dcc5802933c6adb3a8dc5b6455480eaba5e94524df18`  
		Last Modified: Thu, 22 Oct 2020 02:25:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e14d955c58f14fd0febb59fb042d3cd8342fab5521982c4991b35e653cead1d`  
		Last Modified: Thu, 22 Oct 2020 02:25:09 GMT  
		Size: 21.7 MB (21737062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:20.0.0.9-kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:37efc2149e3975b5b70ab0802945f2e4f7672bb74fb07f11cacd8b3dbfcac587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:20.0.0.9-kernel-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:ed2c7eda0a77d99bce951db22b79dec72e6c5b904a638d46258b9300164e3ff6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179544040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08fbb3856ea39faa578c29ac6d1f580639feb789b6d3f6efa96384ffb71d2a0`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 00:39:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 26 Sep 2020 00:39:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:21:19 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:22:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 00:47:06 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 00:47:07 GMT
ARG OPENJ9_SCC=true
# Wed, 30 Sep 2020 00:47:07 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.9 org.opencontainers.image.revision=cl200920200820-0913 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 30 Sep 2020 00:47:07 GMT
ENV LIBERTY_VERSION=20.0.0_09
# Wed, 30 Sep 2020 00:47:07 GMT
ARG LIBERTY_URL
# Wed, 30 Sep 2020 00:47:07 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 30 Sep 2020 00:47:16 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:47:17 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Sep 2020 00:47:17 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.9 BuildLabel=cl200920200820-0913
# Wed, 30 Sep 2020 00:47:17 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 30 Sep 2020 00:47:18 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 02:03:53 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Thu, 22 Oct 2020 02:03:53 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Oct 2020 02:03:53 GMT
COPY dir:224d4e71546da3cefb07cf2f1979378ff1c8b135f955554198d7206b463e22c9 in /licenses/ 
# Thu, 22 Oct 2020 02:03:54 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 02:04:08 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Oct 2020 02:04:08 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Thu, 22 Oct 2020 02:04:08 GMT
USER 1001
# Thu, 22 Oct 2020 02:04:08 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 02:04:08 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Oct 2020 02:04:09 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e87f30ee71d2ba7a1d467dc205703e1443af14fdd58777f796dd35311cc49dc`  
		Last Modified: Sat, 26 Sep 2020 00:44:29 GMT  
		Size: 3.0 MB (2958234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6197f6576703d3211fafc6a64b9bf241bbed280c07aa2aabcc272d0dea695d0`  
		Last Modified: Wed, 30 Sep 2020 00:26:15 GMT  
		Size: 130.3 MB (130288845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2415d740245909d7c1610813c241d6347bdd7b2ab18ace3718338c4027db88`  
		Last Modified: Wed, 30 Sep 2020 00:56:53 GMT  
		Size: 13.8 MB (13792053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4356a6353a8e85e0d9c0f7ae314951b652807102377ff0a7c3469fbcd5421021`  
		Last Modified: Wed, 30 Sep 2020 00:56:52 GMT  
		Size: 651.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf11b2700628fad2c7560024f7a40964132c8ebeaf1c6769172d2125bb90c8bc`  
		Last Modified: Thu, 22 Oct 2020 02:14:02 GMT  
		Size: 9.4 KB (9363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c12adfb03508aeba6b71f8f2f643cade9325c37c18da1c211ed34328e9992bc`  
		Last Modified: Thu, 22 Oct 2020 02:14:02 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90daf153b136a26de3e58bd72ce04fd45900414261291c662b2fb0b63ef5a325`  
		Last Modified: Thu, 22 Oct 2020 02:14:02 GMT  
		Size: 58.8 KB (58771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f99546e7f4dcde1bb25bcbbc06a31381806864c3ff82c97354a885c69b8114d`  
		Last Modified: Thu, 22 Oct 2020 02:14:02 GMT  
		Size: 10.3 KB (10274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398af486048dd2b2eb73f6648a43b4cc8482ec1ece9506b52dbee8dd9b89e06b`  
		Last Modified: Thu, 22 Oct 2020 02:14:02 GMT  
		Size: 5.7 MB (5722974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.9-kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:70ac69934fef90ed76d563e707061a0416f5cfe37f0b994e7a94de97882a1cd5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.4 MB (182397772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4657c1a02980a4d50f6a38342ddf17757fa94b25188dd0ce390279cdd0ed3e`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 04:38:06 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 26 Sep 2020 04:38:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:21:11 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:22:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 00:55:46 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 00:55:50 GMT
ARG OPENJ9_SCC=true
# Wed, 30 Sep 2020 00:55:53 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.9 org.opencontainers.image.revision=cl200920200820-0913 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 30 Sep 2020 00:55:57 GMT
ENV LIBERTY_VERSION=20.0.0_09
# Wed, 30 Sep 2020 00:56:01 GMT
ARG LIBERTY_URL
# Wed, 30 Sep 2020 00:56:03 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 30 Sep 2020 00:56:45 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:56:50 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Sep 2020 00:56:58 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.9 BuildLabel=cl200920200820-0913
# Wed, 30 Sep 2020 00:57:01 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 30 Sep 2020 00:57:20 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 11:38:26 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Thu, 22 Oct 2020 11:38:28 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Oct 2020 11:38:30 GMT
COPY dir:224d4e71546da3cefb07cf2f1979378ff1c8b135f955554198d7206b463e22c9 in /licenses/ 
# Thu, 22 Oct 2020 11:38:44 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 11:39:19 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Oct 2020 11:39:25 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Thu, 22 Oct 2020 11:39:28 GMT
USER 1001
# Thu, 22 Oct 2020 11:39:33 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 11:39:40 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Oct 2020 11:39:45 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405e3c1dd428ca3ff035da6469a7c6c36d02c92adb80d285656f61f8dd866b1`  
		Last Modified: Sat, 26 Sep 2020 04:43:33 GMT  
		Size: 3.1 MB (3075371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3df9e8e9238216b0bc889f73468bb1724d9dd627858e018235ae9634916c005`  
		Last Modified: Wed, 30 Sep 2020 00:28:00 GMT  
		Size: 129.8 MB (129833821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823515bdeca4437818119da5fce43579cc792159f149acf684a45b934386c7eb`  
		Last Modified: Wed, 30 Sep 2020 01:21:08 GMT  
		Size: 13.8 MB (13791813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40d62c5a6f4337c9074d5c4e64744bbe97a3966170165f0feb89023346cfb88`  
		Last Modified: Wed, 30 Sep 2020 01:20:48 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408dcf507268d03c81ececf4a0748770d2540a3d1be27af5ae25b17c573ca308`  
		Last Modified: Thu, 22 Oct 2020 12:02:05 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9b9a5f6eb6784e32fe343bd1fe7ab6cbef43c72e700bd6024356677acff5b5`  
		Last Modified: Thu, 22 Oct 2020 12:02:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea2f98f0ab9c7cadd2a1fe4827e6452de324a147093843fae5aa1b762b85965`  
		Last Modified: Thu, 22 Oct 2020 12:02:05 GMT  
		Size: 58.8 KB (58774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55ae68185ab77ffb005f8a4e8c104cb7286d296b5a138919eb7bb6fbf6fc0a5`  
		Last Modified: Thu, 22 Oct 2020 12:02:05 GMT  
		Size: 10.4 KB (10385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020f88916cded0b689a35ec92a0d25bc7671d88123e3067ed05e380fd4aa656`  
		Last Modified: Thu, 22 Oct 2020 12:02:10 GMT  
		Size: 5.2 MB (5207702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.9-kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:1bcfab20d3a02ef1234c04ab708ffe73c0e9684581ff23ae2d25cf4bf2a3da6c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175213807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcdc2d4b4ba92ea9eaeb29aec96acc2b91382fffca042636dff2e941bef1c812`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:44:45 GMT
ADD file:0a8ec4fb62616b6605197e20e0a7b511dc5b03d4af0e04c929dfd9fb457d2065 in / 
# Fri, 25 Sep 2020 22:44:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:44:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:44:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:44:48 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:01:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 25 Sep 2020 23:01:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:44:39 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:46:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:46:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 01:09:20 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 01:09:21 GMT
ARG OPENJ9_SCC=true
# Wed, 30 Sep 2020 01:09:21 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.9 org.opencontainers.image.revision=cl200920200820-0913 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 30 Sep 2020 01:09:22 GMT
ENV LIBERTY_VERSION=20.0.0_09
# Wed, 30 Sep 2020 01:09:23 GMT
ARG LIBERTY_URL
# Wed, 30 Sep 2020 01:09:23 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 30 Sep 2020 01:09:37 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 01:09:39 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Sep 2020 01:09:39 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.9 BuildLabel=cl200920200820-0913
# Wed, 30 Sep 2020 01:09:40 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 30 Sep 2020 01:09:42 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 02:14:04 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Thu, 22 Oct 2020 02:14:04 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Oct 2020 02:14:04 GMT
COPY dir:224d4e71546da3cefb07cf2f1979378ff1c8b135f955554198d7206b463e22c9 in /licenses/ 
# Thu, 22 Oct 2020 02:14:06 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 02:14:17 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Oct 2020 02:14:18 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Thu, 22 Oct 2020 02:14:19 GMT
USER 1001
# Thu, 22 Oct 2020 02:14:19 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 02:14:20 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Oct 2020 02:14:20 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:dd2de95b9a1c45e92bcc791d469201229b58d68187c99de6b08b00a13fa33393`  
		Last Modified: Fri, 25 Sep 2020 22:45:52 GMT  
		Size: 25.4 MB (25371975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38a48ef4dfab2bd639d381d11b3390b6bf8860b2ef3356e9bb55f7cb8c775f9`  
		Last Modified: Fri, 25 Sep 2020 22:45:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eced51184728468b347a6e3f143c356cd174c4a54be3cc10ec5aeddb402765fd`  
		Last Modified: Fri, 25 Sep 2020 22:45:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba234a37a5b5e77c8926746b575c905aa5fec2800099d1b330e0b05ecae699e5`  
		Last Modified: Fri, 25 Sep 2020 23:06:23 GMT  
		Size: 2.7 MB (2672151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74bce2b49bfe4913da5bc9719137a9c8d8fe4ae973dfa550b069adb24de7048`  
		Last Modified: Wed, 30 Sep 2020 00:49:52 GMT  
		Size: 127.5 MB (127515953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77715da17b219d1c6e5695be8472cb6cd06180077f6f40724b79bf306cf97ce1`  
		Last Modified: Wed, 30 Sep 2020 01:22:43 GMT  
		Size: 13.8 MB (13791205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4aaa48bce574f69fcf6a8bb0f15d6282874aebd87c36fad85be727b1f373429`  
		Last Modified: Wed, 30 Sep 2020 01:22:23 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87c5e1eca5131b91ae9908e974a65e104db6cb5b09573261afd6771953fdade`  
		Last Modified: Thu, 22 Oct 2020 02:24:59 GMT  
		Size: 9.4 KB (9391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89f26fefbc1d652c7cfc9b158c941f44d9ed0d723d6975a1d43b29cfe6e078b`  
		Last Modified: Thu, 22 Oct 2020 02:24:59 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed03a39ae34ac6bc0dc918c06c07143ce0c95827d88bc0845472dd87ef7bf36`  
		Last Modified: Thu, 22 Oct 2020 02:24:59 GMT  
		Size: 58.8 KB (58772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad36e143a9d0fa2a5dcf5ba008f5300ce84bc9ccf01c0c2c0f5d3d4893e5868a`  
		Last Modified: Thu, 22 Oct 2020 02:24:59 GMT  
		Size: 10.4 KB (10378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717919d7ae883353ec4de17453a3f2a77bc928b9eec103d7d31cd290d69874bb`  
		Last Modified: Thu, 22 Oct 2020 02:24:59 GMT  
		Size: 5.8 MB (5781973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:beta`

```console
$ docker pull websphere-liberty@sha256:e7a248aafd95c0d6070a004bed7ee0ef2230941f8aac18a628af88238b84ac77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:beta` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:9246e14374b970fc3f6cad33888b6a12e36c22197b61ae4e97b8798e330d6e70
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.6 MB (252632261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee42788a90a02fab94b491e212862f4b38df3a77bc9b5c3c081af841efbf2ec5`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 00:39:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 26 Sep 2020 00:39:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:21:19 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:22:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 22 Oct 2020 01:53:28 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=2020.10.0.0 org.opencontainers.image.revision=cl201020200915-1100
# Thu, 22 Oct 2020 01:53:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default
# Thu, 22 Oct 2020 01:53:35 GMT
ENV LIBERTY_VERSION=2020.10.0_0
# Thu, 22 Oct 2020 01:53:50 GMT
RUN LIBERTY_URL=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 3 | sed -n 's/\s*webProfile7:\s//p' | tr -d '\r')      && echo $LIBERTY_URL     && wget -q $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp-beta.zip     && unzip -q /tmp/wlp-beta.zip -d /opt/ibm     && rm /tmp/wlp-beta.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp
# Thu, 22 Oct 2020 01:53:50 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Oct 2020 01:53:50 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Thu, 22 Oct 2020 01:53:52 GMT
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 01:53:52 GMT
COPY file:f1015ab5ca098f3a04cde2e721a2aa35a1ebb2e9f5eb01d378eb2264cff9a268 in /opt/ibm/wlp/usr/servers/defaultServer/ 
# Thu, 22 Oct 2020 01:53:53 GMT
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 01:53:53 GMT
USER 1001
# Thu, 22 Oct 2020 01:53:53 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 01:53:53 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e87f30ee71d2ba7a1d467dc205703e1443af14fdd58777f796dd35311cc49dc`  
		Last Modified: Sat, 26 Sep 2020 00:44:29 GMT  
		Size: 3.0 MB (2958234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6197f6576703d3211fafc6a64b9bf241bbed280c07aa2aabcc272d0dea695d0`  
		Last Modified: Wed, 30 Sep 2020 00:26:15 GMT  
		Size: 130.3 MB (130288845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde9ef9b4941082f50ffb8e7c7138ce3eea437d3a81063efdd511323dbb57111`  
		Last Modified: Thu, 22 Oct 2020 02:12:33 GMT  
		Size: 378.5 KB (378452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6f5be5aeb1de8923c87ee81838922d72c38407e7d8b4bda0dc0d22b830c822`  
		Last Modified: Thu, 22 Oct 2020 02:12:40 GMT  
		Size: 92.3 MB (92301539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a508a3cd2b38f224c1f67f1411dd46ce6d8012230be394644565af5893249387`  
		Last Modified: Thu, 22 Oct 2020 02:12:33 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25218c6fe0b02fed4b5f0f0567584b922f4cf229cf5f5236ee15405ca72864a`  
		Last Modified: Thu, 22 Oct 2020 02:12:33 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b327b1b1327e3c7ec0b94e3ff4850ffe15c07f0cae1703fe009b14aca99453d`  
		Last Modified: Thu, 22 Oct 2020 02:12:33 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:beta` - linux; 386

```console
$ docker pull websphere-liberty@sha256:69b6da2a321fc7c687be0a093dcfaf924ec47a8ceb18995897c8fe787569ac94
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241366558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaeb2c119e07bae1886caf0660d8203642878fd9f831e46c3915d06118556bbe`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:41:33 GMT
ADD file:0177f9bf14805cdd9313f5041fcfcf524e21ce1e875849b93095cfaabb18dae6 in / 
# Fri, 25 Sep 2020 22:41:34 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:41:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:41:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:41:36 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:09:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 25 Sep 2020 23:09:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:40:40 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:41:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:41:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 22 Oct 2020 02:02:21 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=2020.10.0.0 org.opencontainers.image.revision=cl201020200915-1100
# Thu, 22 Oct 2020 02:02:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default
# Thu, 22 Oct 2020 02:02:32 GMT
ENV LIBERTY_VERSION=2020.10.0_0
# Thu, 22 Oct 2020 02:02:47 GMT
RUN LIBERTY_URL=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 3 | sed -n 's/\s*webProfile7:\s//p' | tr -d '\r')      && echo $LIBERTY_URL     && wget -q $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp-beta.zip     && unzip -q /tmp/wlp-beta.zip -d /opt/ibm     && rm /tmp/wlp-beta.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp
# Thu, 22 Oct 2020 02:02:48 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Oct 2020 02:02:48 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Thu, 22 Oct 2020 02:02:51 GMT
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 02:02:51 GMT
COPY file:f1015ab5ca098f3a04cde2e721a2aa35a1ebb2e9f5eb01d378eb2264cff9a268 in /opt/ibm/wlp/usr/servers/defaultServer/ 
# Thu, 22 Oct 2020 02:02:53 GMT
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 02:02:53 GMT
USER 1001
# Thu, 22 Oct 2020 02:02:53 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 02:02:54 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:19f7f52229ec38c2b8044ac336baa70ba59eb66cc1ac781e6995beffb021fcd8`  
		Last Modified: Fri, 25 Sep 2020 22:42:39 GMT  
		Size: 27.1 MB (27124997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27d7bc113eaf858b9db78ac2dc9fe9b6f9d1004b5650dbeaf191eb04ed7c76c`  
		Last Modified: Fri, 25 Sep 2020 22:42:30 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda09d9f5ab6a86c598e8b4cd430ae56765731b5f9a9d8b99e59f594e455acc6`  
		Last Modified: Fri, 25 Sep 2020 22:42:30 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae76a3407fa8a1a8d4165b397909993a9b92044d8bafed09db7dda16b9eed015`  
		Last Modified: Fri, 25 Sep 2020 23:11:46 GMT  
		Size: 3.0 MB (2982764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2256d1167989755a566e92ca0a1b1db0b5434690af25e002dfba5d8a0eb2498b`  
		Last Modified: Wed, 30 Sep 2020 00:43:23 GMT  
		Size: 118.6 MB (118588338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e8a8499a50638196020f2323c6be44a06e6b5d132baaa77dd31e049895f758`  
		Last Modified: Thu, 22 Oct 2020 02:05:21 GMT  
		Size: 365.3 KB (365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da0cf4f4195e882d0c41b891831878ffa8ee939179946c174a393921e815b35`  
		Last Modified: Thu, 22 Oct 2020 02:05:31 GMT  
		Size: 92.3 MB (92301554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6c767de965f70877855f2568ef020199a8de8901655bd8cfb4da74ed3180ad`  
		Last Modified: Thu, 22 Oct 2020 02:05:21 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c974b8240aa05f37d4ef91da6ac97b0df0afa4ba4a3c4d460d4930609603c94`  
		Last Modified: Thu, 22 Oct 2020 02:05:21 GMT  
		Size: 425.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620f19fdf51ec57172503e25051703a3e26eb72711df32020836dfeb0d858fb8`  
		Last Modified: Thu, 22 Oct 2020 02:05:21 GMT  
		Size: 919.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:beta` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:5285824cd55b09ef07d3e334cff655ae53f6772cac9095b47399d1139c7b3149
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.0 MB (256028323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade106fa798e75ad638c528835d1738a402c7e07fe17d736e20fcc4c5393e712`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 04:38:06 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 26 Sep 2020 04:38:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:21:11 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:22:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 22 Oct 2020 11:03:24 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=2020.10.0.0 org.opencontainers.image.revision=cl201020200915-1100
# Thu, 22 Oct 2020 11:04:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default
# Thu, 22 Oct 2020 11:04:22 GMT
ENV LIBERTY_VERSION=2020.10.0_0
# Thu, 22 Oct 2020 11:05:15 GMT
RUN LIBERTY_URL=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 3 | sed -n 's/\s*webProfile7:\s//p' | tr -d '\r')      && echo $LIBERTY_URL     && wget -q $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp-beta.zip     && unzip -q /tmp/wlp-beta.zip -d /opt/ibm     && rm /tmp/wlp-beta.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp
# Thu, 22 Oct 2020 11:05:35 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Oct 2020 11:05:47 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Thu, 22 Oct 2020 11:06:26 GMT
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 11:06:31 GMT
COPY file:f1015ab5ca098f3a04cde2e721a2aa35a1ebb2e9f5eb01d378eb2264cff9a268 in /opt/ibm/wlp/usr/servers/defaultServer/ 
# Thu, 22 Oct 2020 11:06:50 GMT
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 11:07:00 GMT
USER 1001
# Thu, 22 Oct 2020 11:07:10 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 11:07:22 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405e3c1dd428ca3ff035da6469a7c6c36d02c92adb80d285656f61f8dd866b1`  
		Last Modified: Sat, 26 Sep 2020 04:43:33 GMT  
		Size: 3.1 MB (3075371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3df9e8e9238216b0bc889f73468bb1724d9dd627858e018235ae9634916c005`  
		Last Modified: Wed, 30 Sep 2020 00:28:00 GMT  
		Size: 129.8 MB (129833821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127a2c9abadc0439423c7c3121729fca4be5327a421872adb55e306df65673f5`  
		Last Modified: Thu, 22 Oct 2020 11:56:16 GMT  
		Size: 405.3 KB (405272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0af68820b624fe47455a29d0c63b5e08adcc8333e0e1598b705ad53bc40e8de`  
		Last Modified: Thu, 22 Oct 2020 11:57:15 GMT  
		Size: 92.3 MB (92301615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab05384543df5fff6debb75742d7d62875c14b760bab65b4163dcc04e0d9e2b7`  
		Last Modified: Thu, 22 Oct 2020 11:56:16 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ce6824b046246d2b4af1843fc4d41015cce17ff4d63c0ff2f049975622e756`  
		Last Modified: Thu, 22 Oct 2020 11:56:16 GMT  
		Size: 429.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345c8967b2d065db3f2b16a00c480b54ffbb3767baea3de216a6634d4a7f8e4e`  
		Last Modified: Thu, 22 Oct 2020 11:56:18 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:beta` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:d9d055efffacb434ee54772173c45d77c7d0508628dbbaed35df847bb880e33c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.2 MB (248237338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092173c16359124954615c2df152cdfe547f41283b371dded7bb67535133e50f`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:44:45 GMT
ADD file:0a8ec4fb62616b6605197e20e0a7b511dc5b03d4af0e04c929dfd9fb457d2065 in / 
# Fri, 25 Sep 2020 22:44:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:44:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:44:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:44:48 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:01:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 25 Sep 2020 23:01:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:44:39 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:46:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:46:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 22 Oct 2020 02:02:54 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=2020.10.0.0 org.opencontainers.image.revision=cl201020200915-1100
# Thu, 22 Oct 2020 02:03:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default
# Thu, 22 Oct 2020 02:03:03 GMT
ENV LIBERTY_VERSION=2020.10.0_0
# Thu, 22 Oct 2020 02:03:23 GMT
RUN LIBERTY_URL=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 3 | sed -n 's/\s*webProfile7:\s//p' | tr -d '\r')      && echo $LIBERTY_URL     && wget -q $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp-beta.zip     && unzip -q /tmp/wlp-beta.zip -d /opt/ibm     && rm /tmp/wlp-beta.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp
# Thu, 22 Oct 2020 02:03:28 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Oct 2020 02:03:28 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Thu, 22 Oct 2020 02:03:32 GMT
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 02:03:32 GMT
COPY file:f1015ab5ca098f3a04cde2e721a2aa35a1ebb2e9f5eb01d378eb2264cff9a268 in /opt/ibm/wlp/usr/servers/defaultServer/ 
# Thu, 22 Oct 2020 02:03:33 GMT
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 02:03:34 GMT
USER 1001
# Thu, 22 Oct 2020 02:03:35 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 02:03:35 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:dd2de95b9a1c45e92bcc791d469201229b58d68187c99de6b08b00a13fa33393`  
		Last Modified: Fri, 25 Sep 2020 22:45:52 GMT  
		Size: 25.4 MB (25371975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38a48ef4dfab2bd639d381d11b3390b6bf8860b2ef3356e9bb55f7cb8c775f9`  
		Last Modified: Fri, 25 Sep 2020 22:45:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eced51184728468b347a6e3f143c356cd174c4a54be3cc10ec5aeddb402765fd`  
		Last Modified: Fri, 25 Sep 2020 22:45:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba234a37a5b5e77c8926746b575c905aa5fec2800099d1b330e0b05ecae699e5`  
		Last Modified: Fri, 25 Sep 2020 23:06:23 GMT  
		Size: 2.7 MB (2672151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74bce2b49bfe4913da5bc9719137a9c8d8fe4ae973dfa550b069adb24de7048`  
		Last Modified: Wed, 30 Sep 2020 00:49:52 GMT  
		Size: 127.5 MB (127515953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40cb0ff16281c785cbb2df74056735b50b3f5cf41a1c95e88263c2ef6599e67f`  
		Last Modified: Thu, 22 Oct 2020 02:23:54 GMT  
		Size: 371.9 KB (371939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a093653b5ec24543339b58f445dd4af557c27de059376514707ccd787347ee2d`  
		Last Modified: Thu, 22 Oct 2020 02:23:59 GMT  
		Size: 92.3 MB (92301590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a97992a63838ad18ac31bb352c465d014dbab52cb7b067734dd0e539e0c0afe`  
		Last Modified: Thu, 22 Oct 2020 02:23:53 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e6e41142afaac7add1c150cf54c63df17b1d4118cb98c511b0322ceb8b419c`  
		Last Modified: Thu, 22 Oct 2020 02:23:53 GMT  
		Size: 426.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9f72722b9cc1f6fb159fb2ecaef2163eb3afea366cde5ad53ec560ead1d24d`  
		Last Modified: Thu, 22 Oct 2020 02:23:54 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:full`

```console
$ docker pull websphere-liberty@sha256:a9ae31d15421aa300827293d49d9b6ea1638fb64c139cc76b7a6ffb2aaea1ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:6032bdf6bcab14693e2a82d1b656c144cb33be964adb46e37c65451f84c756c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.1 MB (414060472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e8db59984d53c5695604feac2737fbee8b380c32eb70d696e7f81d9533436b`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 00:39:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 26 Sep 2020 00:39:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:21:19 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:22:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 00:47:06 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 00:47:07 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Oct 2020 01:53:59 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.10 org.opencontainers.image.revision=cl201020200915-1100 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Oct 2020 01:54:00 GMT
ENV LIBERTY_VERSION=20.0.0_10
# Thu, 22 Oct 2020 01:54:00 GMT
ARG LIBERTY_URL
# Thu, 22 Oct 2020 01:54:00 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Oct 2020 01:54:13 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Oct 2020 01:54:13 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Oct 2020 01:54:14 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.10 BuildLabel=cl201020200915-1100
# Thu, 22 Oct 2020 01:54:14 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Oct 2020 01:54:15 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 01:54:15 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Thu, 22 Oct 2020 01:54:16 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Oct 2020 01:54:17 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 01:54:32 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Oct 2020 01:54:32 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Thu, 22 Oct 2020 01:54:32 GMT
USER 1001
# Thu, 22 Oct 2020 01:54:32 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 01:54:32 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Oct 2020 01:54:33 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Oct 2020 01:54:40 GMT
ARG VERBOSE=false
# Thu, 22 Oct 2020 01:54:40 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Oct 2020 01:57:55 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Thu, 22 Oct 2020 01:57:55 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Oct 2020 01:58:54 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e87f30ee71d2ba7a1d467dc205703e1443af14fdd58777f796dd35311cc49dc`  
		Last Modified: Sat, 26 Sep 2020 00:44:29 GMT  
		Size: 3.0 MB (2958234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6197f6576703d3211fafc6a64b9bf241bbed280c07aa2aabcc272d0dea695d0`  
		Last Modified: Wed, 30 Sep 2020 00:26:15 GMT  
		Size: 130.3 MB (130288845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f02a243cdf520b2db58f93f18c7b5cacfd8ea5668c16977c09b33c72be5d11`  
		Last Modified: Thu, 22 Oct 2020 02:12:48 GMT  
		Size: 27.7 MB (27734634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef48450a5818fc4e1cb4b746fd9a8de28de3defe12f6abf55ca3291af458f1db`  
		Last Modified: Thu, 22 Oct 2020 02:12:44 GMT  
		Size: 656.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e1ec9b9a3339d6c3e47579f2653c144dca0284526b69959012145c73746079`  
		Last Modified: Thu, 22 Oct 2020 02:12:45 GMT  
		Size: 9.4 KB (9364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dac3e62e13da3922c4f688f0be98c41695a9030b163fa342ed50c7f320cf67`  
		Last Modified: Thu, 22 Oct 2020 02:12:44 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd5cc8dce5355c809c982b38550c98bbaf4d34caccc434ddcfd47e8d2ec6bea`  
		Last Modified: Thu, 22 Oct 2020 02:12:44 GMT  
		Size: 10.3 KB (10269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540d02f5639655b60f7c9421031ffadd8e0d63e0d6fdd3467b3a52f4da9c785e`  
		Last Modified: Thu, 22 Oct 2020 02:12:46 GMT  
		Size: 5.6 MB (5646543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8bea44cd7bc9c6f6430f457b7415e212df6cb17bce46131ca2ecf8d1276512a`  
		Last Modified: Thu, 22 Oct 2020 02:13:19 GMT  
		Size: 199.8 MB (199770138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9ca3a8d709ad4fb08a6aa4aad1127658c0c1b163bdd97916f36a0b261cdc45`  
		Last Modified: Thu, 22 Oct 2020 02:12:52 GMT  
		Size: 947.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9e709c4cab95c5d2e10b8c171ed8657ac10a766089035152d56170a9d674ca`  
		Last Modified: Thu, 22 Oct 2020 02:12:57 GMT  
		Size: 20.9 MB (20937967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full` - linux; 386

```console
$ docker pull websphere-liberty@sha256:c847143995aec30ca5d4526544d7c41ca7a42a8baf8195848864d0128e96ecf3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.2 MB (349209019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d2c9374be56a63d6e35820fec8676f2d4ed2b9bdaf09a49c8545b039479bb7`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 20 Mar 2020 18:38:55 GMT
ADD file:d859d389e38b7ac70fd56f97e38d52a77b58e72b96237a4302d1984cdd912a55 in / 
# Fri, 20 Mar 2020 18:38:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:38:57 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:38:58 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:38:58 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:06:34 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 20 Mar 2020 19:06:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:06:42 GMT
ENV JAVA_VERSION=1.8.0_sr6fp6
# Fri, 20 Mar 2020 19:07:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='87f9d45b7e1fa65ec018479f3ca7da69a03b52b0da10b8d1555142eec8ab0093';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='b5f825047c9bb5d360fb83694f12e17b1a5a15abf94ac82cd0a3aea32c9a361c';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3c04cd07ef269c24373840eae6f59c7db7a16d2e206d393ba93efa6dbb8d74f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2bbefda96f7d1a5f1694893961e92ccc59dfa50375ae5450675d7a4213d5812e';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d5b0508d53d1c7382c06f5bc1daf3d57c19c70d851e86e6b1162bcd93f616f7e';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 20 Mar 2020 19:07:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 20 Mar 2020 19:31:53 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.3 org.opencontainers.image.revision=cl200320200305-1433
# Fri, 20 Mar 2020 19:31:53 GMT
ENV LIBERTY_VERSION=20.0.0_03
# Fri, 20 Mar 2020 19:31:53 GMT
ARG LIBERTY_URL
# Fri, 20 Mar 2020 19:31:53 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 20 Mar 2020 19:32:02 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:32:03 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2020 19:32:03 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.3 BuildLabel=cl200320200305-1433
# Fri, 20 Mar 2020 19:32:03 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Fri, 20 Mar 2020 19:32:04 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 20 Mar 2020 19:32:04 GMT
COPY dir:0d0cedab2fbb7208b9d81afa78e9f15b12b71232224a2fe9753c00b7b72bd72e in /opt/ibm/helpers/ 
# Fri, 20 Mar 2020 19:32:05 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 20 Mar 2020 19:32:05 GMT
COPY dir:9277507d983008afcf8df6e0bfe2735bd4e92717515dbb3a7e268c830f213489 in /licenses/ 
# Fri, 20 Mar 2020 19:32:06 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 20 Mar 2020 19:32:06 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Fri, 20 Mar 2020 19:32:06 GMT
USER 1001
# Fri, 20 Mar 2020 19:32:06 GMT
EXPOSE 9080 9443
# Fri, 20 Mar 2020 19:32:07 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 20 Mar 2020 19:32:07 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 20 Mar 2020 19:32:10 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 20 Mar 2020 19:35:01 GMT
# ARGS: REPOSITORIES_PROPERTIES=
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Fri, 20 Mar 2020 19:35:01 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
```

-	Layers:
	-	`sha256:765ce743592771b94ad8ff27e281e66c13f6039962c7dde4dbe47123081e015b`  
		Last Modified: Mon, 16 Mar 2020 15:38:41 GMT  
		Size: 27.1 MB (27122453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59dc9c4739090a3d2f7265f1f8184b1cbd8ae133b863f8aa93ec5cf1761ee7a5`  
		Last Modified: Fri, 20 Mar 2020 18:39:35 GMT  
		Size: 34.6 KB (34625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a5b698281c077f48fc598e698f0619e4d00a2fedc1832fc95e9cf281408f63`  
		Last Modified: Fri, 20 Mar 2020 18:39:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaebe599891b1e1befc10d752a117cc5615ec2dd3913d399fd66e26e0cace3e5`  
		Last Modified: Fri, 20 Mar 2020 18:39:34 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f829150bc8a53a37ac17eb34838fa33c990881a4031bc650a9dae26b3f7880e`  
		Last Modified: Fri, 20 Mar 2020 19:09:23 GMT  
		Size: 3.0 MB (2992132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17b9ccc4baf3a1ffa517a03c7c3d01900136b128b36a83558c67c42e6c1cbaa`  
		Last Modified: Fri, 20 Mar 2020 19:09:35 GMT  
		Size: 118.8 MB (118756706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5011972f1876d464fb62206211a5b5e162ba2603bf20fc4cd0f2b4ffd311cd9`  
		Last Modified: Fri, 20 Mar 2020 19:39:16 GMT  
		Size: 13.6 MB (13600436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5395b713d5baa0917182ca82077b6fa2a0c51789907f96cbb12455586d9fa9b`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389324a3d9489b2fbcd5946f9d24285c0171c3218470e4a5e2d45c731cefc522`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 3.5 KB (3515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38ea596499e1f23ce426826250984869e92da50aec5845a6233a76d7764bfd1`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea3197b55235384f836e31a605c460f6cb7196f68dc29c65640738d8aa50188`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 57.4 KB (57426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683f76bf565cdb9e59c325f24357eb6b164555ed8629a4b8383448239608966d`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 4.4 KB (4358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cd2560c76831311d13d197b4784e0826f6ffae62e3b9a22d2fa5675b9b71a2`  
		Last Modified: Fri, 20 Mar 2020 19:39:42 GMT  
		Size: 186.6 MB (186634496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9891aa2b3e904f8f514677372187983ac12c98c209c433ab5bf0862e09d6f4ef`  
		Last Modified: Fri, 20 Mar 2020 19:39:20 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:f12eee541bc4aa192561d663754de7a0a6bc5360b801d175105fda20e34534b4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.0 MB (413977616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb443729949fe0130cc0960d8065fc7853592d37088c5442f8ff77d4d27c38d1`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 04:38:06 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 26 Sep 2020 04:38:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:21:11 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:22:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 00:55:46 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 00:55:50 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Oct 2020 11:07:50 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.10 org.opencontainers.image.revision=cl201020200915-1100 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Oct 2020 11:08:01 GMT
ENV LIBERTY_VERSION=20.0.0_10
# Thu, 22 Oct 2020 11:08:12 GMT
ARG LIBERTY_URL
# Thu, 22 Oct 2020 11:08:30 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Oct 2020 11:10:28 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Oct 2020 11:10:45 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Oct 2020 11:10:56 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.10 BuildLabel=cl201020200915-1100
# Thu, 22 Oct 2020 11:11:02 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Oct 2020 11:11:28 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 11:11:39 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Thu, 22 Oct 2020 11:11:51 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Oct 2020 11:12:13 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 11:12:59 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Oct 2020 11:13:07 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Thu, 22 Oct 2020 11:13:14 GMT
USER 1001
# Thu, 22 Oct 2020 11:13:22 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 11:13:37 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Oct 2020 11:13:47 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Oct 2020 11:14:01 GMT
ARG VERBOSE=false
# Thu, 22 Oct 2020 11:14:12 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Oct 2020 11:21:50 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Thu, 22 Oct 2020 11:21:56 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Oct 2020 11:23:49 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405e3c1dd428ca3ff035da6469a7c6c36d02c92adb80d285656f61f8dd866b1`  
		Last Modified: Sat, 26 Sep 2020 04:43:33 GMT  
		Size: 3.1 MB (3075371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3df9e8e9238216b0bc889f73468bb1724d9dd627858e018235ae9634916c005`  
		Last Modified: Wed, 30 Sep 2020 00:28:00 GMT  
		Size: 129.8 MB (129833821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e85811818d44d3866c793e9f63fcf6a9442f3327260415669ef9cd91430fb11`  
		Last Modified: Thu, 22 Oct 2020 11:57:45 GMT  
		Size: 27.7 MB (27734441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d7223fa111f6b16c405fa96dfd9deb5d49ffdc84de0eee36137fcd99835712`  
		Last Modified: Thu, 22 Oct 2020 11:57:28 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d57fc475b0b54bbcee66d6d2df7fa21e9cd34970f01a601290802370ccb682b`  
		Last Modified: Thu, 22 Oct 2020 11:57:28 GMT  
		Size: 9.4 KB (9391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9467147813178dbd5346437e1ddd0b474f1eccee566e19d7a7e3aa26e4bbce57`  
		Last Modified: Thu, 22 Oct 2020 11:57:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f860b416028a9ed549d319478f5daf80a1edc63d5577e89fb76ad3155555e2`  
		Last Modified: Thu, 22 Oct 2020 11:57:29 GMT  
		Size: 10.4 KB (10375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c08f7e25f06ce1e713faa04610825054e67687bdb672e6a058244fba819267`  
		Last Modified: Thu, 22 Oct 2020 11:57:31 GMT  
		Size: 5.2 MB (5167147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f6abe802dfabd9f7bd657ce4832cf9473a55d2c758ce5cf6e7decdd76146b6`  
		Last Modified: Thu, 22 Oct 2020 11:59:22 GMT  
		Size: 199.3 MB (199306707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52407b513b45d39ea95e19705fbda368fca48b04652a1b88b92405ed124de30`  
		Last Modified: Thu, 22 Oct 2020 11:57:55 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c25d3fb147f034536a2d9be57ddd31b799aff9bff4d90e99ee522763d690f91`  
		Last Modified: Thu, 22 Oct 2020 11:58:10 GMT  
		Size: 18.4 MB (18428905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:f2d3484947b5ef3eba60da5da7a2933ee1603dde6ca0866231816b49e35ec8ac
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.3 MB (410339605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a7ae09af3a625913020bd0bbd31fc3a99a3f07ceaa24017811dc94fcc95556`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:44:45 GMT
ADD file:0a8ec4fb62616b6605197e20e0a7b511dc5b03d4af0e04c929dfd9fb457d2065 in / 
# Fri, 25 Sep 2020 22:44:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:44:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:44:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:44:48 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:01:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 25 Sep 2020 23:01:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:44:39 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:46:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:46:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 01:09:20 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 01:09:21 GMT
ARG OPENJ9_SCC=true
# Mon, 02 Nov 2020 21:43:28 GMT
ARG EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033
# Mon, 02 Nov 2020 21:43:28 GMT
ARG NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285
# Mon, 02 Nov 2020 21:43:29 GMT
ARG NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4
# Mon, 02 Nov 2020 21:43:29 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.11 org.opencontainers.image.revision=cl201120201014-1215 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Mon, 02 Nov 2020 21:43:29 GMT
ENV LIBERTY_VERSION=20.0.0_11
# Mon, 02 Nov 2020 21:43:29 GMT
ARG LIBERTY_URL
# Mon, 02 Nov 2020 21:43:30 GMT
ARG DOWNLOAD_OPTIONS=
# Mon, 02 Nov 2020 21:43:47 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Mon, 02 Nov 2020 21:43:49 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Nov 2020 21:43:50 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.11 BuildLabel=cl201120201014-1215
# Mon, 02 Nov 2020 21:43:50 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Mon, 02 Nov 2020 21:43:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 02 Nov 2020 21:43:53 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Mon, 02 Nov 2020 21:43:54 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Mon, 02 Nov 2020 21:43:55 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Mon, 02 Nov 2020 21:44:05 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Mon, 02 Nov 2020 21:44:05 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Mon, 02 Nov 2020 21:44:06 GMT
USER 1001
# Mon, 02 Nov 2020 21:44:06 GMT
EXPOSE 9080 9443
# Mon, 02 Nov 2020 21:44:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Mon, 02 Nov 2020 21:44:07 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Mon, 02 Nov 2020 21:44:17 GMT
ARG VERBOSE=false
# Mon, 02 Nov 2020 21:44:17 GMT
ARG REPOSITORIES_PROPERTIES=
# Mon, 02 Nov 2020 21:47:46 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Mon, 02 Nov 2020 21:47:55 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Mon, 02 Nov 2020 21:48:28 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:dd2de95b9a1c45e92bcc791d469201229b58d68187c99de6b08b00a13fa33393`  
		Last Modified: Fri, 25 Sep 2020 22:45:52 GMT  
		Size: 25.4 MB (25371975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38a48ef4dfab2bd639d381d11b3390b6bf8860b2ef3356e9bb55f7cb8c775f9`  
		Last Modified: Fri, 25 Sep 2020 22:45:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eced51184728468b347a6e3f143c356cd174c4a54be3cc10ec5aeddb402765fd`  
		Last Modified: Fri, 25 Sep 2020 22:45:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba234a37a5b5e77c8926746b575c905aa5fec2800099d1b330e0b05ecae699e5`  
		Last Modified: Fri, 25 Sep 2020 23:06:23 GMT  
		Size: 2.7 MB (2672151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74bce2b49bfe4913da5bc9719137a9c8d8fe4ae973dfa550b069adb24de7048`  
		Last Modified: Wed, 30 Sep 2020 00:49:52 GMT  
		Size: 127.5 MB (127515953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08d08612c2861209c25e0388fa03a8f4fe3ddbdf39967f0b4f056365f68c0af`  
		Last Modified: Mon, 02 Nov 2020 21:49:16 GMT  
		Size: 27.8 MB (27750974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed39a525cf22a2bdb1fdf34f9d4af2c54f005fa2143d82dd168392e278d8960a`  
		Last Modified: Mon, 02 Nov 2020 21:49:12 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb8c80357fb12d31581890c1f844deba6fe1345e6ee8daf3204f09c1fa90e59`  
		Last Modified: Mon, 02 Nov 2020 21:49:13 GMT  
		Size: 9.4 KB (9397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec7cfc60cd4170ce48119f317a2ec7bff04d5f2e6eb85c47727eecbd9e3b4e8`  
		Last Modified: Mon, 02 Nov 2020 21:49:12 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e5f963669923f98efcd98c1454d5009eef887d9db09246b36281cd08b4755a`  
		Last Modified: Mon, 02 Nov 2020 21:49:13 GMT  
		Size: 10.4 KB (10380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ffb399aa2d3f3f5521e2ddd71ae1c4508bfcca25d8f9a107209a33101f5ad9`  
		Last Modified: Mon, 02 Nov 2020 21:49:13 GMT  
		Size: 5.7 MB (5740146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbb629819ee5a33b88dc1adba9cd8ab0cf15177ed5b3318c952eef818455fc2`  
		Last Modified: Mon, 02 Nov 2020 21:49:32 GMT  
		Size: 200.1 MB (200106867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d43599856aa54a17ca17d3530ffe68e52b5e63287dd373396868e64b88b91cb`  
		Last Modified: Mon, 02 Nov 2020 21:49:23 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed812a4d484b2133a7ab73d780f1a18896b568aeca2cc5ed26315882dfbb9751`  
		Last Modified: Mon, 02 Nov 2020 21:49:26 GMT  
		Size: 21.2 MB (21158808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:49ab59ca08d8c8511d22d857dd68f50c26ebfdac763a2a841e9062089fbaec36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:kernel` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:642687e1dd264e8086a48ffd67dd5817b04205abedd3e978cf941219622f2bb5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193351420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69909793f9d25c768700f3a7d90237165bf6c854a7840bcf745f200e2f242ac6`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 00:39:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 26 Sep 2020 00:39:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:21:19 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:22:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 00:47:06 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 00:47:07 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Oct 2020 01:53:59 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.10 org.opencontainers.image.revision=cl201020200915-1100 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Oct 2020 01:54:00 GMT
ENV LIBERTY_VERSION=20.0.0_10
# Thu, 22 Oct 2020 01:54:00 GMT
ARG LIBERTY_URL
# Thu, 22 Oct 2020 01:54:00 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Oct 2020 01:54:13 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Oct 2020 01:54:13 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Oct 2020 01:54:14 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.10 BuildLabel=cl201020200915-1100
# Thu, 22 Oct 2020 01:54:14 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Oct 2020 01:54:15 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 01:54:15 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Thu, 22 Oct 2020 01:54:16 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Oct 2020 01:54:17 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 01:54:32 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Oct 2020 01:54:32 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Thu, 22 Oct 2020 01:54:32 GMT
USER 1001
# Thu, 22 Oct 2020 01:54:32 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 01:54:32 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Oct 2020 01:54:33 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e87f30ee71d2ba7a1d467dc205703e1443af14fdd58777f796dd35311cc49dc`  
		Last Modified: Sat, 26 Sep 2020 00:44:29 GMT  
		Size: 3.0 MB (2958234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6197f6576703d3211fafc6a64b9bf241bbed280c07aa2aabcc272d0dea695d0`  
		Last Modified: Wed, 30 Sep 2020 00:26:15 GMT  
		Size: 130.3 MB (130288845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f02a243cdf520b2db58f93f18c7b5cacfd8ea5668c16977c09b33c72be5d11`  
		Last Modified: Thu, 22 Oct 2020 02:12:48 GMT  
		Size: 27.7 MB (27734634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef48450a5818fc4e1cb4b746fd9a8de28de3defe12f6abf55ca3291af458f1db`  
		Last Modified: Thu, 22 Oct 2020 02:12:44 GMT  
		Size: 656.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e1ec9b9a3339d6c3e47579f2653c144dca0284526b69959012145c73746079`  
		Last Modified: Thu, 22 Oct 2020 02:12:45 GMT  
		Size: 9.4 KB (9364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dac3e62e13da3922c4f688f0be98c41695a9030b163fa342ed50c7f320cf67`  
		Last Modified: Thu, 22 Oct 2020 02:12:44 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd5cc8dce5355c809c982b38550c98bbaf4d34caccc434ddcfd47e8d2ec6bea`  
		Last Modified: Thu, 22 Oct 2020 02:12:44 GMT  
		Size: 10.3 KB (10269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540d02f5639655b60f7c9421031ffadd8e0d63e0d6fdd3467b3a52f4da9c785e`  
		Last Modified: Thu, 22 Oct 2020 02:12:46 GMT  
		Size: 5.6 MB (5646543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; 386

```console
$ docker pull websphere-liberty@sha256:21c2835a021b91c09268f12dc8f3c61f590c1b34d7669aeacf3792d83a7ef016
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162573580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e89243446a76e85ea4bf274dd0ad9e6fd0e763e50ced541577b62bee7dfcb74`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 20 Mar 2020 18:38:55 GMT
ADD file:d859d389e38b7ac70fd56f97e38d52a77b58e72b96237a4302d1984cdd912a55 in / 
# Fri, 20 Mar 2020 18:38:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:38:57 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:38:58 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:38:58 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:06:34 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 20 Mar 2020 19:06:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:06:42 GMT
ENV JAVA_VERSION=1.8.0_sr6fp6
# Fri, 20 Mar 2020 19:07:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='87f9d45b7e1fa65ec018479f3ca7da69a03b52b0da10b8d1555142eec8ab0093';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='b5f825047c9bb5d360fb83694f12e17b1a5a15abf94ac82cd0a3aea32c9a361c';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3c04cd07ef269c24373840eae6f59c7db7a16d2e206d393ba93efa6dbb8d74f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2bbefda96f7d1a5f1694893961e92ccc59dfa50375ae5450675d7a4213d5812e';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d5b0508d53d1c7382c06f5bc1daf3d57c19c70d851e86e6b1162bcd93f616f7e';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 20 Mar 2020 19:07:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 20 Mar 2020 19:31:53 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.3 org.opencontainers.image.revision=cl200320200305-1433
# Fri, 20 Mar 2020 19:31:53 GMT
ENV LIBERTY_VERSION=20.0.0_03
# Fri, 20 Mar 2020 19:31:53 GMT
ARG LIBERTY_URL
# Fri, 20 Mar 2020 19:31:53 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 20 Mar 2020 19:32:02 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:32:03 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2020 19:32:03 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.3 BuildLabel=cl200320200305-1433
# Fri, 20 Mar 2020 19:32:03 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Fri, 20 Mar 2020 19:32:04 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 20 Mar 2020 19:32:04 GMT
COPY dir:0d0cedab2fbb7208b9d81afa78e9f15b12b71232224a2fe9753c00b7b72bd72e in /opt/ibm/helpers/ 
# Fri, 20 Mar 2020 19:32:05 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 20 Mar 2020 19:32:05 GMT
COPY dir:9277507d983008afcf8df6e0bfe2735bd4e92717515dbb3a7e268c830f213489 in /licenses/ 
# Fri, 20 Mar 2020 19:32:06 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 20 Mar 2020 19:32:06 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Fri, 20 Mar 2020 19:32:06 GMT
USER 1001
# Fri, 20 Mar 2020 19:32:06 GMT
EXPOSE 9080 9443
# Fri, 20 Mar 2020 19:32:07 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 20 Mar 2020 19:32:07 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:765ce743592771b94ad8ff27e281e66c13f6039962c7dde4dbe47123081e015b`  
		Last Modified: Mon, 16 Mar 2020 15:38:41 GMT  
		Size: 27.1 MB (27122453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59dc9c4739090a3d2f7265f1f8184b1cbd8ae133b863f8aa93ec5cf1761ee7a5`  
		Last Modified: Fri, 20 Mar 2020 18:39:35 GMT  
		Size: 34.6 KB (34625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a5b698281c077f48fc598e698f0619e4d00a2fedc1832fc95e9cf281408f63`  
		Last Modified: Fri, 20 Mar 2020 18:39:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaebe599891b1e1befc10d752a117cc5615ec2dd3913d399fd66e26e0cace3e5`  
		Last Modified: Fri, 20 Mar 2020 18:39:34 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f829150bc8a53a37ac17eb34838fa33c990881a4031bc650a9dae26b3f7880e`  
		Last Modified: Fri, 20 Mar 2020 19:09:23 GMT  
		Size: 3.0 MB (2992132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17b9ccc4baf3a1ffa517a03c7c3d01900136b128b36a83558c67c42e6c1cbaa`  
		Last Modified: Fri, 20 Mar 2020 19:09:35 GMT  
		Size: 118.8 MB (118756706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5011972f1876d464fb62206211a5b5e162ba2603bf20fc4cd0f2b4ffd311cd9`  
		Last Modified: Fri, 20 Mar 2020 19:39:16 GMT  
		Size: 13.6 MB (13600436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5395b713d5baa0917182ca82077b6fa2a0c51789907f96cbb12455586d9fa9b`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389324a3d9489b2fbcd5946f9d24285c0171c3218470e4a5e2d45c731cefc522`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 3.5 KB (3515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38ea596499e1f23ce426826250984869e92da50aec5845a6233a76d7764bfd1`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea3197b55235384f836e31a605c460f6cb7196f68dc29c65640738d8aa50188`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 57.4 KB (57426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683f76bf565cdb9e59c325f24357eb6b164555ed8629a4b8383448239608966d`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 4.4 KB (4358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:3a8680d29dd172b85ef144a7e80ed1adf4950c4f6999dcc76a7dc04202f88e9d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196241053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3614764e2760573fdee6270a75fbcd8b8c40a8aeaf32bbac13749b06bacc74e8`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 04:38:06 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 26 Sep 2020 04:38:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:21:11 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:22:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 00:55:46 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 00:55:50 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Oct 2020 11:07:50 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.10 org.opencontainers.image.revision=cl201020200915-1100 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Oct 2020 11:08:01 GMT
ENV LIBERTY_VERSION=20.0.0_10
# Thu, 22 Oct 2020 11:08:12 GMT
ARG LIBERTY_URL
# Thu, 22 Oct 2020 11:08:30 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Oct 2020 11:10:28 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Oct 2020 11:10:45 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Oct 2020 11:10:56 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.10 BuildLabel=cl201020200915-1100
# Thu, 22 Oct 2020 11:11:02 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Oct 2020 11:11:28 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 11:11:39 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Thu, 22 Oct 2020 11:11:51 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Oct 2020 11:12:13 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 11:12:59 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Oct 2020 11:13:07 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Thu, 22 Oct 2020 11:13:14 GMT
USER 1001
# Thu, 22 Oct 2020 11:13:22 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 11:13:37 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Oct 2020 11:13:47 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405e3c1dd428ca3ff035da6469a7c6c36d02c92adb80d285656f61f8dd866b1`  
		Last Modified: Sat, 26 Sep 2020 04:43:33 GMT  
		Size: 3.1 MB (3075371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3df9e8e9238216b0bc889f73468bb1724d9dd627858e018235ae9634916c005`  
		Last Modified: Wed, 30 Sep 2020 00:28:00 GMT  
		Size: 129.8 MB (129833821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e85811818d44d3866c793e9f63fcf6a9442f3327260415669ef9cd91430fb11`  
		Last Modified: Thu, 22 Oct 2020 11:57:45 GMT  
		Size: 27.7 MB (27734441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d7223fa111f6b16c405fa96dfd9deb5d49ffdc84de0eee36137fcd99835712`  
		Last Modified: Thu, 22 Oct 2020 11:57:28 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d57fc475b0b54bbcee66d6d2df7fa21e9cd34970f01a601290802370ccb682b`  
		Last Modified: Thu, 22 Oct 2020 11:57:28 GMT  
		Size: 9.4 KB (9391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9467147813178dbd5346437e1ddd0b474f1eccee566e19d7a7e3aa26e4bbce57`  
		Last Modified: Thu, 22 Oct 2020 11:57:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f860b416028a9ed549d319478f5daf80a1edc63d5577e89fb76ad3155555e2`  
		Last Modified: Thu, 22 Oct 2020 11:57:29 GMT  
		Size: 10.4 KB (10375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c08f7e25f06ce1e713faa04610825054e67687bdb672e6a058244fba819267`  
		Last Modified: Thu, 22 Oct 2020 11:57:31 GMT  
		Size: 5.2 MB (5167147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:3b8c9f2857caa79ed8def6c26f462034476188e45d64aadbe4e804f3d8b49ecf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189072982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb40c977e0c23dca8f1107e576710f68870ec733c0a10f2b8f633217d856824f`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:44:45 GMT
ADD file:0a8ec4fb62616b6605197e20e0a7b511dc5b03d4af0e04c929dfd9fb457d2065 in / 
# Fri, 25 Sep 2020 22:44:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:44:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:44:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:44:48 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:01:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 25 Sep 2020 23:01:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:44:39 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:46:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:46:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 01:09:20 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 01:09:21 GMT
ARG OPENJ9_SCC=true
# Mon, 02 Nov 2020 21:43:28 GMT
ARG EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033
# Mon, 02 Nov 2020 21:43:28 GMT
ARG NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285
# Mon, 02 Nov 2020 21:43:29 GMT
ARG NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4
# Mon, 02 Nov 2020 21:43:29 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.11 org.opencontainers.image.revision=cl201120201014-1215 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Mon, 02 Nov 2020 21:43:29 GMT
ENV LIBERTY_VERSION=20.0.0_11
# Mon, 02 Nov 2020 21:43:29 GMT
ARG LIBERTY_URL
# Mon, 02 Nov 2020 21:43:30 GMT
ARG DOWNLOAD_OPTIONS=
# Mon, 02 Nov 2020 21:43:47 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Mon, 02 Nov 2020 21:43:49 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Nov 2020 21:43:50 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.11 BuildLabel=cl201120201014-1215
# Mon, 02 Nov 2020 21:43:50 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Mon, 02 Nov 2020 21:43:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 02 Nov 2020 21:43:53 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Mon, 02 Nov 2020 21:43:54 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Mon, 02 Nov 2020 21:43:55 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Mon, 02 Nov 2020 21:44:05 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Mon, 02 Nov 2020 21:44:05 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Mon, 02 Nov 2020 21:44:06 GMT
USER 1001
# Mon, 02 Nov 2020 21:44:06 GMT
EXPOSE 9080 9443
# Mon, 02 Nov 2020 21:44:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Mon, 02 Nov 2020 21:44:07 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:dd2de95b9a1c45e92bcc791d469201229b58d68187c99de6b08b00a13fa33393`  
		Last Modified: Fri, 25 Sep 2020 22:45:52 GMT  
		Size: 25.4 MB (25371975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38a48ef4dfab2bd639d381d11b3390b6bf8860b2ef3356e9bb55f7cb8c775f9`  
		Last Modified: Fri, 25 Sep 2020 22:45:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eced51184728468b347a6e3f143c356cd174c4a54be3cc10ec5aeddb402765fd`  
		Last Modified: Fri, 25 Sep 2020 22:45:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba234a37a5b5e77c8926746b575c905aa5fec2800099d1b330e0b05ecae699e5`  
		Last Modified: Fri, 25 Sep 2020 23:06:23 GMT  
		Size: 2.7 MB (2672151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74bce2b49bfe4913da5bc9719137a9c8d8fe4ae973dfa550b069adb24de7048`  
		Last Modified: Wed, 30 Sep 2020 00:49:52 GMT  
		Size: 127.5 MB (127515953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08d08612c2861209c25e0388fa03a8f4fe3ddbdf39967f0b4f056365f68c0af`  
		Last Modified: Mon, 02 Nov 2020 21:49:16 GMT  
		Size: 27.8 MB (27750974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed39a525cf22a2bdb1fdf34f9d4af2c54f005fa2143d82dd168392e278d8960a`  
		Last Modified: Mon, 02 Nov 2020 21:49:12 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb8c80357fb12d31581890c1f844deba6fe1345e6ee8daf3204f09c1fa90e59`  
		Last Modified: Mon, 02 Nov 2020 21:49:13 GMT  
		Size: 9.4 KB (9397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec7cfc60cd4170ce48119f317a2ec7bff04d5f2e6eb85c47727eecbd9e3b4e8`  
		Last Modified: Mon, 02 Nov 2020 21:49:12 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e5f963669923f98efcd98c1454d5009eef887d9db09246b36281cd08b4755a`  
		Last Modified: Mon, 02 Nov 2020 21:49:13 GMT  
		Size: 10.4 KB (10380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ffb399aa2d3f3f5521e2ddd71ae1c4508bfcca25d8f9a107209a33101f5ad9`  
		Last Modified: Mon, 02 Nov 2020 21:49:13 GMT  
		Size: 5.7 MB (5740146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:latest`

```console
$ docker pull websphere-liberty@sha256:a9ae31d15421aa300827293d49d9b6ea1638fb64c139cc76b7a6ffb2aaea1ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:latest` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:6032bdf6bcab14693e2a82d1b656c144cb33be964adb46e37c65451f84c756c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.1 MB (414060472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e8db59984d53c5695604feac2737fbee8b380c32eb70d696e7f81d9533436b`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 00:39:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 26 Sep 2020 00:39:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:21:19 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:22:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 00:47:06 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 00:47:07 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Oct 2020 01:53:59 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.10 org.opencontainers.image.revision=cl201020200915-1100 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Oct 2020 01:54:00 GMT
ENV LIBERTY_VERSION=20.0.0_10
# Thu, 22 Oct 2020 01:54:00 GMT
ARG LIBERTY_URL
# Thu, 22 Oct 2020 01:54:00 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Oct 2020 01:54:13 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Oct 2020 01:54:13 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Oct 2020 01:54:14 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.10 BuildLabel=cl201020200915-1100
# Thu, 22 Oct 2020 01:54:14 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Oct 2020 01:54:15 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 01:54:15 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Thu, 22 Oct 2020 01:54:16 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Oct 2020 01:54:17 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 01:54:32 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Oct 2020 01:54:32 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Thu, 22 Oct 2020 01:54:32 GMT
USER 1001
# Thu, 22 Oct 2020 01:54:32 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 01:54:32 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Oct 2020 01:54:33 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Oct 2020 01:54:40 GMT
ARG VERBOSE=false
# Thu, 22 Oct 2020 01:54:40 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Oct 2020 01:57:55 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Thu, 22 Oct 2020 01:57:55 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Oct 2020 01:58:54 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e87f30ee71d2ba7a1d467dc205703e1443af14fdd58777f796dd35311cc49dc`  
		Last Modified: Sat, 26 Sep 2020 00:44:29 GMT  
		Size: 3.0 MB (2958234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6197f6576703d3211fafc6a64b9bf241bbed280c07aa2aabcc272d0dea695d0`  
		Last Modified: Wed, 30 Sep 2020 00:26:15 GMT  
		Size: 130.3 MB (130288845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f02a243cdf520b2db58f93f18c7b5cacfd8ea5668c16977c09b33c72be5d11`  
		Last Modified: Thu, 22 Oct 2020 02:12:48 GMT  
		Size: 27.7 MB (27734634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef48450a5818fc4e1cb4b746fd9a8de28de3defe12f6abf55ca3291af458f1db`  
		Last Modified: Thu, 22 Oct 2020 02:12:44 GMT  
		Size: 656.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e1ec9b9a3339d6c3e47579f2653c144dca0284526b69959012145c73746079`  
		Last Modified: Thu, 22 Oct 2020 02:12:45 GMT  
		Size: 9.4 KB (9364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dac3e62e13da3922c4f688f0be98c41695a9030b163fa342ed50c7f320cf67`  
		Last Modified: Thu, 22 Oct 2020 02:12:44 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd5cc8dce5355c809c982b38550c98bbaf4d34caccc434ddcfd47e8d2ec6bea`  
		Last Modified: Thu, 22 Oct 2020 02:12:44 GMT  
		Size: 10.3 KB (10269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540d02f5639655b60f7c9421031ffadd8e0d63e0d6fdd3467b3a52f4da9c785e`  
		Last Modified: Thu, 22 Oct 2020 02:12:46 GMT  
		Size: 5.6 MB (5646543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8bea44cd7bc9c6f6430f457b7415e212df6cb17bce46131ca2ecf8d1276512a`  
		Last Modified: Thu, 22 Oct 2020 02:13:19 GMT  
		Size: 199.8 MB (199770138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9ca3a8d709ad4fb08a6aa4aad1127658c0c1b163bdd97916f36a0b261cdc45`  
		Last Modified: Thu, 22 Oct 2020 02:12:52 GMT  
		Size: 947.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9e709c4cab95c5d2e10b8c171ed8657ac10a766089035152d56170a9d674ca`  
		Last Modified: Thu, 22 Oct 2020 02:12:57 GMT  
		Size: 20.9 MB (20937967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:latest` - linux; 386

```console
$ docker pull websphere-liberty@sha256:c847143995aec30ca5d4526544d7c41ca7a42a8baf8195848864d0128e96ecf3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.2 MB (349209019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d2c9374be56a63d6e35820fec8676f2d4ed2b9bdaf09a49c8545b039479bb7`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 20 Mar 2020 18:38:55 GMT
ADD file:d859d389e38b7ac70fd56f97e38d52a77b58e72b96237a4302d1984cdd912a55 in / 
# Fri, 20 Mar 2020 18:38:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:38:57 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:38:58 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:38:58 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:06:34 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 20 Mar 2020 19:06:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:06:42 GMT
ENV JAVA_VERSION=1.8.0_sr6fp6
# Fri, 20 Mar 2020 19:07:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='87f9d45b7e1fa65ec018479f3ca7da69a03b52b0da10b8d1555142eec8ab0093';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='b5f825047c9bb5d360fb83694f12e17b1a5a15abf94ac82cd0a3aea32c9a361c';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3c04cd07ef269c24373840eae6f59c7db7a16d2e206d393ba93efa6dbb8d74f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2bbefda96f7d1a5f1694893961e92ccc59dfa50375ae5450675d7a4213d5812e';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d5b0508d53d1c7382c06f5bc1daf3d57c19c70d851e86e6b1162bcd93f616f7e';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 20 Mar 2020 19:07:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 20 Mar 2020 19:31:53 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.3 org.opencontainers.image.revision=cl200320200305-1433
# Fri, 20 Mar 2020 19:31:53 GMT
ENV LIBERTY_VERSION=20.0.0_03
# Fri, 20 Mar 2020 19:31:53 GMT
ARG LIBERTY_URL
# Fri, 20 Mar 2020 19:31:53 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 20 Mar 2020 19:32:02 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:32:03 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2020 19:32:03 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.3 BuildLabel=cl200320200305-1433
# Fri, 20 Mar 2020 19:32:03 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Fri, 20 Mar 2020 19:32:04 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 20 Mar 2020 19:32:04 GMT
COPY dir:0d0cedab2fbb7208b9d81afa78e9f15b12b71232224a2fe9753c00b7b72bd72e in /opt/ibm/helpers/ 
# Fri, 20 Mar 2020 19:32:05 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 20 Mar 2020 19:32:05 GMT
COPY dir:9277507d983008afcf8df6e0bfe2735bd4e92717515dbb3a7e268c830f213489 in /licenses/ 
# Fri, 20 Mar 2020 19:32:06 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 20 Mar 2020 19:32:06 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Fri, 20 Mar 2020 19:32:06 GMT
USER 1001
# Fri, 20 Mar 2020 19:32:06 GMT
EXPOSE 9080 9443
# Fri, 20 Mar 2020 19:32:07 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 20 Mar 2020 19:32:07 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 20 Mar 2020 19:32:10 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 20 Mar 2020 19:35:01 GMT
# ARGS: REPOSITORIES_PROPERTIES=
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Fri, 20 Mar 2020 19:35:01 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
```

-	Layers:
	-	`sha256:765ce743592771b94ad8ff27e281e66c13f6039962c7dde4dbe47123081e015b`  
		Last Modified: Mon, 16 Mar 2020 15:38:41 GMT  
		Size: 27.1 MB (27122453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59dc9c4739090a3d2f7265f1f8184b1cbd8ae133b863f8aa93ec5cf1761ee7a5`  
		Last Modified: Fri, 20 Mar 2020 18:39:35 GMT  
		Size: 34.6 KB (34625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a5b698281c077f48fc598e698f0619e4d00a2fedc1832fc95e9cf281408f63`  
		Last Modified: Fri, 20 Mar 2020 18:39:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaebe599891b1e1befc10d752a117cc5615ec2dd3913d399fd66e26e0cace3e5`  
		Last Modified: Fri, 20 Mar 2020 18:39:34 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f829150bc8a53a37ac17eb34838fa33c990881a4031bc650a9dae26b3f7880e`  
		Last Modified: Fri, 20 Mar 2020 19:09:23 GMT  
		Size: 3.0 MB (2992132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17b9ccc4baf3a1ffa517a03c7c3d01900136b128b36a83558c67c42e6c1cbaa`  
		Last Modified: Fri, 20 Mar 2020 19:09:35 GMT  
		Size: 118.8 MB (118756706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5011972f1876d464fb62206211a5b5e162ba2603bf20fc4cd0f2b4ffd311cd9`  
		Last Modified: Fri, 20 Mar 2020 19:39:16 GMT  
		Size: 13.6 MB (13600436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5395b713d5baa0917182ca82077b6fa2a0c51789907f96cbb12455586d9fa9b`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389324a3d9489b2fbcd5946f9d24285c0171c3218470e4a5e2d45c731cefc522`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 3.5 KB (3515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38ea596499e1f23ce426826250984869e92da50aec5845a6233a76d7764bfd1`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea3197b55235384f836e31a605c460f6cb7196f68dc29c65640738d8aa50188`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 57.4 KB (57426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683f76bf565cdb9e59c325f24357eb6b164555ed8629a4b8383448239608966d`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 4.4 KB (4358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cd2560c76831311d13d197b4784e0826f6ffae62e3b9a22d2fa5675b9b71a2`  
		Last Modified: Fri, 20 Mar 2020 19:39:42 GMT  
		Size: 186.6 MB (186634496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9891aa2b3e904f8f514677372187983ac12c98c209c433ab5bf0862e09d6f4ef`  
		Last Modified: Fri, 20 Mar 2020 19:39:20 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:latest` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:f12eee541bc4aa192561d663754de7a0a6bc5360b801d175105fda20e34534b4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.0 MB (413977616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb443729949fe0130cc0960d8065fc7853592d37088c5442f8ff77d4d27c38d1`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 04:38:06 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 26 Sep 2020 04:38:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:21:11 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:22:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 00:55:46 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 00:55:50 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Oct 2020 11:07:50 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.10 org.opencontainers.image.revision=cl201020200915-1100 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Oct 2020 11:08:01 GMT
ENV LIBERTY_VERSION=20.0.0_10
# Thu, 22 Oct 2020 11:08:12 GMT
ARG LIBERTY_URL
# Thu, 22 Oct 2020 11:08:30 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Oct 2020 11:10:28 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Oct 2020 11:10:45 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Oct 2020 11:10:56 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.10 BuildLabel=cl201020200915-1100
# Thu, 22 Oct 2020 11:11:02 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Oct 2020 11:11:28 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Oct 2020 11:11:39 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Thu, 22 Oct 2020 11:11:51 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Oct 2020 11:12:13 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Oct 2020 11:12:59 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Oct 2020 11:13:07 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Thu, 22 Oct 2020 11:13:14 GMT
USER 1001
# Thu, 22 Oct 2020 11:13:22 GMT
EXPOSE 9080 9443
# Thu, 22 Oct 2020 11:13:37 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Oct 2020 11:13:47 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Oct 2020 11:14:01 GMT
ARG VERBOSE=false
# Thu, 22 Oct 2020 11:14:12 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Oct 2020 11:21:50 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Thu, 22 Oct 2020 11:21:56 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Oct 2020 11:23:49 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6405e3c1dd428ca3ff035da6469a7c6c36d02c92adb80d285656f61f8dd866b1`  
		Last Modified: Sat, 26 Sep 2020 04:43:33 GMT  
		Size: 3.1 MB (3075371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3df9e8e9238216b0bc889f73468bb1724d9dd627858e018235ae9634916c005`  
		Last Modified: Wed, 30 Sep 2020 00:28:00 GMT  
		Size: 129.8 MB (129833821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e85811818d44d3866c793e9f63fcf6a9442f3327260415669ef9cd91430fb11`  
		Last Modified: Thu, 22 Oct 2020 11:57:45 GMT  
		Size: 27.7 MB (27734441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d7223fa111f6b16c405fa96dfd9deb5d49ffdc84de0eee36137fcd99835712`  
		Last Modified: Thu, 22 Oct 2020 11:57:28 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d57fc475b0b54bbcee66d6d2df7fa21e9cd34970f01a601290802370ccb682b`  
		Last Modified: Thu, 22 Oct 2020 11:57:28 GMT  
		Size: 9.4 KB (9391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9467147813178dbd5346437e1ddd0b474f1eccee566e19d7a7e3aa26e4bbce57`  
		Last Modified: Thu, 22 Oct 2020 11:57:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f860b416028a9ed549d319478f5daf80a1edc63d5577e89fb76ad3155555e2`  
		Last Modified: Thu, 22 Oct 2020 11:57:29 GMT  
		Size: 10.4 KB (10375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c08f7e25f06ce1e713faa04610825054e67687bdb672e6a058244fba819267`  
		Last Modified: Thu, 22 Oct 2020 11:57:31 GMT  
		Size: 5.2 MB (5167147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f6abe802dfabd9f7bd657ce4832cf9473a55d2c758ce5cf6e7decdd76146b6`  
		Last Modified: Thu, 22 Oct 2020 11:59:22 GMT  
		Size: 199.3 MB (199306707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52407b513b45d39ea95e19705fbda368fca48b04652a1b88b92405ed124de30`  
		Last Modified: Thu, 22 Oct 2020 11:57:55 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c25d3fb147f034536a2d9be57ddd31b799aff9bff4d90e99ee522763d690f91`  
		Last Modified: Thu, 22 Oct 2020 11:58:10 GMT  
		Size: 18.4 MB (18428905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:latest` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:f2d3484947b5ef3eba60da5da7a2933ee1603dde6ca0866231816b49e35ec8ac
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.3 MB (410339605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a7ae09af3a625913020bd0bbd31fc3a99a3f07ceaa24017811dc94fcc95556`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 25 Sep 2020 22:44:45 GMT
ADD file:0a8ec4fb62616b6605197e20e0a7b511dc5b03d4af0e04c929dfd9fb457d2065 in / 
# Fri, 25 Sep 2020 22:44:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:44:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:44:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:44:48 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:01:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 25 Sep 2020 23:01:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 30 Sep 2020 00:44:39 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 30 Sep 2020 00:46:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:46:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 30 Sep 2020 01:09:20 GMT
ARG VERBOSE=false
# Wed, 30 Sep 2020 01:09:21 GMT
ARG OPENJ9_SCC=true
# Mon, 02 Nov 2020 21:43:28 GMT
ARG EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033
# Mon, 02 Nov 2020 21:43:28 GMT
ARG NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285
# Mon, 02 Nov 2020 21:43:29 GMT
ARG NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4
# Mon, 02 Nov 2020 21:43:29 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.11 org.opencontainers.image.revision=cl201120201014-1215 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Mon, 02 Nov 2020 21:43:29 GMT
ENV LIBERTY_VERSION=20.0.0_11
# Mon, 02 Nov 2020 21:43:29 GMT
ARG LIBERTY_URL
# Mon, 02 Nov 2020 21:43:30 GMT
ARG DOWNLOAD_OPTIONS=
# Mon, 02 Nov 2020 21:43:47 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Mon, 02 Nov 2020 21:43:49 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Nov 2020 21:43:50 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.11 BuildLabel=cl201120201014-1215
# Mon, 02 Nov 2020 21:43:50 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Mon, 02 Nov 2020 21:43:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 02 Nov 2020 21:43:53 GMT
COPY dir:27e8dea5a7afd809d10795bd74edfae21b04f711347266a3988c299c526340c9 in /opt/ibm/helpers/ 
# Mon, 02 Nov 2020 21:43:54 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Mon, 02 Nov 2020 21:43:55 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Mon, 02 Nov 2020 21:44:05 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=94d859d22ee00758a00b75f9ef52772ecf1c52b4055a9f997f4f99423b17c033 NON_IBM_SHA=e425adf53bb63f1c53060c1b05f6fb553af433f64460daee51f965cff230e285 NOTICES_SHA=aae32415dc8f4195b2b8393990fee937bd6d5836622ecce1c12c6d77cdb83ad4 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Mon, 02 Nov 2020 21:44:05 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Mon, 02 Nov 2020 21:44:06 GMT
USER 1001
# Mon, 02 Nov 2020 21:44:06 GMT
EXPOSE 9080 9443
# Mon, 02 Nov 2020 21:44:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Mon, 02 Nov 2020 21:44:07 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Mon, 02 Nov 2020 21:44:17 GMT
ARG VERBOSE=false
# Mon, 02 Nov 2020 21:44:17 GMT
ARG REPOSITORIES_PROPERTIES=
# Mon, 02 Nov 2020 21:47:46 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Mon, 02 Nov 2020 21:47:55 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Mon, 02 Nov 2020 21:48:28 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:dd2de95b9a1c45e92bcc791d469201229b58d68187c99de6b08b00a13fa33393`  
		Last Modified: Fri, 25 Sep 2020 22:45:52 GMT  
		Size: 25.4 MB (25371975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38a48ef4dfab2bd639d381d11b3390b6bf8860b2ef3356e9bb55f7cb8c775f9`  
		Last Modified: Fri, 25 Sep 2020 22:45:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eced51184728468b347a6e3f143c356cd174c4a54be3cc10ec5aeddb402765fd`  
		Last Modified: Fri, 25 Sep 2020 22:45:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba234a37a5b5e77c8926746b575c905aa5fec2800099d1b330e0b05ecae699e5`  
		Last Modified: Fri, 25 Sep 2020 23:06:23 GMT  
		Size: 2.7 MB (2672151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74bce2b49bfe4913da5bc9719137a9c8d8fe4ae973dfa550b069adb24de7048`  
		Last Modified: Wed, 30 Sep 2020 00:49:52 GMT  
		Size: 127.5 MB (127515953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08d08612c2861209c25e0388fa03a8f4fe3ddbdf39967f0b4f056365f68c0af`  
		Last Modified: Mon, 02 Nov 2020 21:49:16 GMT  
		Size: 27.8 MB (27750974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed39a525cf22a2bdb1fdf34f9d4af2c54f005fa2143d82dd168392e278d8960a`  
		Last Modified: Mon, 02 Nov 2020 21:49:12 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb8c80357fb12d31581890c1f844deba6fe1345e6ee8daf3204f09c1fa90e59`  
		Last Modified: Mon, 02 Nov 2020 21:49:13 GMT  
		Size: 9.4 KB (9397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec7cfc60cd4170ce48119f317a2ec7bff04d5f2e6eb85c47727eecbd9e3b4e8`  
		Last Modified: Mon, 02 Nov 2020 21:49:12 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e5f963669923f98efcd98c1454d5009eef887d9db09246b36281cd08b4755a`  
		Last Modified: Mon, 02 Nov 2020 21:49:13 GMT  
		Size: 10.4 KB (10380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ffb399aa2d3f3f5521e2ddd71ae1c4508bfcca25d8f9a107209a33101f5ad9`  
		Last Modified: Mon, 02 Nov 2020 21:49:13 GMT  
		Size: 5.7 MB (5740146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbb629819ee5a33b88dc1adba9cd8ab0cf15177ed5b3318c952eef818455fc2`  
		Last Modified: Mon, 02 Nov 2020 21:49:32 GMT  
		Size: 200.1 MB (200106867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d43599856aa54a17ca17d3530ffe68e52b5e63287dd373396868e64b88b91cb`  
		Last Modified: Mon, 02 Nov 2020 21:49:23 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed812a4d484b2133a7ab73d780f1a18896b568aeca2cc5ed26315882dfbb9751`  
		Last Modified: Mon, 02 Nov 2020 21:49:26 GMT  
		Size: 21.2 MB (21158808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
