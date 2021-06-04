## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:163f29231d1d4e6f66ecd43ec0627451bf7353eb899bc1c416a55cd92d80fc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:b0cb302233d554325e284d379e2396cfe3fc95725e66c2e4ab771a44a0aa7230
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196337833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703afcbc4607196548db4dfdbefa88cbaa1006907eeeb5277afeda80231da2f2`
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
# Thu, 03 Jun 2021 21:24:11 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Thu, 03 Jun 2021 21:27:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ebb0fd9e7e49b541663ea152a4c28b4d85c458fb00a35e407bfd922fea418fae';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='dcf59f47f74e6ab9b9b1b36f17f31ce9ae800a54d3f8911ee4380a5f128071d7';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='124006e81d5fb148face2142ff7b6155c62876c6f819844d2d34d8d174a0efe7';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='46e8263da8b7cd80b780f5a9dbdab4f0000c32907af1ecbfe58edfc3068810e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='73fb5069d838eeeecbb801c4a8a03180a96e724dad79ef1b441be36ee8d53195';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 03 Jun 2021 21:27:16 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:6294f071f8dd4bf7a07ef22bc65a13e385dc227d3439be4d51e3679e1bdf8f01`  
		Last Modified: Thu, 03 Jun 2021 21:29:49 GMT  
		Size: 166.7 MB (166680957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:706be7c7ce3e4270e062965b38c680d257fa3602f6dfd09dd776bd7c329bac1b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184867792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e37ec95ddec566af61cd4d1cf3441c64e75ba8a703a3025b9c3c39b2a191798`
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
# Thu, 03 Jun 2021 21:39:27 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Thu, 03 Jun 2021 21:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ebb0fd9e7e49b541663ea152a4c28b4d85c458fb00a35e407bfd922fea418fae';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='dcf59f47f74e6ab9b9b1b36f17f31ce9ae800a54d3f8911ee4380a5f128071d7';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='124006e81d5fb148face2142ff7b6155c62876c6f819844d2d34d8d174a0efe7';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='46e8263da8b7cd80b780f5a9dbdab4f0000c32907af1ecbfe58edfc3068810e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='73fb5069d838eeeecbb801c4a8a03180a96e724dad79ef1b441be36ee8d53195';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 03 Jun 2021 21:41:32 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:54b3a2f6c1a6ff8c35bdbb42fceda187624e5fb7bde561271b6571cdae687573`  
		Last Modified: Thu, 03 Jun 2021 21:43:06 GMT  
		Size: 154.7 MB (154746921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:ffedb9c45afb419c0c08e9ba46e69cf3c16f016eb8d90e073cec17285f308256
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.8 MB (199829486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f55620fceb78b8af8c813d46a8b07cf3131d74c8544e04864271c2e74fc6e35`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 May 2021 21:28:00 GMT
ADD file:4aadf3091aaa7aa0a2de15a19b87dbd768ff54ebf3e30723905e804bafafa7d3 in / 
# Wed, 19 May 2021 21:28:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 21:28:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 21:28:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 21:28:53 GMT
CMD ["/bin/bash"]
# Thu, 20 May 2021 01:17:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 20 May 2021 01:18:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Jun 2021 21:18:23 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Thu, 03 Jun 2021 21:22:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ebb0fd9e7e49b541663ea152a4c28b4d85c458fb00a35e407bfd922fea418fae';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='dcf59f47f74e6ab9b9b1b36f17f31ce9ae800a54d3f8911ee4380a5f128071d7';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='124006e81d5fb148face2142ff7b6155c62876c6f819844d2d34d8d174a0efe7';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='46e8263da8b7cd80b780f5a9dbdab4f0000c32907af1ecbfe58edfc3068810e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='73fb5069d838eeeecbb801c4a8a03180a96e724dad79ef1b441be36ee8d53195';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 03 Jun 2021 21:22:17 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f13c2db25c9606e881665513b807199dbbcf16f443d6077d564a570b13d4cb4b`  
		Last Modified: Wed, 19 May 2021 21:34:00 GMT  
		Size: 30.4 MB (30407160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce0c6d78eb67a510d3a36e870ac4a54aca62069696e64e0f309a1d692066ea6`  
		Last Modified: Wed, 19 May 2021 21:33:52 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7b6c37775ff2aaf526ca7ac92641488b18dadb59f8d00857213e0b8ae0e13e`  
		Last Modified: Wed, 19 May 2021 21:33:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3919e7faac3a82c33e8b0eed1a72a00f407c1847b6417a93a44714b023ebccb`  
		Last Modified: Thu, 20 May 2021 01:28:52 GMT  
		Size: 3.1 MB (3082817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9aba961a19f2c19523182241c256219bf8ee342080e9b3b7eb6d0c29425619`  
		Last Modified: Thu, 03 Jun 2021 21:23:45 GMT  
		Size: 166.3 MB (166338464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:e2bc0c234da0f6a4b4f010104ca293256afee6374a5331b05c16f3ae502270e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (184989547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520b695126a1fdc80d3d5bf8d3e0a8bc5729fd4769f8963c0e779d6988ca457a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 May 2021 23:28:29 GMT
ADD file:718406af36d25bc30b425ddad4eaa810e4f8cfe92388955edc07fd5ec9816dcc in / 
# Wed, 19 May 2021 23:28:36 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 23:28:38 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 23:28:40 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 23:28:40 GMT
CMD ["/bin/bash"]
# Thu, 20 May 2021 00:10:42 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 20 May 2021 00:10:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Jun 2021 21:42:18 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Thu, 03 Jun 2021 21:44:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ebb0fd9e7e49b541663ea152a4c28b4d85c458fb00a35e407bfd922fea418fae';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='dcf59f47f74e6ab9b9b1b36f17f31ce9ae800a54d3f8911ee4380a5f128071d7';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='124006e81d5fb148face2142ff7b6155c62876c6f819844d2d34d8d174a0efe7';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='46e8263da8b7cd80b780f5a9dbdab4f0000c32907af1ecbfe58edfc3068810e7';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='73fb5069d838eeeecbb801c4a8a03180a96e724dad79ef1b441be36ee8d53195';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 03 Jun 2021 21:44:51 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3d5e421eb08da6bcb06173fcdd4e739a0fc77d7b26f72680342d8db9aedebf05`  
		Last Modified: Wed, 19 May 2021 23:30:36 GMT  
		Size: 25.4 MB (25352550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b74c33ee4c205747bbbc098fc12afc14cab69dd5b2186b8bf7ee58f516631b`  
		Last Modified: Wed, 19 May 2021 23:30:32 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb318177ecfab6a1f7a7c8290c83d4d680cf1110f5b4d80fd059793e3b64708`  
		Last Modified: Wed, 19 May 2021 23:30:32 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0490993673c14da219283fb60f1fcd5b87d725aa73640336424edf54013128`  
		Last Modified: Thu, 20 May 2021 00:14:38 GMT  
		Size: 2.7 MB (2676632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0fb1d3f514e0519e8ed79c9df18a845d90de05ee84582452d4cebe12b49205e`  
		Last Modified: Thu, 03 Jun 2021 21:45:59 GMT  
		Size: 157.0 MB (156959323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
