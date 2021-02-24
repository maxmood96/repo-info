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
$ docker pull ibmjava@sha256:2c6cd9177a88637190cf657f22c3bb2eceeb0d73cec1cc26dbb2379899da4aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8` - linux; amd64

```console
$ docker pull ibmjava@sha256:af9bc54a0d4cc90293b9f0bea2b5de5b041d82bf47d2ef7abf7d20d6876b4cfe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160484786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389ecb927a709242b9256a4c061ff0478ae04984dd8f49f1ba5471737b7416df`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:20:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c613955f0130f9e637806f71660c6308e37e2e9abd8456e8216bc7de9eb9ea54';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='4778c7f8a899544ab7ace0777c909b25c9bfcb1ced326fac7dd7feface308e5e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc69a3c2baadcaf23fa0dd3d334d98406a1df0e5a0899ea16b7185807adb6f66';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2d15b35966d94c86227f32f90e9fe2ffdea76e1c355cb12276097318dfdf2841';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='683164578e9c4b0e6a3b6d2c56fc4b68f4a07f0c4183b522cdae4dbca8f4e092';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:20:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:20157353ec7111dde6e7fce5da89f68c27dc333aa9de4f335e6d94169204d888`  
		Last Modified: Fri, 12 Feb 2021 23:24:50 GMT  
		Size: 130.8 MB (130798834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; 386

```console
$ docker pull ibmjava@sha256:9e161eb4163d931d2c8c7c15299ccbaa8c5af361f049baa7c7c82456762a9718
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149224860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b543967d11718c5c13d3d3e19c4c4d6f52e42d5d7097dab86a31560acf379da4`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:39:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c613955f0130f9e637806f71660c6308e37e2e9abd8456e8216bc7de9eb9ea54';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='4778c7f8a899544ab7ace0777c909b25c9bfcb1ced326fac7dd7feface308e5e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc69a3c2baadcaf23fa0dd3d334d98406a1df0e5a0899ea16b7185807adb6f66';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2d15b35966d94c86227f32f90e9fe2ffdea76e1c355cb12276097318dfdf2841';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='683164578e9c4b0e6a3b6d2c56fc4b68f4a07f0c4183b522cdae4dbca8f4e092';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:39:14 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:1e659622b5c16ae75cd24db8fa8ebd49382d4a178adcae4bbcf14fe325767d70`  
		Last Modified: Fri, 12 Feb 2021 23:41:36 GMT  
		Size: 119.1 MB (119083300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:63b2acbbe813870cc0c24e25eb3fa9c460b84f1b19769d7279ff9cc07221a393
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.9 MB (163913108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c11f12841754a487aa17a14d08fa5c18c7e0ecf7059d3b14056d1ccf5393c78`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:16:36 GMT
ENV JAVA_VERSION=1.8.0_sr6fp25
# Fri, 12 Feb 2021 23:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c613955f0130f9e637806f71660c6308e37e2e9abd8456e8216bc7de9eb9ea54';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='4778c7f8a899544ab7ace0777c909b25c9bfcb1ced326fac7dd7feface308e5e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc69a3c2baadcaf23fa0dd3d334d98406a1df0e5a0899ea16b7185807adb6f66';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2d15b35966d94c86227f32f90e9fe2ffdea76e1c355cb12276097318dfdf2841';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='683164578e9c4b0e6a3b6d2c56fc4b68f4a07f0c4183b522cdae4dbca8f4e092';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:18:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:4e68dba75f02a9912d3b4a33c590489355af49cc83e2b23446dc603f8ecfcad7`  
		Last Modified: Fri, 12 Feb 2021 23:21:41 GMT  
		Size: 130.4 MB (130389868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:965303da822076f685f14526c62ec5001a567a8b66f276207360e497cf8c60c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156127225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1527a1d2b2be75662941059161cbddac711d672e5bc01626165adbf84f0fda67`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 22:42:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c613955f0130f9e637806f71660c6308e37e2e9abd8456e8216bc7de9eb9ea54';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='4778c7f8a899544ab7ace0777c909b25c9bfcb1ced326fac7dd7feface308e5e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc69a3c2baadcaf23fa0dd3d334d98406a1df0e5a0899ea16b7185807adb6f66';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2d15b35966d94c86227f32f90e9fe2ffdea76e1c355cb12276097318dfdf2841';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='683164578e9c4b0e6a3b6d2c56fc4b68f4a07f0c4183b522cdae4dbca8f4e092';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 22:42:53 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:9bb05fb5db6f0d88f3e847293d61d3ebc205b3036a2916f29b574f85e3c3f4b9`  
		Last Modified: Fri, 12 Feb 2021 22:45:50 GMT  
		Size: 128.1 MB (128054850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:2c6cd9177a88637190cf657f22c3bb2eceeb0d73cec1cc26dbb2379899da4aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:af9bc54a0d4cc90293b9f0bea2b5de5b041d82bf47d2ef7abf7d20d6876b4cfe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160484786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389ecb927a709242b9256a4c061ff0478ae04984dd8f49f1ba5471737b7416df`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:20:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c613955f0130f9e637806f71660c6308e37e2e9abd8456e8216bc7de9eb9ea54';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='4778c7f8a899544ab7ace0777c909b25c9bfcb1ced326fac7dd7feface308e5e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc69a3c2baadcaf23fa0dd3d334d98406a1df0e5a0899ea16b7185807adb6f66';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2d15b35966d94c86227f32f90e9fe2ffdea76e1c355cb12276097318dfdf2841';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='683164578e9c4b0e6a3b6d2c56fc4b68f4a07f0c4183b522cdae4dbca8f4e092';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:20:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:20157353ec7111dde6e7fce5da89f68c27dc333aa9de4f335e6d94169204d888`  
		Last Modified: Fri, 12 Feb 2021 23:24:50 GMT  
		Size: 130.8 MB (130798834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; 386

```console
$ docker pull ibmjava@sha256:9e161eb4163d931d2c8c7c15299ccbaa8c5af361f049baa7c7c82456762a9718
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149224860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b543967d11718c5c13d3d3e19c4c4d6f52e42d5d7097dab86a31560acf379da4`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:39:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c613955f0130f9e637806f71660c6308e37e2e9abd8456e8216bc7de9eb9ea54';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='4778c7f8a899544ab7ace0777c909b25c9bfcb1ced326fac7dd7feface308e5e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc69a3c2baadcaf23fa0dd3d334d98406a1df0e5a0899ea16b7185807adb6f66';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2d15b35966d94c86227f32f90e9fe2ffdea76e1c355cb12276097318dfdf2841';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='683164578e9c4b0e6a3b6d2c56fc4b68f4a07f0c4183b522cdae4dbca8f4e092';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:39:14 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:1e659622b5c16ae75cd24db8fa8ebd49382d4a178adcae4bbcf14fe325767d70`  
		Last Modified: Fri, 12 Feb 2021 23:41:36 GMT  
		Size: 119.1 MB (119083300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:63b2acbbe813870cc0c24e25eb3fa9c460b84f1b19769d7279ff9cc07221a393
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.9 MB (163913108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c11f12841754a487aa17a14d08fa5c18c7e0ecf7059d3b14056d1ccf5393c78`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:16:36 GMT
ENV JAVA_VERSION=1.8.0_sr6fp25
# Fri, 12 Feb 2021 23:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c613955f0130f9e637806f71660c6308e37e2e9abd8456e8216bc7de9eb9ea54';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='4778c7f8a899544ab7ace0777c909b25c9bfcb1ced326fac7dd7feface308e5e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc69a3c2baadcaf23fa0dd3d334d98406a1df0e5a0899ea16b7185807adb6f66';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2d15b35966d94c86227f32f90e9fe2ffdea76e1c355cb12276097318dfdf2841';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='683164578e9c4b0e6a3b6d2c56fc4b68f4a07f0c4183b522cdae4dbca8f4e092';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:18:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:4e68dba75f02a9912d3b4a33c590489355af49cc83e2b23446dc603f8ecfcad7`  
		Last Modified: Fri, 12 Feb 2021 23:21:41 GMT  
		Size: 130.4 MB (130389868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:965303da822076f685f14526c62ec5001a567a8b66f276207360e497cf8c60c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156127225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1527a1d2b2be75662941059161cbddac711d672e5bc01626165adbf84f0fda67`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 22:42:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c613955f0130f9e637806f71660c6308e37e2e9abd8456e8216bc7de9eb9ea54';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='4778c7f8a899544ab7ace0777c909b25c9bfcb1ced326fac7dd7feface308e5e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc69a3c2baadcaf23fa0dd3d334d98406a1df0e5a0899ea16b7185807adb6f66';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2d15b35966d94c86227f32f90e9fe2ffdea76e1c355cb12276097318dfdf2841';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='683164578e9c4b0e6a3b6d2c56fc4b68f4a07f0c4183b522cdae4dbca8f4e092';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 22:42:53 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:9bb05fb5db6f0d88f3e847293d61d3ebc205b3036a2916f29b574f85e3c3f4b9`  
		Last Modified: Fri, 12 Feb 2021 22:45:50 GMT  
		Size: 128.1 MB (128054850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-jre-alpine`

```console
$ docker pull ibmjava@sha256:403099d7943ae7e5fe369982b1c02354293cb09ea1323c9470a9a58e8d2637f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:8-jre-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:ed4a622e366528f4758019560fe31ce16ee349a0bd070c064c29a13b6fcceebd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139166300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823f0fe3f66b4cf09e2bba93c294509b0aecabc896edab2eed09b7c433aeaf2b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 22:03:57 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 24 Feb 2021 22:03:58 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Wed, 24 Feb 2021 22:04:12 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Wed, 24 Feb 2021 22:04:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp25
# Wed, 24 Feb 2021 22:05:03 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c613955f0130f9e637806f71660c6308e37e2e9abd8456e8216bc7de9eb9ea54';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='4778c7f8a899544ab7ace0777c909b25c9bfcb1ced326fac7dd7feface308e5e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc69a3c2baadcaf23fa0dd3d334d98406a1df0e5a0899ea16b7185807adb6f66';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2d15b35966d94c86227f32f90e9fe2ffdea76e1c355cb12276097318dfdf2841';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='683164578e9c4b0e6a3b6d2c56fc4b68f4a07f0c4183b522cdae4dbca8f4e092';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Wed, 24 Feb 2021 22:05:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f834324fbf093cb517d09789e6a0bc4b51f0514fd03332ecdce7c4472a040e`  
		Last Modified: Wed, 24 Feb 2021 22:07:49 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bb308e1feeb83d59c875ad7f4655d6205e9493115588f2b0811f655c776fd8`  
		Last Modified: Wed, 24 Feb 2021 22:07:50 GMT  
		Size: 5.5 MB (5539664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431cf6555b6a322e4a85b4b543208d10c777202b668a4ed269e70a272f8b1b4`  
		Last Modified: Wed, 24 Feb 2021 22:08:08 GMT  
		Size: 130.8 MB (130826602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:7ef8a1186c5ea86f1bd546a48da33b050bc317b9d7db9e9c5cccc676bf37eefc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:5ccd570189e996c16bbb5b254fb74e8711372de3b023406d6b627abba567204f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.7 MB (197661063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193716c57346419c0b23caef2ad7683c177c2ed51f7122a42804ed3c1ee0e2f1`
-	Default Command: `["\/bin\/bash"]`

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

### `ibmjava:8-sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:ee2f1f36db4766e66af0c838b5b27171445ba13e795645f362ddfd7a9f58ffb6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186304696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ddebb30b0ae5c801ef209a1769e2b3e4f5b020f537324a88f2ec32ba55baa1c`
-	Default Command: `["\/bin\/bash"]`

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

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:4161fc57923c439491bcd3a1f24682145f4f1f3d3e17dcee712e17733d4c94b7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201223546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3c8549b745f925286a896e86dfe29b8759653d022ab82067f6935ba93b7653`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:16:36 GMT
ENV JAVA_VERSION=1.8.0_sr6fp25
# Fri, 12 Feb 2021 23:20:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='066ce6f0b3fe7f9c84e41b4e63f36e83928f7166f7805633741b95dbfd4a1871';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='aedc0bf42ad9dac10e789c8fb8984250d338cbe111683c75c3b5b87f36a9f40a';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f0db52030e38d18d087138c7eea628975af034e381afda101b35d568e0a81230';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='fb4cfdab31d39f060d32a9aa349ae4bd5e12e76164ab938d476e6fe864af7776';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='9357f54317ad62ea4223edcb2d0ca44dbdc153877b6ef077f21fbf462b8288f5';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:20:53 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:311c7fc53e130f9c64d45f18a03cf24934dda2c2539a2b3d1add64363fa065fa`  
		Last Modified: Fri, 12 Feb 2021 23:22:36 GMT  
		Size: 167.7 MB (167700306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:0fabee175ca3b8a042355a913af89afe20de331368e8ca9b0f30afa960d8fd61
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.4 MB (186392925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba40cb4614ebcdd1653f36ec59c9f3a9cf48b920c7dd8eb1ea73016f493b0b3c`
-	Default Command: `["\/bin\/bash"]`

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

## `ibmjava:8-sdk-alpine`

```console
$ docker pull ibmjava@sha256:b0a0515607d3ba3bdb737446d099f9fb7f2868bc466fbf94ff0a686d23377c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:8-sdk-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:946809342e0a2f5803707f33f20238db55f6664b1ccf72e31decebfe7306406e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176335857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63469096d204cab9939e087b5ceca92f5e4a7dba6065c54c816d2d3a36997c03`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 22:03:57 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 24 Feb 2021 22:03:58 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Wed, 24 Feb 2021 22:04:12 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Wed, 24 Feb 2021 22:04:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp25
# Wed, 24 Feb 2021 22:07:08 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='066ce6f0b3fe7f9c84e41b4e63f36e83928f7166f7805633741b95dbfd4a1871';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='aedc0bf42ad9dac10e789c8fb8984250d338cbe111683c75c3b5b87f36a9f40a';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f0db52030e38d18d087138c7eea628975af034e381afda101b35d568e0a81230';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='fb4cfdab31d39f060d32a9aa349ae4bd5e12e76164ab938d476e6fe864af7776';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='9357f54317ad62ea4223edcb2d0ca44dbdc153877b6ef077f21fbf462b8288f5';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Wed, 24 Feb 2021 22:07:09 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f834324fbf093cb517d09789e6a0bc4b51f0514fd03332ecdce7c4472a040e`  
		Last Modified: Wed, 24 Feb 2021 22:07:49 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bb308e1feeb83d59c875ad7f4655d6205e9493115588f2b0811f655c776fd8`  
		Last Modified: Wed, 24 Feb 2021 22:07:50 GMT  
		Size: 5.5 MB (5539664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b24729f0b2c099fa990d5711349e892779534f2fe567c5b8230dd58300de3b6`  
		Last Modified: Wed, 24 Feb 2021 22:08:55 GMT  
		Size: 168.0 MB (167996159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:885f5dbaff061ff915ee3d7d107101de58e984171e475bea35f56d5f05f73dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:396bdc5ee3a67f984abfcd76e24a6f9f1d47a37a862c5587a90fa4fd55537f11
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93886793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4a8d7c8257308d681cf85cde9dd35c48bb6c0ed4c894c33407af8c1495aadd`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:21:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3188a3690c66210b1c2e40cd7dd30f09fd2ed359a37097ff252f28f13035678e';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='30b441dfe3b7aed59b79d8691254ffe55a94f5f63252e391acce5eacacd78b54';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='949e84ece359b09412a6a43b78fcc91b1bf605321db6e9bb19cfc7eb727eb270';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ff1b146367ae61869e342fb6b73c40ad966f199f854bb301ede6d06743f20b14';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='6893eb2913f25c593e4a9d8249e53f0287b4b210f22b331a9eebd6927fcec286';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:21:48 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:a9e27913465f1c663383afcc25034cfc81fd133786e2329bcba424be2d25bf04`  
		Last Modified: Fri, 12 Feb 2021 23:25:20 GMT  
		Size: 64.2 MB (64200841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:4e97a6d8c4dca4083d337c04f0abf58f15f210dea21fa68a5562556b5b123554
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93755375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae49c1e44c39c1dbdb5b60e7247a4e6af29bab33326520f7c84551382e43ab66`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:39:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3188a3690c66210b1c2e40cd7dd30f09fd2ed359a37097ff252f28f13035678e';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='30b441dfe3b7aed59b79d8691254ffe55a94f5f63252e391acce5eacacd78b54';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='949e84ece359b09412a6a43b78fcc91b1bf605321db6e9bb19cfc7eb727eb270';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ff1b146367ae61869e342fb6b73c40ad966f199f854bb301ede6d06743f20b14';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='6893eb2913f25c593e4a9d8249e53f0287b4b210f22b331a9eebd6927fcec286';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:39:58 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:6e710fdbf94a085c5167161f0719812f52cd44ce45c464faef283544a5f759ca`  
		Last Modified: Fri, 12 Feb 2021 23:41:53 GMT  
		Size: 63.6 MB (63613815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:bce53b2ffd72da54e9903cfdcbe3e6f0aed2e8ea5e6d9d2c368b32cbba1bbe78
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (97963514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a35eb528ae9775ab32908e00501032763934a6e3a89e43301c3ab8d4a14289`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:16:36 GMT
ENV JAVA_VERSION=1.8.0_sr6fp25
# Fri, 12 Feb 2021 23:19:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3188a3690c66210b1c2e40cd7dd30f09fd2ed359a37097ff252f28f13035678e';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='30b441dfe3b7aed59b79d8691254ffe55a94f5f63252e391acce5eacacd78b54';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='949e84ece359b09412a6a43b78fcc91b1bf605321db6e9bb19cfc7eb727eb270';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ff1b146367ae61869e342fb6b73c40ad966f199f854bb301ede6d06743f20b14';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='6893eb2913f25c593e4a9d8249e53f0287b4b210f22b331a9eebd6927fcec286';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:19:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:93cae72b5af2de73b5cad983f7d3d5a75cd7e16c4cf5716e2423a824b208fbdb`  
		Last Modified: Fri, 12 Feb 2021 23:22:06 GMT  
		Size: 64.4 MB (64440274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:56211a3a64ea1e22396ea499570a265243da9e9a47698f3187cc5b57a24f674f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93403195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a471e07dde3462aa7414231e62a24a8d06b54f5646b6bc423eec1b28f3adde0`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 22:43:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3188a3690c66210b1c2e40cd7dd30f09fd2ed359a37097ff252f28f13035678e';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='30b441dfe3b7aed59b79d8691254ffe55a94f5f63252e391acce5eacacd78b54';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='949e84ece359b09412a6a43b78fcc91b1bf605321db6e9bb19cfc7eb727eb270';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ff1b146367ae61869e342fb6b73c40ad966f199f854bb301ede6d06743f20b14';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='6893eb2913f25c593e4a9d8249e53f0287b4b210f22b331a9eebd6927fcec286';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 22:43:51 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:59079f60dce5f98065dfa2832a3559404ed831b2dd201ee5bb54e0eb9864e1ee`  
		Last Modified: Fri, 12 Feb 2021 22:47:41 GMT  
		Size: 65.3 MB (65330820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sfj-alpine`

```console
$ docker pull ibmjava@sha256:7b03c78f5ecc29438904acdfeb42be6074c5cfe2944c6e25e7f083ccd5be3d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:8-sfj-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:b474a0098aa285d1cd79513668e69e794cd77b5548ca7343245e9bfa3f56d48c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72556982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2440477f48a8a47e153c6d9792ebcd08e5efbf06c3a57e733536d7d56eba0d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 22:03:57 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 24 Feb 2021 22:03:58 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Wed, 24 Feb 2021 22:04:12 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Wed, 24 Feb 2021 22:04:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp25
# Wed, 24 Feb 2021 22:05:56 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3188a3690c66210b1c2e40cd7dd30f09fd2ed359a37097ff252f28f13035678e';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='30b441dfe3b7aed59b79d8691254ffe55a94f5f63252e391acce5eacacd78b54';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='949e84ece359b09412a6a43b78fcc91b1bf605321db6e9bb19cfc7eb727eb270';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ff1b146367ae61869e342fb6b73c40ad966f199f854bb301ede6d06743f20b14';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='6893eb2913f25c593e4a9d8249e53f0287b4b210f22b331a9eebd6927fcec286';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Wed, 24 Feb 2021 22:05:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f834324fbf093cb517d09789e6a0bc4b51f0514fd03332ecdce7c4472a040e`  
		Last Modified: Wed, 24 Feb 2021 22:07:49 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bb308e1feeb83d59c875ad7f4655d6205e9493115588f2b0811f655c776fd8`  
		Last Modified: Wed, 24 Feb 2021 22:07:50 GMT  
		Size: 5.5 MB (5539664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f068e0002533f89a6ea5afd9c26da5f201e0b700a31517b2561d3f89abec29`  
		Last Modified: Wed, 24 Feb 2021 22:08:25 GMT  
		Size: 64.2 MB (64217284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:2c6cd9177a88637190cf657f22c3bb2eceeb0d73cec1cc26dbb2379899da4aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:af9bc54a0d4cc90293b9f0bea2b5de5b041d82bf47d2ef7abf7d20d6876b4cfe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160484786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389ecb927a709242b9256a4c061ff0478ae04984dd8f49f1ba5471737b7416df`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:20:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c613955f0130f9e637806f71660c6308e37e2e9abd8456e8216bc7de9eb9ea54';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='4778c7f8a899544ab7ace0777c909b25c9bfcb1ced326fac7dd7feface308e5e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc69a3c2baadcaf23fa0dd3d334d98406a1df0e5a0899ea16b7185807adb6f66';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2d15b35966d94c86227f32f90e9fe2ffdea76e1c355cb12276097318dfdf2841';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='683164578e9c4b0e6a3b6d2c56fc4b68f4a07f0c4183b522cdae4dbca8f4e092';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:20:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:20157353ec7111dde6e7fce5da89f68c27dc333aa9de4f335e6d94169204d888`  
		Last Modified: Fri, 12 Feb 2021 23:24:50 GMT  
		Size: 130.8 MB (130798834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; 386

```console
$ docker pull ibmjava@sha256:9e161eb4163d931d2c8c7c15299ccbaa8c5af361f049baa7c7c82456762a9718
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149224860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b543967d11718c5c13d3d3e19c4c4d6f52e42d5d7097dab86a31560acf379da4`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:39:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c613955f0130f9e637806f71660c6308e37e2e9abd8456e8216bc7de9eb9ea54';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='4778c7f8a899544ab7ace0777c909b25c9bfcb1ced326fac7dd7feface308e5e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc69a3c2baadcaf23fa0dd3d334d98406a1df0e5a0899ea16b7185807adb6f66';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2d15b35966d94c86227f32f90e9fe2ffdea76e1c355cb12276097318dfdf2841';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='683164578e9c4b0e6a3b6d2c56fc4b68f4a07f0c4183b522cdae4dbca8f4e092';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:39:14 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:1e659622b5c16ae75cd24db8fa8ebd49382d4a178adcae4bbcf14fe325767d70`  
		Last Modified: Fri, 12 Feb 2021 23:41:36 GMT  
		Size: 119.1 MB (119083300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:63b2acbbe813870cc0c24e25eb3fa9c460b84f1b19769d7279ff9cc07221a393
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.9 MB (163913108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c11f12841754a487aa17a14d08fa5c18c7e0ecf7059d3b14056d1ccf5393c78`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:16:36 GMT
ENV JAVA_VERSION=1.8.0_sr6fp25
# Fri, 12 Feb 2021 23:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c613955f0130f9e637806f71660c6308e37e2e9abd8456e8216bc7de9eb9ea54';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='4778c7f8a899544ab7ace0777c909b25c9bfcb1ced326fac7dd7feface308e5e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc69a3c2baadcaf23fa0dd3d334d98406a1df0e5a0899ea16b7185807adb6f66';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2d15b35966d94c86227f32f90e9fe2ffdea76e1c355cb12276097318dfdf2841';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='683164578e9c4b0e6a3b6d2c56fc4b68f4a07f0c4183b522cdae4dbca8f4e092';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:18:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:4e68dba75f02a9912d3b4a33c590489355af49cc83e2b23446dc603f8ecfcad7`  
		Last Modified: Fri, 12 Feb 2021 23:21:41 GMT  
		Size: 130.4 MB (130389868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:965303da822076f685f14526c62ec5001a567a8b66f276207360e497cf8c60c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156127225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1527a1d2b2be75662941059161cbddac711d672e5bc01626165adbf84f0fda67`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 22:42:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c613955f0130f9e637806f71660c6308e37e2e9abd8456e8216bc7de9eb9ea54';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='4778c7f8a899544ab7ace0777c909b25c9bfcb1ced326fac7dd7feface308e5e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc69a3c2baadcaf23fa0dd3d334d98406a1df0e5a0899ea16b7185807adb6f66';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2d15b35966d94c86227f32f90e9fe2ffdea76e1c355cb12276097318dfdf2841';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='683164578e9c4b0e6a3b6d2c56fc4b68f4a07f0c4183b522cdae4dbca8f4e092';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 22:42:53 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:9bb05fb5db6f0d88f3e847293d61d3ebc205b3036a2916f29b574f85e3c3f4b9`  
		Last Modified: Fri, 12 Feb 2021 22:45:50 GMT  
		Size: 128.1 MB (128054850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:jre-alpine`

```console
$ docker pull ibmjava@sha256:403099d7943ae7e5fe369982b1c02354293cb09ea1323c9470a9a58e8d2637f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:jre-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:ed4a622e366528f4758019560fe31ce16ee349a0bd070c064c29a13b6fcceebd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139166300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823f0fe3f66b4cf09e2bba93c294509b0aecabc896edab2eed09b7c433aeaf2b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 22:03:57 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 24 Feb 2021 22:03:58 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Wed, 24 Feb 2021 22:04:12 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Wed, 24 Feb 2021 22:04:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp25
# Wed, 24 Feb 2021 22:05:03 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c613955f0130f9e637806f71660c6308e37e2e9abd8456e8216bc7de9eb9ea54';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='4778c7f8a899544ab7ace0777c909b25c9bfcb1ced326fac7dd7feface308e5e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc69a3c2baadcaf23fa0dd3d334d98406a1df0e5a0899ea16b7185807adb6f66';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2d15b35966d94c86227f32f90e9fe2ffdea76e1c355cb12276097318dfdf2841';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='683164578e9c4b0e6a3b6d2c56fc4b68f4a07f0c4183b522cdae4dbca8f4e092';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Wed, 24 Feb 2021 22:05:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f834324fbf093cb517d09789e6a0bc4b51f0514fd03332ecdce7c4472a040e`  
		Last Modified: Wed, 24 Feb 2021 22:07:49 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bb308e1feeb83d59c875ad7f4655d6205e9493115588f2b0811f655c776fd8`  
		Last Modified: Wed, 24 Feb 2021 22:07:50 GMT  
		Size: 5.5 MB (5539664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431cf6555b6a322e4a85b4b543208d10c777202b668a4ed269e70a272f8b1b4`  
		Last Modified: Wed, 24 Feb 2021 22:08:08 GMT  
		Size: 130.8 MB (130826602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:2c6cd9177a88637190cf657f22c3bb2eceeb0d73cec1cc26dbb2379899da4aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:latest` - linux; amd64

```console
$ docker pull ibmjava@sha256:af9bc54a0d4cc90293b9f0bea2b5de5b041d82bf47d2ef7abf7d20d6876b4cfe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160484786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389ecb927a709242b9256a4c061ff0478ae04984dd8f49f1ba5471737b7416df`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:20:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c613955f0130f9e637806f71660c6308e37e2e9abd8456e8216bc7de9eb9ea54';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='4778c7f8a899544ab7ace0777c909b25c9bfcb1ced326fac7dd7feface308e5e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc69a3c2baadcaf23fa0dd3d334d98406a1df0e5a0899ea16b7185807adb6f66';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2d15b35966d94c86227f32f90e9fe2ffdea76e1c355cb12276097318dfdf2841';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='683164578e9c4b0e6a3b6d2c56fc4b68f4a07f0c4183b522cdae4dbca8f4e092';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:20:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:20157353ec7111dde6e7fce5da89f68c27dc333aa9de4f335e6d94169204d888`  
		Last Modified: Fri, 12 Feb 2021 23:24:50 GMT  
		Size: 130.8 MB (130798834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; 386

```console
$ docker pull ibmjava@sha256:9e161eb4163d931d2c8c7c15299ccbaa8c5af361f049baa7c7c82456762a9718
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149224860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b543967d11718c5c13d3d3e19c4c4d6f52e42d5d7097dab86a31560acf379da4`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:39:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c613955f0130f9e637806f71660c6308e37e2e9abd8456e8216bc7de9eb9ea54';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='4778c7f8a899544ab7ace0777c909b25c9bfcb1ced326fac7dd7feface308e5e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc69a3c2baadcaf23fa0dd3d334d98406a1df0e5a0899ea16b7185807adb6f66';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2d15b35966d94c86227f32f90e9fe2ffdea76e1c355cb12276097318dfdf2841';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='683164578e9c4b0e6a3b6d2c56fc4b68f4a07f0c4183b522cdae4dbca8f4e092';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:39:14 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:1e659622b5c16ae75cd24db8fa8ebd49382d4a178adcae4bbcf14fe325767d70`  
		Last Modified: Fri, 12 Feb 2021 23:41:36 GMT  
		Size: 119.1 MB (119083300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:63b2acbbe813870cc0c24e25eb3fa9c460b84f1b19769d7279ff9cc07221a393
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.9 MB (163913108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c11f12841754a487aa17a14d08fa5c18c7e0ecf7059d3b14056d1ccf5393c78`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:16:36 GMT
ENV JAVA_VERSION=1.8.0_sr6fp25
# Fri, 12 Feb 2021 23:17:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c613955f0130f9e637806f71660c6308e37e2e9abd8456e8216bc7de9eb9ea54';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='4778c7f8a899544ab7ace0777c909b25c9bfcb1ced326fac7dd7feface308e5e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc69a3c2baadcaf23fa0dd3d334d98406a1df0e5a0899ea16b7185807adb6f66';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2d15b35966d94c86227f32f90e9fe2ffdea76e1c355cb12276097318dfdf2841';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='683164578e9c4b0e6a3b6d2c56fc4b68f4a07f0c4183b522cdae4dbca8f4e092';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:18:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:4e68dba75f02a9912d3b4a33c590489355af49cc83e2b23446dc603f8ecfcad7`  
		Last Modified: Fri, 12 Feb 2021 23:21:41 GMT  
		Size: 130.4 MB (130389868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:965303da822076f685f14526c62ec5001a567a8b66f276207360e497cf8c60c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156127225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1527a1d2b2be75662941059161cbddac711d672e5bc01626165adbf84f0fda67`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 22:42:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c613955f0130f9e637806f71660c6308e37e2e9abd8456e8216bc7de9eb9ea54';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='4778c7f8a899544ab7ace0777c909b25c9bfcb1ced326fac7dd7feface308e5e';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc69a3c2baadcaf23fa0dd3d334d98406a1df0e5a0899ea16b7185807adb6f66';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2d15b35966d94c86227f32f90e9fe2ffdea76e1c355cb12276097318dfdf2841';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='683164578e9c4b0e6a3b6d2c56fc4b68f4a07f0c4183b522cdae4dbca8f4e092';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 22:42:53 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:9bb05fb5db6f0d88f3e847293d61d3ebc205b3036a2916f29b574f85e3c3f4b9`  
		Last Modified: Fri, 12 Feb 2021 22:45:50 GMT  
		Size: 128.1 MB (128054850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:7ef8a1186c5ea86f1bd546a48da33b050bc317b9d7db9e9c5cccc676bf37eefc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:5ccd570189e996c16bbb5b254fb74e8711372de3b023406d6b627abba567204f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.7 MB (197661063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193716c57346419c0b23caef2ad7683c177c2ed51f7122a42804ed3c1ee0e2f1`
-	Default Command: `["\/bin\/bash"]`

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

### `ibmjava:sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:ee2f1f36db4766e66af0c838b5b27171445ba13e795645f362ddfd7a9f58ffb6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186304696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ddebb30b0ae5c801ef209a1769e2b3e4f5b020f537324a88f2ec32ba55baa1c`
-	Default Command: `["\/bin\/bash"]`

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

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:4161fc57923c439491bcd3a1f24682145f4f1f3d3e17dcee712e17733d4c94b7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201223546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3c8549b745f925286a896e86dfe29b8759653d022ab82067f6935ba93b7653`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:16:36 GMT
ENV JAVA_VERSION=1.8.0_sr6fp25
# Fri, 12 Feb 2021 23:20:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='066ce6f0b3fe7f9c84e41b4e63f36e83928f7166f7805633741b95dbfd4a1871';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='aedc0bf42ad9dac10e789c8fb8984250d338cbe111683c75c3b5b87f36a9f40a';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f0db52030e38d18d087138c7eea628975af034e381afda101b35d568e0a81230';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='fb4cfdab31d39f060d32a9aa349ae4bd5e12e76164ab938d476e6fe864af7776';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='9357f54317ad62ea4223edcb2d0ca44dbdc153877b6ef077f21fbf462b8288f5';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:20:53 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:311c7fc53e130f9c64d45f18a03cf24934dda2c2539a2b3d1add64363fa065fa`  
		Last Modified: Fri, 12 Feb 2021 23:22:36 GMT  
		Size: 167.7 MB (167700306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:0fabee175ca3b8a042355a913af89afe20de331368e8ca9b0f30afa960d8fd61
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.4 MB (186392925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba40cb4614ebcdd1653f36ec59c9f3a9cf48b920c7dd8eb1ea73016f493b0b3c`
-	Default Command: `["\/bin\/bash"]`

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

## `ibmjava:sdk-alpine`

```console
$ docker pull ibmjava@sha256:b0a0515607d3ba3bdb737446d099f9fb7f2868bc466fbf94ff0a686d23377c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:sdk-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:946809342e0a2f5803707f33f20238db55f6664b1ccf72e31decebfe7306406e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176335857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63469096d204cab9939e087b5ceca92f5e4a7dba6065c54c816d2d3a36997c03`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 22:03:57 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 24 Feb 2021 22:03:58 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Wed, 24 Feb 2021 22:04:12 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Wed, 24 Feb 2021 22:04:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp25
# Wed, 24 Feb 2021 22:07:08 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='066ce6f0b3fe7f9c84e41b4e63f36e83928f7166f7805633741b95dbfd4a1871';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='aedc0bf42ad9dac10e789c8fb8984250d338cbe111683c75c3b5b87f36a9f40a';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f0db52030e38d18d087138c7eea628975af034e381afda101b35d568e0a81230';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='fb4cfdab31d39f060d32a9aa349ae4bd5e12e76164ab938d476e6fe864af7776';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='9357f54317ad62ea4223edcb2d0ca44dbdc153877b6ef077f21fbf462b8288f5';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Wed, 24 Feb 2021 22:07:09 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f834324fbf093cb517d09789e6a0bc4b51f0514fd03332ecdce7c4472a040e`  
		Last Modified: Wed, 24 Feb 2021 22:07:49 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bb308e1feeb83d59c875ad7f4655d6205e9493115588f2b0811f655c776fd8`  
		Last Modified: Wed, 24 Feb 2021 22:07:50 GMT  
		Size: 5.5 MB (5539664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b24729f0b2c099fa990d5711349e892779534f2fe567c5b8230dd58300de3b6`  
		Last Modified: Wed, 24 Feb 2021 22:08:55 GMT  
		Size: 168.0 MB (167996159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:885f5dbaff061ff915ee3d7d107101de58e984171e475bea35f56d5f05f73dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:396bdc5ee3a67f984abfcd76e24a6f9f1d47a37a862c5587a90fa4fd55537f11
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93886793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4a8d7c8257308d681cf85cde9dd35c48bb6c0ed4c894c33407af8c1495aadd`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:21:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3188a3690c66210b1c2e40cd7dd30f09fd2ed359a37097ff252f28f13035678e';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='30b441dfe3b7aed59b79d8691254ffe55a94f5f63252e391acce5eacacd78b54';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='949e84ece359b09412a6a43b78fcc91b1bf605321db6e9bb19cfc7eb727eb270';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ff1b146367ae61869e342fb6b73c40ad966f199f854bb301ede6d06743f20b14';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='6893eb2913f25c593e4a9d8249e53f0287b4b210f22b331a9eebd6927fcec286';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:21:48 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:a9e27913465f1c663383afcc25034cfc81fd133786e2329bcba424be2d25bf04`  
		Last Modified: Fri, 12 Feb 2021 23:25:20 GMT  
		Size: 64.2 MB (64200841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:4e97a6d8c4dca4083d337c04f0abf58f15f210dea21fa68a5562556b5b123554
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93755375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae49c1e44c39c1dbdb5b60e7247a4e6af29bab33326520f7c84551382e43ab66`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:39:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3188a3690c66210b1c2e40cd7dd30f09fd2ed359a37097ff252f28f13035678e';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='30b441dfe3b7aed59b79d8691254ffe55a94f5f63252e391acce5eacacd78b54';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='949e84ece359b09412a6a43b78fcc91b1bf605321db6e9bb19cfc7eb727eb270';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ff1b146367ae61869e342fb6b73c40ad966f199f854bb301ede6d06743f20b14';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='6893eb2913f25c593e4a9d8249e53f0287b4b210f22b331a9eebd6927fcec286';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:39:58 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:6e710fdbf94a085c5167161f0719812f52cd44ce45c464faef283544a5f759ca`  
		Last Modified: Fri, 12 Feb 2021 23:41:53 GMT  
		Size: 63.6 MB (63613815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:bce53b2ffd72da54e9903cfdcbe3e6f0aed2e8ea5e6d9d2c368b32cbba1bbe78
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (97963514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a35eb528ae9775ab32908e00501032763934a6e3a89e43301c3ab8d4a14289`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 23:16:36 GMT
ENV JAVA_VERSION=1.8.0_sr6fp25
# Fri, 12 Feb 2021 23:19:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3188a3690c66210b1c2e40cd7dd30f09fd2ed359a37097ff252f28f13035678e';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='30b441dfe3b7aed59b79d8691254ffe55a94f5f63252e391acce5eacacd78b54';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='949e84ece359b09412a6a43b78fcc91b1bf605321db6e9bb19cfc7eb727eb270';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ff1b146367ae61869e342fb6b73c40ad966f199f854bb301ede6d06743f20b14';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='6893eb2913f25c593e4a9d8249e53f0287b4b210f22b331a9eebd6927fcec286';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 23:19:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:93cae72b5af2de73b5cad983f7d3d5a75cd7e16c4cf5716e2423a824b208fbdb`  
		Last Modified: Fri, 12 Feb 2021 23:22:06 GMT  
		Size: 64.4 MB (64440274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:56211a3a64ea1e22396ea499570a265243da9e9a47698f3187cc5b57a24f674f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93403195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a471e07dde3462aa7414231e62a24a8d06b54f5646b6bc423eec1b28f3adde0`
-	Default Command: `["\/bin\/bash"]`

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
# Fri, 12 Feb 2021 22:43:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3188a3690c66210b1c2e40cd7dd30f09fd2ed359a37097ff252f28f13035678e';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='30b441dfe3b7aed59b79d8691254ffe55a94f5f63252e391acce5eacacd78b54';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='949e84ece359b09412a6a43b78fcc91b1bf605321db6e9bb19cfc7eb727eb270';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ff1b146367ae61869e342fb6b73c40ad966f199f854bb301ede6d06743f20b14';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='6893eb2913f25c593e4a9d8249e53f0287b4b210f22b331a9eebd6927fcec286';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 12 Feb 2021 22:43:51 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:59079f60dce5f98065dfa2832a3559404ed831b2dd201ee5bb54e0eb9864e1ee`  
		Last Modified: Fri, 12 Feb 2021 22:47:41 GMT  
		Size: 65.3 MB (65330820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sfj-alpine`

```console
$ docker pull ibmjava@sha256:7b03c78f5ecc29438904acdfeb42be6074c5cfe2944c6e25e7f083ccd5be3d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:sfj-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:b474a0098aa285d1cd79513668e69e794cd77b5548ca7343245e9bfa3f56d48c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72556982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2440477f48a8a47e153c6d9792ebcd08e5efbf06c3a57e733536d7d56eba0d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 22:03:57 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 24 Feb 2021 22:03:58 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Wed, 24 Feb 2021 22:04:12 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Wed, 24 Feb 2021 22:04:12 GMT
ENV JAVA_VERSION=1.8.0_sr6fp25
# Wed, 24 Feb 2021 22:05:56 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3188a3690c66210b1c2e40cd7dd30f09fd2ed359a37097ff252f28f13035678e';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='30b441dfe3b7aed59b79d8691254ffe55a94f5f63252e391acce5eacacd78b54';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='949e84ece359b09412a6a43b78fcc91b1bf605321db6e9bb19cfc7eb727eb270';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='ff1b146367ae61869e342fb6b73c40ad966f199f854bb301ede6d06743f20b14';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='6893eb2913f25c593e4a9d8249e53f0287b4b210f22b331a9eebd6927fcec286';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Wed, 24 Feb 2021 22:05:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f834324fbf093cb517d09789e6a0bc4b51f0514fd03332ecdce7c4472a040e`  
		Last Modified: Wed, 24 Feb 2021 22:07:49 GMT  
		Size: 541.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bb308e1feeb83d59c875ad7f4655d6205e9493115588f2b0811f655c776fd8`  
		Last Modified: Wed, 24 Feb 2021 22:07:50 GMT  
		Size: 5.5 MB (5539664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f068e0002533f89a6ea5afd9c26da5f201e0b700a31517b2561d3f89abec29`  
		Last Modified: Wed, 24 Feb 2021 22:08:25 GMT  
		Size: 64.2 MB (64217284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
