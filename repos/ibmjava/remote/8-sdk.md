## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:effee2e1e980b5ef29f4df43595b68f39ad92f274ac39aacba6ab9d1362093b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:051874343550402f3f89bdf2a5cf124ba7a6d29cc5eb26608e87ece6db1620b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.2 MB (195199441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d67bfaaeebfa826931b1d1b68b3e11c4531d8d4027eb5eea24018492048cd9e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:35:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Aug 2021 03:35:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Sep 2021 19:21:11 GMT
ENV JAVA_VERSION=8.0.6.36
# Fri, 17 Sep 2021 19:24:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='953586dcb1870406d51fc0f346e2be062471d7dc67dce21ba2009cff0a46724f';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='09705ba9b6c53105062fd7764f9a066bfe5e2f58a64662d29c1eb030d51252e1';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e233b23f00ecda6a8e8fffe4b7c0675c3574754d300b680e70f423a60d047874';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e81cde52da8dd39160a70c98453e379f1286bb39e58f01ba94a63e45e31e2d34';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='dfc67c2861e00265140287091a713496840f5793946e087825f96c7afd4a8a50';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 17 Sep 2021 19:24:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdd64484112f6def7fd2349a813854240b9f909a6ccebf3acc55c3db9e9c1b1`  
		Last Modified: Tue, 31 Aug 2021 03:38:45 GMT  
		Size: 3.0 MB (2959747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad802f28dcf52bf67c93c5082c903ce7ef4ecc856ca22faba4b7fc2489998cc8`  
		Last Modified: Fri, 17 Sep 2021 19:27:40 GMT  
		Size: 165.5 MB (165531183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:f8a9cfc3537e3becfc6332ff9d49c49cea8aba9b104edd07884e6caa1dd4e3ef
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183892510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6866a1c1db1647162d69cab0090d8c9fa925c5c3c74659d3911e3ba4b39a4f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:39:08 GMT
ADD file:615269b4e3662feffa9257a896456387554777532f070eae2226fa704e50150e in / 
# Tue, 31 Aug 2021 01:39:08 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:12:23 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Aug 2021 02:12:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Sep 2021 19:15:18 GMT
ENV JAVA_VERSION=8.0.6.36
# Fri, 17 Sep 2021 19:17:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='953586dcb1870406d51fc0f346e2be062471d7dc67dce21ba2009cff0a46724f';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='09705ba9b6c53105062fd7764f9a066bfe5e2f58a64662d29c1eb030d51252e1';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e233b23f00ecda6a8e8fffe4b7c0675c3574754d300b680e70f423a60d047874';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e81cde52da8dd39160a70c98453e379f1286bb39e58f01ba94a63e45e31e2d34';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='dfc67c2861e00265140287091a713496840f5793946e087825f96c7afd4a8a50';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 17 Sep 2021 19:17:30 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:01a6f9651a524383d1aac8b05ceaf7a079d305146c6bf120b7ffb27247b18230`  
		Last Modified: Tue, 31 Aug 2021 01:40:06 GMT  
		Size: 27.2 MB (27162437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2dc5982ecfcf15c732820dee42795101949b64c04ef86dc8296f7b9a16509d4`  
		Last Modified: Tue, 31 Aug 2021 02:15:07 GMT  
		Size: 3.0 MB (2989388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e194dda9defae1cccccbcea602f2ff07ce30fdeb97311250a600515acb843124`  
		Last Modified: Fri, 17 Sep 2021 19:18:59 GMT  
		Size: 153.7 MB (153740685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:13300e3b13ffc5b18ccf20b4af7712bb99d8a8fbca5227a79ee4cbe7de8d2af1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 MB (198692128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05a660b4c9b5f093f8c4379e5c59aebe48f99a4bccac3342946e24e83773d94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 02:10:11 GMT
ADD file:32c084b07cf88f4b46c2c94d6e8634a245a8ea46f4c166fe98b49a7e3d44a700 in / 
# Tue, 31 Aug 2021 02:10:18 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 06:11:59 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Aug 2021 06:14:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Sep 2021 19:44:02 GMT
ENV JAVA_VERSION=8.0.6.36
# Fri, 17 Sep 2021 19:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='953586dcb1870406d51fc0f346e2be062471d7dc67dce21ba2009cff0a46724f';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='09705ba9b6c53105062fd7764f9a066bfe5e2f58a64662d29c1eb030d51252e1';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e233b23f00ecda6a8e8fffe4b7c0675c3574754d300b680e70f423a60d047874';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e81cde52da8dd39160a70c98453e379f1286bb39e58f01ba94a63e45e31e2d34';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='dfc67c2861e00265140287091a713496840f5793946e087825f96c7afd4a8a50';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 17 Sep 2021 19:48:14 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b66177991333478fe4de9a7fc6ee8c546debb78334473278e085735e8a88072d`  
		Last Modified: Tue, 31 Aug 2021 02:13:59 GMT  
		Size: 30.4 MB (30437758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a83a649f63bfaad86f8628a777426148c29a6119ce301cd77dbdf1d4c48ddcb`  
		Last Modified: Tue, 31 Aug 2021 06:19:28 GMT  
		Size: 3.1 MB (3084352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf6cdd2754d3060e4d16ef0d9b1bb817e8e074f5f5d320262e6947293a7c1af`  
		Last Modified: Fri, 17 Sep 2021 19:50:11 GMT  
		Size: 165.2 MB (165170018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:1b0996b33b63067bd3401b4aaa8daca5aae6919b43ed3532d65ceda02cbfbd79
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183721741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379dca721401f3fdee1f6596aff61fd6e797b584b7bf19caac683ba36193a167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:42:06 GMT
ADD file:587feabbf5ad530bb19e438490116110e0c3f5fd5c8b98bcce6767af928c66de in / 
# Tue, 31 Aug 2021 01:42:10 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:00:34 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Aug 2021 02:00:47 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 17 Sep 2021 19:06:42 GMT
ENV JAVA_VERSION=8.0.6.36
# Fri, 17 Sep 2021 19:09:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='953586dcb1870406d51fc0f346e2be062471d7dc67dce21ba2009cff0a46724f';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='09705ba9b6c53105062fd7764f9a066bfe5e2f58a64662d29c1eb030d51252e1';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e233b23f00ecda6a8e8fffe4b7c0675c3574754d300b680e70f423a60d047874';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e81cde52da8dd39160a70c98453e379f1286bb39e58f01ba94a63e45e31e2d34';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='dfc67c2861e00265140287091a713496840f5793946e087825f96c7afd4a8a50';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 17 Sep 2021 19:09:11 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:8a5845e3ee3e2d93d3bcf0f827afe41d646f59cdf52f107306c232b60ffeb3a4`  
		Last Modified: Tue, 31 Aug 2021 01:43:59 GMT  
		Size: 25.4 MB (25366401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3910b4a125e933281c490aa153e2a43cf8e21bbe2142e9491a5c3004481598c9`  
		Last Modified: Tue, 31 Aug 2021 02:06:15 GMT  
		Size: 2.7 MB (2677633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:308476b5b0a0f83b306c2189630de42d38550226e34cfee7844b4ad5ef51f426`  
		Last Modified: Fri, 17 Sep 2021 19:10:30 GMT  
		Size: 155.7 MB (155677707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
