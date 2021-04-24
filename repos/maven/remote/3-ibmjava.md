## `maven:3-ibmjava`

```console
$ docker pull maven@sha256:c6ed7f907351d039bede9a1d8651c16fa8806d233860696b1e1823a66bff6362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `maven:3-ibmjava` - linux; amd64

```console
$ docker pull maven@sha256:67608463abd1081ae37b4978d65826a0374034a5567a936e8306b25de307edbb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.4 MB (236354274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c0cb7f42067456a17a99f0246283fe14d9eaabff8c8bf9c3dd33e94baad2b9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:30:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 26 Mar 2021 09:31:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:31:04 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 26 Mar 2021 09:34:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c51b7afed4911a4eefdf02c44ee440de726a5a605c5507cc50d4795394b418c2';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='dfe87d34c40cd0c23dc4b7ee47c85f84e26d21ff75476b234998bb9132379659';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bbc55934ec867290cd9307422beae48e5032dfabb7cb496bed6e47b7ab3f90be';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='a1ed2722f283a3f3eb0a71f23354b0b4d2761865e759a3bf7f89297e17c20e6f';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c2ddf185daafacd0b50f3e4e593d613b2e9b70d66b88a8da6ee313181376aef6';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Mar 2021 09:34:34 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Mon, 05 Apr 2021 17:53:05 GMT
ARG MAVEN_VERSION=3.8.1
# Mon, 05 Apr 2021 17:53:05 GMT
ARG USER_HOME_DIR=/root
# Mon, 05 Apr 2021 17:53:06 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Mon, 05 Apr 2021 17:53:06 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Mon, 05 Apr 2021 17:53:36 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN apt-get update && apt-get install -y curl   && mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 05 Apr 2021 17:53:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 05 Apr 2021 17:53:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 05 Apr 2021 17:53:37 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 05 Apr 2021 17:53:37 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 05 Apr 2021 17:53:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 05 Apr 2021 17:53:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4764ed71d2900c9874838108e377eb8821088502d5504fadeb080e5dd1a3e65d`  
		Last Modified: Fri, 26 Mar 2021 09:35:47 GMT  
		Size: 3.0 MB (2958415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86949eeef16a3389800d71fc509c42bf38f63c03fc1a49fffbc6dbedd587391`  
		Last Modified: Fri, 26 Mar 2021 09:37:24 GMT  
		Size: 168.0 MB (168001680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191123f915a8a832f3d9551f2e6ca4ff3af4540d22cdc2ddbd039abfffaa3b2c`  
		Last Modified: Mon, 05 Apr 2021 18:04:13 GMT  
		Size: 38.7 MB (38681148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78e7276c0fd392b900ee1fad28e18cf847e79d6abd7ac24b42703da05106f95`  
		Last Modified: Mon, 05 Apr 2021 18:04:09 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90227f982f4216ce414b3cfd451f4202b8c062a5a2d435512ba5039dd462622`  
		Last Modified: Mon, 05 Apr 2021 18:04:09 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibmjava` - linux; 386

```console
$ docker pull maven@sha256:5f423ec9efadbbf9b83d3f1f14d04d2a34cc914a2b08de896719138892b28360
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223284965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d583f525b73c5254a76ff12bf68577239d09ae8e06d4d9fcd85d936aa928602`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 23 Apr 2021 22:39:49 GMT
ADD file:90725d5ecc587065bcac0f628d4fca740e70b473ad2304167c86a3929979ab6d in / 
# Fri, 23 Apr 2021 22:39:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:39:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:39:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:39:53 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:56:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 22:56:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:56:57 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 22:59:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c51b7afed4911a4eefdf02c44ee440de726a5a605c5507cc50d4795394b418c2';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='dfe87d34c40cd0c23dc4b7ee47c85f84e26d21ff75476b234998bb9132379659';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bbc55934ec867290cd9307422beae48e5032dfabb7cb496bed6e47b7ab3f90be';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='a1ed2722f283a3f3eb0a71f23354b0b4d2761865e759a3bf7f89297e17c20e6f';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c2ddf185daafacd0b50f3e4e593d613b2e9b70d66b88a8da6ee313181376aef6';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 22:59:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:25:18 GMT
ARG MAVEN_VERSION=3.8.1
# Fri, 23 Apr 2021 23:25:18 GMT
ARG USER_HOME_DIR=/root
# Fri, 23 Apr 2021 23:25:18 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Fri, 23 Apr 2021 23:25:18 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Fri, 23 Apr 2021 23:25:28 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN apt-get update && apt-get install -y curl   && mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 23 Apr 2021 23:25:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 23 Apr 2021 23:25:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 23 Apr 2021 23:25:29 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 23 Apr 2021 23:25:29 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 23 Apr 2021 23:25:29 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 23 Apr 2021 23:25:30 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3ca505a8d0cb8bb3cbc0acdf7779f1042c7bdc466c7b025c91341342e5f91d11`  
		Last Modified: Fri, 23 Apr 2021 22:40:49 GMT  
		Size: 27.1 MB (27131171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d026bc940387371d3fe09319970ec5fb8b5412664a63d601a0b0d2ee6f932d`  
		Last Modified: Fri, 23 Apr 2021 22:40:43 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3c95f0f20e6979f6c17445cbb1ad51c1ad261f6a18edd64cc2cbe88fe56b7c`  
		Last Modified: Fri, 23 Apr 2021 22:40:43 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a16c08709439f10e0228f8ddd5aeee22678c1ffaf756f7c56377c229aeedcd2`  
		Last Modified: Fri, 23 Apr 2021 22:59:32 GMT  
		Size: 3.0 MB (2988497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c44e9043d3b21cb010ded20db7daa97ae2a50968acd7906d38a0747dd6bf452`  
		Last Modified: Fri, 23 Apr 2021 23:00:37 GMT  
		Size: 156.2 MB (156172312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab5dfd30a685935114d6146bf29107841acf54f100a03c8b82c2451ee65a3ad`  
		Last Modified: Fri, 23 Apr 2021 23:26:02 GMT  
		Size: 37.0 MB (36990732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab42df1b006b6c8e66ba3a5c9749be3f5f7b31d912778c2dda1f804f5041c9ef`  
		Last Modified: Fri, 23 Apr 2021 23:25:58 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56057ea9cac9c57cd8da39643465e662f550f6a4d0afedbbe389bb775a89d0ea`  
		Last Modified: Fri, 23 Apr 2021 23:25:57 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibmjava` - linux; ppc64le

```console
$ docker pull maven@sha256:732e0ac7b839e77e189ca72f373c3581aa8687f096ef4bc3898c0cbf4bbbb128
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235622200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac4107743fdc1cb1617d14e326ea78b6b1dd54b98bc29559ae88ed52b5e16c7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 25 Mar 2021 22:54:50 GMT
ADD file:16a7a25947f319127d6b6ca6c99ff4e36bc4112c64ed67d2678b949eea2ad7e9 in / 
# Thu, 25 Mar 2021 22:56:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:57:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:57:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:59:22 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:57:32 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 26 Mar 2021 14:58:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:58:33 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 26 Mar 2021 15:02:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c51b7afed4911a4eefdf02c44ee440de726a5a605c5507cc50d4795394b418c2';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='dfe87d34c40cd0c23dc4b7ee47c85f84e26d21ff75476b234998bb9132379659';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bbc55934ec867290cd9307422beae48e5032dfabb7cb496bed6e47b7ab3f90be';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='a1ed2722f283a3f3eb0a71f23354b0b4d2761865e759a3bf7f89297e17c20e6f';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c2ddf185daafacd0b50f3e4e593d613b2e9b70d66b88a8da6ee313181376aef6';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Mar 2021 15:02:33 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Mon, 05 Apr 2021 17:31:15 GMT
ARG MAVEN_VERSION=3.8.1
# Mon, 05 Apr 2021 17:31:22 GMT
ARG USER_HOME_DIR=/root
# Mon, 05 Apr 2021 17:31:27 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Mon, 05 Apr 2021 17:31:33 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Mon, 05 Apr 2021 17:32:52 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN apt-get update && apt-get install -y curl   && mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 05 Apr 2021 17:32:57 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 05 Apr 2021 17:32:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 05 Apr 2021 17:33:00 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 05 Apr 2021 17:33:01 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 05 Apr 2021 17:33:05 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 05 Apr 2021 17:33:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5ade347cf74df0ad62b82c57b0a6f0411ef9ecad9336a99c9e116ee5d1ff3d82`  
		Last Modified: Thu, 25 Mar 2021 23:15:40 GMT  
		Size: 30.4 MB (30423262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918394a3ae216a0c5018f2cb9895614a0b9689fca3efc24700f5e1b1866273ad`  
		Last Modified: Thu, 25 Mar 2021 23:15:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5795a499c24598e294527992a703053ab615879af048f3b809a3ad86141684d`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746a8b760dceb1369716f09f0677ac6e4c109c24e134a9c883c7e48e1ee0d081`  
		Last Modified: Fri, 26 Mar 2021 15:03:04 GMT  
		Size: 3.1 MB (3082734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f177ef92bfa2c096f2186bb3e01694633a997fb0eb3feaa5c18e869c21009ad1`  
		Last Modified: Fri, 26 Mar 2021 15:04:19 GMT  
		Size: 167.7 MB (167715540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a261a23194016632fd62d3816014089b60ec216cf24e5d741951ff7f7f497f`  
		Last Modified: Mon, 05 Apr 2021 17:36:17 GMT  
		Size: 34.4 MB (34398411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe13a2fb2bea445f02895a8ba339fb1ef993a01ead05cf272dd083e1fca83bc7`  
		Last Modified: Mon, 05 Apr 2021 17:36:12 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c615da99187a899b74138601ad4605d513c7a746249a806ee2870768e2348b`  
		Last Modified: Mon, 05 Apr 2021 17:36:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibmjava` - linux; s390x

```console
$ docker pull maven@sha256:569a1c3e27edc795aa566fe2abe92c324c62c4cbd6d75cbd36c8738969dec29a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218826317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a513dcf6becbd40e263e2342d0cef5008c864b72c71996f615c0c85cd614287`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:00 GMT
ADD file:5e61a5300d520d61a2130623465ba2e46da8e80dc2afa042473a42cbcd8d88d2 in / 
# Fri, 23 Apr 2021 21:45:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:05 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:07 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:25:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 22:25:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:25:17 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 22:28:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c51b7afed4911a4eefdf02c44ee440de726a5a605c5507cc50d4795394b418c2';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='dfe87d34c40cd0c23dc4b7ee47c85f84e26d21ff75476b234998bb9132379659';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bbc55934ec867290cd9307422beae48e5032dfabb7cb496bed6e47b7ab3f90be';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='a1ed2722f283a3f3eb0a71f23354b0b4d2761865e759a3bf7f89297e17c20e6f';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c2ddf185daafacd0b50f3e4e593d613b2e9b70d66b88a8da6ee313181376aef6';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 22:28:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:13:09 GMT
ARG MAVEN_VERSION=3.8.1
# Fri, 23 Apr 2021 23:13:10 GMT
ARG USER_HOME_DIR=/root
# Fri, 23 Apr 2021 23:13:10 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Fri, 23 Apr 2021 23:13:11 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Fri, 23 Apr 2021 23:13:31 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN apt-get update && apt-get install -y curl   && mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 23 Apr 2021 23:13:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 23 Apr 2021 23:13:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 23 Apr 2021 23:13:36 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 23 Apr 2021 23:13:36 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 23 Apr 2021 23:13:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 23 Apr 2021 23:13:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:33ddddc4572ffe1f294f9f599ed989cc41eee5da4cdcf7db12d10700aa8c894e`  
		Last Modified: Fri, 23 Apr 2021 21:47:03 GMT  
		Size: 25.4 MB (25352756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4395f372a786db91b2f50dc8e43d8b7c3533eb4bd86f6728eb2a0c7108c077d2`  
		Last Modified: Fri, 23 Apr 2021 21:46:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e39753730df188282ca8193f14bbbb8cbe0b76ec02b34283a28449b1e41c05`  
		Last Modified: Fri, 23 Apr 2021 21:47:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93b87da546ac7aa6705cd2f20bfe70cf04793ac73561e5dd8c579af88754aec`  
		Last Modified: Fri, 23 Apr 2021 22:28:41 GMT  
		Size: 2.7 MB (2676643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18c1e96adf75ae238488fd2f91294e27181f02520c837b3b4b53cc603a7fd7d`  
		Last Modified: Fri, 23 Apr 2021 22:29:22 GMT  
		Size: 158.3 MB (158332137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02997c8f11c33211748b0e705925ef8f9667819557d80862f37f4a745530d050`  
		Last Modified: Fri, 23 Apr 2021 23:16:27 GMT  
		Size: 32.5 MB (32462527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043fd71a0e14cff8323115d69135c124011e0f0512ac4ef3989a514f0993f9ce`  
		Last Modified: Fri, 23 Apr 2021 23:16:23 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d553732fa296a833fa1efdc55a25dc3f323bc88f563abd2e7dcfc4bee878ec7d`  
		Last Modified: Fri, 23 Apr 2021 23:16:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
