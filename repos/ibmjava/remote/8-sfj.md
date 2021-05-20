## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:d723fca4bfc3bbe2a1d04c2899ffc0a528db6ea6294080619c856d5263522a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:3ff06f0f1bbd213193cc5bde89698ef4f2dd135924cb74df3c294fece4f39844
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93920084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80985950a1500540f493c0fec9000e377066cad8105fdf8b221b759380ca6766`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 May 2021 19:44:30 GMT
ADD file:e05689b5b0d51a2316f8a87b1a9d6cbf90d98b19a424dbb924ee3d0b1cc17bfc in / 
# Wed, 19 May 2021 19:44:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:44:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:44:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:44:33 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 22:38:47 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 May 2021 22:38:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 22:38:55 GMT
ENV JAVA_VERSION=1.8.0_sr6fp30
# Wed, 19 May 2021 22:40:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='7fd642bb37d6859e32775742b886fbb68dc0c22e27db90572d78978c43a65532';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='1d44c1fe42336cab994267589d9be742c79b1937fb204662dc7bc22b41e74253';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='065b7d2be5d6744767e49b2116bf261e11396e1eba80dc838796f10b1627e95b';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='30c1d89cef9c6ea061ad013f2ec3621d51a7dc7e268884d7c3be9b0056ea5e05';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='2564a4ef1ba37a0ffe1098c598ac49e0b98661ca2c2198ea6349a2d437fd354d';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 May 2021 22:40:08 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4bbfd2c87b7524455f144a03bf387c88b6d4200e5e0df9139a9d5e79110f89ca`  
		Last Modified: Thu, 13 May 2021 14:54:04 GMT  
		Size: 26.7 MB (26696304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e110be24e168b42c1a2ddbc4a476a217b73cccdba69cdcb212b812a88f5726`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a7173dcfeb409f9d88054a97ab2445f5a799a823f719a5573365ee3662b6f`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8a6eba08d45a10a659a07163e4c6ef1e4ae0b77bc8c094078704c584a4aea3`  
		Last Modified: Wed, 19 May 2021 22:41:17 GMT  
		Size: 3.0 MB (2959526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c553c956cc839850d3153a0c367cb0922d371e469f13fef6d20d779d90e0d50b`  
		Last Modified: Wed, 19 May 2021 22:41:48 GMT  
		Size: 64.3 MB (64263208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:f787316ebeb262aa0d3af76e2266e57168371b2f3ee9cd95284a7ce1aacca270
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93768169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfc318b6ec4736406e7d132f9534f33f00636516c644e3ce095ab8333301c23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 May 2021 19:40:52 GMT
ADD file:e0284f44e9a104546ff12ccb0b485d12a45fef6c2035358fc5620e7a702b358e in / 
# Wed, 19 May 2021 19:40:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:40:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:40:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:40:55 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 20:21:14 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 May 2021 20:21:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 20:21:21 GMT
ENV JAVA_VERSION=1.8.0_sr6fp30
# Wed, 19 May 2021 20:22:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='7fd642bb37d6859e32775742b886fbb68dc0c22e27db90572d78978c43a65532';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='1d44c1fe42336cab994267589d9be742c79b1937fb204662dc7bc22b41e74253';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='065b7d2be5d6744767e49b2116bf261e11396e1eba80dc838796f10b1627e95b';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='30c1d89cef9c6ea061ad013f2ec3621d51a7dc7e268884d7c3be9b0056ea5e05';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='2564a4ef1ba37a0ffe1098c598ac49e0b98661ca2c2198ea6349a2d437fd354d';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 May 2021 20:22:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:da97bc6b7e988f4f13b3e5091db2330133381a463cb607de469e04742900f5f4`  
		Last Modified: Wed, 19 May 2021 19:41:52 GMT  
		Size: 27.1 MB (27131287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652d638a400430b9b485097830ca789323f97806c727fdace35095c1314272a5`  
		Last Modified: Wed, 19 May 2021 19:41:47 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7449e958dde8dd03ed487ed6b0df2995490dab77191cdb761ceeda156fd24689`  
		Last Modified: Wed, 19 May 2021 19:41:47 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad30e2584fb44cf60f513e5d25fd408fcbb575231328410c646ef332323dac96`  
		Last Modified: Wed, 19 May 2021 20:23:55 GMT  
		Size: 3.0 MB (2988539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65001b7e7b45add490695d6654de8091862a2747ac912120fa51effc89f21f0b`  
		Last Modified: Wed, 19 May 2021 20:24:31 GMT  
		Size: 63.6 MB (63647298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:87f924165a3a3ef5323058053df043601c159fd3eb4caaa0044c816bfd54d167
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (97959082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf693c42fb1e50ddff017b41206107ddc7ba7e99a3407548320078f1ebaea178`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Apr 2021 22:30:25 GMT
ADD file:818f810cd30ef74fd4690c6265d80265647ba3353880cf8323500df6d2c48b69 in / 
# Fri, 23 Apr 2021 22:30:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:31:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:31:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:31:32 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:16:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 23:17:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 19:16:51 GMT
ENV JAVA_VERSION=1.8.0_sr6fp30
# Wed, 19 May 2021 19:19:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='7fd642bb37d6859e32775742b886fbb68dc0c22e27db90572d78978c43a65532';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='1d44c1fe42336cab994267589d9be742c79b1937fb204662dc7bc22b41e74253';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='065b7d2be5d6744767e49b2116bf261e11396e1eba80dc838796f10b1627e95b';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='30c1d89cef9c6ea061ad013f2ec3621d51a7dc7e268884d7c3be9b0056ea5e05';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='2564a4ef1ba37a0ffe1098c598ac49e0b98661ca2c2198ea6349a2d437fd354d';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 May 2021 19:19:47 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bb3095714506c08a64a49e29ab001d7000d94957d52e05db35361fd4a54c460c`  
		Last Modified: Fri, 23 Apr 2021 22:36:52 GMT  
		Size: 30.4 MB (30407300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd29acc6f7bfef8034eaca0bfb069f0d66e50351c84b062e224d6eae710afa79`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645fc50c9e70df51732b36ef7f8b21ebacd148c3bee4f1b29ca6dcba1bbb949`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab6dc42492fe0eca98f1e563f3e8dabb70f122b45b752264bacb4ea14f59354`  
		Last Modified: Fri, 23 Apr 2021 23:22:26 GMT  
		Size: 3.1 MB (3082775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3860edb8f676bb8719dfc766d1e0127a3c4450caa3647fcc5328db226379ba1`  
		Last Modified: Wed, 19 May 2021 19:22:36 GMT  
		Size: 64.5 MB (64467963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:a5b5074efef95cf8ea02cf13916c370160ceaf2e6cedc6b800de0dcb244570fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93399121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a814d495c1bcbefe389102a6868f6696953f4cc5dbe781b663273f78f94bf038`
-	Default Command: `["\/bin\/bash"]`

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
# Wed, 19 May 2021 18:41:40 GMT
ENV JAVA_VERSION=1.8.0_sr6fp30
# Wed, 19 May 2021 18:43:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='7fd642bb37d6859e32775742b886fbb68dc0c22e27db90572d78978c43a65532';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='1d44c1fe42336cab994267589d9be742c79b1937fb204662dc7bc22b41e74253';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='065b7d2be5d6744767e49b2116bf261e11396e1eba80dc838796f10b1627e95b';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='30c1d89cef9c6ea061ad013f2ec3621d51a7dc7e268884d7c3be9b0056ea5e05';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='2564a4ef1ba37a0ffe1098c598ac49e0b98661ca2c2198ea6349a2d437fd354d';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 May 2021 18:43:30 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:1cd5b22c950f95752badf3ad4cfacba3176aa964b06ef50e5e64d5143f332801`  
		Last Modified: Wed, 19 May 2021 18:45:30 GMT  
		Size: 65.4 MB (65368682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
