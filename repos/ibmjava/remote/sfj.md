## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:d2d2fdf6a38881bbdc0ecf57bcbf570474a347c2f3d783e2521339e46e290856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:804ab29137c376b768a9ae6b5524d3c1be723ba564137096eb6fbc3707edf4d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (93959658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ac9673ba51de75a68c529225440cf55b1d10272b258b2e954fd7dd4dea92a1`
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
# Fri, 17 Sep 2021 19:23:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='aee78edcb2b1eed2e89b60ecfd787c77cc86e1fea646d06e5064f33615379bef';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='1a7c2738e1843d3bc117168ceb8f2969592ff75488d381aa380d647892603204';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f0872801318d37b29f962c4e1ff7f4ea3b201bd401f68b41f1f670b2059c58aa';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6f8e7f2dfc04a4fddf6ef46640791048d9b87d437cd5f724dbf90f1e5ed38f56';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='1a16198540ec2b521d8290bdb37f4ed9848e1d85c6f20c4ef4aa9ae8d4d8cb1e';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 17 Sep 2021 19:23:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:3e39e2f392741042d32a5fc55c382a488281e517cf391c12c049962b4370dad2`  
		Last Modified: Fri, 17 Sep 2021 19:26:58 GMT  
		Size: 64.3 MB (64291400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:45faec2056c0d570c7c3852c4f785e3dd7dfbc588a3bb5dd1a58087bf0f79160
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93843492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26bae58b674c6ca3775ac60e3007e0be74c63067d6f302dda4dc7ecc021e3f5`
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
# Fri, 17 Sep 2021 19:16:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='aee78edcb2b1eed2e89b60ecfd787c77cc86e1fea646d06e5064f33615379bef';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='1a7c2738e1843d3bc117168ceb8f2969592ff75488d381aa380d647892603204';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f0872801318d37b29f962c4e1ff7f4ea3b201bd401f68b41f1f670b2059c58aa';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6f8e7f2dfc04a4fddf6ef46640791048d9b87d437cd5f724dbf90f1e5ed38f56';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='1a16198540ec2b521d8290bdb37f4ed9848e1d85c6f20c4ef4aa9ae8d4d8cb1e';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 17 Sep 2021 19:16:40 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:a693545e455074219da1c44c0610edd6f803f1c7e4b345e62751d8fb79f7fe1c`  
		Last Modified: Fri, 17 Sep 2021 19:18:34 GMT  
		Size: 63.7 MB (63691667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:010833452738238d98167b464761022907330e9aa4a85251d7ba80f4394a2880
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98015862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be045541a1544bf2c53fef0999022c94dffd57753f04d5d966f77e1c0ed4b05`
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
# Fri, 17 Sep 2021 19:46:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='aee78edcb2b1eed2e89b60ecfd787c77cc86e1fea646d06e5064f33615379bef';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='1a7c2738e1843d3bc117168ceb8f2969592ff75488d381aa380d647892603204';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f0872801318d37b29f962c4e1ff7f4ea3b201bd401f68b41f1f670b2059c58aa';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6f8e7f2dfc04a4fddf6ef46640791048d9b87d437cd5f724dbf90f1e5ed38f56';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='1a16198540ec2b521d8290bdb37f4ed9848e1d85c6f20c4ef4aa9ae8d4d8cb1e';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 17 Sep 2021 19:46:37 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:b33341b2dd8475914236a4f164a02332dcbe995c1df8518bafe8811a5fa707e3`  
		Last Modified: Fri, 17 Sep 2021 19:49:41 GMT  
		Size: 64.5 MB (64493752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:1d8fb118d4f7d0e7eaefd5294e1f9185cf2d700f3df62ca3610ea7b8b4e829f4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93383015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7413899986905b08e087bbe95427f25abb7ea014152b55ee0205c530adf06e4f`
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
# Fri, 17 Sep 2021 19:08:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='aee78edcb2b1eed2e89b60ecfd787c77cc86e1fea646d06e5064f33615379bef';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='1a7c2738e1843d3bc117168ceb8f2969592ff75488d381aa380d647892603204';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f0872801318d37b29f962c4e1ff7f4ea3b201bd401f68b41f1f670b2059c58aa';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6f8e7f2dfc04a4fddf6ef46640791048d9b87d437cd5f724dbf90f1e5ed38f56';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='1a16198540ec2b521d8290bdb37f4ed9848e1d85c6f20c4ef4aa9ae8d4d8cb1e';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 17 Sep 2021 19:08:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:d6416fb8b2796845cb6546966c9c84729a815f9fb66f6a1fed998bfee0accc05`  
		Last Modified: Fri, 17 Sep 2021 19:10:12 GMT  
		Size: 65.3 MB (65338981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
