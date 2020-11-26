## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:94a1249a6099a9cd1fd9aaa33f31a5dc1048e67c444b3192c9fb6c78259b3b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:c9b034d52e5b8f727b1d04f877cd9d1789cf5f9f3b46e8077411e0d77a16bddf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 MB (197143393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810afae739bb6dbd896a19b5450a047d87a97598f71e58931ef2c9776552b269`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:13 GMT
ADD file:6ef542de9959c3061f2d0758adb031e226b221a1a2cd748ff59e6fc13216a1c0 in / 
# Wed, 25 Nov 2020 22:25:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:16 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:17 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:12:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 25 Nov 2020 23:12:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 23:12:17 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 25 Nov 2020 23:15:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='827cb2596be7b729e16f39550114e058b76f9ea0b97dae3182ad89b0b12d38e9';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='35b08931eb28518828222aca9bd02a425d20c14c5c2aed1d62b480a6a6eb9491';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='208be3d8a6f9d294e6a94d932703de74dd663694184762adb5af2699b303da2a';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='24accef18871f294599ed01df50c3838b2deb0bc8b2d9a9cff097d16dae759e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='28043cceb4e70796062c928aaa503c07f344aa692fa8b2a40836ac9581471f34';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 25 Nov 2020 23:15:09 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f22ccc0b8772d8e1bcb40f137b373686bc27427a70c0e41dd22b38016e09e7e0`  
		Last Modified: Fri, 20 Nov 2020 13:21:30 GMT  
		Size: 26.7 MB (26708056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf8fb62ba5ffb221a2edb2208741346eb4d2d99a174138e4afbb69ce1fd9966`  
		Last Modified: Wed, 25 Nov 2020 22:26:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80c964ece6a3edf0db1cfc72ae0e6f0699fb776bbfcc92b708fbb945b0b9547`  
		Last Modified: Wed, 25 Nov 2020 22:26:30 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbdc1b81f30dbbd36bce786a7db45a7e80384faea0379723165445aab33d793`  
		Last Modified: Wed, 25 Nov 2020 23:15:46 GMT  
		Size: 3.0 MB (2975364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2687a5acc6614fcc336194da3a79fcf9bfce6cffe054e0b705cd74b2704d0a3c`  
		Last Modified: Wed, 25 Nov 2020 23:16:41 GMT  
		Size: 167.5 MB (167458961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:27da03e55873dae650a51a6d2e8b757faf857d100da0ca6d6b7b2f0d78ee5b9c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185778755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:287939c37daefad13bb84ba1891f49a092314c3ce0bd8d5915bafb6f76d0362d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:39:43 GMT
ADD file:0c5561447fe076ca64e04bad6a202d27c7f34e112c49a4f1d6c019f69df4018d in / 
# Wed, 25 Nov 2020 22:39:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:39:44 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:39:45 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:39:45 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 22:56:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 25 Nov 2020 22:56:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:56:11 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Wed, 25 Nov 2020 22:58:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='827cb2596be7b729e16f39550114e058b76f9ea0b97dae3182ad89b0b12d38e9';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='35b08931eb28518828222aca9bd02a425d20c14c5c2aed1d62b480a6a6eb9491';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='208be3d8a6f9d294e6a94d932703de74dd663694184762adb5af2699b303da2a';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='24accef18871f294599ed01df50c3838b2deb0bc8b2d9a9cff097d16dae759e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='28043cceb4e70796062c928aaa503c07f344aa692fa8b2a40836ac9581471f34';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 25 Nov 2020 22:58:37 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:73fd230d9c9346a670d4a2eca6e4352405d1bfcfeb6039b4018158cde52d0767`  
		Last Modified: Mon, 23 Nov 2020 17:14:15 GMT  
		Size: 27.1 MB (27135125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354328fbe40a654d4fff7b284bbe510445e5c0722de56b7c28dccd50c0b7acf5`  
		Last Modified: Wed, 25 Nov 2020 22:40:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100b74721cd5ea3ed3868db1c4835480d2f5332ea99fc6ade8f74b448ec551ac`  
		Last Modified: Wed, 25 Nov 2020 22:40:16 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b27efed6e3036e6bb536fc15474c5c0d57768dfdcbd2a2e8cd670b3e517abb`  
		Last Modified: Wed, 25 Nov 2020 22:58:56 GMT  
		Size: 3.0 MB (3001762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5dc16fbc48af840e3ceda015b221e09750efbdc820c3925171f5cb35531b75`  
		Last Modified: Wed, 25 Nov 2020 22:59:51 GMT  
		Size: 155.6 MB (155640857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:78d5e746ccc063ba4a8a4e27d26b7c0c32022e9bf606bda1e978ba0ac067265c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 MB (200608371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafd735811db7101623ebc09a6978532a9b9860693d819cb202be4946ea536c4`
-	Default Command: `["\/bin\/bash"]`

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
# Wed, 30 Sep 2020 00:26:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='827cb2596be7b729e16f39550114e058b76f9ea0b97dae3182ad89b0b12d38e9';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='35b08931eb28518828222aca9bd02a425d20c14c5c2aed1d62b480a6a6eb9491';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='208be3d8a6f9d294e6a94d932703de74dd663694184762adb5af2699b303da2a';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='24accef18871f294599ed01df50c3838b2deb0bc8b2d9a9cff097d16dae759e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='28043cceb4e70796062c928aaa503c07f344aa692fa8b2a40836ac9581471f34';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:26:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:9424fd68e6111b3f01e1dba2d84256899ee1e07fdc1b71a4104897227dae7c65`  
		Last Modified: Wed, 30 Sep 2020 00:30:57 GMT  
		Size: 167.1 MB (167123467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:c21d92e1bc17da6b2fee577bc74c640020fe75c40c76e0a1a5a9841f4c4b3680
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185820119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48205470e76ebca3617fef5b06b82262c559c7b30ce95312847091428426c8c2`
-	Default Command: `["\/bin\/bash"]`

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
# Wed, 30 Sep 2020 00:49:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='827cb2596be7b729e16f39550114e058b76f9ea0b97dae3182ad89b0b12d38e9';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='35b08931eb28518828222aca9bd02a425d20c14c5c2aed1d62b480a6a6eb9491';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='208be3d8a6f9d294e6a94d932703de74dd663694184762adb5af2699b303da2a';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='24accef18871f294599ed01df50c3838b2deb0bc8b2d9a9cff097d16dae759e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='28043cceb4e70796062c928aaa503c07f344aa692fa8b2a40836ac9581471f34';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:49:24 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:2e3c1a88d7b71236c7d97c42bddb3d720f2d2e8ee5c624218ad88ceb81247f84`  
		Last Modified: Wed, 30 Sep 2020 00:50:31 GMT  
		Size: 157.8 MB (157774956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
