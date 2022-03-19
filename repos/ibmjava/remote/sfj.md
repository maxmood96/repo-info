## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:ca685a8d0a8316eec02a65b29e512598417abe957ecd0fafc550761a448731f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:b2bf287ba93cafa85f5bb24758cb429da243db41b7e157cea670536ca137e97a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94250256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18f22ea21be819d02ac641c0875f509c7a8b93fa1ab86d29073819fb7aa9bd6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 08:40:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 19 Mar 2022 08:41:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 08:41:08 GMT
ENV JAVA_VERSION=8.0.7.5
# Sat, 19 Mar 2022 08:43:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f3d0d6cf854f1cd5c6908be9ab77fa133dee458a11a52220a0b2685a18e69aef';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='79c24135b40cbe7e1fa10c8e49192ff87a76547d34d31d07f85b29684212228b';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9635b3d236dfbe32e342d5e5c6e2e29aa323fa5b005dec604c399c711f0053a7';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6240eacc70f4331836349fb52f6327a5a4f4191d89dab1a70a07fc6fd0517ce7';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='3ceb64e606904c38a45d58fd7917bb2ffb29a107e780aeef6aed5cd678c4c842';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Sat, 19 Mar 2022 08:43:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01cc9baeb16a491ae8108620b4a3d924d6c096f56f292cba3c6b4616f628d27`  
		Last Modified: Sat, 19 Mar 2022 08:45:17 GMT  
		Size: 3.0 MB (2959867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b16f645ea562e051f1a2ab0a21e36fc54be7230ef9f34b5139c2890fe70b48`  
		Last Modified: Sat, 19 Mar 2022 08:46:04 GMT  
		Size: 64.6 MB (64581755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:fe304dc2e7e5de054abf0f9d41f2b39dfe00f762e2b1aa29e91774cc6e3c6c82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94119743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88240fa4302cb2b470a66b016af6d3c5abe66a49fa94fc028f4206ef464b555e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 10:41:23 GMT
ADD file:72f05c1b10aca0acb5e79b003217b981354d67a2f72a45a5a48a74d5a22d8a52 in / 
# Fri, 18 Mar 2022 10:41:24 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 12:26:44 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 19 Mar 2022 12:27:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 12:27:00 GMT
ENV JAVA_VERSION=8.0.7.5
# Sat, 19 Mar 2022 12:28:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f3d0d6cf854f1cd5c6908be9ab77fa133dee458a11a52220a0b2685a18e69aef';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='79c24135b40cbe7e1fa10c8e49192ff87a76547d34d31d07f85b29684212228b';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9635b3d236dfbe32e342d5e5c6e2e29aa323fa5b005dec604c399c711f0053a7';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6240eacc70f4331836349fb52f6327a5a4f4191d89dab1a70a07fc6fd0517ce7';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='3ceb64e606904c38a45d58fd7917bb2ffb29a107e780aeef6aed5cd678c4c842';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Sat, 19 Mar 2022 12:28:12 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2ae2a3052b0bf32822826824df976f36386fcf8a79f3777f41da7a64101a1603`  
		Last Modified: Fri, 18 Mar 2022 10:42:30 GMT  
		Size: 27.2 MB (27162241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347fcf94cb333168fccb81463b586454ab2396eb24fbb62b2ee35cf9a54a2ba3`  
		Last Modified: Sat, 19 Mar 2022 12:29:28 GMT  
		Size: 3.0 MB (2988883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78cafdcd1018dbe375c39d2414aeb4af28287957e347c3d49442fb15462b3823`  
		Last Modified: Sat, 19 Mar 2022 12:30:09 GMT  
		Size: 64.0 MB (63968619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:37a47d5bbad12c19968f79a0081e018bca21daeab5bcbdfca5702e6a92b3eb63
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98308735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b98ffc35992255cdd7c8d60097766be8ad0828e57cd9b98a4835f63c620290`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 03:49:58 GMT
ADD file:19b6b516bfde37805273abae0012aaceb45030dcc0c1dbc11828a4dfa6549c29 in / 
# Wed, 02 Feb 2022 03:50:03 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:01:20 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 02 Feb 2022 06:01:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Feb 2022 18:17:17 GMT
ENV JAVA_VERSION=8.0.7.5
# Wed, 23 Feb 2022 18:19:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f3d0d6cf854f1cd5c6908be9ab77fa133dee458a11a52220a0b2685a18e69aef';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='79c24135b40cbe7e1fa10c8e49192ff87a76547d34d31d07f85b29684212228b';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9635b3d236dfbe32e342d5e5c6e2e29aa323fa5b005dec604c399c711f0053a7';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6240eacc70f4331836349fb52f6327a5a4f4191d89dab1a70a07fc6fd0517ce7';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='3ceb64e606904c38a45d58fd7917bb2ffb29a107e780aeef6aed5cd678c4c842';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 23 Feb 2022 18:19:53 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1dc99fe180768d17487534d27fca7d2aea3e7473c284314a65af7be77144eeaa`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 30.4 MB (30437685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e519c40c78b488d71991dd0054bffe8260611286580cb61463ffb1d4b81bb2`  
		Last Modified: Wed, 02 Feb 2022 06:05:57 GMT  
		Size: 3.1 MB (3081867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d2262119fae173b6e10c9be53d4eead199f26b5cb69fcb787cfe2be40b2e32`  
		Last Modified: Wed, 23 Feb 2022 18:23:07 GMT  
		Size: 64.8 MB (64789183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:c9e5b86dba32062146d31b300c9cc336dc02d4014e99485a998534b343c4acb4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93668693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003a3d08d624b59b7cf8a8ab24e324ec2c50d0ab20b507ef5d50f1ef3a4e2b3e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:02 GMT
ADD file:ca83c77547f5f41417a9bcad24827780f3cecda3aadc05e3ea075ef651e7a96c in / 
# Fri, 18 Mar 2022 00:37:05 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:39:07 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 18 Mar 2022 17:39:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:39:13 GMT
ENV JAVA_VERSION=8.0.7.5
# Fri, 18 Mar 2022 17:40:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f3d0d6cf854f1cd5c6908be9ab77fa133dee458a11a52220a0b2685a18e69aef';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='79c24135b40cbe7e1fa10c8e49192ff87a76547d34d31d07f85b29684212228b';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='9635b3d236dfbe32e342d5e5c6e2e29aa323fa5b005dec604c399c711f0053a7';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6240eacc70f4331836349fb52f6327a5a4f4191d89dab1a70a07fc6fd0517ce7';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='3ceb64e606904c38a45d58fd7917bb2ffb29a107e780aeef6aed5cd678c4c842';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 18 Mar 2022 17:40:40 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:19966aaba2fa737074d039f29b54f413d837daaa9d85f02bc54eddd7d645b73c`  
		Last Modified: Fri, 18 Mar 2022 00:38:33 GMT  
		Size: 25.4 MB (25365461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553aa2187de6f86b870a92100c799a91aeea6cdba4160c02ae3405046344347b`  
		Last Modified: Fri, 18 Mar 2022 17:42:03 GMT  
		Size: 2.7 MB (2676789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b3904b5b7cc3a80a79f1a04bcc1642af73d267b0606e89d9be1565a5ef5db2`  
		Last Modified: Fri, 18 Mar 2022 17:42:27 GMT  
		Size: 65.6 MB (65626443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
