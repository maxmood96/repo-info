<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `websphere-liberty`

-	[`websphere-liberty:19.0.0.12-full-java8-ibmjava`](#websphere-liberty190012-full-java8-ibmjava)
-	[`websphere-liberty:19.0.0.12-kernel-java8-ibmjava`](#websphere-liberty190012-kernel-java8-ibmjava)
-	[`websphere-liberty:20.0.0.3-full-java8-ibmjava`](#websphere-liberty20003-full-java8-ibmjava)
-	[`websphere-liberty:20.0.0.3-kernel-java8-ibmjava`](#websphere-liberty20003-kernel-java8-ibmjava)
-	[`websphere-liberty:20.0.0.5-full-java8-ibmjava`](#websphere-liberty20005-full-java8-ibmjava)
-	[`websphere-liberty:20.0.0.5-kernel-java8-ibmjava`](#websphere-liberty20005-kernel-java8-ibmjava)
-	[`websphere-liberty:beta`](#websphere-libertybeta)
-	[`websphere-liberty:full`](#websphere-libertyfull)
-	[`websphere-liberty:kernel`](#websphere-libertykernel)
-	[`websphere-liberty:latest`](#websphere-libertylatest)

## `websphere-liberty:19.0.0.12-full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:a6d09f067c1e5a23eebd8be455214bafce1906247141b2145aaca5da3453ac3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:19.0.0.12-full-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:019047dd0c75719493f9338868be580dce3a2be3347626ce7af587e2855d927c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.7 MB (361723467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304d66de053228596c2df692376a3f8b4aab2a4abcea2aa035cbd52864a4f59d`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 14:38:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 14:39:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 17:22:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 17:22:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 17:22:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 19:07:40 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=19.0.0.12 org.opencontainers.image.revision=cl191220191120-0300 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 May 2020 19:07:40 GMT
ENV LIBERTY_VERSION=19.0.0_12
# Wed, 06 May 2020 19:07:40 GMT
ARG LIBERTY_URL
# Wed, 06 May 2020 19:07:40 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 May 2020 19:07:49 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:07:49 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2020 19:07:49 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=19.0.0.12 BuildLabel=cl191220191120-0300
# Wed, 06 May 2020 19:07:49 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Wed, 06 May 2020 19:07:50 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 06 May 2020 19:07:51 GMT
COPY dir:0d0cedab2fbb7208b9d81afa78e9f15b12b71232224a2fe9753c00b7b72bd72e in /opt/ibm/helpers/ 
# Wed, 06 May 2020 19:07:51 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 06 May 2020 19:07:51 GMT
COPY dir:ac01ddd10295d427b1e05fe08b779c3a46df170405e703dc88e5be095b14c1e4 in /licenses/ 
# Wed, 06 May 2020 19:07:52 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 06 May 2020 19:07:52 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 06 May 2020 19:07:52 GMT
USER 1001
# Wed, 06 May 2020 19:07:52 GMT
EXPOSE 9080 9443
# Wed, 06 May 2020 19:07:53 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 06 May 2020 19:07:53 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 06 May 2020 19:07:58 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 06 May 2020 19:10:41 GMT
# ARGS: REPOSITORIES_PROPERTIES=
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 06 May 2020 19:10:42 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a528cffcbfa77f36f260d896e265cfb925555d14069b6cb510319dbe87d2e393`  
		Last Modified: Wed, 29 Apr 2020 03:27:55 GMT  
		Size: 3.0 MB (2965011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc65fe0ac24ec55f1cda0e25f07bba60ccd2ee3ff62f7355c9773cf51145e7e0`  
		Last Modified: Wed, 06 May 2020 17:27:06 GMT  
		Size: 130.3 MB (130335315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de57ac949ac66af02e3039eaaaa30e96e93db5aa61008051c894d02686da671`  
		Last Modified: Wed, 13 May 2020 01:51:46 GMT  
		Size: 13.2 MB (13201131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1eb1243a1487158c2191c4d684ae986dabe480d8d849eeae59b96fc07f7628`  
		Last Modified: Wed, 13 May 2020 01:51:41 GMT  
		Size: 675.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39ba719eea17fcc69050adb5012e5276049d975c4301f3ca3c557ca80b08cc3`  
		Last Modified: Wed, 13 May 2020 01:51:42 GMT  
		Size: 3.5 KB (3517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198679892e9c2294d4da3ac7fa2f0d1603ea20913d87ce9b197256ac9f45643e`  
		Last Modified: Wed, 13 May 2020 01:51:42 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3772554407bad00e7751e2931e7f79233e19c8c9fbd9c8c355f66cfd595d3847`  
		Last Modified: Wed, 13 May 2020 01:51:42 GMT  
		Size: 58.2 KB (58241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4ced1987c1e70a3416dea1d5bf320a741ae74aff3292591d9c6f564064725f`  
		Last Modified: Wed, 13 May 2020 01:51:41 GMT  
		Size: 4.4 KB (4357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e538f49756ed82d34368298ace145106da8a032e9e27040f115fb3c145887a`  
		Last Modified: Wed, 13 May 2020 01:52:05 GMT  
		Size: 188.4 MB (188427847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ff6edf8aa89f00af3c8a41ddaf4b9d0c69252fa6b4801a83b365b2b5a2d786`  
		Last Modified: Wed, 13 May 2020 01:51:50 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:19.0.0.12-full-java8-ibmjava` - linux; 386

```console
$ docker pull websphere-liberty@sha256:4079cfd89fea30e1e438ac8bd7d3f3d88675488433e1d08d848d9139b5451ba6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.6 MB (350602116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade42234b7e3e4764823383a76107d35f1e490b4d8643c89acf782a6c19a601e`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 21:17:02 GMT
ADD file:93916d8759465832704c50a78cd4ca1ad83e80baefd96a15563505b3374b8f3c in / 
# Thu, 23 Apr 2020 21:17:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 21:17:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 21:17:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 21:17:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 08:57:23 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 08:57:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 17:38:27 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 17:39:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 17:39:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:04:41 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=19.0.0.12 org.opencontainers.image.revision=cl191220191120-0300 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 May 2020 18:04:41 GMT
ENV LIBERTY_VERSION=19.0.0_12
# Wed, 06 May 2020 18:04:42 GMT
ARG LIBERTY_URL
# Wed, 06 May 2020 18:04:42 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 May 2020 18:04:51 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 18:04:51 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2020 18:04:51 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=19.0.0.12 BuildLabel=cl191220191120-0300
# Wed, 06 May 2020 18:04:51 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Wed, 06 May 2020 18:04:52 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 06 May 2020 18:04:53 GMT
COPY dir:0d0cedab2fbb7208b9d81afa78e9f15b12b71232224a2fe9753c00b7b72bd72e in /opt/ibm/helpers/ 
# Wed, 06 May 2020 18:04:53 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 06 May 2020 18:04:53 GMT
COPY dir:ac01ddd10295d427b1e05fe08b779c3a46df170405e703dc88e5be095b14c1e4 in /licenses/ 
# Wed, 06 May 2020 18:04:54 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 06 May 2020 18:04:54 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 06 May 2020 18:04:54 GMT
USER 1001
# Wed, 06 May 2020 18:04:55 GMT
EXPOSE 9080 9443
# Wed, 06 May 2020 18:04:55 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 06 May 2020 18:04:55 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 06 May 2020 18:05:00 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 06 May 2020 18:07:58 GMT
# ARGS: REPOSITORIES_PROPERTIES=
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 06 May 2020 18:07:58 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
```

-	Layers:
	-	`sha256:32febc939a10ccd7e09d79d3844314e0ddd7186a038a8129711026e33bb52944`  
		Last Modified: Sun, 05 Apr 2020 20:23:59 GMT  
		Size: 27.1 MB (27123063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1172dfcc3d758ff57c194883a4e3f387b056879cb1366a4b6917f0f111b57c0`  
		Last Modified: Thu, 23 Apr 2020 21:17:53 GMT  
		Size: 34.6 KB (34621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cec8eab9aff7ebcd137e82043cc8bce36e7807a6101c176aeecb5f45229468`  
		Last Modified: Thu, 23 Apr 2020 21:17:53 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d2624c94975a0cf9135648d1bfdbbbc91abd34977488f6fb47df8d674c34d8`  
		Last Modified: Thu, 23 Apr 2020 21:17:53 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5c544544748d32930489934c3525b4efcef3711c7af60fb4936333b00963af`  
		Last Modified: Fri, 24 Apr 2020 08:59:58 GMT  
		Size: 3.0 MB (2992510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022dedc8b7eaee6c7517f31d3ce49ee8f3f514f36b4ee146fb366db909bff8bf`  
		Last Modified: Wed, 06 May 2020 17:41:07 GMT  
		Size: 118.8 MB (118781405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6dacff20ca3a6ac8bd76edf36d7bf45521c7b85c437369ba5c2c7e68deed96b`  
		Last Modified: Wed, 06 May 2020 18:08:53 GMT  
		Size: 13.2 MB (13201739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98ffdabe21a7a18827d1669c6d89c6b15dcb48ee6e9ca11c555114e71074ba1`  
		Last Modified: Wed, 06 May 2020 18:08:50 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc123d40644d2f695e51fb4b8c152a73e72f158736917829042f544719852a99`  
		Last Modified: Wed, 06 May 2020 18:08:50 GMT  
		Size: 3.5 KB (3515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fe447588a3b117a914e80e522bfeaa6b9a178d67ad5f179f11ba28850547b0`  
		Last Modified: Wed, 06 May 2020 18:08:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8ff6835007bb9e4272be932a0f587f49f760578dc121d857c3c0ece89dfd06`  
		Last Modified: Wed, 06 May 2020 18:08:51 GMT  
		Size: 58.2 KB (58239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19997b5c67d3fdeb7a8bd95702bb6945e88659dc21c980ebf31492b04c0fcf2a`  
		Last Modified: Wed, 06 May 2020 18:08:50 GMT  
		Size: 4.4 KB (4367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4641ccc324852b7f412cdba91bc62186d41ca9c173940b6804bf45a26c64ddf`  
		Last Modified: Wed, 06 May 2020 18:10:30 GMT  
		Size: 188.4 MB (188399777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d0aa76338c2e2eccb54bfbcc69cc7ec0b0f9eb6da9387817217538d22b0e35`  
		Last Modified: Wed, 06 May 2020 18:10:13 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:19.0.0.12-full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:5900bf3d7740a0ba375384ee067229d4c3f3031579cf7cbd207717c6f2c07fff
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.0 MB (372950986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a78b47b73a95a78d02e8068a94ed30430f9ce1de5cd2e1a09bcfe59e9ab749d`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:49:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 11:50:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 18:16:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 18:17:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 18:18:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 19:11:07 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=19.0.0.12 org.opencontainers.image.revision=cl191220191120-0300 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 May 2020 19:11:10 GMT
ENV LIBERTY_VERSION=19.0.0_12
# Wed, 06 May 2020 19:11:14 GMT
ARG LIBERTY_URL
# Wed, 06 May 2020 19:11:18 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 May 2020 19:11:54 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:11:59 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2020 19:12:03 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=19.0.0.12 BuildLabel=cl191220191120-0300
# Wed, 06 May 2020 19:12:07 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Wed, 06 May 2020 19:12:16 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 06 May 2020 19:12:17 GMT
COPY dir:0d0cedab2fbb7208b9d81afa78e9f15b12b71232224a2fe9753c00b7b72bd72e in /opt/ibm/helpers/ 
# Wed, 06 May 2020 19:12:19 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 06 May 2020 19:12:20 GMT
COPY dir:ac01ddd10295d427b1e05fe08b779c3a46df170405e703dc88e5be095b14c1e4 in /licenses/ 
# Wed, 06 May 2020 19:12:28 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 06 May 2020 19:12:33 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 06 May 2020 19:12:35 GMT
USER 1001
# Wed, 06 May 2020 19:12:36 GMT
EXPOSE 9080 9443
# Wed, 06 May 2020 19:12:39 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 06 May 2020 19:12:43 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 06 May 2020 19:13:06 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 06 May 2020 19:17:14 GMT
# ARGS: REPOSITORIES_PROPERTIES=
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 06 May 2020 19:17:19 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df114b83a5a3444a39237d52fb0ddee6b46bc18624f26febb7c6a00effacdd4`  
		Last Modified: Fri, 24 Apr 2020 11:54:50 GMT  
		Size: 3.1 MB (3093321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a3df9e59dafede5e9e49376b8d92ca46f947103b310001473fb6ed575cc9c4`  
		Last Modified: Wed, 06 May 2020 18:21:07 GMT  
		Size: 138.8 MB (138811758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40cd19ea7009328eb44c444ef8b77721ca7ceff1216e8348b397a4d4cc61f92`  
		Last Modified: Wed, 06 May 2020 19:19:44 GMT  
		Size: 13.2 MB (13201842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4eace076c7f04bc8d898d5e0294657505bc22df1bbb00524af505d3ec40b8f5`  
		Last Modified: Wed, 06 May 2020 19:19:38 GMT  
		Size: 725.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6471e355e21673ffffd4105d25f3fc3c7ca903931a7ac72eefb0f1179fe8886`  
		Last Modified: Wed, 06 May 2020 19:19:38 GMT  
		Size: 3.6 KB (3552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5bd825368543e8861f9107d5b2567ec658b743d9b74e264b4f8a59f3947a1a`  
		Last Modified: Wed, 06 May 2020 19:19:38 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be2aa53d065c846a1a65d2d087e160f6ee5364b954fc715b57cdeb47159ee4a`  
		Last Modified: Wed, 06 May 2020 19:19:38 GMT  
		Size: 58.2 KB (58242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13add789a4fbc4be44488757e32a45f603dad4b626bc567e47ae425e3839723c`  
		Last Modified: Wed, 06 May 2020 19:19:38 GMT  
		Size: 4.5 KB (4482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708013d654fabe5cca5909fa3ff477d8fdf4d7b9361d150dd7412fbf0b0dbcec`  
		Last Modified: Wed, 06 May 2020 19:20:09 GMT  
		Size: 187.3 MB (187339307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d4136c5209f637537bea45cf4750d0cddfa9a7d3341805e72672a3f9a0fbdd`  
		Last Modified: Wed, 06 May 2020 19:19:52 GMT  
		Size: 947.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:19.0.0.12-full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:17b58d365bb5fff88031f72ba2f863cadeec9033618d91ac0bc838bbe452a23a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358598528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523763406bf28ce18c2cb5854d7f472fab953e4e32cd5a372c310f13f65c1720`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:57:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 07:57:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:01:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 19:02:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 19:02:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 20:12:38 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=19.0.0.12 org.opencontainers.image.revision=cl191220191120-0300 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 May 2020 20:12:38 GMT
ENV LIBERTY_VERSION=19.0.0_12
# Wed, 06 May 2020 20:12:38 GMT
ARG LIBERTY_URL
# Wed, 06 May 2020 20:12:39 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 May 2020 20:12:49 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 20:12:50 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2020 20:12:50 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=19.0.0.12 BuildLabel=cl191220191120-0300
# Wed, 06 May 2020 20:12:50 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Wed, 06 May 2020 20:12:51 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 06 May 2020 20:12:52 GMT
COPY dir:0d0cedab2fbb7208b9d81afa78e9f15b12b71232224a2fe9753c00b7b72bd72e in /opt/ibm/helpers/ 
# Wed, 06 May 2020 20:12:52 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 06 May 2020 20:12:52 GMT
COPY dir:ac01ddd10295d427b1e05fe08b779c3a46df170405e703dc88e5be095b14c1e4 in /licenses/ 
# Wed, 06 May 2020 20:12:53 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 06 May 2020 20:12:54 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 06 May 2020 20:12:54 GMT
USER 1001
# Wed, 06 May 2020 20:12:54 GMT
EXPOSE 9080 9443
# Wed, 06 May 2020 20:12:54 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 06 May 2020 20:12:55 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 06 May 2020 20:13:01 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 06 May 2020 20:16:14 GMT
# ARGS: REPOSITORIES_PROPERTIES=
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 06 May 2020 20:16:20 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcddcb26914bba3154202a6794cc606bb36373fd4a5954207d25c2acbb21027`  
		Last Modified: Fri, 24 Apr 2020 08:00:28 GMT  
		Size: 2.7 MB (2678829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629705dbca4f2a1136866fdaec045c1f892fffb23cc1ccafc872548ab2f0f07`  
		Last Modified: Wed, 06 May 2020 19:04:43 GMT  
		Size: 127.6 MB (127581919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18d5954dfdf1d5f210e68a5ba400328841608daa92a297b2289ad154cc25c5d`  
		Last Modified: Wed, 06 May 2020 20:19:11 GMT  
		Size: 13.2 MB (13201231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20c8a0f82aff98c4d55fee5da917a6acf54abdef9e349c18edfb8904124a7ef`  
		Last Modified: Wed, 06 May 2020 20:19:01 GMT  
		Size: 720.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8901329e2bd1b1051377ad5ed1e25dc078e821baf04edd63480e557731956da8`  
		Last Modified: Wed, 06 May 2020 20:19:07 GMT  
		Size: 3.5 KB (3547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6400a6f922069227579183553afe05b31302d1248e34d1972800120045a1277d`  
		Last Modified: Wed, 06 May 2020 20:19:02 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1f0980052b87533a3734c8b832d373081186eeac7526532fd5b27523a95bf5`  
		Last Modified: Wed, 06 May 2020 20:19:06 GMT  
		Size: 58.2 KB (58241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8925e9345bf02e1c6ed1e6c82d970f2c823a8be3d2bfa4aa9b2c36554e5e0c1d`  
		Last Modified: Wed, 06 May 2020 20:19:17 GMT  
		Size: 4.5 KB (4464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6e07b864cdea94a19779df192fd3ce1d4da9d774a80287945016758fbd3f76`  
		Last Modified: Wed, 06 May 2020 20:19:35 GMT  
		Size: 189.7 MB (189665813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277ca8456f586fe803872470844687606c365319794087349f0e699db88902ab`  
		Last Modified: Wed, 06 May 2020 20:19:45 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:19.0.0.12-kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:9bd5bacb8cc904d3bb21a4efebcbd25fc40081095f132c36e8effc965ff4537d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:19.0.0.12-kernel-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:4a0e631e7a2c7506af0911cac6adc287e9162941c90c8e05389fce86f9db1462
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173294672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bc79bfe4ab658f56237a777d2126bdecc241db24440498729aefc8f9cb0429`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 14:38:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 14:39:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 17:22:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 17:22:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 17:22:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 19:07:40 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=19.0.0.12 org.opencontainers.image.revision=cl191220191120-0300 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 May 2020 19:07:40 GMT
ENV LIBERTY_VERSION=19.0.0_12
# Wed, 06 May 2020 19:07:40 GMT
ARG LIBERTY_URL
# Wed, 06 May 2020 19:07:40 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 May 2020 19:07:49 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:07:49 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2020 19:07:49 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=19.0.0.12 BuildLabel=cl191220191120-0300
# Wed, 06 May 2020 19:07:49 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Wed, 06 May 2020 19:07:50 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 06 May 2020 19:07:51 GMT
COPY dir:0d0cedab2fbb7208b9d81afa78e9f15b12b71232224a2fe9753c00b7b72bd72e in /opt/ibm/helpers/ 
# Wed, 06 May 2020 19:07:51 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 06 May 2020 19:07:51 GMT
COPY dir:ac01ddd10295d427b1e05fe08b779c3a46df170405e703dc88e5be095b14c1e4 in /licenses/ 
# Wed, 06 May 2020 19:07:52 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 06 May 2020 19:07:52 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 06 May 2020 19:07:52 GMT
USER 1001
# Wed, 06 May 2020 19:07:52 GMT
EXPOSE 9080 9443
# Wed, 06 May 2020 19:07:53 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 06 May 2020 19:07:53 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a528cffcbfa77f36f260d896e265cfb925555d14069b6cb510319dbe87d2e393`  
		Last Modified: Wed, 29 Apr 2020 03:27:55 GMT  
		Size: 3.0 MB (2965011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc65fe0ac24ec55f1cda0e25f07bba60ccd2ee3ff62f7355c9773cf51145e7e0`  
		Last Modified: Wed, 06 May 2020 17:27:06 GMT  
		Size: 130.3 MB (130335315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de57ac949ac66af02e3039eaaaa30e96e93db5aa61008051c894d02686da671`  
		Last Modified: Wed, 13 May 2020 01:51:46 GMT  
		Size: 13.2 MB (13201131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1eb1243a1487158c2191c4d684ae986dabe480d8d849eeae59b96fc07f7628`  
		Last Modified: Wed, 13 May 2020 01:51:41 GMT  
		Size: 675.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39ba719eea17fcc69050adb5012e5276049d975c4301f3ca3c557ca80b08cc3`  
		Last Modified: Wed, 13 May 2020 01:51:42 GMT  
		Size: 3.5 KB (3517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198679892e9c2294d4da3ac7fa2f0d1603ea20913d87ce9b197256ac9f45643e`  
		Last Modified: Wed, 13 May 2020 01:51:42 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3772554407bad00e7751e2931e7f79233e19c8c9fbd9c8c355f66cfd595d3847`  
		Last Modified: Wed, 13 May 2020 01:51:42 GMT  
		Size: 58.2 KB (58241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4ced1987c1e70a3416dea1d5bf320a741ae74aff3292591d9c6f564064725f`  
		Last Modified: Wed, 13 May 2020 01:51:41 GMT  
		Size: 4.4 KB (4357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:19.0.0.12-kernel-java8-ibmjava` - linux; 386

```console
$ docker pull websphere-liberty@sha256:556ac25104eaa8249b0341f3480e79ffd775479afe0b99153d597e78301381d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162201394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89fbfde02b4caea8403d54f780e8f8cc1cdeb4df1117feba7bbde349426ab8b`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 21:17:02 GMT
ADD file:93916d8759465832704c50a78cd4ca1ad83e80baefd96a15563505b3374b8f3c in / 
# Thu, 23 Apr 2020 21:17:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 21:17:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 21:17:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 21:17:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 08:57:23 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 08:57:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 17:38:27 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 17:39:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 17:39:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:04:41 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=19.0.0.12 org.opencontainers.image.revision=cl191220191120-0300 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 May 2020 18:04:41 GMT
ENV LIBERTY_VERSION=19.0.0_12
# Wed, 06 May 2020 18:04:42 GMT
ARG LIBERTY_URL
# Wed, 06 May 2020 18:04:42 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 May 2020 18:04:51 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 18:04:51 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2020 18:04:51 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=19.0.0.12 BuildLabel=cl191220191120-0300
# Wed, 06 May 2020 18:04:51 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Wed, 06 May 2020 18:04:52 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 06 May 2020 18:04:53 GMT
COPY dir:0d0cedab2fbb7208b9d81afa78e9f15b12b71232224a2fe9753c00b7b72bd72e in /opt/ibm/helpers/ 
# Wed, 06 May 2020 18:04:53 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 06 May 2020 18:04:53 GMT
COPY dir:ac01ddd10295d427b1e05fe08b779c3a46df170405e703dc88e5be095b14c1e4 in /licenses/ 
# Wed, 06 May 2020 18:04:54 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 06 May 2020 18:04:54 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 06 May 2020 18:04:54 GMT
USER 1001
# Wed, 06 May 2020 18:04:55 GMT
EXPOSE 9080 9443
# Wed, 06 May 2020 18:04:55 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 06 May 2020 18:04:55 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:32febc939a10ccd7e09d79d3844314e0ddd7186a038a8129711026e33bb52944`  
		Last Modified: Sun, 05 Apr 2020 20:23:59 GMT  
		Size: 27.1 MB (27123063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1172dfcc3d758ff57c194883a4e3f387b056879cb1366a4b6917f0f111b57c0`  
		Last Modified: Thu, 23 Apr 2020 21:17:53 GMT  
		Size: 34.6 KB (34621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cec8eab9aff7ebcd137e82043cc8bce36e7807a6101c176aeecb5f45229468`  
		Last Modified: Thu, 23 Apr 2020 21:17:53 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d2624c94975a0cf9135648d1bfdbbbc91abd34977488f6fb47df8d674c34d8`  
		Last Modified: Thu, 23 Apr 2020 21:17:53 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5c544544748d32930489934c3525b4efcef3711c7af60fb4936333b00963af`  
		Last Modified: Fri, 24 Apr 2020 08:59:58 GMT  
		Size: 3.0 MB (2992510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022dedc8b7eaee6c7517f31d3ce49ee8f3f514f36b4ee146fb366db909bff8bf`  
		Last Modified: Wed, 06 May 2020 17:41:07 GMT  
		Size: 118.8 MB (118781405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6dacff20ca3a6ac8bd76edf36d7bf45521c7b85c437369ba5c2c7e68deed96b`  
		Last Modified: Wed, 06 May 2020 18:08:53 GMT  
		Size: 13.2 MB (13201739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98ffdabe21a7a18827d1669c6d89c6b15dcb48ee6e9ca11c555114e71074ba1`  
		Last Modified: Wed, 06 May 2020 18:08:50 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc123d40644d2f695e51fb4b8c152a73e72f158736917829042f544719852a99`  
		Last Modified: Wed, 06 May 2020 18:08:50 GMT  
		Size: 3.5 KB (3515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fe447588a3b117a914e80e522bfeaa6b9a178d67ad5f179f11ba28850547b0`  
		Last Modified: Wed, 06 May 2020 18:08:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8ff6835007bb9e4272be932a0f587f49f760578dc121d857c3c0ece89dfd06`  
		Last Modified: Wed, 06 May 2020 18:08:51 GMT  
		Size: 58.2 KB (58239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19997b5c67d3fdeb7a8bd95702bb6945e88659dc21c980ebf31492b04c0fcf2a`  
		Last Modified: Wed, 06 May 2020 18:08:50 GMT  
		Size: 4.4 KB (4367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:19.0.0.12-kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:29f31a72e2532f9e879d716d8534a38ce4e7f1f6712b6a2486f860a3945e093b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185610732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8efa4e6a0ab6389c9c9157fe9fbd9b49baeff6c2af41e2970aafa61ab6053d7`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:49:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 11:50:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 18:16:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 18:17:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 18:18:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 19:11:07 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=19.0.0.12 org.opencontainers.image.revision=cl191220191120-0300 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 May 2020 19:11:10 GMT
ENV LIBERTY_VERSION=19.0.0_12
# Wed, 06 May 2020 19:11:14 GMT
ARG LIBERTY_URL
# Wed, 06 May 2020 19:11:18 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 May 2020 19:11:54 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:11:59 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2020 19:12:03 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=19.0.0.12 BuildLabel=cl191220191120-0300
# Wed, 06 May 2020 19:12:07 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Wed, 06 May 2020 19:12:16 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 06 May 2020 19:12:17 GMT
COPY dir:0d0cedab2fbb7208b9d81afa78e9f15b12b71232224a2fe9753c00b7b72bd72e in /opt/ibm/helpers/ 
# Wed, 06 May 2020 19:12:19 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 06 May 2020 19:12:20 GMT
COPY dir:ac01ddd10295d427b1e05fe08b779c3a46df170405e703dc88e5be095b14c1e4 in /licenses/ 
# Wed, 06 May 2020 19:12:28 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 06 May 2020 19:12:33 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 06 May 2020 19:12:35 GMT
USER 1001
# Wed, 06 May 2020 19:12:36 GMT
EXPOSE 9080 9443
# Wed, 06 May 2020 19:12:39 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 06 May 2020 19:12:43 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df114b83a5a3444a39237d52fb0ddee6b46bc18624f26febb7c6a00effacdd4`  
		Last Modified: Fri, 24 Apr 2020 11:54:50 GMT  
		Size: 3.1 MB (3093321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a3df9e59dafede5e9e49376b8d92ca46f947103b310001473fb6ed575cc9c4`  
		Last Modified: Wed, 06 May 2020 18:21:07 GMT  
		Size: 138.8 MB (138811758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40cd19ea7009328eb44c444ef8b77721ca7ceff1216e8348b397a4d4cc61f92`  
		Last Modified: Wed, 06 May 2020 19:19:44 GMT  
		Size: 13.2 MB (13201842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4eace076c7f04bc8d898d5e0294657505bc22df1bbb00524af505d3ec40b8f5`  
		Last Modified: Wed, 06 May 2020 19:19:38 GMT  
		Size: 725.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6471e355e21673ffffd4105d25f3fc3c7ca903931a7ac72eefb0f1179fe8886`  
		Last Modified: Wed, 06 May 2020 19:19:38 GMT  
		Size: 3.6 KB (3552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5bd825368543e8861f9107d5b2567ec658b743d9b74e264b4f8a59f3947a1a`  
		Last Modified: Wed, 06 May 2020 19:19:38 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be2aa53d065c846a1a65d2d087e160f6ee5364b954fc715b57cdeb47159ee4a`  
		Last Modified: Wed, 06 May 2020 19:19:38 GMT  
		Size: 58.2 KB (58242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13add789a4fbc4be44488757e32a45f603dad4b626bc567e47ae425e3839723c`  
		Last Modified: Wed, 06 May 2020 19:19:38 GMT  
		Size: 4.5 KB (4482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:19.0.0.12-kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:71ccc54b20ca7a2c3355b6be31096cf686b33e5b5d69e71986088c4800c7a6e9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168931770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3561111c454ac02b284a94f52a4d56065fc87875930b7a816d5619fd9bdda1a7`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:57:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 07:57:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:01:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 19:02:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 19:02:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 20:12:38 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=19.0.0.12 org.opencontainers.image.revision=cl191220191120-0300 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 May 2020 20:12:38 GMT
ENV LIBERTY_VERSION=19.0.0_12
# Wed, 06 May 2020 20:12:38 GMT
ARG LIBERTY_URL
# Wed, 06 May 2020 20:12:39 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 May 2020 20:12:49 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 20:12:50 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2020 20:12:50 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=19.0.0.12 BuildLabel=cl191220191120-0300
# Wed, 06 May 2020 20:12:50 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Wed, 06 May 2020 20:12:51 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 06 May 2020 20:12:52 GMT
COPY dir:0d0cedab2fbb7208b9d81afa78e9f15b12b71232224a2fe9753c00b7b72bd72e in /opt/ibm/helpers/ 
# Wed, 06 May 2020 20:12:52 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 06 May 2020 20:12:52 GMT
COPY dir:ac01ddd10295d427b1e05fe08b779c3a46df170405e703dc88e5be095b14c1e4 in /licenses/ 
# Wed, 06 May 2020 20:12:53 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 06 May 2020 20:12:54 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 06 May 2020 20:12:54 GMT
USER 1001
# Wed, 06 May 2020 20:12:54 GMT
EXPOSE 9080 9443
# Wed, 06 May 2020 20:12:54 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 06 May 2020 20:12:55 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcddcb26914bba3154202a6794cc606bb36373fd4a5954207d25c2acbb21027`  
		Last Modified: Fri, 24 Apr 2020 08:00:28 GMT  
		Size: 2.7 MB (2678829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629705dbca4f2a1136866fdaec045c1f892fffb23cc1ccafc872548ab2f0f07`  
		Last Modified: Wed, 06 May 2020 19:04:43 GMT  
		Size: 127.6 MB (127581919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18d5954dfdf1d5f210e68a5ba400328841608daa92a297b2289ad154cc25c5d`  
		Last Modified: Wed, 06 May 2020 20:19:11 GMT  
		Size: 13.2 MB (13201231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20c8a0f82aff98c4d55fee5da917a6acf54abdef9e349c18edfb8904124a7ef`  
		Last Modified: Wed, 06 May 2020 20:19:01 GMT  
		Size: 720.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8901329e2bd1b1051377ad5ed1e25dc078e821baf04edd63480e557731956da8`  
		Last Modified: Wed, 06 May 2020 20:19:07 GMT  
		Size: 3.5 KB (3547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6400a6f922069227579183553afe05b31302d1248e34d1972800120045a1277d`  
		Last Modified: Wed, 06 May 2020 20:19:02 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1f0980052b87533a3734c8b832d373081186eeac7526532fd5b27523a95bf5`  
		Last Modified: Wed, 06 May 2020 20:19:06 GMT  
		Size: 58.2 KB (58241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8925e9345bf02e1c6ed1e6c82d970f2c823a8be3d2bfa4aa9b2c36554e5e0c1d`  
		Last Modified: Wed, 06 May 2020 20:19:17 GMT  
		Size: 4.5 KB (4464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:20.0.0.3-full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:3bd6d5bb4d05a202d6cc10504500ad5c4db7e11259bf2cb9fb6604262214d06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:20.0.0.3-full-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:ec8addfd3b0c0cc2a51276f0d6efb5fda721c889a2160ca7b93a341d21be67ba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.5 MB (393502549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c413cd0408b8fc993b42fe481c3d267bb25afa93aca9b5abb5d3df42c3f9c1ca`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 14:38:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 14:39:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 17:22:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 17:22:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 17:22:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:58:38 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 18:58:38 GMT
ARG OPENJ9_SCC=true
# Wed, 06 May 2020 19:03:38 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.3 org.opencontainers.image.revision=cl200320200305-1433 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 May 2020 19:03:38 GMT
ENV LIBERTY_VERSION=20.0.0_03
# Wed, 06 May 2020 19:03:39 GMT
ARG LIBERTY_URL
# Wed, 06 May 2020 19:03:39 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 May 2020 19:03:48 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:03:48 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2020 19:03:49 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.3 BuildLabel=cl200320200305-1433
# Wed, 06 May 2020 19:03:49 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 06 May 2020 19:03:50 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 01:45:18 GMT
COPY dir:9bf54ffdc4f4c7668f2f626dc636555b60354b8e5fb3510b77868c9d2b4b15cd in /opt/ibm/helpers/ 
# Wed, 13 May 2020 01:45:18 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 01:45:18 GMT
COPY dir:9277507d983008afcf8df6e0bfe2735bd4e92717515dbb3a7e268c830f213489 in /licenses/ 
# Wed, 13 May 2020 01:45:19 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 01:45:30 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 01:45:31 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 01:45:31 GMT
USER 1001
# Wed, 13 May 2020 01:45:31 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 01:45:31 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 01:45:31 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 13 May 2020 01:45:36 GMT
ARG VERBOSE=false
# Wed, 13 May 2020 01:45:36 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 13 May 2020 01:48:15 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 13 May 2020 01:48:15 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 13 May 2020 01:48:58 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a528cffcbfa77f36f260d896e265cfb925555d14069b6cb510319dbe87d2e393`  
		Last Modified: Wed, 29 Apr 2020 03:27:55 GMT  
		Size: 3.0 MB (2965011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc65fe0ac24ec55f1cda0e25f07bba60ccd2ee3ff62f7355c9773cf51145e7e0`  
		Last Modified: Wed, 06 May 2020 17:27:06 GMT  
		Size: 130.3 MB (130335315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d8fd65b2cd16f9b23b5c09efdd7d9fbc6ea3b285337cecccfad701b6f532ee`  
		Last Modified: Wed, 13 May 2020 01:50:57 GMT  
		Size: 13.6 MB (13600337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7f551046a24ae12bc3964eab1886d8be1719bbeb044e94cb94ae5c780295f6`  
		Last Modified: Wed, 13 May 2020 01:50:54 GMT  
		Size: 679.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4b61409dbba63a53a475f55c0da4424bcbf5774806f59ed0ddc40efdc9f583`  
		Last Modified: Wed, 13 May 2020 01:50:54 GMT  
		Size: 5.6 KB (5619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949540976af5fafb0916c38c7d2bc7b037a28051e607c8914cb61e2dad86f192`  
		Last Modified: Wed, 13 May 2020 01:50:53 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed18a361ff00d8bef3f7069c2cfbd8e8f1dc25101c2bb354d307659b66af09a`  
		Last Modified: Wed, 13 May 2020 01:50:53 GMT  
		Size: 57.4 KB (57426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a68d527edcd13b08e6cb98989cd746030a41192f419b732483dd06b3f68d9d2`  
		Last Modified: Wed, 13 May 2020 01:50:53 GMT  
		Size: 6.5 KB (6499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5ce5c6b8829d12575ec25e509114d723ef6491008a8459da6942e6dae84b39`  
		Last Modified: Wed, 13 May 2020 01:50:55 GMT  
		Size: 5.6 MB (5608532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cd90e2f1764de77ef27bf503c488a4734f1f50047164848b6be01ad6757915`  
		Last Modified: Wed, 13 May 2020 01:51:36 GMT  
		Size: 192.2 MB (192203409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88adae6700f3f7ba890d32bca3726693200e8a5f263577cccfedc38712b1eec`  
		Last Modified: Wed, 13 May 2020 01:51:02 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c9a8e0be2ed119ba9f10661934017e8f304896b6a0cc9faa41d79b44f1aa5c`  
		Last Modified: Wed, 13 May 2020 01:51:06 GMT  
		Size: 22.0 MB (21992349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.3-full-java8-ibmjava` - linux; 386

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

### `websphere-liberty:20.0.0.3-full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:f65cafe7ddf493fb3f3959997a76458408b0bc993761bea079c32210f33f5354
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.4 MB (401434235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e85e702fc8c8a4109080b508ad0ad43eaddb8d52d7ac1172cce1c36b717fd00`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:49:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 11:50:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 18:16:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 18:17:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 18:18:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:57:25 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 18:57:29 GMT
ARG OPENJ9_SCC=true
# Wed, 06 May 2020 19:04:26 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.3 org.opencontainers.image.revision=cl200320200305-1433 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 May 2020 19:04:27 GMT
ENV LIBERTY_VERSION=20.0.0_03
# Wed, 06 May 2020 19:04:29 GMT
ARG LIBERTY_URL
# Wed, 06 May 2020 19:04:30 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 May 2020 19:04:52 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:04:54 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2020 19:04:55 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.3 BuildLabel=cl200320200305-1433
# Wed, 06 May 2020 19:04:57 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 06 May 2020 19:05:02 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 02:32:48 GMT
COPY dir:9bf54ffdc4f4c7668f2f626dc636555b60354b8e5fb3510b77868c9d2b4b15cd in /opt/ibm/helpers/ 
# Wed, 13 May 2020 02:32:49 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 02:32:49 GMT
COPY dir:9277507d983008afcf8df6e0bfe2735bd4e92717515dbb3a7e268c830f213489 in /licenses/ 
# Wed, 13 May 2020 02:33:01 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 02:33:23 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 02:33:25 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 02:33:27 GMT
USER 1001
# Wed, 13 May 2020 02:33:29 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 02:33:31 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 02:33:34 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 13 May 2020 02:33:41 GMT
ARG VERBOSE=false
# Wed, 13 May 2020 02:33:43 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 13 May 2020 02:40:28 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 13 May 2020 02:40:33 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 13 May 2020 02:41:31 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df114b83a5a3444a39237d52fb0ddee6b46bc18624f26febb7c6a00effacdd4`  
		Last Modified: Fri, 24 Apr 2020 11:54:50 GMT  
		Size: 3.1 MB (3093321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a3df9e59dafede5e9e49376b8d92ca46f947103b310001473fb6ed575cc9c4`  
		Last Modified: Wed, 06 May 2020 18:21:07 GMT  
		Size: 138.8 MB (138811758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2060ca91bb278eae221f1731d67999b95bd2743ce66e712a8206026619ce2d03`  
		Last Modified: Wed, 06 May 2020 19:19:03 GMT  
		Size: 13.6 MB (13600949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1171248e6691c8ab637eaeec2cd617fbb855e29afb89409004759571a113a075`  
		Last Modified: Wed, 06 May 2020 19:18:59 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d741b3c630e08392c94e50b2882ecf54230218cfe1f6b0bf1a4b699919377f8c`  
		Last Modified: Wed, 13 May 2020 02:44:38 GMT  
		Size: 5.7 KB (5654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3606c48c11e5c0a52ff233a24e7ed72f5d51002e1d3bb7424413f7a16a9a98`  
		Last Modified: Wed, 13 May 2020 02:44:38 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4dc66dfe2aa7eca192bdaebafcb3e4950d8268cc0e71a8423f95feecdb9f55`  
		Last Modified: Wed, 13 May 2020 02:44:38 GMT  
		Size: 57.4 KB (57427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63c6a4c2ea8ca8e2f4a27836ce744f14eda97fdb5fd511af13b430fd2e17a91`  
		Last Modified: Wed, 13 May 2020 02:44:37 GMT  
		Size: 6.6 KB (6600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a20becd6acbbd307f870e5658ec87c4373be1fc5566166ea518cef323faad05`  
		Last Modified: Wed, 13 May 2020 02:44:39 GMT  
		Size: 5.1 MB (5126655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41b557e46db443ac9bb2bd62ef338d4f21f28102d1dbf98251fe8389bc0cc3f`  
		Last Modified: Wed, 13 May 2020 02:45:39 GMT  
		Size: 191.7 MB (191730202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760d615569926d6548476e9412593b720f176b15204afdac263ccfe00be72dcc`  
		Last Modified: Wed, 13 May 2020 02:44:46 GMT  
		Size: 952.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1465ec6744da915519482dfab24342038d672c848bfda59a3bbd251fced7042`  
		Last Modified: Wed, 13 May 2020 02:44:50 GMT  
		Size: 18.6 MB (18563193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.3-full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:48e52d1c83f8a1d3a7a478edddef268a75d1570b237f412096bc4f6179132e99
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.9 MB (388885245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba1ab0402dc0cbb9a27bd65d10fa642026a9cdcd38e765e82a579ad7d51d8677`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:57:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 07:57:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:01:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 19:02:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 19:02:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 20:03:05 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 20:03:06 GMT
ARG OPENJ9_SCC=true
# Wed, 06 May 2020 20:07:55 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.3 org.opencontainers.image.revision=cl200320200305-1433 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 May 2020 20:07:56 GMT
ENV LIBERTY_VERSION=20.0.0_03
# Wed, 06 May 2020 20:07:56 GMT
ARG LIBERTY_URL
# Wed, 06 May 2020 20:07:56 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 May 2020 20:08:06 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 20:08:07 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2020 20:08:08 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.3 BuildLabel=cl200320200305-1433
# Wed, 06 May 2020 20:08:08 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 06 May 2020 20:08:09 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 02:09:04 GMT
COPY dir:9bf54ffdc4f4c7668f2f626dc636555b60354b8e5fb3510b77868c9d2b4b15cd in /opt/ibm/helpers/ 
# Wed, 13 May 2020 02:09:04 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 02:09:04 GMT
COPY dir:9277507d983008afcf8df6e0bfe2735bd4e92717515dbb3a7e268c830f213489 in /licenses/ 
# Wed, 13 May 2020 02:09:06 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 02:09:14 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 02:09:15 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 02:09:15 GMT
USER 1001
# Wed, 13 May 2020 02:09:15 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 02:09:15 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 02:09:15 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 13 May 2020 02:09:22 GMT
ARG VERBOSE=false
# Wed, 13 May 2020 02:09:22 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 13 May 2020 02:12:16 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 13 May 2020 02:12:20 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 13 May 2020 02:13:14 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcddcb26914bba3154202a6794cc606bb36373fd4a5954207d25c2acbb21027`  
		Last Modified: Fri, 24 Apr 2020 08:00:28 GMT  
		Size: 2.7 MB (2678829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629705dbca4f2a1136866fdaec045c1f892fffb23cc1ccafc872548ab2f0f07`  
		Last Modified: Wed, 06 May 2020 19:04:43 GMT  
		Size: 127.6 MB (127581919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259b37412ae2c8ee23cb674766278dde99aa86533de548cb85ceae7475d56fe3`  
		Last Modified: Wed, 06 May 2020 20:18:19 GMT  
		Size: 13.6 MB (13600388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b40301cef1e5e466b96f0a61b645f60c041a1c326ca6022d713cfebb9e541bb`  
		Last Modified: Wed, 06 May 2020 20:18:18 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea656b4f5f19be2f5c8b48da01100f6f64fe1edd61c3ebce3c50ce8602c1d26`  
		Last Modified: Wed, 13 May 2020 02:14:49 GMT  
		Size: 5.7 KB (5652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6e798869b8e2ddc89663ade1847a65ddc1cf4276a49f4f413b782ed09ee02d`  
		Last Modified: Wed, 13 May 2020 02:14:48 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fc11b561452e88bb51912d69dfee22d98e83bf8ef98dce50e593966de06b81`  
		Last Modified: Wed, 13 May 2020 02:14:49 GMT  
		Size: 57.4 KB (57426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac27955fb8780af9494ee32d395e4e83f156f9758979d67ce5ad7ceddd882efd`  
		Last Modified: Wed, 13 May 2020 02:14:54 GMT  
		Size: 6.6 KB (6605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59aeee8d41b0d17ab3ace89ebad7d5e5ab923014b289e9aac281d8a7787e3b12`  
		Last Modified: Wed, 13 May 2020 02:14:49 GMT  
		Size: 5.8 MB (5756809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905f15e12ecd946111e227224a8ca76906b259a7c32d538ffc0d77398ceb0313`  
		Last Modified: Wed, 13 May 2020 02:15:19 GMT  
		Size: 192.4 MB (192359954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fba0e6ccb5666307c7fd64feca47bb90577ea33fae491a81f78e9bf840b352b`  
		Last Modified: Wed, 13 May 2020 02:14:57 GMT  
		Size: 950.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa8f15a355217bbbee3779c66ef6a6952154d9ce9992d7d0a6d96cdbd183910`  
		Last Modified: Wed, 13 May 2020 02:15:01 GMT  
		Size: 21.4 MB (21433177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:20.0.0.3-kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:a7b0beb0c6abe04c75bf6d5d7645e6332f6ca8dfda4e49575b8e0ef0b9b921f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:20.0.0.3-kernel-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:10419f2cc34321452811c6ba17475d54cb8e477951b20ac3c89c4e302422a697
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179305843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88fb1022b1c694421f689983396a2250befd862fae22f6044b14369a681480d6`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 14:38:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 14:39:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 17:22:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 17:22:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 17:22:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:58:38 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 18:58:38 GMT
ARG OPENJ9_SCC=true
# Wed, 06 May 2020 19:03:38 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.3 org.opencontainers.image.revision=cl200320200305-1433 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 May 2020 19:03:38 GMT
ENV LIBERTY_VERSION=20.0.0_03
# Wed, 06 May 2020 19:03:39 GMT
ARG LIBERTY_URL
# Wed, 06 May 2020 19:03:39 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 May 2020 19:03:48 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:03:48 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2020 19:03:49 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.3 BuildLabel=cl200320200305-1433
# Wed, 06 May 2020 19:03:49 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 06 May 2020 19:03:50 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 01:45:18 GMT
COPY dir:9bf54ffdc4f4c7668f2f626dc636555b60354b8e5fb3510b77868c9d2b4b15cd in /opt/ibm/helpers/ 
# Wed, 13 May 2020 01:45:18 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 01:45:18 GMT
COPY dir:9277507d983008afcf8df6e0bfe2735bd4e92717515dbb3a7e268c830f213489 in /licenses/ 
# Wed, 13 May 2020 01:45:19 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 01:45:30 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 01:45:31 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 01:45:31 GMT
USER 1001
# Wed, 13 May 2020 01:45:31 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 01:45:31 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 01:45:31 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a528cffcbfa77f36f260d896e265cfb925555d14069b6cb510319dbe87d2e393`  
		Last Modified: Wed, 29 Apr 2020 03:27:55 GMT  
		Size: 3.0 MB (2965011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc65fe0ac24ec55f1cda0e25f07bba60ccd2ee3ff62f7355c9773cf51145e7e0`  
		Last Modified: Wed, 06 May 2020 17:27:06 GMT  
		Size: 130.3 MB (130335315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d8fd65b2cd16f9b23b5c09efdd7d9fbc6ea3b285337cecccfad701b6f532ee`  
		Last Modified: Wed, 13 May 2020 01:50:57 GMT  
		Size: 13.6 MB (13600337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7f551046a24ae12bc3964eab1886d8be1719bbeb044e94cb94ae5c780295f6`  
		Last Modified: Wed, 13 May 2020 01:50:54 GMT  
		Size: 679.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4b61409dbba63a53a475f55c0da4424bcbf5774806f59ed0ddc40efdc9f583`  
		Last Modified: Wed, 13 May 2020 01:50:54 GMT  
		Size: 5.6 KB (5619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949540976af5fafb0916c38c7d2bc7b037a28051e607c8914cb61e2dad86f192`  
		Last Modified: Wed, 13 May 2020 01:50:53 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed18a361ff00d8bef3f7069c2cfbd8e8f1dc25101c2bb354d307659b66af09a`  
		Last Modified: Wed, 13 May 2020 01:50:53 GMT  
		Size: 57.4 KB (57426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a68d527edcd13b08e6cb98989cd746030a41192f419b732483dd06b3f68d9d2`  
		Last Modified: Wed, 13 May 2020 01:50:53 GMT  
		Size: 6.5 KB (6499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5ce5c6b8829d12575ec25e509114d723ef6491008a8459da6942e6dae84b39`  
		Last Modified: Wed, 13 May 2020 01:50:55 GMT  
		Size: 5.6 MB (5608532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.3-kernel-java8-ibmjava` - linux; 386

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

### `websphere-liberty:20.0.0.3-kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:56c6a1f50d8e3a6d37802a4eb7cda6fd856b28a7bf20e7726458c3f028fb5cee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191139888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5183f6e4b328a3c6cbfc202cdf30d671cacb384626cb2b77742a92ce91b5cfb`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:49:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 11:50:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 18:16:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 18:17:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 18:18:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:57:25 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 18:57:29 GMT
ARG OPENJ9_SCC=true
# Wed, 06 May 2020 19:04:26 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.3 org.opencontainers.image.revision=cl200320200305-1433 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 May 2020 19:04:27 GMT
ENV LIBERTY_VERSION=20.0.0_03
# Wed, 06 May 2020 19:04:29 GMT
ARG LIBERTY_URL
# Wed, 06 May 2020 19:04:30 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 May 2020 19:04:52 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:04:54 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2020 19:04:55 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.3 BuildLabel=cl200320200305-1433
# Wed, 06 May 2020 19:04:57 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 06 May 2020 19:05:02 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 02:32:48 GMT
COPY dir:9bf54ffdc4f4c7668f2f626dc636555b60354b8e5fb3510b77868c9d2b4b15cd in /opt/ibm/helpers/ 
# Wed, 13 May 2020 02:32:49 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 02:32:49 GMT
COPY dir:9277507d983008afcf8df6e0bfe2735bd4e92717515dbb3a7e268c830f213489 in /licenses/ 
# Wed, 13 May 2020 02:33:01 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 02:33:23 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 02:33:25 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 02:33:27 GMT
USER 1001
# Wed, 13 May 2020 02:33:29 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 02:33:31 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 02:33:34 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df114b83a5a3444a39237d52fb0ddee6b46bc18624f26febb7c6a00effacdd4`  
		Last Modified: Fri, 24 Apr 2020 11:54:50 GMT  
		Size: 3.1 MB (3093321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a3df9e59dafede5e9e49376b8d92ca46f947103b310001473fb6ed575cc9c4`  
		Last Modified: Wed, 06 May 2020 18:21:07 GMT  
		Size: 138.8 MB (138811758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2060ca91bb278eae221f1731d67999b95bd2743ce66e712a8206026619ce2d03`  
		Last Modified: Wed, 06 May 2020 19:19:03 GMT  
		Size: 13.6 MB (13600949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1171248e6691c8ab637eaeec2cd617fbb855e29afb89409004759571a113a075`  
		Last Modified: Wed, 06 May 2020 19:18:59 GMT  
		Size: 715.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d741b3c630e08392c94e50b2882ecf54230218cfe1f6b0bf1a4b699919377f8c`  
		Last Modified: Wed, 13 May 2020 02:44:38 GMT  
		Size: 5.7 KB (5654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3606c48c11e5c0a52ff233a24e7ed72f5d51002e1d3bb7424413f7a16a9a98`  
		Last Modified: Wed, 13 May 2020 02:44:38 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4dc66dfe2aa7eca192bdaebafcb3e4950d8268cc0e71a8423f95feecdb9f55`  
		Last Modified: Wed, 13 May 2020 02:44:38 GMT  
		Size: 57.4 KB (57427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63c6a4c2ea8ca8e2f4a27836ce744f14eda97fdb5fd511af13b430fd2e17a91`  
		Last Modified: Wed, 13 May 2020 02:44:37 GMT  
		Size: 6.6 KB (6600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a20becd6acbbd307f870e5658ec87c4373be1fc5566166ea518cef323faad05`  
		Last Modified: Wed, 13 May 2020 02:44:39 GMT  
		Size: 5.1 MB (5126655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.3-kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:17859209f78e1d78e4ce83a1fb250e068e3f8c77a06d4790590accdb120c06db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175091164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b1c13295268e1f7745d111f6e7058c4c4515164f1a75ff8bf9edf0986c873c`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:57:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 07:57:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:01:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 19:02:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 19:02:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 20:03:05 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 20:03:06 GMT
ARG OPENJ9_SCC=true
# Wed, 06 May 2020 20:07:55 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.3 org.opencontainers.image.revision=cl200320200305-1433 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 06 May 2020 20:07:56 GMT
ENV LIBERTY_VERSION=20.0.0_03
# Wed, 06 May 2020 20:07:56 GMT
ARG LIBERTY_URL
# Wed, 06 May 2020 20:07:56 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 06 May 2020 20:08:06 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 20:08:07 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2020 20:08:08 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.3 BuildLabel=cl200320200305-1433
# Wed, 06 May 2020 20:08:08 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 06 May 2020 20:08:09 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 02:09:04 GMT
COPY dir:9bf54ffdc4f4c7668f2f626dc636555b60354b8e5fb3510b77868c9d2b4b15cd in /opt/ibm/helpers/ 
# Wed, 13 May 2020 02:09:04 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 02:09:04 GMT
COPY dir:9277507d983008afcf8df6e0bfe2735bd4e92717515dbb3a7e268c830f213489 in /licenses/ 
# Wed, 13 May 2020 02:09:06 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 02:09:14 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 02:09:15 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 02:09:15 GMT
USER 1001
# Wed, 13 May 2020 02:09:15 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 02:09:15 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 02:09:15 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcddcb26914bba3154202a6794cc606bb36373fd4a5954207d25c2acbb21027`  
		Last Modified: Fri, 24 Apr 2020 08:00:28 GMT  
		Size: 2.7 MB (2678829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629705dbca4f2a1136866fdaec045c1f892fffb23cc1ccafc872548ab2f0f07`  
		Last Modified: Wed, 06 May 2020 19:04:43 GMT  
		Size: 127.6 MB (127581919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259b37412ae2c8ee23cb674766278dde99aa86533de548cb85ceae7475d56fe3`  
		Last Modified: Wed, 06 May 2020 20:18:19 GMT  
		Size: 13.6 MB (13600388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b40301cef1e5e466b96f0a61b645f60c041a1c326ca6022d713cfebb9e541bb`  
		Last Modified: Wed, 06 May 2020 20:18:18 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea656b4f5f19be2f5c8b48da01100f6f64fe1edd61c3ebce3c50ce8602c1d26`  
		Last Modified: Wed, 13 May 2020 02:14:49 GMT  
		Size: 5.7 KB (5652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6e798869b8e2ddc89663ade1847a65ddc1cf4276a49f4f413b782ed09ee02d`  
		Last Modified: Wed, 13 May 2020 02:14:48 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fc11b561452e88bb51912d69dfee22d98e83bf8ef98dce50e593966de06b81`  
		Last Modified: Wed, 13 May 2020 02:14:49 GMT  
		Size: 57.4 KB (57426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac27955fb8780af9494ee32d395e4e83f156f9758979d67ce5ad7ceddd882efd`  
		Last Modified: Wed, 13 May 2020 02:14:54 GMT  
		Size: 6.6 KB (6605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59aeee8d41b0d17ab3ace89ebad7d5e5ab923014b289e9aac281d8a7787e3b12`  
		Last Modified: Wed, 13 May 2020 02:14:49 GMT  
		Size: 5.8 MB (5756809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:20.0.0.5-full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:7d44849ae64983c05e8cd54eda11c7de9833eeebf40927747d6b9957f04f48dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:20.0.0.5-full-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:fe80520338636cdd3cf9d458e70c81488ac256cf352d78e81bf3d04eb362cf2b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.4 MB (394438865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f10c0370c9a924dbd2e15ffd4eb123b86cfc2d2eef405a6497d841286c7cfc`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 14:38:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 14:39:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 17:22:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 17:22:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 17:22:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:58:38 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 18:58:38 GMT
ARG OPENJ9_SCC=true
# Wed, 13 May 2020 01:40:48 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.5 org.opencontainers.image.revision=cl200520200429-1655 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 May 2020 01:40:48 GMT
ENV LIBERTY_VERSION=20.0.0_05
# Wed, 13 May 2020 01:40:49 GMT
ARG LIBERTY_URL
# Wed, 13 May 2020 01:40:49 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 May 2020 01:40:57 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 01:40:57 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 01:40:58 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.5 BuildLabel=cl200520200429-1655
# Wed, 13 May 2020 01:40:58 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 May 2020 01:40:59 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 01:40:59 GMT
COPY dir:bb23f4a336cfd1ff1404ca5678fffa89fb2b03183a93be37634e2c00eb179c47 in /opt/ibm/helpers/ 
# Wed, 13 May 2020 01:41:00 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 01:41:00 GMT
COPY dir:666712edd8ef5cc75494f8a2dc944895b0c1ec9b80e66f7bb4de84169066792b in /licenses/ 
# Wed, 13 May 2020 01:41:01 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 01:41:13 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 01:41:13 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 01:41:13 GMT
USER 1001
# Wed, 13 May 2020 01:41:13 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 01:41:14 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 01:41:14 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 13 May 2020 01:41:22 GMT
ARG VERBOSE=false
# Wed, 13 May 2020 01:41:22 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 13 May 2020 01:44:03 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 13 May 2020 01:44:03 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 13 May 2020 01:44:47 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a528cffcbfa77f36f260d896e265cfb925555d14069b6cb510319dbe87d2e393`  
		Last Modified: Wed, 29 Apr 2020 03:27:55 GMT  
		Size: 3.0 MB (2965011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc65fe0ac24ec55f1cda0e25f07bba60ccd2ee3ff62f7355c9773cf51145e7e0`  
		Last Modified: Wed, 06 May 2020 17:27:06 GMT  
		Size: 130.3 MB (130335315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6d4ca5f8bb632c0e80975540d27cbd5093c3d88251220e0f669a6fce7c36ea`  
		Last Modified: Wed, 13 May 2020 01:49:53 GMT  
		Size: 13.6 MB (13597568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723394fd9b1bafaf15079181404a2ea004e0cc0232c2a9de7723e8e8b96e8ca2`  
		Last Modified: Wed, 13 May 2020 01:49:51 GMT  
		Size: 653.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bc471ea1672f3bb39faa09fb14ba48c9170e262b409e902a88695394f786b0`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 6.7 KB (6722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9c6d9083abad2a2df794fec61738a9c29fa783b4db7c4b92500f44ed6f2158`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4518abc222a3a41ebb58c46a1fca9306bce1de9c0aa8af2b2ca364bede51ce`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 57.4 KB (57423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2dedf70964323fdef7a448f65a9edbcbf762a6ba987e24174953b47cfec390`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0d3aa0717ec9b2b85d2fd203a2afceaee8c0dc9607bcdb90af6eb39dfdfb0e`  
		Last Modified: Wed, 13 May 2020 01:49:51 GMT  
		Size: 5.6 MB (5638946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd11762d823ac8d2fc74bf3c9e3d8bd1ef39886c689e8f734042e596d813773`  
		Last Modified: Wed, 13 May 2020 01:50:40 GMT  
		Size: 193.2 MB (193154664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfc65c714cc7e988a03a221b02c1dc4fc6dd36899adfeba3767ade62eabe2c1`  
		Last Modified: Wed, 13 May 2020 01:49:57 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aad094feea9dc08b2515c9025afb6c7d38314cc9c74921f71b4cf610a66c936`  
		Last Modified: Wed, 13 May 2020 01:50:02 GMT  
		Size: 21.9 MB (21947635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.5-full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:8fe4f47d0109890909be739b0c9c00985e999bb867a3a88cc05f46b749476348
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.4 MB (402423057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655dfec18e14221a4edcba51c4163d45acda6ad4092167987cf6641ab72c56dd`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:49:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 11:50:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 18:16:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 18:17:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 18:18:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:57:25 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 18:57:29 GMT
ARG OPENJ9_SCC=true
# Wed, 13 May 2020 02:25:17 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.5 org.opencontainers.image.revision=cl200520200429-1655 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 May 2020 02:25:19 GMT
ENV LIBERTY_VERSION=20.0.0_05
# Wed, 13 May 2020 02:25:23 GMT
ARG LIBERTY_URL
# Wed, 13 May 2020 02:25:26 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 May 2020 02:25:54 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 02:25:57 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 02:26:00 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.5 BuildLabel=cl200520200429-1655
# Wed, 13 May 2020 02:26:02 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 May 2020 02:26:08 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 02:26:10 GMT
COPY dir:bb23f4a336cfd1ff1404ca5678fffa89fb2b03183a93be37634e2c00eb179c47 in /opt/ibm/helpers/ 
# Wed, 13 May 2020 02:26:11 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 02:26:11 GMT
COPY dir:666712edd8ef5cc75494f8a2dc944895b0c1ec9b80e66f7bb4de84169066792b in /licenses/ 
# Wed, 13 May 2020 02:26:18 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 02:26:37 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 02:26:41 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 02:26:42 GMT
USER 1001
# Wed, 13 May 2020 02:26:45 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 02:26:48 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 02:26:50 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 13 May 2020 02:27:00 GMT
ARG VERBOSE=false
# Wed, 13 May 2020 02:27:06 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 13 May 2020 02:30:51 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 13 May 2020 02:30:55 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 13 May 2020 02:31:49 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df114b83a5a3444a39237d52fb0ddee6b46bc18624f26febb7c6a00effacdd4`  
		Last Modified: Fri, 24 Apr 2020 11:54:50 GMT  
		Size: 3.1 MB (3093321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a3df9e59dafede5e9e49376b8d92ca46f947103b310001473fb6ed575cc9c4`  
		Last Modified: Wed, 06 May 2020 18:21:07 GMT  
		Size: 138.8 MB (138811758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03009e7a193af76f04c5ba944a88b4dd9068c7043515fd05548e92f1267119b4`  
		Last Modified: Wed, 13 May 2020 02:43:17 GMT  
		Size: 13.6 MB (13598163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba10b719d7dbe1418741db6d97d13495eb1806f80fbad1b090862cc7b1a27e`  
		Last Modified: Wed, 13 May 2020 02:43:10 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ed01840c95fc2ae00ca4b04aa99eed46226c776b0bedd40664cab6892b9e3`  
		Last Modified: Wed, 13 May 2020 02:43:05 GMT  
		Size: 6.8 KB (6756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcb38b1aafd6805891a5a2d91e97f67d927a1abc8d5eeb15ba0f73407db6028`  
		Last Modified: Wed, 13 May 2020 02:43:04 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7311255d391474821e6ff5aba8d6844bc5c9e2e40471b5dd96bf62ba2405d63`  
		Last Modified: Wed, 13 May 2020 02:43:05 GMT  
		Size: 57.4 KB (57423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4086b9a963efb5453b0fea08bcf7e2929b72c96b01c26a75e664c9f3afa08073`  
		Last Modified: Wed, 13 May 2020 02:43:05 GMT  
		Size: 7.7 KB (7667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10845d30a458cfbc46d86e2e1b648a37e2179fa8b3decaecb2ef008679f1811d`  
		Last Modified: Wed, 13 May 2020 02:43:09 GMT  
		Size: 5.2 MB (5155624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72303d12158105721cb9441a7e5918a46074d1f3ed76abac25d14ab055e64c1a`  
		Last Modified: Wed, 13 May 2020 02:44:11 GMT  
		Size: 192.7 MB (192684182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280d75f103b14e13026d506d16a35f9d836db86d2403695f2036c8814840f73c`  
		Last Modified: Wed, 13 May 2020 02:43:25 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9adb418083c1173fded9536ea2e6e06cbcc9ca7855386742f03c79e473ad719`  
		Last Modified: Wed, 13 May 2020 02:43:29 GMT  
		Size: 18.6 MB (18569720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.5-full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:ba4dce538d791635953cbf049456de94e78499b8f4d431e2f1dff8b828331dc6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 MB (389740191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1734c56e6cabde8493cad01e2115f4277104df41612422df026dac80feb13bed`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:57:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 07:57:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:01:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 19:02:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 19:02:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 20:03:05 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 20:03:06 GMT
ARG OPENJ9_SCC=true
# Wed, 13 May 2020 02:04:17 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.5 org.opencontainers.image.revision=cl200520200429-1655 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 May 2020 02:04:17 GMT
ENV LIBERTY_VERSION=20.0.0_05
# Wed, 13 May 2020 02:04:17 GMT
ARG LIBERTY_URL
# Wed, 13 May 2020 02:04:17 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 May 2020 02:04:28 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 02:04:29 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 02:04:29 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.5 BuildLabel=cl200520200429-1655
# Wed, 13 May 2020 02:04:30 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 May 2020 02:04:31 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 02:04:31 GMT
COPY dir:bb23f4a336cfd1ff1404ca5678fffa89fb2b03183a93be37634e2c00eb179c47 in /opt/ibm/helpers/ 
# Wed, 13 May 2020 02:04:31 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 02:04:32 GMT
COPY dir:666712edd8ef5cc75494f8a2dc944895b0c1ec9b80e66f7bb4de84169066792b in /licenses/ 
# Wed, 13 May 2020 02:04:33 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 02:04:42 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 02:04:43 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 02:04:43 GMT
USER 1001
# Wed, 13 May 2020 02:04:44 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 02:04:44 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 02:04:44 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 13 May 2020 02:04:53 GMT
ARG VERBOSE=false
# Wed, 13 May 2020 02:04:53 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 13 May 2020 02:07:54 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 13 May 2020 02:08:01 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 13 May 2020 02:08:31 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcddcb26914bba3154202a6794cc606bb36373fd4a5954207d25c2acbb21027`  
		Last Modified: Fri, 24 Apr 2020 08:00:28 GMT  
		Size: 2.7 MB (2678829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629705dbca4f2a1136866fdaec045c1f892fffb23cc1ccafc872548ab2f0f07`  
		Last Modified: Wed, 06 May 2020 19:04:43 GMT  
		Size: 127.6 MB (127581919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe801f2b89f9345aadeb354549d0292e450fb0dcb2f05114267dfa41dc17c7b`  
		Last Modified: Wed, 13 May 2020 02:14:07 GMT  
		Size: 13.6 MB (13597693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb074960db033d0fe77cb254530c8fb0f3165054fcd05cb25b48bf46709d934f`  
		Last Modified: Wed, 13 May 2020 02:14:06 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf8ce9ccdeef14be347d4eea0454804c26c05c937050bfe9acedadba6d8ed1d`  
		Last Modified: Wed, 13 May 2020 02:14:05 GMT  
		Size: 6.8 KB (6752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19aae72bbb91e65c36cc465befcbe663afa035418ebd33b67c0691d0045ddc6d`  
		Last Modified: Wed, 13 May 2020 02:14:05 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78cf06b5fdf737a91c52f4e8883e6c49264ca7d67ba4dc52921c740c0f860c5`  
		Last Modified: Wed, 13 May 2020 02:14:10 GMT  
		Size: 57.4 KB (57422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160e16fbd6a9b4d1f8234afbded3916eb1c7a390f1cfbc35bef8fd0795b4de25`  
		Last Modified: Wed, 13 May 2020 02:14:09 GMT  
		Size: 7.7 KB (7657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949d85f370790b38f9728f9bddcfca885a18f077b6f6661c4f70815574ac798a`  
		Last Modified: Wed, 13 May 2020 02:14:06 GMT  
		Size: 5.7 MB (5723545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e762ed76672ad83c89701abd175d24bfe06e4b0e5c981b0b1831be4b08f5059a`  
		Last Modified: Wed, 13 May 2020 02:14:32 GMT  
		Size: 193.2 MB (193249328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b16f76e72b58c13a688821d217bb27bbb5227b1e512f7ebc406336d2165f230`  
		Last Modified: Wed, 13 May 2020 02:14:28 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead0808c72f3a92f87e64e8c2e1dd71387b4a5339a99fd51b5f2e8e41665f3c4`  
		Last Modified: Wed, 13 May 2020 02:14:18 GMT  
		Size: 21.4 MB (21432587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:20.0.0.5-kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:921fdd3639ffe562d8117a45d413cbafe5b3aa4878a793a20877c03ea2ac9953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:20.0.0.5-kernel-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:ae8c5ff28e90dafa3a5111e4116aab94aea4c6a31c2dadda4c5f0aaa4329b1cb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179252858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91bab117b104fa73759aba50398074a7f031c5d404d941d2be279704516df1e`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 14:38:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 14:39:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 17:22:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 17:22:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 17:22:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:58:38 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 18:58:38 GMT
ARG OPENJ9_SCC=true
# Wed, 13 May 2020 01:40:48 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.5 org.opencontainers.image.revision=cl200520200429-1655 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 May 2020 01:40:48 GMT
ENV LIBERTY_VERSION=20.0.0_05
# Wed, 13 May 2020 01:40:49 GMT
ARG LIBERTY_URL
# Wed, 13 May 2020 01:40:49 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 May 2020 01:40:57 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 01:40:57 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 01:40:58 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.5 BuildLabel=cl200520200429-1655
# Wed, 13 May 2020 01:40:58 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 May 2020 01:40:59 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 01:44:55 GMT
COPY dir:ccf022d8efc2d6327df7cbd666e0013e161167b7f53f0df37be2559cc5b3d79d in /opt/ibm/helpers/ 
# Wed, 13 May 2020 01:44:55 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 01:44:55 GMT
COPY dir:666712edd8ef5cc75494f8a2dc944895b0c1ec9b80e66f7bb4de84169066792b in /licenses/ 
# Wed, 13 May 2020 01:44:56 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 01:45:07 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 01:45:07 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 01:45:08 GMT
USER 1001
# Wed, 13 May 2020 01:45:08 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 01:45:08 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 01:45:08 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a528cffcbfa77f36f260d896e265cfb925555d14069b6cb510319dbe87d2e393`  
		Last Modified: Wed, 29 Apr 2020 03:27:55 GMT  
		Size: 3.0 MB (2965011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc65fe0ac24ec55f1cda0e25f07bba60ccd2ee3ff62f7355c9773cf51145e7e0`  
		Last Modified: Wed, 06 May 2020 17:27:06 GMT  
		Size: 130.3 MB (130335315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6d4ca5f8bb632c0e80975540d27cbd5093c3d88251220e0f669a6fce7c36ea`  
		Last Modified: Wed, 13 May 2020 01:49:53 GMT  
		Size: 13.6 MB (13597568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723394fd9b1bafaf15079181404a2ea004e0cc0232c2a9de7723e8e8b96e8ca2`  
		Last Modified: Wed, 13 May 2020 01:49:51 GMT  
		Size: 653.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11349848fb7d8eee8e5f66048a2d9ff6f302eb5cccb66e1d72583140a17919c`  
		Last Modified: Wed, 13 May 2020 01:50:47 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d88d44cd8c48cf2b7e1716ee211cf4dd22660d9592ae9d72fc075404dcb696e`  
		Last Modified: Wed, 13 May 2020 01:50:46 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb0b88bdcb2789f5009a2f650b351e45d5f2fb9a981e4e184753ece0733a0ad`  
		Last Modified: Wed, 13 May 2020 01:50:46 GMT  
		Size: 57.4 KB (57421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6981e3dc05fe87852832636c643f1d75795d7248f92350029a4be0951cc6b2c`  
		Last Modified: Wed, 13 May 2020 01:50:47 GMT  
		Size: 6.5 KB (6473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbf8e2b1ee5162bb4e339c642d6f54cf28d77a1ae985d030b5c53d5bfb358e5`  
		Last Modified: Wed, 13 May 2020 01:50:48 GMT  
		Size: 5.6 MB (5558365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.5-kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:9216824df066b8eb53147786c008ea76bfd190bb13ee629ff901d9acf9bf9071
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191155007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b09c169e2cea261f08487228645ba0d8e59e0c025731ba157469211d9320b9`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:49:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 11:50:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 18:16:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 18:17:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 18:18:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:57:25 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 18:57:29 GMT
ARG OPENJ9_SCC=true
# Wed, 13 May 2020 02:25:17 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.5 org.opencontainers.image.revision=cl200520200429-1655 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 May 2020 02:25:19 GMT
ENV LIBERTY_VERSION=20.0.0_05
# Wed, 13 May 2020 02:25:23 GMT
ARG LIBERTY_URL
# Wed, 13 May 2020 02:25:26 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 May 2020 02:25:54 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 02:25:57 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 02:26:00 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.5 BuildLabel=cl200520200429-1655
# Wed, 13 May 2020 02:26:02 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 May 2020 02:26:08 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 02:32:01 GMT
COPY dir:ccf022d8efc2d6327df7cbd666e0013e161167b7f53f0df37be2559cc5b3d79d in /opt/ibm/helpers/ 
# Wed, 13 May 2020 02:32:03 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 02:32:04 GMT
COPY dir:666712edd8ef5cc75494f8a2dc944895b0c1ec9b80e66f7bb4de84169066792b in /licenses/ 
# Wed, 13 May 2020 02:32:11 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 02:32:28 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 02:32:31 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 02:32:33 GMT
USER 1001
# Wed, 13 May 2020 02:32:36 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 02:32:38 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 02:32:41 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df114b83a5a3444a39237d52fb0ddee6b46bc18624f26febb7c6a00effacdd4`  
		Last Modified: Fri, 24 Apr 2020 11:54:50 GMT  
		Size: 3.1 MB (3093321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a3df9e59dafede5e9e49376b8d92ca46f947103b310001473fb6ed575cc9c4`  
		Last Modified: Wed, 06 May 2020 18:21:07 GMT  
		Size: 138.8 MB (138811758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03009e7a193af76f04c5ba944a88b4dd9068c7043515fd05548e92f1267119b4`  
		Last Modified: Wed, 13 May 2020 02:43:17 GMT  
		Size: 13.6 MB (13598163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba10b719d7dbe1418741db6d97d13495eb1806f80fbad1b090862cc7b1a27e`  
		Last Modified: Wed, 13 May 2020 02:43:10 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150dc4069d5f2827e7f04f4dd6608606750f54b85b4e2dac86d172da5830c7de`  
		Last Modified: Wed, 13 May 2020 02:44:24 GMT  
		Size: 5.7 KB (5653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e4d348d78b2e2c1379326a6450a89e438e969581cfb93ccae5b3de78dcf13b`  
		Last Modified: Wed, 13 May 2020 02:44:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3735b66534f0e2708a78f3f63a78c26e9c6f366cfd26a8a0ab3827a94e156efd`  
		Last Modified: Wed, 13 May 2020 02:44:24 GMT  
		Size: 57.4 KB (57423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f149528a7fb231deee1fd28787ab792ff67afc20cc65155b2fa1499ae876c1`  
		Last Modified: Wed, 13 May 2020 02:44:24 GMT  
		Size: 6.6 KB (6576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae08d5d9014470c37ae3fdad3ffdbceb53104100850e8ec39d691fa7a5d7e612`  
		Last Modified: Wed, 13 May 2020 02:44:26 GMT  
		Size: 5.1 MB (5144616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.5-kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:8a02a71616c39342c45f204e3964c5dbdc24c4b85b56b9ca3618c87dbe21de0f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175075645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a536d124db920542bae6b5c08108fb963a6ab7272acc880f0fd2f78f17042b6`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:57:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 07:57:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:01:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 19:02:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 19:02:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 20:03:05 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 20:03:06 GMT
ARG OPENJ9_SCC=true
# Wed, 13 May 2020 02:04:17 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.5 org.opencontainers.image.revision=cl200520200429-1655 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 May 2020 02:04:17 GMT
ENV LIBERTY_VERSION=20.0.0_05
# Wed, 13 May 2020 02:04:17 GMT
ARG LIBERTY_URL
# Wed, 13 May 2020 02:04:17 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 May 2020 02:04:28 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 02:04:29 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 02:04:29 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.5 BuildLabel=cl200520200429-1655
# Wed, 13 May 2020 02:04:30 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 May 2020 02:04:31 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 02:08:44 GMT
COPY dir:ccf022d8efc2d6327df7cbd666e0013e161167b7f53f0df37be2559cc5b3d79d in /opt/ibm/helpers/ 
# Wed, 13 May 2020 02:08:44 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 02:08:44 GMT
COPY dir:666712edd8ef5cc75494f8a2dc944895b0c1ec9b80e66f7bb4de84169066792b in /licenses/ 
# Wed, 13 May 2020 02:08:46 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 02:08:53 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 02:08:54 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 02:08:54 GMT
USER 1001
# Wed, 13 May 2020 02:08:54 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 02:08:54 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 02:08:55 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcddcb26914bba3154202a6794cc606bb36373fd4a5954207d25c2acbb21027`  
		Last Modified: Fri, 24 Apr 2020 08:00:28 GMT  
		Size: 2.7 MB (2678829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629705dbca4f2a1136866fdaec045c1f892fffb23cc1ccafc872548ab2f0f07`  
		Last Modified: Wed, 06 May 2020 19:04:43 GMT  
		Size: 127.6 MB (127581919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe801f2b89f9345aadeb354549d0292e450fb0dcb2f05114267dfa41dc17c7b`  
		Last Modified: Wed, 13 May 2020 02:14:07 GMT  
		Size: 13.6 MB (13597693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb074960db033d0fe77cb254530c8fb0f3165054fcd05cb25b48bf46709d934f`  
		Last Modified: Wed, 13 May 2020 02:14:06 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96baa59e67c044199fcb8754fcee9ef516105b5a34ccc9cde0fe9b36d6468c6e`  
		Last Modified: Wed, 13 May 2020 02:14:37 GMT  
		Size: 5.7 KB (5652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952f4d3556fccf7eae06aa696ef86c0c47fbff1b4cfc01a826dfc7f5c8afb07f`  
		Last Modified: Wed, 13 May 2020 02:14:43 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91e7a9a1215c407e51ec31d3264b4ce2360c33cb2513d7e62efb87793ec732b`  
		Last Modified: Wed, 13 May 2020 02:14:37 GMT  
		Size: 57.4 KB (57419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b76e8c1f2b42c85bf00235ed08bf417cb2b839a6111be8801453f4b9c058448`  
		Last Modified: Wed, 13 May 2020 02:14:43 GMT  
		Size: 6.6 KB (6568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47070b15bc42540ac83ad8eebeac89e7836e3058bd909fa5bf324b75d1296c15`  
		Last Modified: Wed, 13 May 2020 02:14:39 GMT  
		Size: 5.7 MB (5744054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:beta`

```console
$ docker pull websphere-liberty@sha256:70e6808347af1b908b933518a2e2b445c833c87ef355469f7c66cec86264ed8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:beta` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:31d8a37bdf686b3d44777e56a6a432114aaee304eeb553871374098f53849b43
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260241888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67266e65da444cf16376f8a9fb67dc50f0e6c2398ac4fe569bcace2cfc859bf`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 14:38:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 14:39:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 17:22:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 17:22:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 17:22:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 13 May 2020 01:40:19 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=2020.5.0.0 org.opencontainers.image.revision=cl200520200429-1655
# Wed, 13 May 2020 01:40:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default
# Wed, 13 May 2020 01:40:25 GMT
ENV LIBERTY_VERSION=2020.5.0_0
# Wed, 13 May 2020 01:40:39 GMT
RUN LIBERTY_URL=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 3 | sed -n 's/\s*webProfile7:\s//p' | tr -d '\r')      && echo $LIBERTY_URL     && wget -q $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp-beta.zip     && unzip -q /tmp/wlp-beta.zip -d /opt/ibm     && rm /tmp/wlp-beta.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp
# Wed, 13 May 2020 01:40:39 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 01:40:39 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Wed, 13 May 2020 01:40:41 GMT
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 01:40:41 GMT
COPY file:f1015ab5ca098f3a04cde2e721a2aa35a1ebb2e9f5eb01d378eb2264cff9a268 in /opt/ibm/wlp/usr/servers/defaultServer/ 
# Wed, 13 May 2020 01:40:42 GMT
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 01:40:42 GMT
USER 1001
# Wed, 13 May 2020 01:40:42 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 01:40:42 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a528cffcbfa77f36f260d896e265cfb925555d14069b6cb510319dbe87d2e393`  
		Last Modified: Wed, 29 Apr 2020 03:27:55 GMT  
		Size: 3.0 MB (2965011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc65fe0ac24ec55f1cda0e25f07bba60ccd2ee3ff62f7355c9773cf51145e7e0`  
		Last Modified: Wed, 06 May 2020 17:27:06 GMT  
		Size: 130.3 MB (130335315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41b6529e320b7e5231a982abee71514fdc60730d0d5825e8d62d9685f2fb64c`  
		Last Modified: Wed, 13 May 2020 01:49:22 GMT  
		Size: 377.4 KB (377437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24daadd2f5230cda420c714ed270f9e647d81a44d41278019b448cfba831b3db`  
		Last Modified: Wed, 13 May 2020 01:49:45 GMT  
		Size: 99.8 MB (99835417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a849ce42fc61586534669314a3df15dba31f7e6e8395b351f73e05447d07fb6b`  
		Last Modified: Wed, 13 May 2020 01:49:22 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bc5d69e3a313ae72ce645ff1afef4615522090b88e123f5a32803cc28f2444`  
		Last Modified: Wed, 13 May 2020 01:49:22 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22b08df17a3283094a53632c0267dfd39d4b993d0bcee6e78d6bfcb65b858f0`  
		Last Modified: Wed, 13 May 2020 01:49:22 GMT  
		Size: 916.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:beta` - linux; 386

```console
$ docker pull websphere-liberty@sha256:70d197fa1e65a0541efc0c142afda48a4180577fa6ba6de450bf94a9bb32042c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249136387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa09ba143bc805ed929cadb4787aa281838e1bb5b08b2fc0385ea7bee80aa40c`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 21:17:02 GMT
ADD file:93916d8759465832704c50a78cd4ca1ad83e80baefd96a15563505b3374b8f3c in / 
# Thu, 23 Apr 2020 21:17:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 21:17:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 21:17:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 21:17:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 08:57:23 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 08:57:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 17:38:27 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 17:39:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 17:39:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 13 May 2020 01:40:35 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=2020.5.0.0 org.opencontainers.image.revision=cl200520200429-1655
# Wed, 13 May 2020 01:40:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default
# Wed, 13 May 2020 01:40:43 GMT
ENV LIBERTY_VERSION=2020.5.0_0
# Wed, 13 May 2020 01:40:58 GMT
RUN LIBERTY_URL=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 3 | sed -n 's/\s*webProfile7:\s//p' | tr -d '\r')      && echo $LIBERTY_URL     && wget -q $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp-beta.zip     && unzip -q /tmp/wlp-beta.zip -d /opt/ibm     && rm /tmp/wlp-beta.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp
# Wed, 13 May 2020 01:40:58 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 01:40:59 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Wed, 13 May 2020 01:41:00 GMT
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 01:41:01 GMT
COPY file:f1015ab5ca098f3a04cde2e721a2aa35a1ebb2e9f5eb01d378eb2264cff9a268 in /opt/ibm/wlp/usr/servers/defaultServer/ 
# Wed, 13 May 2020 01:41:02 GMT
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 01:41:02 GMT
USER 1001
# Wed, 13 May 2020 01:41:02 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 01:41:02 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:32febc939a10ccd7e09d79d3844314e0ddd7186a038a8129711026e33bb52944`  
		Last Modified: Sun, 05 Apr 2020 20:23:59 GMT  
		Size: 27.1 MB (27123063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1172dfcc3d758ff57c194883a4e3f387b056879cb1366a4b6917f0f111b57c0`  
		Last Modified: Thu, 23 Apr 2020 21:17:53 GMT  
		Size: 34.6 KB (34621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cec8eab9aff7ebcd137e82043cc8bce36e7807a6101c176aeecb5f45229468`  
		Last Modified: Thu, 23 Apr 2020 21:17:53 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d2624c94975a0cf9135648d1bfdbbbc91abd34977488f6fb47df8d674c34d8`  
		Last Modified: Thu, 23 Apr 2020 21:17:53 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5c544544748d32930489934c3525b4efcef3711c7af60fb4936333b00963af`  
		Last Modified: Fri, 24 Apr 2020 08:59:58 GMT  
		Size: 3.0 MB (2992510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022dedc8b7eaee6c7517f31d3ce49ee8f3f514f36b4ee146fb366db909bff8bf`  
		Last Modified: Wed, 06 May 2020 17:41:07 GMT  
		Size: 118.8 MB (118781405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34b7eb763862a791e5953b93b2ec38d951c98dcdc6c9245243b46e491a49efa`  
		Last Modified: Wed, 13 May 2020 01:42:18 GMT  
		Size: 365.8 KB (365795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833bc0cc10ebcc94e8c5fe28db140f07396fcb3c230ac5fa7c5099eb30d47585`  
		Last Modified: Wed, 13 May 2020 01:42:28 GMT  
		Size: 99.8 MB (99835441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c29dadd9bf44e7ac9a47113142e2bcbe4886c4474af19126230136ddeeba59`  
		Last Modified: Wed, 13 May 2020 01:42:17 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d3058a13876c017005757d87ee20aef58135c8158ac0b8e386d49054061e82`  
		Last Modified: Wed, 13 May 2020 01:42:17 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10269da079c646dfdbf189a0ab71b9ffa284f13beb8ba21266a0c526eea9374e`  
		Last Modified: Wed, 13 May 2020 01:42:17 GMT  
		Size: 919.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:beta` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:398d0443777ab92a68b02ec314e1956fbbf710235630e4775c1b45da323c89a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272584909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bccd3ba9473097b8f33faca3c1b4b3dd3404f788aa7eef1ca9d8031f6e8462`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:49:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 11:50:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 18:16:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 18:17:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 18:18:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 13 May 2020 02:23:36 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=2020.5.0.0 org.opencontainers.image.revision=cl200520200429-1655
# Wed, 13 May 2020 02:24:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default
# Wed, 13 May 2020 02:24:06 GMT
ENV LIBERTY_VERSION=2020.5.0_0
# Wed, 13 May 2020 02:24:31 GMT
RUN LIBERTY_URL=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 3 | sed -n 's/\s*webProfile7:\s//p' | tr -d '\r')      && echo $LIBERTY_URL     && wget -q $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp-beta.zip     && unzip -q /tmp/wlp-beta.zip -d /opt/ibm     && rm /tmp/wlp-beta.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp
# Wed, 13 May 2020 02:24:35 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 02:24:38 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Wed, 13 May 2020 02:24:49 GMT
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 02:24:50 GMT
COPY file:f1015ab5ca098f3a04cde2e721a2aa35a1ebb2e9f5eb01d378eb2264cff9a268 in /opt/ibm/wlp/usr/servers/defaultServer/ 
# Wed, 13 May 2020 02:24:55 GMT
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 02:24:59 GMT
USER 1001
# Wed, 13 May 2020 02:25:05 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 02:25:07 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df114b83a5a3444a39237d52fb0ddee6b46bc18624f26febb7c6a00effacdd4`  
		Last Modified: Fri, 24 Apr 2020 11:54:50 GMT  
		Size: 3.1 MB (3093321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a3df9e59dafede5e9e49376b8d92ca46f947103b310001473fb6ed575cc9c4`  
		Last Modified: Wed, 06 May 2020 18:21:07 GMT  
		Size: 138.8 MB (138811758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2e413e139b34a129d64f9e2cd1f1a4539cf882e611ce047e4a0fbbde384f02`  
		Last Modified: Wed, 13 May 2020 02:42:26 GMT  
		Size: 405.2 KB (405186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99da5d67b30c9b5095baab2480caa9397f0f88372a8ef178cb311b77975e3b1e`  
		Last Modified: Wed, 13 May 2020 02:42:54 GMT  
		Size: 99.8 MB (99835427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc8491febff3f61c44986ec27bf9f4f991fff826337dca198101d2b9531d3c2`  
		Last Modified: Wed, 13 May 2020 02:42:26 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc7eb9c8c71878757896e6b8fffc5e9dab9840a9e4fb93605256f9353bea1b9`  
		Last Modified: Wed, 13 May 2020 02:42:26 GMT  
		Size: 426.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b068d5636924a0bc6c786eeae8903864f2dd3270339cdc87032f6c9a0bf4dd85`  
		Last Modified: Wed, 13 May 2020 02:42:26 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:beta` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:1af44d37ff1438dce2acb2ecadf4ecea97e619dde6ad13f401eb903a9197cf1a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255873262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a1398eef530cd1de057c307a988cf73a8790229d70f466de583d572330cb86`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:57:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 07:57:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:01:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 19:02:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 19:02:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 13 May 2020 02:03:35 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=2020.5.0.0 org.opencontainers.image.revision=cl200520200429-1655
# Wed, 13 May 2020 02:03:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default
# Wed, 13 May 2020 02:03:41 GMT
ENV LIBERTY_VERSION=2020.5.0_0
# Wed, 13 May 2020 02:03:59 GMT
RUN LIBERTY_URL=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 3 | sed -n 's/\s*webProfile7:\s//p' | tr -d '\r')      && echo $LIBERTY_URL     && wget -q $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp-beta.zip     && unzip -q /tmp/wlp-beta.zip -d /opt/ibm     && rm /tmp/wlp-beta.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp
# Wed, 13 May 2020 02:04:03 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 02:04:03 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Wed, 13 May 2020 02:04:06 GMT
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 02:04:06 GMT
COPY file:f1015ab5ca098f3a04cde2e721a2aa35a1ebb2e9f5eb01d378eb2264cff9a268 in /opt/ibm/wlp/usr/servers/defaultServer/ 
# Wed, 13 May 2020 02:04:07 GMT
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 02:04:08 GMT
USER 1001
# Wed, 13 May 2020 02:04:08 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 02:04:08 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcddcb26914bba3154202a6794cc606bb36373fd4a5954207d25c2acbb21027`  
		Last Modified: Fri, 24 Apr 2020 08:00:28 GMT  
		Size: 2.7 MB (2678829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629705dbca4f2a1136866fdaec045c1f892fffb23cc1ccafc872548ab2f0f07`  
		Last Modified: Wed, 06 May 2020 19:04:43 GMT  
		Size: 127.6 MB (127581919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec48944c8effaa6bdc3f8abc55ba56c3cdf4f2ab9a0c035286b5329bb2506ba`  
		Last Modified: Wed, 13 May 2020 02:13:45 GMT  
		Size: 371.9 KB (371898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d47a6ae488cadb70d6170837c6a612c5594cdbab4d58112bfd336d90949fccf`  
		Last Modified: Wed, 13 May 2020 02:13:50 GMT  
		Size: 99.8 MB (99835393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc90eb2a6d68c1c1ec1a12f6bf847592d3a51e21a4a2a69fa803bf148859f93`  
		Last Modified: Wed, 13 May 2020 02:13:50 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb412a71d7a14f650a77389e5c800ab7fcab6a701d6711b8239a846068f78ae3`  
		Last Modified: Wed, 13 May 2020 02:14:00 GMT  
		Size: 425.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115e18104a280c2b3bc581b2f581729f6c6e35f6d181fb9cdcf178310f2041b8`  
		Last Modified: Wed, 13 May 2020 02:13:50 GMT  
		Size: 1.0 KB (1005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:full`

```console
$ docker pull websphere-liberty@sha256:0e10592ae4a7dccdba0a4d9e3814c760e7a1185667c0255922dc4706df483b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:fe80520338636cdd3cf9d458e70c81488ac256cf352d78e81bf3d04eb362cf2b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.4 MB (394438865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f10c0370c9a924dbd2e15ffd4eb123b86cfc2d2eef405a6497d841286c7cfc`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 14:38:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 14:39:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 17:22:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 17:22:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 17:22:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:58:38 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 18:58:38 GMT
ARG OPENJ9_SCC=true
# Wed, 13 May 2020 01:40:48 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.5 org.opencontainers.image.revision=cl200520200429-1655 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 May 2020 01:40:48 GMT
ENV LIBERTY_VERSION=20.0.0_05
# Wed, 13 May 2020 01:40:49 GMT
ARG LIBERTY_URL
# Wed, 13 May 2020 01:40:49 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 May 2020 01:40:57 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 01:40:57 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 01:40:58 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.5 BuildLabel=cl200520200429-1655
# Wed, 13 May 2020 01:40:58 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 May 2020 01:40:59 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 01:40:59 GMT
COPY dir:bb23f4a336cfd1ff1404ca5678fffa89fb2b03183a93be37634e2c00eb179c47 in /opt/ibm/helpers/ 
# Wed, 13 May 2020 01:41:00 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 01:41:00 GMT
COPY dir:666712edd8ef5cc75494f8a2dc944895b0c1ec9b80e66f7bb4de84169066792b in /licenses/ 
# Wed, 13 May 2020 01:41:01 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 01:41:13 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 01:41:13 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 01:41:13 GMT
USER 1001
# Wed, 13 May 2020 01:41:13 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 01:41:14 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 01:41:14 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 13 May 2020 01:41:22 GMT
ARG VERBOSE=false
# Wed, 13 May 2020 01:41:22 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 13 May 2020 01:44:03 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 13 May 2020 01:44:03 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 13 May 2020 01:44:47 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a528cffcbfa77f36f260d896e265cfb925555d14069b6cb510319dbe87d2e393`  
		Last Modified: Wed, 29 Apr 2020 03:27:55 GMT  
		Size: 3.0 MB (2965011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc65fe0ac24ec55f1cda0e25f07bba60ccd2ee3ff62f7355c9773cf51145e7e0`  
		Last Modified: Wed, 06 May 2020 17:27:06 GMT  
		Size: 130.3 MB (130335315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6d4ca5f8bb632c0e80975540d27cbd5093c3d88251220e0f669a6fce7c36ea`  
		Last Modified: Wed, 13 May 2020 01:49:53 GMT  
		Size: 13.6 MB (13597568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723394fd9b1bafaf15079181404a2ea004e0cc0232c2a9de7723e8e8b96e8ca2`  
		Last Modified: Wed, 13 May 2020 01:49:51 GMT  
		Size: 653.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bc471ea1672f3bb39faa09fb14ba48c9170e262b409e902a88695394f786b0`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 6.7 KB (6722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9c6d9083abad2a2df794fec61738a9c29fa783b4db7c4b92500f44ed6f2158`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4518abc222a3a41ebb58c46a1fca9306bce1de9c0aa8af2b2ca364bede51ce`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 57.4 KB (57423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2dedf70964323fdef7a448f65a9edbcbf762a6ba987e24174953b47cfec390`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0d3aa0717ec9b2b85d2fd203a2afceaee8c0dc9607bcdb90af6eb39dfdfb0e`  
		Last Modified: Wed, 13 May 2020 01:49:51 GMT  
		Size: 5.6 MB (5638946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd11762d823ac8d2fc74bf3c9e3d8bd1ef39886c689e8f734042e596d813773`  
		Last Modified: Wed, 13 May 2020 01:50:40 GMT  
		Size: 193.2 MB (193154664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfc65c714cc7e988a03a221b02c1dc4fc6dd36899adfeba3767ade62eabe2c1`  
		Last Modified: Wed, 13 May 2020 01:49:57 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aad094feea9dc08b2515c9025afb6c7d38314cc9c74921f71b4cf610a66c936`  
		Last Modified: Wed, 13 May 2020 01:50:02 GMT  
		Size: 21.9 MB (21947635 bytes)  
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
$ docker pull websphere-liberty@sha256:8fe4f47d0109890909be739b0c9c00985e999bb867a3a88cc05f46b749476348
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.4 MB (402423057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655dfec18e14221a4edcba51c4163d45acda6ad4092167987cf6641ab72c56dd`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:49:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 11:50:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 18:16:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 18:17:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 18:18:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:57:25 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 18:57:29 GMT
ARG OPENJ9_SCC=true
# Wed, 13 May 2020 02:25:17 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.5 org.opencontainers.image.revision=cl200520200429-1655 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 May 2020 02:25:19 GMT
ENV LIBERTY_VERSION=20.0.0_05
# Wed, 13 May 2020 02:25:23 GMT
ARG LIBERTY_URL
# Wed, 13 May 2020 02:25:26 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 May 2020 02:25:54 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 02:25:57 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 02:26:00 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.5 BuildLabel=cl200520200429-1655
# Wed, 13 May 2020 02:26:02 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 May 2020 02:26:08 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 02:26:10 GMT
COPY dir:bb23f4a336cfd1ff1404ca5678fffa89fb2b03183a93be37634e2c00eb179c47 in /opt/ibm/helpers/ 
# Wed, 13 May 2020 02:26:11 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 02:26:11 GMT
COPY dir:666712edd8ef5cc75494f8a2dc944895b0c1ec9b80e66f7bb4de84169066792b in /licenses/ 
# Wed, 13 May 2020 02:26:18 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 02:26:37 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 02:26:41 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 02:26:42 GMT
USER 1001
# Wed, 13 May 2020 02:26:45 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 02:26:48 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 02:26:50 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 13 May 2020 02:27:00 GMT
ARG VERBOSE=false
# Wed, 13 May 2020 02:27:06 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 13 May 2020 02:30:51 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 13 May 2020 02:30:55 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 13 May 2020 02:31:49 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df114b83a5a3444a39237d52fb0ddee6b46bc18624f26febb7c6a00effacdd4`  
		Last Modified: Fri, 24 Apr 2020 11:54:50 GMT  
		Size: 3.1 MB (3093321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a3df9e59dafede5e9e49376b8d92ca46f947103b310001473fb6ed575cc9c4`  
		Last Modified: Wed, 06 May 2020 18:21:07 GMT  
		Size: 138.8 MB (138811758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03009e7a193af76f04c5ba944a88b4dd9068c7043515fd05548e92f1267119b4`  
		Last Modified: Wed, 13 May 2020 02:43:17 GMT  
		Size: 13.6 MB (13598163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba10b719d7dbe1418741db6d97d13495eb1806f80fbad1b090862cc7b1a27e`  
		Last Modified: Wed, 13 May 2020 02:43:10 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ed01840c95fc2ae00ca4b04aa99eed46226c776b0bedd40664cab6892b9e3`  
		Last Modified: Wed, 13 May 2020 02:43:05 GMT  
		Size: 6.8 KB (6756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcb38b1aafd6805891a5a2d91e97f67d927a1abc8d5eeb15ba0f73407db6028`  
		Last Modified: Wed, 13 May 2020 02:43:04 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7311255d391474821e6ff5aba8d6844bc5c9e2e40471b5dd96bf62ba2405d63`  
		Last Modified: Wed, 13 May 2020 02:43:05 GMT  
		Size: 57.4 KB (57423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4086b9a963efb5453b0fea08bcf7e2929b72c96b01c26a75e664c9f3afa08073`  
		Last Modified: Wed, 13 May 2020 02:43:05 GMT  
		Size: 7.7 KB (7667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10845d30a458cfbc46d86e2e1b648a37e2179fa8b3decaecb2ef008679f1811d`  
		Last Modified: Wed, 13 May 2020 02:43:09 GMT  
		Size: 5.2 MB (5155624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72303d12158105721cb9441a7e5918a46074d1f3ed76abac25d14ab055e64c1a`  
		Last Modified: Wed, 13 May 2020 02:44:11 GMT  
		Size: 192.7 MB (192684182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280d75f103b14e13026d506d16a35f9d836db86d2403695f2036c8814840f73c`  
		Last Modified: Wed, 13 May 2020 02:43:25 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9adb418083c1173fded9536ea2e6e06cbcc9ca7855386742f03c79e473ad719`  
		Last Modified: Wed, 13 May 2020 02:43:29 GMT  
		Size: 18.6 MB (18569720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:ba4dce538d791635953cbf049456de94e78499b8f4d431e2f1dff8b828331dc6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 MB (389740191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1734c56e6cabde8493cad01e2115f4277104df41612422df026dac80feb13bed`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:57:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 07:57:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:01:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 19:02:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 19:02:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 20:03:05 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 20:03:06 GMT
ARG OPENJ9_SCC=true
# Wed, 13 May 2020 02:04:17 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.5 org.opencontainers.image.revision=cl200520200429-1655 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 May 2020 02:04:17 GMT
ENV LIBERTY_VERSION=20.0.0_05
# Wed, 13 May 2020 02:04:17 GMT
ARG LIBERTY_URL
# Wed, 13 May 2020 02:04:17 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 May 2020 02:04:28 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 02:04:29 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 02:04:29 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.5 BuildLabel=cl200520200429-1655
# Wed, 13 May 2020 02:04:30 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 May 2020 02:04:31 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 02:04:31 GMT
COPY dir:bb23f4a336cfd1ff1404ca5678fffa89fb2b03183a93be37634e2c00eb179c47 in /opt/ibm/helpers/ 
# Wed, 13 May 2020 02:04:31 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 02:04:32 GMT
COPY dir:666712edd8ef5cc75494f8a2dc944895b0c1ec9b80e66f7bb4de84169066792b in /licenses/ 
# Wed, 13 May 2020 02:04:33 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 02:04:42 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 02:04:43 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 02:04:43 GMT
USER 1001
# Wed, 13 May 2020 02:04:44 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 02:04:44 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 02:04:44 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 13 May 2020 02:04:53 GMT
ARG VERBOSE=false
# Wed, 13 May 2020 02:04:53 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 13 May 2020 02:07:54 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 13 May 2020 02:08:01 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 13 May 2020 02:08:31 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcddcb26914bba3154202a6794cc606bb36373fd4a5954207d25c2acbb21027`  
		Last Modified: Fri, 24 Apr 2020 08:00:28 GMT  
		Size: 2.7 MB (2678829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629705dbca4f2a1136866fdaec045c1f892fffb23cc1ccafc872548ab2f0f07`  
		Last Modified: Wed, 06 May 2020 19:04:43 GMT  
		Size: 127.6 MB (127581919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe801f2b89f9345aadeb354549d0292e450fb0dcb2f05114267dfa41dc17c7b`  
		Last Modified: Wed, 13 May 2020 02:14:07 GMT  
		Size: 13.6 MB (13597693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb074960db033d0fe77cb254530c8fb0f3165054fcd05cb25b48bf46709d934f`  
		Last Modified: Wed, 13 May 2020 02:14:06 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf8ce9ccdeef14be347d4eea0454804c26c05c937050bfe9acedadba6d8ed1d`  
		Last Modified: Wed, 13 May 2020 02:14:05 GMT  
		Size: 6.8 KB (6752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19aae72bbb91e65c36cc465befcbe663afa035418ebd33b67c0691d0045ddc6d`  
		Last Modified: Wed, 13 May 2020 02:14:05 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78cf06b5fdf737a91c52f4e8883e6c49264ca7d67ba4dc52921c740c0f860c5`  
		Last Modified: Wed, 13 May 2020 02:14:10 GMT  
		Size: 57.4 KB (57422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160e16fbd6a9b4d1f8234afbded3916eb1c7a390f1cfbc35bef8fd0795b4de25`  
		Last Modified: Wed, 13 May 2020 02:14:09 GMT  
		Size: 7.7 KB (7657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949d85f370790b38f9728f9bddcfca885a18f077b6f6661c4f70815574ac798a`  
		Last Modified: Wed, 13 May 2020 02:14:06 GMT  
		Size: 5.7 MB (5723545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e762ed76672ad83c89701abd175d24bfe06e4b0e5c981b0b1831be4b08f5059a`  
		Last Modified: Wed, 13 May 2020 02:14:32 GMT  
		Size: 193.2 MB (193249328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b16f76e72b58c13a688821d217bb27bbb5227b1e512f7ebc406336d2165f230`  
		Last Modified: Wed, 13 May 2020 02:14:28 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead0808c72f3a92f87e64e8c2e1dd71387b4a5339a99fd51b5f2e8e41665f3c4`  
		Last Modified: Wed, 13 May 2020 02:14:18 GMT  
		Size: 21.4 MB (21432587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:d319d7331660734e602a4162c01e1887687b3f6da25cdc2840e9455eedd3dbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:kernel` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:c4e4967dc9add09e1dc9168c2f3d2fccd6731bae5a28f48eefc0cee96b7aaaf5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179335624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5627435747f905d4176a02a88d1ea9a515badef1ac075ebea32be80c3c250ce9`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 14:38:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 14:39:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 17:22:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 17:22:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 17:22:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:58:38 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 18:58:38 GMT
ARG OPENJ9_SCC=true
# Wed, 13 May 2020 01:40:48 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.5 org.opencontainers.image.revision=cl200520200429-1655 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 May 2020 01:40:48 GMT
ENV LIBERTY_VERSION=20.0.0_05
# Wed, 13 May 2020 01:40:49 GMT
ARG LIBERTY_URL
# Wed, 13 May 2020 01:40:49 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 May 2020 01:40:57 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 01:40:57 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 01:40:58 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.5 BuildLabel=cl200520200429-1655
# Wed, 13 May 2020 01:40:58 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 May 2020 01:40:59 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 01:40:59 GMT
COPY dir:bb23f4a336cfd1ff1404ca5678fffa89fb2b03183a93be37634e2c00eb179c47 in /opt/ibm/helpers/ 
# Wed, 13 May 2020 01:41:00 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 01:41:00 GMT
COPY dir:666712edd8ef5cc75494f8a2dc944895b0c1ec9b80e66f7bb4de84169066792b in /licenses/ 
# Wed, 13 May 2020 01:41:01 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 01:41:13 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 01:41:13 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 01:41:13 GMT
USER 1001
# Wed, 13 May 2020 01:41:13 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 01:41:14 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 01:41:14 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a528cffcbfa77f36f260d896e265cfb925555d14069b6cb510319dbe87d2e393`  
		Last Modified: Wed, 29 Apr 2020 03:27:55 GMT  
		Size: 3.0 MB (2965011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc65fe0ac24ec55f1cda0e25f07bba60ccd2ee3ff62f7355c9773cf51145e7e0`  
		Last Modified: Wed, 06 May 2020 17:27:06 GMT  
		Size: 130.3 MB (130335315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6d4ca5f8bb632c0e80975540d27cbd5093c3d88251220e0f669a6fce7c36ea`  
		Last Modified: Wed, 13 May 2020 01:49:53 GMT  
		Size: 13.6 MB (13597568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723394fd9b1bafaf15079181404a2ea004e0cc0232c2a9de7723e8e8b96e8ca2`  
		Last Modified: Wed, 13 May 2020 01:49:51 GMT  
		Size: 653.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bc471ea1672f3bb39faa09fb14ba48c9170e262b409e902a88695394f786b0`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 6.7 KB (6722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9c6d9083abad2a2df794fec61738a9c29fa783b4db7c4b92500f44ed6f2158`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4518abc222a3a41ebb58c46a1fca9306bce1de9c0aa8af2b2ca364bede51ce`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 57.4 KB (57423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2dedf70964323fdef7a448f65a9edbcbf762a6ba987e24174953b47cfec390`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0d3aa0717ec9b2b85d2fd203a2afceaee8c0dc9607bcdb90af6eb39dfdfb0e`  
		Last Modified: Wed, 13 May 2020 01:49:51 GMT  
		Size: 5.6 MB (5638946 bytes)  
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
$ docker pull websphere-liberty@sha256:1c8e0b6667bc3601fdc8c43e5ea053aa1a72b40660f4491543216d5aaf87e5d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191168210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7714c7550e477477ca52f770f359e80c66ee4e79debb6ac675a5f944c73f7252`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:49:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 11:50:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 18:16:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 18:17:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 18:18:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:57:25 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 18:57:29 GMT
ARG OPENJ9_SCC=true
# Wed, 13 May 2020 02:25:17 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.5 org.opencontainers.image.revision=cl200520200429-1655 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 May 2020 02:25:19 GMT
ENV LIBERTY_VERSION=20.0.0_05
# Wed, 13 May 2020 02:25:23 GMT
ARG LIBERTY_URL
# Wed, 13 May 2020 02:25:26 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 May 2020 02:25:54 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 02:25:57 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 02:26:00 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.5 BuildLabel=cl200520200429-1655
# Wed, 13 May 2020 02:26:02 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 May 2020 02:26:08 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 02:26:10 GMT
COPY dir:bb23f4a336cfd1ff1404ca5678fffa89fb2b03183a93be37634e2c00eb179c47 in /opt/ibm/helpers/ 
# Wed, 13 May 2020 02:26:11 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 02:26:11 GMT
COPY dir:666712edd8ef5cc75494f8a2dc944895b0c1ec9b80e66f7bb4de84169066792b in /licenses/ 
# Wed, 13 May 2020 02:26:18 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 02:26:37 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 02:26:41 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 02:26:42 GMT
USER 1001
# Wed, 13 May 2020 02:26:45 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 02:26:48 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 02:26:50 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df114b83a5a3444a39237d52fb0ddee6b46bc18624f26febb7c6a00effacdd4`  
		Last Modified: Fri, 24 Apr 2020 11:54:50 GMT  
		Size: 3.1 MB (3093321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a3df9e59dafede5e9e49376b8d92ca46f947103b310001473fb6ed575cc9c4`  
		Last Modified: Wed, 06 May 2020 18:21:07 GMT  
		Size: 138.8 MB (138811758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03009e7a193af76f04c5ba944a88b4dd9068c7043515fd05548e92f1267119b4`  
		Last Modified: Wed, 13 May 2020 02:43:17 GMT  
		Size: 13.6 MB (13598163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba10b719d7dbe1418741db6d97d13495eb1806f80fbad1b090862cc7b1a27e`  
		Last Modified: Wed, 13 May 2020 02:43:10 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ed01840c95fc2ae00ca4b04aa99eed46226c776b0bedd40664cab6892b9e3`  
		Last Modified: Wed, 13 May 2020 02:43:05 GMT  
		Size: 6.8 KB (6756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcb38b1aafd6805891a5a2d91e97f67d927a1abc8d5eeb15ba0f73407db6028`  
		Last Modified: Wed, 13 May 2020 02:43:04 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7311255d391474821e6ff5aba8d6844bc5c9e2e40471b5dd96bf62ba2405d63`  
		Last Modified: Wed, 13 May 2020 02:43:05 GMT  
		Size: 57.4 KB (57423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4086b9a963efb5453b0fea08bcf7e2929b72c96b01c26a75e664c9f3afa08073`  
		Last Modified: Wed, 13 May 2020 02:43:05 GMT  
		Size: 7.7 KB (7667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10845d30a458cfbc46d86e2e1b648a37e2179fa8b3decaecb2ef008679f1811d`  
		Last Modified: Wed, 13 May 2020 02:43:09 GMT  
		Size: 5.2 MB (5155624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:17ad53f6e73154f07f7d62b27b65207e3dd08c181d788c62e15813be75ca9054
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175057327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff8cf332833514b77a40c245be412aa8e54ab2f2e7e6ee72a38333702324d69`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:57:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 07:57:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:01:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 19:02:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 19:02:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 20:03:05 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 20:03:06 GMT
ARG OPENJ9_SCC=true
# Wed, 13 May 2020 02:04:17 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.5 org.opencontainers.image.revision=cl200520200429-1655 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 May 2020 02:04:17 GMT
ENV LIBERTY_VERSION=20.0.0_05
# Wed, 13 May 2020 02:04:17 GMT
ARG LIBERTY_URL
# Wed, 13 May 2020 02:04:17 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 May 2020 02:04:28 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 02:04:29 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 02:04:29 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.5 BuildLabel=cl200520200429-1655
# Wed, 13 May 2020 02:04:30 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 May 2020 02:04:31 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 02:04:31 GMT
COPY dir:bb23f4a336cfd1ff1404ca5678fffa89fb2b03183a93be37634e2c00eb179c47 in /opt/ibm/helpers/ 
# Wed, 13 May 2020 02:04:31 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 02:04:32 GMT
COPY dir:666712edd8ef5cc75494f8a2dc944895b0c1ec9b80e66f7bb4de84169066792b in /licenses/ 
# Wed, 13 May 2020 02:04:33 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 02:04:42 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 02:04:43 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 02:04:43 GMT
USER 1001
# Wed, 13 May 2020 02:04:44 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 02:04:44 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 02:04:44 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcddcb26914bba3154202a6794cc606bb36373fd4a5954207d25c2acbb21027`  
		Last Modified: Fri, 24 Apr 2020 08:00:28 GMT  
		Size: 2.7 MB (2678829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629705dbca4f2a1136866fdaec045c1f892fffb23cc1ccafc872548ab2f0f07`  
		Last Modified: Wed, 06 May 2020 19:04:43 GMT  
		Size: 127.6 MB (127581919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe801f2b89f9345aadeb354549d0292e450fb0dcb2f05114267dfa41dc17c7b`  
		Last Modified: Wed, 13 May 2020 02:14:07 GMT  
		Size: 13.6 MB (13597693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb074960db033d0fe77cb254530c8fb0f3165054fcd05cb25b48bf46709d934f`  
		Last Modified: Wed, 13 May 2020 02:14:06 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf8ce9ccdeef14be347d4eea0454804c26c05c937050bfe9acedadba6d8ed1d`  
		Last Modified: Wed, 13 May 2020 02:14:05 GMT  
		Size: 6.8 KB (6752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19aae72bbb91e65c36cc465befcbe663afa035418ebd33b67c0691d0045ddc6d`  
		Last Modified: Wed, 13 May 2020 02:14:05 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78cf06b5fdf737a91c52f4e8883e6c49264ca7d67ba4dc52921c740c0f860c5`  
		Last Modified: Wed, 13 May 2020 02:14:10 GMT  
		Size: 57.4 KB (57422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160e16fbd6a9b4d1f8234afbded3916eb1c7a390f1cfbc35bef8fd0795b4de25`  
		Last Modified: Wed, 13 May 2020 02:14:09 GMT  
		Size: 7.7 KB (7657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949d85f370790b38f9728f9bddcfca885a18f077b6f6661c4f70815574ac798a`  
		Last Modified: Wed, 13 May 2020 02:14:06 GMT  
		Size: 5.7 MB (5723545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:latest`

```console
$ docker pull websphere-liberty@sha256:0e10592ae4a7dccdba0a4d9e3814c760e7a1185667c0255922dc4706df483b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:latest` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:fe80520338636cdd3cf9d458e70c81488ac256cf352d78e81bf3d04eb362cf2b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.4 MB (394438865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f10c0370c9a924dbd2e15ffd4eb123b86cfc2d2eef405a6497d841286c7cfc`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 14:38:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 14:39:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 17:22:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 17:22:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 17:22:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:58:38 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 18:58:38 GMT
ARG OPENJ9_SCC=true
# Wed, 13 May 2020 01:40:48 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.5 org.opencontainers.image.revision=cl200520200429-1655 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 May 2020 01:40:48 GMT
ENV LIBERTY_VERSION=20.0.0_05
# Wed, 13 May 2020 01:40:49 GMT
ARG LIBERTY_URL
# Wed, 13 May 2020 01:40:49 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 May 2020 01:40:57 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 01:40:57 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 01:40:58 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.5 BuildLabel=cl200520200429-1655
# Wed, 13 May 2020 01:40:58 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 May 2020 01:40:59 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 01:40:59 GMT
COPY dir:bb23f4a336cfd1ff1404ca5678fffa89fb2b03183a93be37634e2c00eb179c47 in /opt/ibm/helpers/ 
# Wed, 13 May 2020 01:41:00 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 01:41:00 GMT
COPY dir:666712edd8ef5cc75494f8a2dc944895b0c1ec9b80e66f7bb4de84169066792b in /licenses/ 
# Wed, 13 May 2020 01:41:01 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 01:41:13 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 01:41:13 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 01:41:13 GMT
USER 1001
# Wed, 13 May 2020 01:41:13 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 01:41:14 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 01:41:14 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 13 May 2020 01:41:22 GMT
ARG VERBOSE=false
# Wed, 13 May 2020 01:41:22 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 13 May 2020 01:44:03 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 13 May 2020 01:44:03 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 13 May 2020 01:44:47 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a528cffcbfa77f36f260d896e265cfb925555d14069b6cb510319dbe87d2e393`  
		Last Modified: Wed, 29 Apr 2020 03:27:55 GMT  
		Size: 3.0 MB (2965011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc65fe0ac24ec55f1cda0e25f07bba60ccd2ee3ff62f7355c9773cf51145e7e0`  
		Last Modified: Wed, 06 May 2020 17:27:06 GMT  
		Size: 130.3 MB (130335315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6d4ca5f8bb632c0e80975540d27cbd5093c3d88251220e0f669a6fce7c36ea`  
		Last Modified: Wed, 13 May 2020 01:49:53 GMT  
		Size: 13.6 MB (13597568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723394fd9b1bafaf15079181404a2ea004e0cc0232c2a9de7723e8e8b96e8ca2`  
		Last Modified: Wed, 13 May 2020 01:49:51 GMT  
		Size: 653.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bc471ea1672f3bb39faa09fb14ba48c9170e262b409e902a88695394f786b0`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 6.7 KB (6722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9c6d9083abad2a2df794fec61738a9c29fa783b4db7c4b92500f44ed6f2158`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4518abc222a3a41ebb58c46a1fca9306bce1de9c0aa8af2b2ca364bede51ce`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 57.4 KB (57423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2dedf70964323fdef7a448f65a9edbcbf762a6ba987e24174953b47cfec390`  
		Last Modified: Wed, 13 May 2020 01:49:50 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0d3aa0717ec9b2b85d2fd203a2afceaee8c0dc9607bcdb90af6eb39dfdfb0e`  
		Last Modified: Wed, 13 May 2020 01:49:51 GMT  
		Size: 5.6 MB (5638946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd11762d823ac8d2fc74bf3c9e3d8bd1ef39886c689e8f734042e596d813773`  
		Last Modified: Wed, 13 May 2020 01:50:40 GMT  
		Size: 193.2 MB (193154664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfc65c714cc7e988a03a221b02c1dc4fc6dd36899adfeba3767ade62eabe2c1`  
		Last Modified: Wed, 13 May 2020 01:49:57 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aad094feea9dc08b2515c9025afb6c7d38314cc9c74921f71b4cf610a66c936`  
		Last Modified: Wed, 13 May 2020 01:50:02 GMT  
		Size: 21.9 MB (21947635 bytes)  
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
$ docker pull websphere-liberty@sha256:8fe4f47d0109890909be739b0c9c00985e999bb867a3a88cc05f46b749476348
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.4 MB (402423057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655dfec18e14221a4edcba51c4163d45acda6ad4092167987cf6641ab72c56dd`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:49:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 11:50:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 18:16:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 18:17:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 18:18:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 18:57:25 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 18:57:29 GMT
ARG OPENJ9_SCC=true
# Wed, 13 May 2020 02:25:17 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.5 org.opencontainers.image.revision=cl200520200429-1655 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 May 2020 02:25:19 GMT
ENV LIBERTY_VERSION=20.0.0_05
# Wed, 13 May 2020 02:25:23 GMT
ARG LIBERTY_URL
# Wed, 13 May 2020 02:25:26 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 May 2020 02:25:54 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 02:25:57 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 02:26:00 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.5 BuildLabel=cl200520200429-1655
# Wed, 13 May 2020 02:26:02 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 May 2020 02:26:08 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 02:26:10 GMT
COPY dir:bb23f4a336cfd1ff1404ca5678fffa89fb2b03183a93be37634e2c00eb179c47 in /opt/ibm/helpers/ 
# Wed, 13 May 2020 02:26:11 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 02:26:11 GMT
COPY dir:666712edd8ef5cc75494f8a2dc944895b0c1ec9b80e66f7bb4de84169066792b in /licenses/ 
# Wed, 13 May 2020 02:26:18 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 02:26:37 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 02:26:41 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 02:26:42 GMT
USER 1001
# Wed, 13 May 2020 02:26:45 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 02:26:48 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 02:26:50 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 13 May 2020 02:27:00 GMT
ARG VERBOSE=false
# Wed, 13 May 2020 02:27:06 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 13 May 2020 02:30:51 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 13 May 2020 02:30:55 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 13 May 2020 02:31:49 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df114b83a5a3444a39237d52fb0ddee6b46bc18624f26febb7c6a00effacdd4`  
		Last Modified: Fri, 24 Apr 2020 11:54:50 GMT  
		Size: 3.1 MB (3093321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a3df9e59dafede5e9e49376b8d92ca46f947103b310001473fb6ed575cc9c4`  
		Last Modified: Wed, 06 May 2020 18:21:07 GMT  
		Size: 138.8 MB (138811758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03009e7a193af76f04c5ba944a88b4dd9068c7043515fd05548e92f1267119b4`  
		Last Modified: Wed, 13 May 2020 02:43:17 GMT  
		Size: 13.6 MB (13598163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ba10b719d7dbe1418741db6d97d13495eb1806f80fbad1b090862cc7b1a27e`  
		Last Modified: Wed, 13 May 2020 02:43:10 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ed01840c95fc2ae00ca4b04aa99eed46226c776b0bedd40664cab6892b9e3`  
		Last Modified: Wed, 13 May 2020 02:43:05 GMT  
		Size: 6.8 KB (6756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcb38b1aafd6805891a5a2d91e97f67d927a1abc8d5eeb15ba0f73407db6028`  
		Last Modified: Wed, 13 May 2020 02:43:04 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7311255d391474821e6ff5aba8d6844bc5c9e2e40471b5dd96bf62ba2405d63`  
		Last Modified: Wed, 13 May 2020 02:43:05 GMT  
		Size: 57.4 KB (57423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4086b9a963efb5453b0fea08bcf7e2929b72c96b01c26a75e664c9f3afa08073`  
		Last Modified: Wed, 13 May 2020 02:43:05 GMT  
		Size: 7.7 KB (7667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10845d30a458cfbc46d86e2e1b648a37e2179fa8b3decaecb2ef008679f1811d`  
		Last Modified: Wed, 13 May 2020 02:43:09 GMT  
		Size: 5.2 MB (5155624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72303d12158105721cb9441a7e5918a46074d1f3ed76abac25d14ab055e64c1a`  
		Last Modified: Wed, 13 May 2020 02:44:11 GMT  
		Size: 192.7 MB (192684182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280d75f103b14e13026d506d16a35f9d836db86d2403695f2036c8814840f73c`  
		Last Modified: Wed, 13 May 2020 02:43:25 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9adb418083c1173fded9536ea2e6e06cbcc9ca7855386742f03c79e473ad719`  
		Last Modified: Wed, 13 May 2020 02:43:29 GMT  
		Size: 18.6 MB (18569720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:latest` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:ba4dce538d791635953cbf049456de94e78499b8f4d431e2f1dff8b828331dc6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 MB (389740191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1734c56e6cabde8493cad01e2115f4277104df41612422df026dac80feb13bed`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:57:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Apr 2020 07:57:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 06 May 2020 19:01:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp10
# Wed, 06 May 2020 19:02:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='77b893a2b4e3f31c9de91b8db96af1ecd93e8571b6779e9464f5d039310f83ca';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='19c61106210bb8aa497be4ecb6ce0f0da83f2b66b38dfd9388b7762c1874ea72';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='c0869107e776056d6fda87e570cf427556c5cab0fe99ece45f750bbedb4d33eb';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ef360d3e24fc3811cded701bf5fe6245864c88facfeb2de6b290f829ee0be620';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9ffdc8772f91c9fb6c72432f65d48b8fc6ccb34e41e6e225a34e2b3aa93c3047';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 06 May 2020 19:02:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 06 May 2020 20:03:05 GMT
ARG VERBOSE=false
# Wed, 06 May 2020 20:03:06 GMT
ARG OPENJ9_SCC=true
# Wed, 13 May 2020 02:04:17 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.5 org.opencontainers.image.revision=cl200520200429-1655 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 13 May 2020 02:04:17 GMT
ENV LIBERTY_VERSION=20.0.0_05
# Wed, 13 May 2020 02:04:17 GMT
ARG LIBERTY_URL
# Wed, 13 May 2020 02:04:17 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 13 May 2020 02:04:28 GMT
# ARGS: DOWNLOAD_OPTIONS= OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 02:04:29 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 May 2020 02:04:29 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.5 BuildLabel=cl200520200429-1655
# Wed, 13 May 2020 02:04:30 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 13 May 2020 02:04:31 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 13 May 2020 02:04:31 GMT
COPY dir:bb23f4a336cfd1ff1404ca5678fffa89fb2b03183a93be37634e2c00eb179c47 in /opt/ibm/helpers/ 
# Wed, 13 May 2020 02:04:31 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 13 May 2020 02:04:32 GMT
COPY dir:666712edd8ef5cc75494f8a2dc944895b0c1ec9b80e66f7bb4de84169066792b in /licenses/ 
# Wed, 13 May 2020 02:04:33 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 13 May 2020 02:04:42 GMT
# ARGS: DOWNLOAD_OPTIONS= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 13 May 2020 02:04:43 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 13 May 2020 02:04:43 GMT
USER 1001
# Wed, 13 May 2020 02:04:44 GMT
EXPOSE 9080 9443
# Wed, 13 May 2020 02:04:44 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 13 May 2020 02:04:44 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 13 May 2020 02:04:53 GMT
ARG VERBOSE=false
# Wed, 13 May 2020 02:04:53 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 13 May 2020 02:07:54 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 13 May 2020 02:08:01 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 13 May 2020 02:08:31 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcddcb26914bba3154202a6794cc606bb36373fd4a5954207d25c2acbb21027`  
		Last Modified: Fri, 24 Apr 2020 08:00:28 GMT  
		Size: 2.7 MB (2678829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c629705dbca4f2a1136866fdaec045c1f892fffb23cc1ccafc872548ab2f0f07`  
		Last Modified: Wed, 06 May 2020 19:04:43 GMT  
		Size: 127.6 MB (127581919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe801f2b89f9345aadeb354549d0292e450fb0dcb2f05114267dfa41dc17c7b`  
		Last Modified: Wed, 13 May 2020 02:14:07 GMT  
		Size: 13.6 MB (13597693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb074960db033d0fe77cb254530c8fb0f3165054fcd05cb25b48bf46709d934f`  
		Last Modified: Wed, 13 May 2020 02:14:06 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf8ce9ccdeef14be347d4eea0454804c26c05c937050bfe9acedadba6d8ed1d`  
		Last Modified: Wed, 13 May 2020 02:14:05 GMT  
		Size: 6.8 KB (6752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19aae72bbb91e65c36cc465befcbe663afa035418ebd33b67c0691d0045ddc6d`  
		Last Modified: Wed, 13 May 2020 02:14:05 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78cf06b5fdf737a91c52f4e8883e6c49264ca7d67ba4dc52921c740c0f860c5`  
		Last Modified: Wed, 13 May 2020 02:14:10 GMT  
		Size: 57.4 KB (57422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160e16fbd6a9b4d1f8234afbded3916eb1c7a390f1cfbc35bef8fd0795b4de25`  
		Last Modified: Wed, 13 May 2020 02:14:09 GMT  
		Size: 7.7 KB (7657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949d85f370790b38f9728f9bddcfca885a18f077b6f6661c4f70815574ac798a`  
		Last Modified: Wed, 13 May 2020 02:14:06 GMT  
		Size: 5.7 MB (5723545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e762ed76672ad83c89701abd175d24bfe06e4b0e5c981b0b1831be4b08f5059a`  
		Last Modified: Wed, 13 May 2020 02:14:32 GMT  
		Size: 193.2 MB (193249328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b16f76e72b58c13a688821d217bb27bbb5227b1e512f7ebc406336d2165f230`  
		Last Modified: Wed, 13 May 2020 02:14:28 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead0808c72f3a92f87e64e8c2e1dd71387b4a5339a99fd51b5f2e8e41665f3c4`  
		Last Modified: Wed, 13 May 2020 02:14:18 GMT  
		Size: 21.4 MB (21432587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
