## `maven:3-ibmjava`

```console
$ docker pull maven@sha256:1378c4ace6b6106eb33a9f745a4ded742366774f8318cc37f200d920355ef1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `maven:3-ibmjava` - linux; amd64

```console
$ docker pull maven@sha256:8c57b99dfb0cf019836bd7aa5bdb20b2e47fa8c36da4a9c45699d32b48f24294
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (235952843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e9ce0be72c6016bfb4d1defae0bee5ffec0ffb528b4f8f56d706441972b8c1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 21 Jan 2021 03:37:59 GMT
ADD file:ef36fee25b0bd1d99979ecb8d54b206cec33d4e8fd2232189f0d8e5ab9754798 in / 
# Thu, 21 Jan 2021 03:38:01 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:38:03 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:38:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:38:05 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 08:57:29 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 21 Jan 2021 08:57:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 23:19:44 GMT
ENV JAVA_VERSION=1.8.0_sr6fp25
# Fri, 12 Feb 2021 23:23:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='066ce6f0b3fe7f9c84e41b4e63f36e83928f7166f7805633741b95dbfd4a1871';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='aedc0bf42ad9dac10e789c8fb8984250d338cbe111683c75c3b5b87f36a9f40a';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f0db52030e38d18d087138c7eea628975af034e381afda101b35d568e0a81230';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='fb4cfdab31d39f060d32a9aa349ae4bd5e12e76164ab938d476e6fe864af7776';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='9357f54317ad62ea4223edcb2d0ca44dbdc153877b6ef077f21fbf462b8288f5';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:23:21 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 13 Feb 2021 00:54:27 GMT
ARG MAVEN_VERSION=3.6.3
# Sat, 13 Feb 2021 00:54:27 GMT
ARG USER_HOME_DIR=/root
# Sat, 13 Feb 2021 00:54:27 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Sat, 13 Feb 2021 00:54:28 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Sat, 13 Feb 2021 00:54:41 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN apt-get update && apt-get install -y curl   && mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Sat, 13 Feb 2021 00:54:42 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 13 Feb 2021 00:54:42 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 13 Feb 2021 00:54:42 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Sat, 13 Feb 2021 00:54:42 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Sat, 13 Feb 2021 00:54:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 13 Feb 2021 00:54:43 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d519e2592276828ca171d85e0532899cd4f98c70f5c697b45fa2e126e9f9fe49`  
		Last Modified: Thu, 21 Jan 2021 03:40:27 GMT  
		Size: 26.7 MB (26709716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22d2dfcfa9cd230ed3c47defec2670d45081598c721dd85cafc34ea459f970e`  
		Last Modified: Thu, 21 Jan 2021 03:40:17 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3afe92c540b778c64ca316d1e679d55d2d2e812e450f516a808ee591f0c3f77`  
		Last Modified: Thu, 21 Jan 2021 03:40:17 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b819c4184ad93f8a53b96dc021e208287e23a140e45bca99950d7b043ed9fd12`  
		Last Modified: Thu, 21 Jan 2021 09:00:33 GMT  
		Size: 3.0 MB (2975222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6d8c73c7bafca67448b116e719f1f7c7caba284372690df339f04bbbe77e1d`  
		Last Modified: Fri, 12 Feb 2021 23:25:50 GMT  
		Size: 168.0 MB (167975111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ed475afbaba60a4f854a18b4873f8c51a022a70c80d13336249e0d322ac37c`  
		Last Modified: Sat, 13 Feb 2021 00:58:03 GMT  
		Size: 38.3 MB (38290568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5331da2ed1324dc18f3e8557cf73d5b45900673ea0a1da61a538443a03b8b4`  
		Last Modified: Sat, 13 Feb 2021 00:57:57 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85226f0c8fb64e27d3bbf558e352d55e0c2e72297add8a9e4580f01e594d077c`  
		Last Modified: Sat, 13 Feb 2021 00:57:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibmjava` - linux; 386

```console
$ docker pull maven@sha256:744f2718414d7b61d098fd65aaede8a036ec7abda35f8c4aafdf1a749beb58b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223085591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86793b0aafd6d171d9a441764c570211e2376a562950cdb59558c5defc4d049b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 21 Jan 2021 03:44:18 GMT
ADD file:01b59ee8b65705b370ca0ae3515a429e8cbb9ab8fb22cce728108feff4ab182d in / 
# Thu, 21 Jan 2021 03:44:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:44:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:44:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:44:21 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:23:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 21 Jan 2021 04:23:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 23:38:30 GMT
ENV JAVA_VERSION=1.8.0_sr6fp25
# Fri, 12 Feb 2021 23:40:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='066ce6f0b3fe7f9c84e41b4e63f36e83928f7166f7805633741b95dbfd4a1871';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='aedc0bf42ad9dac10e789c8fb8984250d338cbe111683c75c3b5b87f36a9f40a';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f0db52030e38d18d087138c7eea628975af034e381afda101b35d568e0a81230';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='fb4cfdab31d39f060d32a9aa349ae4bd5e12e76164ab938d476e6fe864af7776';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='9357f54317ad62ea4223edcb2d0ca44dbdc153877b6ef077f21fbf462b8288f5';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:40:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 13 Feb 2021 01:02:39 GMT
ARG MAVEN_VERSION=3.6.3
# Sat, 13 Feb 2021 01:02:40 GMT
ARG USER_HOME_DIR=/root
# Sat, 13 Feb 2021 01:02:40 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Sat, 13 Feb 2021 01:02:40 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Sat, 13 Feb 2021 01:02:54 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN apt-get update && apt-get install -y curl   && mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Sat, 13 Feb 2021 01:02:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 13 Feb 2021 01:02:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 13 Feb 2021 01:02:55 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Sat, 13 Feb 2021 01:02:55 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Sat, 13 Feb 2021 01:02:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 13 Feb 2021 01:02:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a392d9ac4da4a6bfef8e4b1a5b3d67f0903ca47c0e6be7c0fa2d1207ea4ebc33`  
		Last Modified: Thu, 21 Jan 2021 03:45:04 GMT  
		Size: 27.1 MB (27137859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf47d4a0f4a9097aa0700057361f5bed24133938a630ee7fa36bef895bae976`  
		Last Modified: Thu, 21 Jan 2021 03:44:58 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d12f528b6dd5a2c96b3770017f558a77a79d82870a18293fc7d88afec2b52f`  
		Last Modified: Thu, 21 Jan 2021 03:44:58 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1145eae9404f424e7e41a234071086cd229f76465a493e0a5124e249263bfcd9`  
		Last Modified: Thu, 21 Jan 2021 04:26:13 GMT  
		Size: 3.0 MB (3002689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f458be8e107516ca5fbc770b62d687d0f6dff3ad64ede57ac059076f999823`  
		Last Modified: Fri, 12 Feb 2021 23:42:17 GMT  
		Size: 156.2 MB (156163136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c993fff56b24cbf179ed27f38197a6585979c9aad8c5cd096a03a6e0c9d8c69`  
		Last Modified: Sat, 13 Feb 2021 01:03:15 GMT  
		Size: 36.8 MB (36779686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1b12a2dc0dd86ea14f14aa691de1d09f84c1283a194c3824ca6db54eb4d9fe`  
		Last Modified: Sat, 13 Feb 2021 01:03:09 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e4a2570df42a6dd241cf0b4bcf930d547361dd2872665911e2b90ebf06ccc`  
		Last Modified: Sat, 13 Feb 2021 01:03:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibmjava` - linux; ppc64le

```console
$ docker pull maven@sha256:b4fad0b4658cd2e157a8469349f260cf371163ea989a689a847895db486ef8da
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (234969357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd4db204e7d81caa4005b147b5da8eb427ca03626aafcc7c5b8382135892831`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:03 GMT
ADD file:f6214eb5991df55aa5198d84442d6ddd28b67d4043d1832afba8b30e0249dcf5 in / 
# Thu, 21 Jan 2021 03:49:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:50:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:44:44 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 21 Jan 2021 05:45:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:45:22 GMT
ENV JAVA_VERSION=1.8.0_sr6fp20
# Thu, 21 Jan 2021 05:49:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='367a777afa71945eeaf623ff4f04d5dcd930eac2c1a234adbba4afe2d88926c1';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='a0e7eb3a68c2883e62b4a34e45c59c3f2880cfe57dbff09484c6b18fc2925e68';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4a7ac4712548d7630f2471a067406c94c3846fff75a0afc660682129dcf80e5b';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e6b476694cef95a2653a823dc5ed8e662ea08c975fe8564672385b5346ba29fe';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='17fad00b25231a85d15d681db2329f54d95cab48c1bab6bcd23b6306ad60d785';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 21 Jan 2021 05:49:21 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 21 Jan 2021 09:50:20 GMT
ARG MAVEN_VERSION=3.6.3
# Thu, 21 Jan 2021 09:50:24 GMT
ARG USER_HOME_DIR=/root
# Thu, 21 Jan 2021 09:50:30 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Thu, 21 Jan 2021 09:50:36 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Thu, 21 Jan 2021 09:51:54 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN apt-get update && apt-get install -y curl   && mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 21 Jan 2021 09:51:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 21 Jan 2021 09:52:04 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 21 Jan 2021 09:52:06 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 21 Jan 2021 09:52:12 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 21 Jan 2021 09:52:16 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 21 Jan 2021 09:52:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e07786faec2ce77c08f20befe52a3eac52d983b0dfae9cb8d58dfa0ede0648e1`  
		Last Modified: Thu, 21 Jan 2021 03:54:37 GMT  
		Size: 30.4 MB (30422854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a41aaf71d5cf82fa1f9e11d2d352906ae135d0b216c665ed76ad9a8e1ce046`  
		Last Modified: Thu, 21 Jan 2021 03:54:30 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc53e2219c78f010d93258041f54f396b471d272d99ada00f64b9061b456a440`  
		Last Modified: Thu, 21 Jan 2021 05:49:42 GMT  
		Size: 3.1 MB (3099342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df14aa719358219c5f53d1310a2fe249022d62d0385a39f7be48175776b580ca`  
		Last Modified: Thu, 21 Jan 2021 05:50:59 GMT  
		Size: 167.2 MB (167191465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ba0f2f3a5cd5fdb17c439a864e68224a548ed57f7e2b33932f530fff6d45ca`  
		Last Modified: Thu, 21 Jan 2021 09:57:40 GMT  
		Size: 34.3 MB (34253438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7b22908ed33fd113608b238cfd4cfd69350ef6a54a0d8c5bf747fcc7b2e54c`  
		Last Modified: Thu, 21 Jan 2021 09:57:35 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096e4035f17f9f3d3c384e98a2cf78efdd423117262282c76b762db69fe8eba4`  
		Last Modified: Thu, 21 Jan 2021 09:57:35 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibmjava` - linux; s390x

```console
$ docker pull maven@sha256:77ba0996c6b6610fc6a966021513d0cb34faadac32250e9a122dfc08d4cd64e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218723575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9938ffba060b331a4ecdcb92cd40fd3f449ddbb6f6822a044ea3ea5008a1cb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 21 Jan 2021 04:00:45 GMT
ADD file:d443bbf06b974365e3cb2d99eea08d454059cf95b82a6023e4260fba5ead568e in / 
# Thu, 21 Jan 2021 04:00:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 04:00:53 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 04:00:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 04:00:56 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:33:11 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 21 Jan 2021 04:33:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 12 Feb 2021 22:41:51 GMT
ENV JAVA_VERSION=1.8.0_sr6fp25
# Fri, 12 Feb 2021 22:45:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='066ce6f0b3fe7f9c84e41b4e63f36e83928f7166f7805633741b95dbfd4a1871';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='aedc0bf42ad9dac10e789c8fb8984250d338cbe111683c75c3b5b87f36a9f40a';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f0db52030e38d18d087138c7eea628975af034e381afda101b35d568e0a81230';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='fb4cfdab31d39f060d32a9aa349ae4bd5e12e76164ab938d476e6fe864af7776';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='9357f54317ad62ea4223edcb2d0ca44dbdc153877b6ef077f21fbf462b8288f5';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 22:45:11 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 12 Feb 2021 23:07:56 GMT
ARG MAVEN_VERSION=3.6.3
# Fri, 12 Feb 2021 23:07:56 GMT
ARG USER_HOME_DIR=/root
# Fri, 12 Feb 2021 23:07:57 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Fri, 12 Feb 2021 23:07:57 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Fri, 12 Feb 2021 23:08:17 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN apt-get update && apt-get install -y curl   && mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 12 Feb 2021 23:08:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 12 Feb 2021 23:08:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 12 Feb 2021 23:08:18 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 12 Feb 2021 23:08:18 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 12 Feb 2021 23:08:19 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 12 Feb 2021 23:08:19 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1a4e1c3f599543fe1043f321c3c5e14f5ca6073cba211f2144b569c5d0cff014`  
		Last Modified: Thu, 21 Jan 2021 04:03:17 GMT  
		Size: 25.4 MB (25381801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1202f2791a7390dbd7197d4cfde724e184be1b2f9d4791890fb64341336f889e`  
		Last Modified: Thu, 21 Jan 2021 04:03:13 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c44bad24828f92a8ff703d4d356f2969f0c1de9f6d852d3cec338a3aff6265`  
		Last Modified: Thu, 21 Jan 2021 04:03:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0790b1b850d834bc1ab5fc092fd86cfa28871f179c73453c07e80e721245333`  
		Last Modified: Thu, 21 Jan 2021 04:38:09 GMT  
		Size: 2.7 MB (2689532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53607955aecd64901c1ed0f9b3fe2d3a3472564de2b287bab6a45d3a8b746fe`  
		Last Modified: Fri, 12 Feb 2021 22:48:55 GMT  
		Size: 158.3 MB (158320550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3f85960489105188109e4811a472ef219df78f3b4e0a155e060b707b2badcb`  
		Last Modified: Fri, 12 Feb 2021 23:09:34 GMT  
		Size: 32.3 MB (32329435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7668921447b37ec02d56a68661e14cbb9924cfff4d6326dd76b4ebdb0023d3a`  
		Last Modified: Fri, 12 Feb 2021 23:09:33 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f890e22457c384c1a162451a04841041e08cc801637a8a9c949403d5c54c08`  
		Last Modified: Fri, 12 Feb 2021 23:09:33 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
