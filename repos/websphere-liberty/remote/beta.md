## `websphere-liberty:beta`

```console
$ docker pull websphere-liberty@sha256:9b526577cbea9a60413f9d1e2cbc706e36a4bef28b04e790927ce723808c3630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:beta` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:586f1e64fa875666b1b3d9fc41d7273fdd3a7c8656c717a6b93924b986c96699
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252481801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e994cec920f5f1570d3cff55d20d5e75ea09becda30f74898d4a01622c62580c`
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
# Sat, 26 Sep 2020 00:39:25 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Sat, 26 Sep 2020 00:40:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Sat, 26 Sep 2020 00:40:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 26 Sep 2020 04:04:10 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=2020.9.0.0 org.opencontainers.image.revision=cl200920200820-0913
# Sat, 26 Sep 2020 04:04:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default
# Sat, 26 Sep 2020 04:04:16 GMT
ENV LIBERTY_VERSION=2020.9.0_0
# Sat, 26 Sep 2020 04:04:29 GMT
RUN LIBERTY_URL=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 3 | sed -n 's/\s*webProfile7:\s//p' | tr -d '\r')      && echo $LIBERTY_URL     && wget -q $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp-beta.zip     && unzip -q /tmp/wlp-beta.zip -d /opt/ibm     && rm /tmp/wlp-beta.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp
# Sat, 26 Sep 2020 04:04:29 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 26 Sep 2020 04:04:29 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Sat, 26 Sep 2020 04:04:31 GMT
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 26 Sep 2020 04:04:31 GMT
COPY file:f1015ab5ca098f3a04cde2e721a2aa35a1ebb2e9f5eb01d378eb2264cff9a268 in /opt/ibm/wlp/usr/servers/defaultServer/ 
# Sat, 26 Sep 2020 04:04:32 GMT
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 26 Sep 2020 04:04:32 GMT
USER 1001
# Sat, 26 Sep 2020 04:04:32 GMT
EXPOSE 9080 9443
# Sat, 26 Sep 2020 04:04:32 GMT
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
	-	`sha256:465b54257d914349b14692edd72923f691ddd63fdd3c9fedd98359877049c591`  
		Last Modified: Sat, 26 Sep 2020 00:44:40 GMT  
		Size: 130.2 MB (130222387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9df1624968a857c38a6647f42b36c1e701f32e340ce23e5761e115d757c58a`  
		Last Modified: Sat, 26 Sep 2020 04:14:07 GMT  
		Size: 378.4 KB (378435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35629186ebb3dc9fbbe74bb8d5c59788ec9e9d2cfee4175a776d045ae72d720`  
		Last Modified: Sat, 26 Sep 2020 04:14:14 GMT  
		Size: 92.2 MB (92217567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9caafb59dccf1092deb10551974802d1b7209aae5f789dfe8659ab7cfe40976d`  
		Last Modified: Sat, 26 Sep 2020 04:14:07 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab63a1402599a2b7202805da92a65f3026bfa5b4e398b46ac810d80a1a5cf84`  
		Last Modified: Sat, 26 Sep 2020 04:14:07 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396d70247f86dab68b867d3dc3839de4979802d9da16e302a48167e3a6120c0d`  
		Last Modified: Sat, 26 Sep 2020 04:14:07 GMT  
		Size: 917.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:beta` - linux; 386

```console
$ docker pull websphere-liberty@sha256:220d1fb9f09ab4e801a121530c7bec71500af51a94c425e77c473cc5df02cd28
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241242543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0961085eede0b71971f9563b12793ee6405a735378f504d02301f36d8d12a5d3`
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
# Fri, 25 Sep 2020 23:09:09 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Fri, 25 Sep 2020 23:09:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 25 Sep 2020 23:09:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 25 Sep 2020 23:34:19 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=2020.9.0.0 org.opencontainers.image.revision=cl200920200820-0913
# Fri, 25 Sep 2020 23:34:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default
# Fri, 25 Sep 2020 23:34:26 GMT
ENV LIBERTY_VERSION=2020.9.0_0
# Fri, 25 Sep 2020 23:34:40 GMT
RUN LIBERTY_URL=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 3 | sed -n 's/\s*webProfile7:\s//p' | tr -d '\r')      && echo $LIBERTY_URL     && wget -q $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp-beta.zip     && unzip -q /tmp/wlp-beta.zip -d /opt/ibm     && rm /tmp/wlp-beta.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp
# Fri, 25 Sep 2020 23:34:40 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Sep 2020 23:34:40 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Fri, 25 Sep 2020 23:34:42 GMT
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 25 Sep 2020 23:34:42 GMT
COPY file:f1015ab5ca098f3a04cde2e721a2aa35a1ebb2e9f5eb01d378eb2264cff9a268 in /opt/ibm/wlp/usr/servers/defaultServer/ 
# Fri, 25 Sep 2020 23:34:44 GMT
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 25 Sep 2020 23:34:44 GMT
USER 1001
# Fri, 25 Sep 2020 23:34:44 GMT
EXPOSE 9080 9443
# Fri, 25 Sep 2020 23:34:44 GMT
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
	-	`sha256:a7bdb9c98897ae4e83620a3111f0b7fecab079e7588a2cb2cd851ef0d9957bca`  
		Last Modified: Fri, 25 Sep 2020 23:12:01 GMT  
		Size: 118.5 MB (118548369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31ee65eafcc6c4b8acf3b324c1c9f7e64c23feed2cfd2608cbd56c07a0af19c`  
		Last Modified: Fri, 25 Sep 2020 23:35:57 GMT  
		Size: 365.3 KB (365305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2b52f67fd4906bc81759d26db843b5265cddc7f1343cdbda62a6f033798dab`  
		Last Modified: Fri, 25 Sep 2020 23:36:06 GMT  
		Size: 92.2 MB (92217540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479503d9881e5e71ddb479337ce84c4d8e53594de0bd040a573dd44e1df69063`  
		Last Modified: Fri, 25 Sep 2020 23:35:57 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b746fd93610d583d71925188e3fe16c47be026be1b5c03856421d9007b968f`  
		Last Modified: Fri, 25 Sep 2020 23:35:57 GMT  
		Size: 424.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2943b26a4cdd214d6da0625ac8367ffcd8830f57b0046271b4629b6e1a92abe9`  
		Last Modified: Fri, 25 Sep 2020 23:35:57 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:beta` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:6743e6c983ee85406d9ca1ba275f51e946db043a6b1600128b56e01d1dcb2157
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255900481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fdba28b6bc305a948fd3222b4fd013c5ffb6279895ad0f7ae8aac5ad1d4a81`
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
# Sat, 26 Sep 2020 04:39:05 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Sat, 26 Sep 2020 04:40:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Sat, 26 Sep 2020 04:40:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 26 Sep 2020 05:34:33 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=2020.9.0.0 org.opencontainers.image.revision=cl200920200820-0913
# Sat, 26 Sep 2020 05:34:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default
# Sat, 26 Sep 2020 05:34:59 GMT
ENV LIBERTY_VERSION=2020.9.0_0
# Sat, 26 Sep 2020 05:35:28 GMT
RUN LIBERTY_URL=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 3 | sed -n 's/\s*webProfile7:\s//p' | tr -d '\r')      && echo $LIBERTY_URL     && wget -q $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp-beta.zip     && unzip -q /tmp/wlp-beta.zip -d /opt/ibm     && rm /tmp/wlp-beta.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp
# Sat, 26 Sep 2020 05:35:32 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 26 Sep 2020 05:35:34 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Sat, 26 Sep 2020 05:35:58 GMT
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 26 Sep 2020 05:36:01 GMT
COPY file:f1015ab5ca098f3a04cde2e721a2aa35a1ebb2e9f5eb01d378eb2264cff9a268 in /opt/ibm/wlp/usr/servers/defaultServer/ 
# Sat, 26 Sep 2020 05:36:15 GMT
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 26 Sep 2020 05:36:19 GMT
USER 1001
# Sat, 26 Sep 2020 05:36:25 GMT
EXPOSE 9080 9443
# Sat, 26 Sep 2020 05:36:31 GMT
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
	-	`sha256:c38952e3221db62e6aec454d1d3c5a2afc4f357625bb0599c2e3635f3ea4382b`  
		Last Modified: Sat, 26 Sep 2020 04:43:48 GMT  
		Size: 129.8 MB (129790034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12da40f15bce54bf153190054ab5ee92fcf6894bce4ef0530a21e9710f9dc2b4`  
		Last Modified: Sat, 26 Sep 2020 05:53:02 GMT  
		Size: 405.2 KB (405237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29380df5cfd8ea65da00f8415307bc6414fec3b23d1234a17ce96d76b6327978`  
		Last Modified: Sat, 26 Sep 2020 05:53:26 GMT  
		Size: 92.2 MB (92217592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc0e4c9cc7124ccc866759e19391e991bd13d38365d78d7c667d330337f4689`  
		Last Modified: Sat, 26 Sep 2020 05:53:02 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a52fbdb2bc47ab428b9b7b59426dcc77c87e799443708a7475ca7a1f5dc4f79`  
		Last Modified: Sat, 26 Sep 2020 05:53:02 GMT  
		Size: 426.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db5b579cea2c73e02a73a9bc09b7c0b59a511efa2d18af056c7cd0667917de6`  
		Last Modified: Sat, 26 Sep 2020 05:53:02 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:beta` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:e9c197ad5b7f9432c06338f628b2439807ae89958a85efffcae148cce3331a07
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248104138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17131ca3b684cc714062d9ff34dedd57dc61505053551d3935d0873e40b49c99`
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
# Fri, 25 Sep 2020 23:01:57 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Fri, 25 Sep 2020 23:03:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 25 Sep 2020 23:03:24 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 25 Sep 2020 23:40:56 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=2020.9.0.0 org.opencontainers.image.revision=cl200920200820-0913
# Fri, 25 Sep 2020 23:41:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default
# Fri, 25 Sep 2020 23:41:02 GMT
ENV LIBERTY_VERSION=2020.9.0_0
# Fri, 25 Sep 2020 23:41:15 GMT
RUN LIBERTY_URL=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 3 | sed -n 's/\s*webProfile7:\s//p' | tr -d '\r')      && echo $LIBERTY_URL     && wget -q $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp-beta.zip     && unzip -q /tmp/wlp-beta.zip -d /opt/ibm     && rm /tmp/wlp-beta.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp
# Fri, 25 Sep 2020 23:41:17 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Sep 2020 23:41:17 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Fri, 25 Sep 2020 23:41:18 GMT
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 25 Sep 2020 23:41:18 GMT
COPY file:f1015ab5ca098f3a04cde2e721a2aa35a1ebb2e9f5eb01d378eb2264cff9a268 in /opt/ibm/wlp/usr/servers/defaultServer/ 
# Fri, 25 Sep 2020 23:41:19 GMT
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 25 Sep 2020 23:41:19 GMT
USER 1001
# Fri, 25 Sep 2020 23:41:19 GMT
EXPOSE 9080 9443
# Fri, 25 Sep 2020 23:41:20 GMT
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
	-	`sha256:b471e96aeff094e19d3d2e1a0dd5e0a0691e99498c198fbfdf56baf391c003d6`  
		Last Modified: Fri, 25 Sep 2020 23:06:32 GMT  
		Size: 127.5 MB (127466693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c7c08ccd95f60a478165f7695b0aaf4a277404c23ed99c8bdb4fc939644a0c`  
		Last Modified: Fri, 25 Sep 2020 23:49:49 GMT  
		Size: 371.9 KB (371921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9037b353b146dbe8f4d3191648632c056e7d1ab448d352deead429246ddaa1ac`  
		Last Modified: Fri, 25 Sep 2020 23:49:54 GMT  
		Size: 92.2 MB (92217666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148975f958dc777d4785ce822bf46bf82ac975fa86d060408731e504f4aed386`  
		Last Modified: Fri, 25 Sep 2020 23:49:49 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176e6de450ea0fb31b58dfc1e7537f9f68fe51057c0266898fc992d00967fd24`  
		Last Modified: Fri, 25 Sep 2020 23:49:49 GMT  
		Size: 424.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff5aa723750b308921aa94a421e6e1b5a1a532cd36a619cc160c8699cdd20d7`  
		Last Modified: Fri, 25 Sep 2020 23:49:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
