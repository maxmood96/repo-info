## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:0b980a6275e78178189f035cc25358bba8550e07c6cd5dfdb17a1988cf986fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:9a2391efb9b4152daeb6867186c6c3ff320d78024d6a57a902fdeeb3e4495611
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94035661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebabe592bb7443cb609a85d65d5067282c4ae2f900b61f95d9c17ac22025827`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:19:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:19:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:20:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='459e3c990073af4ccbc7b774b94e495c9a1ab93884fc102b9078450afde345e2';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='b750f58b7623eb184602172122040128d534e3442e2b299670124f5be91cd0db';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='81a3e97371ce2fc85e2e07ad1498c9152a81bfe7d57fe074cd29ecc8df120f86';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8511e455579014b94a9d8fca686b2bd25391c1ff985cad7320206987b8d4178e';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4857271dfb8db4eb910dc14561789439a4777b8fe1c61a57112592398e6b95e';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:20:29 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22821a14390caaab5b1f7ca9feb8e54ce64d3d81ca1fa64c6f1eee32ae92da5b`  
		Last Modified: Tue, 13 Jul 2021 23:23:03 GMT  
		Size: 3.0 MB (2959004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76d35690198d2592eef10baa51062473dbf9635abc81fef63eb4aa9eb63dbfc`  
		Last Modified: Tue, 13 Jul 2021 23:23:35 GMT  
		Size: 64.4 MB (64370512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:896c5b46fc5a91b2c0dde6e426132fa9deb23212711574d18f490e6aea2b60d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93878655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e8cc15d2afd7fbc238e86b1476fe2e2f42342dee3df092783fc82c2495dfe9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:39:15 GMT
ADD file:2478887c0caae58ac755f71306211decbf5e69b832b9939974a93743e5c440f5 in / 
# Tue, 13 Jul 2021 22:39:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:05:28 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:05:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:05:35 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:07:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='459e3c990073af4ccbc7b774b94e495c9a1ab93884fc102b9078450afde345e2';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='b750f58b7623eb184602172122040128d534e3442e2b299670124f5be91cd0db';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='81a3e97371ce2fc85e2e07ad1498c9152a81bfe7d57fe074cd29ecc8df120f86';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8511e455579014b94a9d8fca686b2bd25391c1ff985cad7320206987b8d4178e';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4857271dfb8db4eb910dc14561789439a4777b8fe1c61a57112592398e6b95e';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:07:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4c0067b0d84ac31443135f34e6bf8eacb1e1da0b388d042fbdd498858738047f`  
		Last Modified: Tue, 13 Jul 2021 22:40:10 GMT  
		Size: 27.2 MB (27153547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbe1128ef2eac594ca8c851354f334bde2c6c46096bbce3775054be4560ce98`  
		Last Modified: Tue, 13 Jul 2021 23:08:30 GMT  
		Size: 3.0 MB (2988008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e121d23e1afcf0579dfcfc6cc82bf9f6b37594e83b710df3f350dfa48de2dceb`  
		Last Modified: Tue, 13 Jul 2021 23:09:08 GMT  
		Size: 63.7 MB (63737100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:da64748a60ee5be441ede534145404f7ca1fadfbd24567b39eb084ab180d45bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103229086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ca35aa1e774d4c707aa84aa3a41a539a86f2613c1243cc576348b505d4d333`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:38:03 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 14 Jul 2021 04:38:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:38:50 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Wed, 14 Jul 2021 04:41:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='459e3c990073af4ccbc7b774b94e495c9a1ab93884fc102b9078450afde345e2';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='b750f58b7623eb184602172122040128d534e3442e2b299670124f5be91cd0db';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='81a3e97371ce2fc85e2e07ad1498c9152a81bfe7d57fe074cd29ecc8df120f86';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8511e455579014b94a9d8fca686b2bd25391c1ff985cad7320206987b8d4178e';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4857271dfb8db4eb910dc14561789439a4777b8fe1c61a57112592398e6b95e';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 14 Jul 2021 04:41:27 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ab9a4a9b7968cedcece7ccbd278b539ab11dc1c8c1b32042f293b4152f52fd`  
		Last Modified: Wed, 14 Jul 2021 04:46:40 GMT  
		Size: 3.1 MB (3082897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63e575ef18593a4591a7b17be251c5c1b49fd5956290149fc58433dffce5f9f`  
		Last Modified: Wed, 14 Jul 2021 04:47:23 GMT  
		Size: 69.7 MB (69718202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:f6b31a9d71ee9746f2f420e4b6111fef4338cae3f1e8329d6c843519053dc82c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93510658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63b7c02a34ba4c27ae8639330e649e62e3d71e80abc0c0c6184f6dc1de658c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:12:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:12:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:12:20 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:13:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='459e3c990073af4ccbc7b774b94e495c9a1ab93884fc102b9078450afde345e2';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='b750f58b7623eb184602172122040128d534e3442e2b299670124f5be91cd0db';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='81a3e97371ce2fc85e2e07ad1498c9152a81bfe7d57fe074cd29ecc8df120f86';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='8511e455579014b94a9d8fca686b2bd25391c1ff985cad7320206987b8d4178e';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='a4857271dfb8db4eb910dc14561789439a4777b8fe1c61a57112592398e6b95e';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:13:51 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6fe4e2b151f33398a6ef48bbb5d9ace538aa5ecf3fab9182babc3a85b9166b`  
		Last Modified: Tue, 13 Jul 2021 23:16:59 GMT  
		Size: 2.7 MB (2676828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ffda74c5d06c573f1001bc58b41bf8ced98133bfb16efeb134cd98948786009`  
		Last Modified: Tue, 13 Jul 2021 23:17:24 GMT  
		Size: 65.5 MB (65468181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
