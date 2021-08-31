## `ibmjava:11-jdk`

```console
$ docker pull ibmjava@sha256:87999ab4f3ac702fe32c3ad9fa13b1875af79fce8fc8c2af037981c7567588a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:11-jdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:26c5f821584ffc052899c94f286241bd3bb89e2813418759a9d6262c6b847eaa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (261987803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb359b683dd2a0c766d4265edd67786399d8b9e62ede231cf7203d8424c6da50`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:55 GMT
ADD file:d2abf27fe2e8b0b5f4da68c018560c73e11c53098329246e3e6fe176698ef941 in / 
# Tue, 31 Aug 2021 01:20:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:37:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Aug 2021 03:37:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:37:24 GMT
ENV JAVA_VERSION=11.0.11.0
# Tue, 31 Aug 2021 03:38:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='037363b1dd35d7b6a67137baf1c73589b4f7b4e177d40394897726ad6056babd';          YML_FILE='11.0/jdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='717d3c0427d34af710f10f62be68cc78576ebb80523ff65ab3e8c1fe6a785569';          YML_FILE='11.0/jdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='b2e64a73dab3fed0a845144377a9cd2945b87c005ba2418f1abbefea45321167';          YML_FILE='11.0/jdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     mv /opt/ibm/jdk-11* /opt/ibm/java;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Aug 2021 03:38:13 GMT
ENV JAVA_HOME=/opt/ibm/java PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:35807b77a593c1147d13dc926a91dcc3015616ff7307cc30442c5a8e07546283`  
		Last Modified: Sat, 28 Aug 2021 03:03:19 GMT  
		Size: 28.6 MB (28570074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e27118f718011549d574aaa58e0ff3e00d24f2c8a4b5b4e3a9dff5070032b51`  
		Last Modified: Tue, 31 Aug 2021 03:39:51 GMT  
		Size: 3.0 MB (3039356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df218c055698a0e9bc5f4631e4a3250b51ff2a3224c13a255b5593d68758b08f`  
		Last Modified: Tue, 31 Aug 2021 03:40:08 GMT  
		Size: 230.4 MB (230378373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:11-jdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:8e8a1f9ab13131b25f7eb693bb493becc204a8331ed3cfd18585ba96e6cf9b48
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267888974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5def2354e3de88d539b2b794a96ea5d97482834219bd9ae2bb57b5072d00ca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:00:48 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 27 Jul 2021 02:01:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:01:29 GMT
ENV JAVA_VERSION=11.0.11.0
# Tue, 27 Jul 2021 02:02:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='037363b1dd35d7b6a67137baf1c73589b4f7b4e177d40394897726ad6056babd';          YML_FILE='11.0/jdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='717d3c0427d34af710f10f62be68cc78576ebb80523ff65ab3e8c1fe6a785569';          YML_FILE='11.0/jdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='b2e64a73dab3fed0a845144377a9cd2945b87c005ba2418f1abbefea45321167';          YML_FILE='11.0/jdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     mv /opt/ibm/jdk-11* /opt/ibm/java;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 27 Jul 2021 02:02:44 GMT
ENV JAVA_HOME=/opt/ibm/java PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669e58f1f347891c9de25b88b61460bc92fe7348cd685a1e338984b18b4c52f9`  
		Last Modified: Tue, 27 Jul 2021 02:04:48 GMT  
		Size: 3.3 MB (3292569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa664c7a8863f0e1fe63d018f9ba22a169c07ef306f73b33ee700e1747f6bcf`  
		Last Modified: Tue, 27 Jul 2021 02:05:14 GMT  
		Size: 231.3 MB (231305978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:11-jdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:d1f2d06fd52d221ba1ddb6c728e66138b46d109d6e5384ca7d5342d90e22a1de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260808982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f30a02810cb0a4c615c1ceda9cc06556aa515d0f4fb7b86f2808151d897a74a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:42:23 GMT
ADD file:979855f79ebaca36cc7878f71b2326f1cd189970fdb223b37cd64ee12d1c9a2b in / 
# Tue, 31 Aug 2021 01:42:27 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:04:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Aug 2021 02:04:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:04:12 GMT
ENV JAVA_VERSION=11.0.11.0
# Tue, 31 Aug 2021 02:05:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='037363b1dd35d7b6a67137baf1c73589b4f7b4e177d40394897726ad6056babd';          YML_FILE='11.0/jdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='717d3c0427d34af710f10f62be68cc78576ebb80523ff65ab3e8c1fe6a785569';          YML_FILE='11.0/jdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='b2e64a73dab3fed0a845144377a9cd2945b87c005ba2418f1abbefea45321167';          YML_FILE='11.0/jdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     mv /opt/ibm/jdk-11* /opt/ibm/java;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Aug 2021 02:05:34 GMT
ENV JAVA_HOME=/opt/ibm/java PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9fbf86d355c92d30b8de4c0360b0d79e1100e392d0885b6b5b302a1c3781dbf1`  
		Last Modified: Tue, 31 Aug 2021 01:44:13 GMT  
		Size: 27.1 MB (27127470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f82a80fc57ecf5920da007b382a89f3cf656ec0dde08098ce0e2f2225b4eeb`  
		Last Modified: Tue, 31 Aug 2021 02:07:09 GMT  
		Size: 2.7 MB (2738594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994bf1d16de5ff4a0dd6c6b6224013a29c99d15478790f88662bb5fc25ca1888`  
		Last Modified: Tue, 31 Aug 2021 02:07:25 GMT  
		Size: 230.9 MB (230942918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
