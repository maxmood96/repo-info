<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ibmjava`

-	[`ibmjava:8`](#ibmjava8)
-	[`ibmjava:8-jre`](#ibmjava8-jre)
-	[`ibmjava:8-jre-alpine`](#ibmjava8-jre-alpine)
-	[`ibmjava:8-sdk`](#ibmjava8-sdk)
-	[`ibmjava:8-sdk-alpine`](#ibmjava8-sdk-alpine)
-	[`ibmjava:8-sfj`](#ibmjava8-sfj)
-	[`ibmjava:8-sfj-alpine`](#ibmjava8-sfj-alpine)
-	[`ibmjava:jre`](#ibmjavajre)
-	[`ibmjava:jre-alpine`](#ibmjavajre-alpine)
-	[`ibmjava:latest`](#ibmjavalatest)
-	[`ibmjava:sdk`](#ibmjavasdk)
-	[`ibmjava:sdk-alpine`](#ibmjavasdk-alpine)
-	[`ibmjava:sfj`](#ibmjavasfj)
-	[`ibmjava:sfj-alpine`](#ibmjavasfj-alpine)

## `ibmjava:8`

```console
$ docker pull ibmjava@sha256:789c8a2b124af236dbf016191602834950c5385e949b575fc008030c4ead10fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8` - linux; amd64

```console
$ docker pull ibmjava@sha256:e48adaa2b49f415d1c4bbed2b721bd5e67d2f101805db14c720b86de6bc562b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159973207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c652880482e559b77efb84beb48aea4713336fb9aabe0fdbf8d5d230a3881f91`
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
# Wed, 25 Nov 2020 23:13:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 25 Nov 2020 23:13:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:e4bdd33b61c6dca21f6e441eb6f50cecaa6407065e4a789832a5be135841cada`  
		Last Modified: Wed, 25 Nov 2020 23:16:00 GMT  
		Size: 130.3 MB (130288775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; 386

```console
$ docker pull ibmjava@sha256:31a5423f2da1d9c730e57142c3997c1964f70d25f245c76eb990429881b7622b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148726216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb76d467a7e827ddd54574b4cbea4f2f54df878378a101815f81e224c9f9b7bd`
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
# Wed, 25 Nov 2020 22:56:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 25 Nov 2020 22:56:53 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:fd526243946dc969ea1591ddbecf92ca2b2d4e7634f7307da4972a12aabf4aa7`  
		Last Modified: Wed, 25 Nov 2020 22:59:11 GMT  
		Size: 118.6 MB (118588318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0b180c150cb335b4d61657ea96e87ba8222876d307eabeca25775477bcc179c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163318725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ec414ea60acb16244075ad748cc16b114dd714dd6433f68a9da449a29535e5`
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
# Wed, 30 Sep 2020 00:22:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:9e13354ac79541b84d9788ee7dddd94ef6804b72632b846ce9f3848f68b16244
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155561116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e34606f517ab07181d58b6755594c47b2f57c889befed77539e7b475bef0aa2`
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
# Wed, 30 Sep 2020 00:46:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:46:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:789c8a2b124af236dbf016191602834950c5385e949b575fc008030c4ead10fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:e48adaa2b49f415d1c4bbed2b721bd5e67d2f101805db14c720b86de6bc562b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159973207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c652880482e559b77efb84beb48aea4713336fb9aabe0fdbf8d5d230a3881f91`
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
# Wed, 25 Nov 2020 23:13:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 25 Nov 2020 23:13:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:e4bdd33b61c6dca21f6e441eb6f50cecaa6407065e4a789832a5be135841cada`  
		Last Modified: Wed, 25 Nov 2020 23:16:00 GMT  
		Size: 130.3 MB (130288775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; 386

```console
$ docker pull ibmjava@sha256:31a5423f2da1d9c730e57142c3997c1964f70d25f245c76eb990429881b7622b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148726216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb76d467a7e827ddd54574b4cbea4f2f54df878378a101815f81e224c9f9b7bd`
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
# Wed, 25 Nov 2020 22:56:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 25 Nov 2020 22:56:53 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:fd526243946dc969ea1591ddbecf92ca2b2d4e7634f7307da4972a12aabf4aa7`  
		Last Modified: Wed, 25 Nov 2020 22:59:11 GMT  
		Size: 118.6 MB (118588318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0b180c150cb335b4d61657ea96e87ba8222876d307eabeca25775477bcc179c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163318725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ec414ea60acb16244075ad748cc16b114dd714dd6433f68a9da449a29535e5`
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
# Wed, 30 Sep 2020 00:22:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:9e13354ac79541b84d9788ee7dddd94ef6804b72632b846ce9f3848f68b16244
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155561116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e34606f517ab07181d58b6755594c47b2f57c889befed77539e7b475bef0aa2`
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
# Wed, 30 Sep 2020 00:46:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:46:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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

## `ibmjava:8-jre-alpine`

```console
$ docker pull ibmjava@sha256:dbf317d5a22c95aa7d0b9c92fff75082b4cbf1827cfd879821b8e04ad5aab38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:8-jre-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:4ff5e209bee919f13ec34b38b23be62399c3d1c8fac8e2af9b059fe22e637d0d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138589331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd7e612bb0f778ee3ade5fd43badfa5fd2613f858b48c3e0347fa7c9b45c195`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:22:55 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 22 Oct 2020 04:22:55 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Thu, 22 Oct 2020 04:23:11 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Thu, 22 Oct 2020 04:23:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Thu, 22 Oct 2020 04:24:08 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Thu, 22 Oct 2020 04:24:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff72c28c2856cce8b5bb14c29cb3a7b7e92b2a1fe599487a09e9a4c8bd8ee724`  
		Last Modified: Thu, 22 Oct 2020 04:26:27 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9988d2cbc75b3e34b9e4c6fc0ec8a2ac7c383d7bf917b00156455900546622f5`  
		Last Modified: Thu, 22 Oct 2020 04:26:28 GMT  
		Size: 5.5 MB (5539661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68dac7cd48a5d02d75618d7e5499efb375390970071a2eadcd851421102d4ca2`  
		Last Modified: Thu, 22 Oct 2020 04:26:45 GMT  
		Size: 130.3 MB (130252264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

## `ibmjava:8-sdk-alpine`

```console
$ docker pull ibmjava@sha256:5a69be7cb352b456633ca6733588e4c308537c7d69f1b840d1783c0b685c2cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:8-sdk-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:b01d352b567fd7ff2def2bd0327f9d843f2385685151ce968dd8b6ff22389c22
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175759236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6710c9833fbc6c9c4238e20d937e74373b53178031eb3b4e508405bd0b6d38f2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:22:55 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 22 Oct 2020 04:22:55 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Thu, 22 Oct 2020 04:23:11 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Thu, 22 Oct 2020 04:23:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Thu, 22 Oct 2020 04:26:03 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='827cb2596be7b729e16f39550114e058b76f9ea0b97dae3182ad89b0b12d38e9';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='35b08931eb28518828222aca9bd02a425d20c14c5c2aed1d62b480a6a6eb9491';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='208be3d8a6f9d294e6a94d932703de74dd663694184762adb5af2699b303da2a';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='24accef18871f294599ed01df50c3838b2deb0bc8b2d9a9cff097d16dae759e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='28043cceb4e70796062c928aaa503c07f344aa692fa8b2a40836ac9581471f34';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Thu, 22 Oct 2020 04:26:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff72c28c2856cce8b5bb14c29cb3a7b7e92b2a1fe599487a09e9a4c8bd8ee724`  
		Last Modified: Thu, 22 Oct 2020 04:26:27 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9988d2cbc75b3e34b9e4c6fc0ec8a2ac7c383d7bf917b00156455900546622f5`  
		Last Modified: Thu, 22 Oct 2020 04:26:28 GMT  
		Size: 5.5 MB (5539661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade252aa832eda1944663030e19f62a410379ff17f6a1676b70607040846c2b1`  
		Last Modified: Thu, 22 Oct 2020 04:27:32 GMT  
		Size: 167.4 MB (167422169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:1bbd17a6467b97df240edbc53e72624e9964a8ea0d012b96742f3f247125fe88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:6ce0758d1b2e89b395cf5c8114a057ba402440f6cad7c496e200c48f42efab6e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93176122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edc4992a6cebdf70c81c142effe9ab8cb25c0bf91980740e259251b2c421bc50`
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
# Wed, 25 Nov 2020 23:13:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d143836caa7e7777f6bf4539b249c48341da97ca4d27f012cf5541b35376e479';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='104b7d07afb812acf1d37a1409cf9dbf360745f346a50a3954ae465315966ad5';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d2d5ca9484d0801816a74b66551a07d5f69fb41e52aeb5f10ddf1d55c1a46d06';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='dd5d853e9dbbcd7342c7dfb0259b675b951ae1faadbbb667f6553270ceb5b4f8';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4b617ba4614317f92159a6930a7ae369923b909377a4d0f2aff9ce3b098ac39';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 25 Nov 2020 23:13:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:7d13de64a7cae4a9585b661df831eff6edd11908e8d35b2295637d9cfa318d12`  
		Last Modified: Wed, 25 Nov 2020 23:16:14 GMT  
		Size: 63.5 MB (63491690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:b3313f5fbb09faf3df5b2ac87e0713b9080a7120e90aa49633273beb00e5ed35
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93053181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100318974eb9c77e277992f95fe60baa0e4ae9b6db8062e2914b78cc605f6d66`
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
# Wed, 25 Nov 2020 22:57:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d143836caa7e7777f6bf4539b249c48341da97ca4d27f012cf5541b35376e479';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='104b7d07afb812acf1d37a1409cf9dbf360745f346a50a3954ae465315966ad5';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d2d5ca9484d0801816a74b66551a07d5f69fb41e52aeb5f10ddf1d55c1a46d06';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='dd5d853e9dbbcd7342c7dfb0259b675b951ae1faadbbb667f6553270ceb5b4f8';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4b617ba4614317f92159a6930a7ae369923b909377a4d0f2aff9ce3b098ac39';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 25 Nov 2020 22:57:40 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:9dd5a0ec5490fe626ff95181159e1c8cc36f9011f9f4ca11998c489d00d8a326`  
		Last Modified: Wed, 25 Nov 2020 22:59:25 GMT  
		Size: 62.9 MB (62915283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:6c7ab789c56f4bd8a946a3da507c44ae76560bb496b0d3efd97e522ed8f4d801
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97192753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35ebd6e91e25a825dd97582d10edefba25d79e9a9d853478334acfa9002a05b`
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
# Wed, 30 Sep 2020 00:24:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d143836caa7e7777f6bf4539b249c48341da97ca4d27f012cf5541b35376e479';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='104b7d07afb812acf1d37a1409cf9dbf360745f346a50a3954ae465315966ad5';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d2d5ca9484d0801816a74b66551a07d5f69fb41e52aeb5f10ddf1d55c1a46d06';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='dd5d853e9dbbcd7342c7dfb0259b675b951ae1faadbbb667f6553270ceb5b4f8';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4b617ba4614317f92159a6930a7ae369923b909377a4d0f2aff9ce3b098ac39';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:24:51 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:35e21eb6a02583a941df3dec0c0a89fcc197557832a5ad9f0990a6209ed57696`  
		Last Modified: Wed, 30 Sep 2020 00:30:25 GMT  
		Size: 63.7 MB (63707849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:758190c0435a9aa82a9ee86a82dc55a56f5aa9c234b008c04db3be709ee3b23a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92665024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8b6c2c64d52a3fbf78f5efd1ef3971f4da6aa6d976c40c983916fc186bcdad`
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
# Wed, 30 Sep 2020 00:48:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d143836caa7e7777f6bf4539b249c48341da97ca4d27f012cf5541b35376e479';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='104b7d07afb812acf1d37a1409cf9dbf360745f346a50a3954ae465315966ad5';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d2d5ca9484d0801816a74b66551a07d5f69fb41e52aeb5f10ddf1d55c1a46d06';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='dd5d853e9dbbcd7342c7dfb0259b675b951ae1faadbbb667f6553270ceb5b4f8';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4b617ba4614317f92159a6930a7ae369923b909377a4d0f2aff9ce3b098ac39';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:48:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:2ba985507d29b79f1747eb1cac6bbd623c7d893dbfd39baa22f1fd74d6b8dc18`  
		Last Modified: Wed, 30 Sep 2020 00:50:08 GMT  
		Size: 64.6 MB (64619861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sfj-alpine`

```console
$ docker pull ibmjava@sha256:935bea7c67ddc13d1bbb848c440514f30884f6f74c2da2ce06e657609523925a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:8-sfj-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:9df168619527b85850892633d6d1fb91acbe4e233a61ad59fb2aeed6d3ece7fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71846740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5339d69acc0ff35ee81583f56cf0550f921c41f75549caa2495dfade042675d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:22:55 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 22 Oct 2020 04:22:55 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Thu, 22 Oct 2020 04:23:11 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Thu, 22 Oct 2020 04:23:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Thu, 22 Oct 2020 04:25:01 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d143836caa7e7777f6bf4539b249c48341da97ca4d27f012cf5541b35376e479';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='104b7d07afb812acf1d37a1409cf9dbf360745f346a50a3954ae465315966ad5';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d2d5ca9484d0801816a74b66551a07d5f69fb41e52aeb5f10ddf1d55c1a46d06';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='dd5d853e9dbbcd7342c7dfb0259b675b951ae1faadbbb667f6553270ceb5b4f8';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4b617ba4614317f92159a6930a7ae369923b909377a4d0f2aff9ce3b098ac39';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Thu, 22 Oct 2020 04:25:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff72c28c2856cce8b5bb14c29cb3a7b7e92b2a1fe599487a09e9a4c8bd8ee724`  
		Last Modified: Thu, 22 Oct 2020 04:26:27 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9988d2cbc75b3e34b9e4c6fc0ec8a2ac7c383d7bf917b00156455900546622f5`  
		Last Modified: Thu, 22 Oct 2020 04:26:28 GMT  
		Size: 5.5 MB (5539661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9b24a2f8b346b1775696077c041c185c0ec68d7c9f1844587cdcc57227a69e`  
		Last Modified: Thu, 22 Oct 2020 04:27:02 GMT  
		Size: 63.5 MB (63509673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:789c8a2b124af236dbf016191602834950c5385e949b575fc008030c4ead10fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:e48adaa2b49f415d1c4bbed2b721bd5e67d2f101805db14c720b86de6bc562b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159973207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c652880482e559b77efb84beb48aea4713336fb9aabe0fdbf8d5d230a3881f91`
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
# Wed, 25 Nov 2020 23:13:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 25 Nov 2020 23:13:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:e4bdd33b61c6dca21f6e441eb6f50cecaa6407065e4a789832a5be135841cada`  
		Last Modified: Wed, 25 Nov 2020 23:16:00 GMT  
		Size: 130.3 MB (130288775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; 386

```console
$ docker pull ibmjava@sha256:31a5423f2da1d9c730e57142c3997c1964f70d25f245c76eb990429881b7622b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148726216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb76d467a7e827ddd54574b4cbea4f2f54df878378a101815f81e224c9f9b7bd`
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
# Wed, 25 Nov 2020 22:56:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 25 Nov 2020 22:56:53 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:fd526243946dc969ea1591ddbecf92ca2b2d4e7634f7307da4972a12aabf4aa7`  
		Last Modified: Wed, 25 Nov 2020 22:59:11 GMT  
		Size: 118.6 MB (118588318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0b180c150cb335b4d61657ea96e87ba8222876d307eabeca25775477bcc179c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163318725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ec414ea60acb16244075ad748cc16b114dd714dd6433f68a9da449a29535e5`
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
# Wed, 30 Sep 2020 00:22:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:9e13354ac79541b84d9788ee7dddd94ef6804b72632b846ce9f3848f68b16244
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155561116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e34606f517ab07181d58b6755594c47b2f57c889befed77539e7b475bef0aa2`
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
# Wed, 30 Sep 2020 00:46:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:46:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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

## `ibmjava:jre-alpine`

```console
$ docker pull ibmjava@sha256:dbf317d5a22c95aa7d0b9c92fff75082b4cbf1827cfd879821b8e04ad5aab38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:jre-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:4ff5e209bee919f13ec34b38b23be62399c3d1c8fac8e2af9b059fe22e637d0d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138589331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd7e612bb0f778ee3ade5fd43badfa5fd2613f858b48c3e0347fa7c9b45c195`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:22:55 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 22 Oct 2020 04:22:55 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Thu, 22 Oct 2020 04:23:11 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Thu, 22 Oct 2020 04:23:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Thu, 22 Oct 2020 04:24:08 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Thu, 22 Oct 2020 04:24:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff72c28c2856cce8b5bb14c29cb3a7b7e92b2a1fe599487a09e9a4c8bd8ee724`  
		Last Modified: Thu, 22 Oct 2020 04:26:27 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9988d2cbc75b3e34b9e4c6fc0ec8a2ac7c383d7bf917b00156455900546622f5`  
		Last Modified: Thu, 22 Oct 2020 04:26:28 GMT  
		Size: 5.5 MB (5539661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68dac7cd48a5d02d75618d7e5499efb375390970071a2eadcd851421102d4ca2`  
		Last Modified: Thu, 22 Oct 2020 04:26:45 GMT  
		Size: 130.3 MB (130252264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:789c8a2b124af236dbf016191602834950c5385e949b575fc008030c4ead10fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:latest` - linux; amd64

```console
$ docker pull ibmjava@sha256:e48adaa2b49f415d1c4bbed2b721bd5e67d2f101805db14c720b86de6bc562b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159973207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c652880482e559b77efb84beb48aea4713336fb9aabe0fdbf8d5d230a3881f91`
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
# Wed, 25 Nov 2020 23:13:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 25 Nov 2020 23:13:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:e4bdd33b61c6dca21f6e441eb6f50cecaa6407065e4a789832a5be135841cada`  
		Last Modified: Wed, 25 Nov 2020 23:16:00 GMT  
		Size: 130.3 MB (130288775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; 386

```console
$ docker pull ibmjava@sha256:31a5423f2da1d9c730e57142c3997c1964f70d25f245c76eb990429881b7622b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148726216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb76d467a7e827ddd54574b4cbea4f2f54df878378a101815f81e224c9f9b7bd`
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
# Wed, 25 Nov 2020 22:56:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 25 Nov 2020 22:56:53 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:fd526243946dc969ea1591ddbecf92ca2b2d4e7634f7307da4972a12aabf4aa7`  
		Last Modified: Wed, 25 Nov 2020 22:59:11 GMT  
		Size: 118.6 MB (118588318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0b180c150cb335b4d61657ea96e87ba8222876d307eabeca25775477bcc179c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163318725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ec414ea60acb16244075ad748cc16b114dd714dd6433f68a9da449a29535e5`
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
# Wed, 30 Sep 2020 00:22:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:22:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:9e13354ac79541b84d9788ee7dddd94ef6804b72632b846ce9f3848f68b16244
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155561116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e34606f517ab07181d58b6755594c47b2f57c889befed77539e7b475bef0aa2`
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
# Wed, 30 Sep 2020 00:46:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f6f3e3c66aa8bcd328dd72ae90640f45161fba8a278e95ea071bbfceb4203de2';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='081b14ceaffcd99d2d106a3b85f262f97d0b42e0af50b9285df67f7d2c57208e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4237c98b9535dd229b458ccb33ff430eb018cceec7d92d196b8e0607668aed2f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6342785e7f48f59b3cbf8c89e9b463a13bf5d8313257a1587cc3fbd72f4c5ebb';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='0259f2da8b62d5563dc0ffaeed50705376f56ae81abfb8bf2d35db7f9c83ce1a';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:46:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:94a1249a6099a9cd1fd9aaa33f31a5dc1048e67c444b3192c9fb6c78259b3b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sdk` - linux; amd64

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

### `ibmjava:sdk` - linux; 386

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

### `ibmjava:sdk` - linux; ppc64le

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

### `ibmjava:sdk` - linux; s390x

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

## `ibmjava:sdk-alpine`

```console
$ docker pull ibmjava@sha256:5a69be7cb352b456633ca6733588e4c308537c7d69f1b840d1783c0b685c2cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:sdk-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:b01d352b567fd7ff2def2bd0327f9d843f2385685151ce968dd8b6ff22389c22
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175759236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6710c9833fbc6c9c4238e20d937e74373b53178031eb3b4e508405bd0b6d38f2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:22:55 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 22 Oct 2020 04:22:55 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Thu, 22 Oct 2020 04:23:11 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Thu, 22 Oct 2020 04:23:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Thu, 22 Oct 2020 04:26:03 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='827cb2596be7b729e16f39550114e058b76f9ea0b97dae3182ad89b0b12d38e9';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='35b08931eb28518828222aca9bd02a425d20c14c5c2aed1d62b480a6a6eb9491';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='208be3d8a6f9d294e6a94d932703de74dd663694184762adb5af2699b303da2a';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='24accef18871f294599ed01df50c3838b2deb0bc8b2d9a9cff097d16dae759e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='28043cceb4e70796062c928aaa503c07f344aa692fa8b2a40836ac9581471f34';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Thu, 22 Oct 2020 04:26:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff72c28c2856cce8b5bb14c29cb3a7b7e92b2a1fe599487a09e9a4c8bd8ee724`  
		Last Modified: Thu, 22 Oct 2020 04:26:27 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9988d2cbc75b3e34b9e4c6fc0ec8a2ac7c383d7bf917b00156455900546622f5`  
		Last Modified: Thu, 22 Oct 2020 04:26:28 GMT  
		Size: 5.5 MB (5539661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade252aa832eda1944663030e19f62a410379ff17f6a1676b70607040846c2b1`  
		Last Modified: Thu, 22 Oct 2020 04:27:32 GMT  
		Size: 167.4 MB (167422169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:1bbd17a6467b97df240edbc53e72624e9964a8ea0d012b96742f3f247125fe88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:6ce0758d1b2e89b395cf5c8114a057ba402440f6cad7c496e200c48f42efab6e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93176122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edc4992a6cebdf70c81c142effe9ab8cb25c0bf91980740e259251b2c421bc50`
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
# Wed, 25 Nov 2020 23:13:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d143836caa7e7777f6bf4539b249c48341da97ca4d27f012cf5541b35376e479';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='104b7d07afb812acf1d37a1409cf9dbf360745f346a50a3954ae465315966ad5';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d2d5ca9484d0801816a74b66551a07d5f69fb41e52aeb5f10ddf1d55c1a46d06';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='dd5d853e9dbbcd7342c7dfb0259b675b951ae1faadbbb667f6553270ceb5b4f8';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4b617ba4614317f92159a6930a7ae369923b909377a4d0f2aff9ce3b098ac39';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 25 Nov 2020 23:13:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:7d13de64a7cae4a9585b661df831eff6edd11908e8d35b2295637d9cfa318d12`  
		Last Modified: Wed, 25 Nov 2020 23:16:14 GMT  
		Size: 63.5 MB (63491690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:b3313f5fbb09faf3df5b2ac87e0713b9080a7120e90aa49633273beb00e5ed35
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93053181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100318974eb9c77e277992f95fe60baa0e4ae9b6db8062e2914b78cc605f6d66`
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
# Wed, 25 Nov 2020 22:57:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d143836caa7e7777f6bf4539b249c48341da97ca4d27f012cf5541b35376e479';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='104b7d07afb812acf1d37a1409cf9dbf360745f346a50a3954ae465315966ad5';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d2d5ca9484d0801816a74b66551a07d5f69fb41e52aeb5f10ddf1d55c1a46d06';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='dd5d853e9dbbcd7342c7dfb0259b675b951ae1faadbbb667f6553270ceb5b4f8';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4b617ba4614317f92159a6930a7ae369923b909377a4d0f2aff9ce3b098ac39';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 25 Nov 2020 22:57:40 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:9dd5a0ec5490fe626ff95181159e1c8cc36f9011f9f4ca11998c489d00d8a326`  
		Last Modified: Wed, 25 Nov 2020 22:59:25 GMT  
		Size: 62.9 MB (62915283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:6c7ab789c56f4bd8a946a3da507c44ae76560bb496b0d3efd97e522ed8f4d801
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97192753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35ebd6e91e25a825dd97582d10edefba25d79e9a9d853478334acfa9002a05b`
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
# Wed, 30 Sep 2020 00:24:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d143836caa7e7777f6bf4539b249c48341da97ca4d27f012cf5541b35376e479';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='104b7d07afb812acf1d37a1409cf9dbf360745f346a50a3954ae465315966ad5';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d2d5ca9484d0801816a74b66551a07d5f69fb41e52aeb5f10ddf1d55c1a46d06';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='dd5d853e9dbbcd7342c7dfb0259b675b951ae1faadbbb667f6553270ceb5b4f8';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4b617ba4614317f92159a6930a7ae369923b909377a4d0f2aff9ce3b098ac39';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:24:51 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:35e21eb6a02583a941df3dec0c0a89fcc197557832a5ad9f0990a6209ed57696`  
		Last Modified: Wed, 30 Sep 2020 00:30:25 GMT  
		Size: 63.7 MB (63707849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:758190c0435a9aa82a9ee86a82dc55a56f5aa9c234b008c04db3be709ee3b23a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92665024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8b6c2c64d52a3fbf78f5efd1ef3971f4da6aa6d976c40c983916fc186bcdad`
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
# Wed, 30 Sep 2020 00:48:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d143836caa7e7777f6bf4539b249c48341da97ca4d27f012cf5541b35376e479';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='104b7d07afb812acf1d37a1409cf9dbf360745f346a50a3954ae465315966ad5';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d2d5ca9484d0801816a74b66551a07d5f69fb41e52aeb5f10ddf1d55c1a46d06';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='dd5d853e9dbbcd7342c7dfb0259b675b951ae1faadbbb667f6553270ceb5b4f8';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4b617ba4614317f92159a6930a7ae369923b909377a4d0f2aff9ce3b098ac39';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 30 Sep 2020 00:48:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:2ba985507d29b79f1747eb1cac6bbd623c7d893dbfd39baa22f1fd74d6b8dc18`  
		Last Modified: Wed, 30 Sep 2020 00:50:08 GMT  
		Size: 64.6 MB (64619861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sfj-alpine`

```console
$ docker pull ibmjava@sha256:935bea7c67ddc13d1bbb848c440514f30884f6f74c2da2ce06e657609523925a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:sfj-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:9df168619527b85850892633d6d1fb91acbe4e233a61ad59fb2aeed6d3ece7fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71846740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5339d69acc0ff35ee81583f56cf0550f921c41f75549caa2495dfade042675d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 04:22:55 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 22 Oct 2020 04:22:55 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Thu, 22 Oct 2020 04:23:11 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Thu, 22 Oct 2020 04:23:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp16
# Thu, 22 Oct 2020 04:25:01 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d143836caa7e7777f6bf4539b249c48341da97ca4d27f012cf5541b35376e479';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='104b7d07afb812acf1d37a1409cf9dbf360745f346a50a3954ae465315966ad5';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d2d5ca9484d0801816a74b66551a07d5f69fb41e52aeb5f10ddf1d55c1a46d06';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='dd5d853e9dbbcd7342c7dfb0259b675b951ae1faadbbb667f6553270ceb5b4f8';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4b617ba4614317f92159a6930a7ae369923b909377a4d0f2aff9ce3b098ac39';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Thu, 22 Oct 2020 04:25:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff72c28c2856cce8b5bb14c29cb3a7b7e92b2a1fe599487a09e9a4c8bd8ee724`  
		Last Modified: Thu, 22 Oct 2020 04:26:27 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9988d2cbc75b3e34b9e4c6fc0ec8a2ac7c383d7bf917b00156455900546622f5`  
		Last Modified: Thu, 22 Oct 2020 04:26:28 GMT  
		Size: 5.5 MB (5539661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9b24a2f8b346b1775696077c041c185c0ec68d7c9f1844587cdcc57227a69e`  
		Last Modified: Thu, 22 Oct 2020 04:27:02 GMT  
		Size: 63.5 MB (63509673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
