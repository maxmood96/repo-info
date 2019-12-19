## `websphere-liberty:beta`

```console
$ docker pull websphere-liberty@sha256:e97d5061407d18619c17cda7b30f0383fa41edfa1acc9d392ae4f30c06553416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:beta` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:2c80cef26e3ef2513817cf8c3ebce6646e9d6391faf163c321ecc425c94c1582
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.6 MB (260649028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc1ffe8eb17b9b88257b986ee85e5b97eda17328c9d7a0925a90ed5b3941177`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 19 Dec 2019 04:21:25 GMT
ADD file:53f100793e6c0adfca99977a42bb65cb7971c26e4d6e4499d1c30a1f51f06854 in / 
# Thu, 19 Dec 2019 04:21:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:21:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:21:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:21:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:44:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 19 Dec 2019 07:44:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:44:16 GMT
ENV JAVA_VERSION=1.8.0_sr6
# Thu, 19 Dec 2019 07:45:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='31a6f7e851749343cb4fe3956202bdde0beabff901ba926e78cdf013e6d7e725';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='35d0aa5e54b8d68873a2b5de27e834ff4801dcaf598e180b820366f902cef345';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e10ce4e0ba88febefeffef246d59a746c6b9cbe3a3259c792bcf5af807304332';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bfdb5e450cf4dc9d6f322e8969bb9e7c75d371e38ebf325c635b91ff55eb3ffb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='3956e363357c68e60c5df1e98a51f75f2e680c237320dea59a02b38e5541ce23';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 19 Dec 2019 07:45:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 19 Dec 2019 10:23:04 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=2019.12.0.0 org.opencontainers.image.revision=cl191020191002-0300
# Thu, 19 Dec 2019 10:23:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default
# Thu, 19 Dec 2019 10:23:09 GMT
ENV LIBERTY_VERSION=2019.12.0_0
# Thu, 19 Dec 2019 10:23:24 GMT
RUN LIBERTY_URL=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 3 | sed -n 's/\s*webProfile7:\s//p' | tr -d '\r')      && echo $LIBERTY_URL     && wget -q $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp-beta.zip     && unzip -q /tmp/wlp-beta.zip -d /opt/ibm     && rm /tmp/wlp-beta.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp
# Thu, 19 Dec 2019 10:23:24 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:23:24 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Thu, 19 Dec 2019 10:23:26 GMT
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 19 Dec 2019 10:23:26 GMT
COPY file:f1015ab5ca098f3a04cde2e721a2aa35a1ebb2e9f5eb01d378eb2264cff9a268 in /opt/ibm/wlp/usr/servers/defaultServer/ 
# Thu, 19 Dec 2019 10:23:26 GMT
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 19 Dec 2019 10:23:27 GMT
USER 1001
# Thu, 19 Dec 2019 10:23:27 GMT
EXPOSE 9080 9443
# Thu, 19 Dec 2019 10:23:27 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:2746a4a261c9e18bfd7ff0429c18fd7522acc14fa4c7ec8ab37ba5ebaadbc584`  
		Last Modified: Mon, 02 Dec 2019 13:22:09 GMT  
		Size: 26.7 MB (26689544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1d20cdee96111c8acf1858b62655a37ce81ae48648993542b7ac363ac5c0e5`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 35.4 KB (35361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3160e1d0de4061b5b32ee09af687b898921d36ed9556df5910ddc3104449cd`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e37668deea784f47c8726d934adc12b8d20a2b1c50b0b0c18cb62771cd3684`  
		Last Modified: Thu, 19 Dec 2019 04:24:53 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085242bc10e9fa1a5d25c07eb610766df458e26540b003729c76f351cc481783`  
		Last Modified: Thu, 19 Dec 2019 07:47:10 GMT  
		Size: 3.0 MB (2964982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2801e2e097236a9be40c56619306655ea640d2e97cdfa1de1cdab4def1407cd`  
		Last Modified: Thu, 19 Dec 2019 07:47:23 GMT  
		Size: 130.2 MB (130210498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056d29f76043c0b0fea58b986d693881eb58ac71f4594c2cb295e789a599a938`  
		Last Modified: Thu, 19 Dec 2019 10:50:25 GMT  
		Size: 377.3 KB (377303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5849d78b05d31b5574a10ed55c542ccd7e868b23a19104a16b86ed3ea021cccc`  
		Last Modified: Thu, 19 Dec 2019 10:50:33 GMT  
		Size: 100.4 MB (100367732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d087f1564d526a7aa6cebf27e5365b950e0d1bf6532d214e97dc1ef88559f30`  
		Last Modified: Thu, 19 Dec 2019 10:50:25 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7f974f0c50b17220672baf732c86b63b81a539a1b49d0e497fe89f7ee46984`  
		Last Modified: Thu, 19 Dec 2019 10:50:24 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc50d7be1d04e2fd6c857e6a8291605046b27922201558e9805f09c9dee737b`  
		Last Modified: Thu, 19 Dec 2019 10:50:24 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:beta` - linux; 386

```console
$ docker pull websphere-liberty@sha256:cbdea23699cfa36c108b177dd4b02b0f9447a5a2eaaee219515f668a6c285650
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249562985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba46675e3f23d88044011b982ed55499e3fe4caf07c1e3cc237bed555e101a0`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 19 Dec 2019 04:40:59 GMT
ADD file:f938a7a3701fa8ceccf978bec8de1e8199af0ab5f04295ee7ecf8f105bcf16a8 in / 
# Thu, 19 Dec 2019 04:41:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:41:01 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:41:02 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:41:02 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 07:12:31 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 19 Dec 2019 07:12:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 07:12:40 GMT
ENV JAVA_VERSION=1.8.0_sr6
# Thu, 19 Dec 2019 07:13:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='31a6f7e851749343cb4fe3956202bdde0beabff901ba926e78cdf013e6d7e725';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='35d0aa5e54b8d68873a2b5de27e834ff4801dcaf598e180b820366f902cef345';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e10ce4e0ba88febefeffef246d59a746c6b9cbe3a3259c792bcf5af807304332';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bfdb5e450cf4dc9d6f322e8969bb9e7c75d371e38ebf325c635b91ff55eb3ffb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='3956e363357c68e60c5df1e98a51f75f2e680c237320dea59a02b38e5541ce23';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 19 Dec 2019 07:13:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 19 Dec 2019 07:44:32 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=2019.12.0.0 org.opencontainers.image.revision=cl191020191002-0300
# Thu, 19 Dec 2019 07:44:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default
# Thu, 19 Dec 2019 07:44:38 GMT
ENV LIBERTY_VERSION=2019.12.0_0
# Thu, 19 Dec 2019 07:44:53 GMT
RUN LIBERTY_URL=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 3 | sed -n 's/\s*webProfile7:\s//p' | tr -d '\r')      && echo $LIBERTY_URL     && wget -q $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp-beta.zip     && unzip -q /tmp/wlp-beta.zip -d /opt/ibm     && rm /tmp/wlp-beta.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp
# Thu, 19 Dec 2019 07:44:54 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 07:44:54 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Thu, 19 Dec 2019 07:44:55 GMT
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 19 Dec 2019 07:44:56 GMT
COPY file:f1015ab5ca098f3a04cde2e721a2aa35a1ebb2e9f5eb01d378eb2264cff9a268 in /opt/ibm/wlp/usr/servers/defaultServer/ 
# Thu, 19 Dec 2019 07:44:56 GMT
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 19 Dec 2019 07:44:56 GMT
USER 1001
# Thu, 19 Dec 2019 07:44:57 GMT
EXPOSE 9080 9443
# Thu, 19 Dec 2019 07:44:57 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:0b51dc8dbf8499fb6b53473b0cf555ca82158b4929e708c2c06d0e6d697fc902`  
		Last Modified: Mon, 02 Dec 2019 15:29:48 GMT  
		Size: 27.1 MB (27123217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59cbd14d28f8ed07956f247809a9efdba1add16a79ce82f16103130ad64d3b22`  
		Last Modified: Thu, 19 Dec 2019 04:42:51 GMT  
		Size: 34.6 KB (34618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9336c889d27d4765152cee05b32891b251e0fd1c9e88c3ecb1b61dcad8f1f2c`  
		Last Modified: Thu, 19 Dec 2019 04:42:51 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4525139ccc6ce7302aec0373ce71cc36a6ede71cec121ec56bd72306de5785e8`  
		Last Modified: Thu, 19 Dec 2019 04:42:51 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc671f513acbf11ad7e152a4961978a6bddd64e62f79aceff43447e8ed1e75b`  
		Last Modified: Thu, 19 Dec 2019 07:15:27 GMT  
		Size: 3.0 MB (2992426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74f4fa14cf3fd9bc7819adac826e1016fe2f4d2786f7bc00266e0590a5753d1`  
		Last Modified: Thu, 19 Dec 2019 07:15:42 GMT  
		Size: 118.7 MB (118675808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cb91fecde88953b1bd6df99fdfeb780089353e4135b738e42d4584badb0c41`  
		Last Modified: Thu, 19 Dec 2019 08:01:22 GMT  
		Size: 365.6 KB (365592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684124bfdbc4ae42cb3defab0916bd09a5c9b4106373adad7df37fba62e77a67`  
		Last Modified: Thu, 19 Dec 2019 08:01:35 GMT  
		Size: 100.4 MB (100367737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5590d4d115e3d092bf835733fec1c873efed65add1a0665ef78b8ad54fa4a927`  
		Last Modified: Thu, 19 Dec 2019 08:01:22 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef322f44885efdda45a3bee38d74c37277aebee7b6db8b89e621fa80d37475f3`  
		Last Modified: Thu, 19 Dec 2019 08:01:23 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9485ca7f2850be93d942f6cdd3c25f9f1343b72d1c8f478c769166bfcabd3bba`  
		Last Modified: Thu, 19 Dec 2019 08:01:22 GMT  
		Size: 941.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:beta` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:22c71460b1998ce9360d9d13776cb1750bd392e73bcead7d15f0a9eaa1230478
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277426183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afef1412879e5d337e08d19b7a84fcd8323320867221d42be50d71684a8b0816`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 19 Dec 2019 04:17:50 GMT
ADD file:04095d1b229274e65c9beb48f6cf33050e58d8ee2cd59c0063d23301a1b68f40 in / 
# Thu, 19 Dec 2019 04:17:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 04:18:00 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:18:06 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:18:08 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 09:11:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 19 Dec 2019 09:11:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 09:11:39 GMT
ENV JAVA_VERSION=1.8.0_sr6
# Thu, 19 Dec 2019 09:12:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='31a6f7e851749343cb4fe3956202bdde0beabff901ba926e78cdf013e6d7e725';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='35d0aa5e54b8d68873a2b5de27e834ff4801dcaf598e180b820366f902cef345';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e10ce4e0ba88febefeffef246d59a746c6b9cbe3a3259c792bcf5af807304332';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bfdb5e450cf4dc9d6f322e8969bb9e7c75d371e38ebf325c635b91ff55eb3ffb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='3956e363357c68e60c5df1e98a51f75f2e680c237320dea59a02b38e5541ce23';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 19 Dec 2019 09:12:45 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 19 Dec 2019 10:49:41 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=2019.12.0.0 org.opencontainers.image.revision=cl191020191002-0300
# Thu, 19 Dec 2019 10:50:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default
# Thu, 19 Dec 2019 10:50:14 GMT
ENV LIBERTY_VERSION=2019.12.0_0
# Thu, 19 Dec 2019 10:50:37 GMT
RUN LIBERTY_URL=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 3 | sed -n 's/\s*webProfile7:\s//p' | tr -d '\r')      && echo $LIBERTY_URL     && wget -q $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp-beta.zip     && unzip -q /tmp/wlp-beta.zip -d /opt/ibm     && rm /tmp/wlp-beta.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp
# Thu, 19 Dec 2019 10:50:40 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 10:50:42 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Thu, 19 Dec 2019 10:50:53 GMT
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 19 Dec 2019 10:50:54 GMT
COPY file:f1015ab5ca098f3a04cde2e721a2aa35a1ebb2e9f5eb01d378eb2264cff9a268 in /opt/ibm/wlp/usr/servers/defaultServer/ 
# Thu, 19 Dec 2019 10:50:59 GMT
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 19 Dec 2019 10:51:01 GMT
USER 1001
# Thu, 19 Dec 2019 10:51:03 GMT
EXPOSE 9080 9443
# Thu, 19 Dec 2019 10:51:05 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:fc185e8867852536dd99638d9087ed0059bd4d581436d4c2aac0d0e17666457a`  
		Last Modified: Mon, 02 Dec 2019 15:30:19 GMT  
		Size: 30.4 MB (30400283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e561dfe3fdb898460f7652cbe0a7bb83e64b240d2504cec93d1b4a1cff37951`  
		Last Modified: Thu, 19 Dec 2019 04:24:04 GMT  
		Size: 35.2 KB (35212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5731b4e21c4ef8f9ab7c0d9535bc069ed88e51e1701f2c89b9260bbabc3ab4`  
		Last Modified: Thu, 19 Dec 2019 04:24:04 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66c7d0deb99d27ed750b5a40c0b038d79913a8644af69d2954631935aab9d88`  
		Last Modified: Thu, 19 Dec 2019 04:24:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110b73a0698b11aa26925db87977ab5f369152866a29e845fe1fb9fa1bad3670`  
		Last Modified: Thu, 19 Dec 2019 09:15:34 GMT  
		Size: 3.1 MB (3093327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59fd8f653f147d3c25546c93f72dce0fce42aaad95ad5a08cf8d7e49e439764`  
		Last Modified: Thu, 19 Dec 2019 09:15:51 GMT  
		Size: 143.1 MB (143120646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afd973e4d7c37271efad803e93a37cf28d9b52a1af205b7b7aa301af2a7e10d`  
		Last Modified: Thu, 19 Dec 2019 11:35:10 GMT  
		Size: 405.2 KB (405164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395933abae4b38031311f8da9919d64b89d50d6a7d7d1713cb84d6de71ed8da4`  
		Last Modified: Thu, 19 Dec 2019 11:35:36 GMT  
		Size: 100.4 MB (100367773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110572289d052696b2137ff7b7fa1d166e9f8e4501ebfbaa1074e09fd1070f8`  
		Last Modified: Thu, 19 Dec 2019 11:35:09 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cf09aa8e6d8f260bc204f6b36785b356b344dad4acc493872f409da3a6ecb1`  
		Last Modified: Thu, 19 Dec 2019 11:35:08 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7604d99929e6b37d80a3aa0a25e4effbf12ac259ca09db61fa57df7d1ef29fad`  
		Last Modified: Thu, 19 Dec 2019 11:35:08 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:beta` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:eb3ffcdc3988b3a640bcec593d57005ae4a34b56094e5d3487a53e608b490360
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256325682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb84c5e93925ab0d04b75bada595856f7ef32e934db3a51691de52a0168976ce`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 19 Dec 2019 01:18:53 GMT
ADD file:71a0e537d0c67d313ccdb48e99409227ca2b68d50d7b1c82b2d069057dd72491 in / 
# Thu, 19 Dec 2019 01:18:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 19 Dec 2019 01:18:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 01:18:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 01:18:55 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 01:43:38 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 19 Dec 2019 01:43:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 01:43:44 GMT
ENV JAVA_VERSION=1.8.0_sr6
# Thu, 19 Dec 2019 01:44:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='31a6f7e851749343cb4fe3956202bdde0beabff901ba926e78cdf013e6d7e725';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='35d0aa5e54b8d68873a2b5de27e834ff4801dcaf598e180b820366f902cef345';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e10ce4e0ba88febefeffef246d59a746c6b9cbe3a3259c792bcf5af807304332';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='bfdb5e450cf4dc9d6f322e8969bb9e7c75d371e38ebf325c635b91ff55eb3ffb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='3956e363357c68e60c5df1e98a51f75f2e680c237320dea59a02b38e5541ce23';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 19 Dec 2019 01:44:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 19 Dec 2019 02:21:37 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=2019.12.0.0 org.opencontainers.image.revision=cl191020191002-0300
# Thu, 19 Dec 2019 02:21:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends unzip     && rm -rf /var/lib/apt/lists/*     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default
# Thu, 19 Dec 2019 02:21:42 GMT
ENV LIBERTY_VERSION=2019.12.0_0
# Thu, 19 Dec 2019 02:21:56 GMT
RUN LIBERTY_URL=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 3 | sed -n 's/\s*webProfile7:\s//p' | tr -d '\r')      && echo $LIBERTY_URL     && wget -q $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp-beta.zip     && unzip -q /tmp/wlp-beta.zip -d /opt/ibm     && rm /tmp/wlp-beta.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp
# Thu, 19 Dec 2019 02:21:57 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 02:21:57 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Thu, 19 Dec 2019 02:21:58 GMT
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 19 Dec 2019 02:21:58 GMT
COPY file:f1015ab5ca098f3a04cde2e721a2aa35a1ebb2e9f5eb01d378eb2264cff9a268 in /opt/ibm/wlp/usr/servers/defaultServer/ 
# Thu, 19 Dec 2019 02:21:59 GMT
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 19 Dec 2019 02:21:59 GMT
USER 1001
# Thu, 19 Dec 2019 02:21:59 GMT
EXPOSE 9080 9443
# Thu, 19 Dec 2019 02:21:59 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:9015d1e9fd5bbafd5a9ab0a774dfb9d9cc36c1bd9cb89822c3416ab04878e685`  
		Last Modified: Mon, 02 Dec 2019 15:31:08 GMT  
		Size: 25.4 MB (25365188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e1186eb2726687c98475f19f4d0ed50e2da9a171069c5fcfd2f5e04fc656c2`  
		Last Modified: Thu, 19 Dec 2019 01:19:51 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86643ed2fb70b22576aa6d06dc041dbc603accc3240237d6790312c954a872c`  
		Last Modified: Thu, 19 Dec 2019 01:19:51 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2e9f669fe720fe3dae748411a09729a654978872e3f094ab10eff5c5d2d0cb`  
		Last Modified: Thu, 19 Dec 2019 01:19:51 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a06445218832e4c51569e3aa592516061170fbdd13c5c992d545773509ac0d4`  
		Last Modified: Thu, 19 Dec 2019 01:46:02 GMT  
		Size: 2.7 MB (2678580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b0b103574164db14ffa22926342b5f79db95bf7dd9b193eafc176be1bf3093`  
		Last Modified: Thu, 19 Dec 2019 01:46:12 GMT  
		Size: 127.5 MB (127502609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a211188b9c7e8322d722b3adb27c3d6779a43c1f9b72f1b9bd47fa636bbae13`  
		Last Modified: Thu, 19 Dec 2019 02:37:56 GMT  
		Size: 371.8 KB (371794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7beadea09b8744a5dd593ca9f40760badf002f13dd242f2811a796bcf0452692`  
		Last Modified: Thu, 19 Dec 2019 02:38:02 GMT  
		Size: 100.4 MB (100367739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1067b4e46c57d2fa8be320025f9271b875ccfddb183519be51f503a512b47a78`  
		Last Modified: Thu, 19 Dec 2019 02:37:56 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cf10158f00098d3c44e1bc0bd4ae29616da2a063cead97708331c657e53ce27`  
		Last Modified: Thu, 19 Dec 2019 02:37:56 GMT  
		Size: 424.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3254117a4a52f896660bbebb13ed74e0331a06541b6a08b7adfebb96f57d309f`  
		Last Modified: Thu, 19 Dec 2019 02:37:56 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
