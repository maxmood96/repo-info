<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ibmjava`

-	[`ibmjava:8`](#ibmjava8)
-	[`ibmjava:8-jre`](#ibmjava8-jre)
-	[`ibmjava:8-sdk`](#ibmjava8-sdk)
-	[`ibmjava:8-sfj`](#ibmjava8-sfj)
-	[`ibmjava:jre`](#ibmjavajre)
-	[`ibmjava:latest`](#ibmjavalatest)
-	[`ibmjava:sdk`](#ibmjavasdk)
-	[`ibmjava:sfj`](#ibmjavasfj)

## `ibmjava:8`

```console
$ docker pull ibmjava@sha256:75221bf9a1c2ccc846ce05205b26db6da6fe1ab33b4e2ae1aea7e6fbe51e2c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8` - linux; amd64

```console
$ docker pull ibmjava@sha256:2f84ac129faa2e8d64207bae1ef5d99149a9553b4de834f6b372a4a1d7cdc4ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159010292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f05c3b9b99fee213cdf386a94fce39816fab1c25ee708b151f53621ff3ad85c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:09:52 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 20:10:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 19:19:41 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 19:20:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 19:20:40 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6715a1bb89fcf5e91403be2bc6130f23e6b3cfd0da73e6b09e937d028409d3`  
		Last Modified: Tue, 02 Aug 2022 20:13:24 GMT  
		Size: 3.0 MB (2957815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a98fa70bcc08366a44c285d736a35471c6af0c09f278e8a51e1687daec0d70`  
		Last Modified: Fri, 26 Aug 2022 19:23:23 GMT  
		Size: 129.3 MB (129342207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; 386

```console
$ docker pull ibmjava@sha256:85e74c913750585e66de9c1d97c2c1f146eedd22746528ae81ce1df3d7558010
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147610305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137d978d6d28922ed0f50e0e710066b7bd1f0fd2cac9f5c2e49094945bd29978`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:50:55 GMT
ADD file:6d22c6318075d01068d0a9213f33655abf6c251f8a71d98c17b857b9021b43bd in / 
# Tue, 02 Aug 2022 00:50:55 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:23:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 16:23:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 18:38:36 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 18:39:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 18:39:27 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:5496b4c91dece81ce997c62cf2e1ef6f1764e612c6e8f0b385722c6645e4ad30`  
		Last Modified: Tue, 02 Aug 2022 00:51:39 GMT  
		Size: 27.2 MB (27164268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0dd584134d885dc07df56cb1531c30c56e50d96a7cc1cb92c61c41813d18e0`  
		Last Modified: Tue, 02 Aug 2022 16:27:10 GMT  
		Size: 3.0 MB (2983285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4754877954ce670bc1c090044af2c4dde2de36f4ad1ea1d2cdaa9e1ecce40df9`  
		Last Modified: Fri, 26 Aug 2022 18:42:09 GMT  
		Size: 117.5 MB (117462752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:5adc59a78a71a51002e2422e59defb3084a9339aa30fb54acf018a2318e26041
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162412482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c153f6fec2349df07565406ea5f5563a153be3673c7622b87f48b5eebfd648`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:50 GMT
ADD file:32fc7b9b5853c93c45b1a96054c30104fd200ac7d40d0388aff736c478f917cb in / 
# Tue, 02 Aug 2022 01:30:52 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 03:44:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 03 Aug 2022 03:44:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 19:16:47 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 19:19:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 19:19:19 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1a9ff13e38cae7994b55e6db5c3d190d2b7a03043ae238a6f71a285376de46bb`  
		Last Modified: Tue, 02 Aug 2022 01:33:07 GMT  
		Size: 30.4 MB (30441470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99970d1735353adabddaef52faa1237908c9cdf39198088cf543cb21ecb3fa69`  
		Last Modified: Wed, 03 Aug 2022 03:52:54 GMT  
		Size: 3.1 MB (3075943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9501b5b22fed4db7ff494e125e8d08db9f15c579219c407c9707f7051a82644`  
		Last Modified: Fri, 26 Aug 2022 19:25:25 GMT  
		Size: 128.9 MB (128895069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:00cd2eaa02ca5ad01bf0373fd720cca3cc59c7518e1e95dad2857cddc3a5d839
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154502164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73d216c3a69dba42223d14fdb977e1cbc0656370a8474e89450c14ecd90d196`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:01:57 GMT
ADD file:3d2e9b401524527b395347bc3847be7c9cb465b9a214a1a1d31e74330e293c45 in / 
# Tue, 02 Aug 2022 01:01:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:19:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 13:19:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 18:41:51 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 18:42:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 18:42:46 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:be3ed498266c519f84268ff1f02085fa249c0e32fb60a59466e24c862b5f094b`  
		Last Modified: Tue, 02 Aug 2022 01:03:25 GMT  
		Size: 25.4 MB (25369584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2ed0adcefe11b30e3dff027bcb1cb9fe759f39f50b008bafb3644d3d2fcba8`  
		Last Modified: Tue, 02 Aug 2022 13:22:41 GMT  
		Size: 2.7 MB (2671706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811ae78985ec89d3fada71c34fdf570518d7e32fa5472f26184d5756ae76fdd3`  
		Last Modified: Fri, 26 Aug 2022 18:45:21 GMT  
		Size: 126.5 MB (126460874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:75221bf9a1c2ccc846ce05205b26db6da6fe1ab33b4e2ae1aea7e6fbe51e2c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:2f84ac129faa2e8d64207bae1ef5d99149a9553b4de834f6b372a4a1d7cdc4ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159010292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f05c3b9b99fee213cdf386a94fce39816fab1c25ee708b151f53621ff3ad85c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:09:52 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 20:10:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 19:19:41 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 19:20:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 19:20:40 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6715a1bb89fcf5e91403be2bc6130f23e6b3cfd0da73e6b09e937d028409d3`  
		Last Modified: Tue, 02 Aug 2022 20:13:24 GMT  
		Size: 3.0 MB (2957815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a98fa70bcc08366a44c285d736a35471c6af0c09f278e8a51e1687daec0d70`  
		Last Modified: Fri, 26 Aug 2022 19:23:23 GMT  
		Size: 129.3 MB (129342207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; 386

```console
$ docker pull ibmjava@sha256:85e74c913750585e66de9c1d97c2c1f146eedd22746528ae81ce1df3d7558010
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147610305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137d978d6d28922ed0f50e0e710066b7bd1f0fd2cac9f5c2e49094945bd29978`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:50:55 GMT
ADD file:6d22c6318075d01068d0a9213f33655abf6c251f8a71d98c17b857b9021b43bd in / 
# Tue, 02 Aug 2022 00:50:55 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:23:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 16:23:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 18:38:36 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 18:39:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 18:39:27 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:5496b4c91dece81ce997c62cf2e1ef6f1764e612c6e8f0b385722c6645e4ad30`  
		Last Modified: Tue, 02 Aug 2022 00:51:39 GMT  
		Size: 27.2 MB (27164268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0dd584134d885dc07df56cb1531c30c56e50d96a7cc1cb92c61c41813d18e0`  
		Last Modified: Tue, 02 Aug 2022 16:27:10 GMT  
		Size: 3.0 MB (2983285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4754877954ce670bc1c090044af2c4dde2de36f4ad1ea1d2cdaa9e1ecce40df9`  
		Last Modified: Fri, 26 Aug 2022 18:42:09 GMT  
		Size: 117.5 MB (117462752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:5adc59a78a71a51002e2422e59defb3084a9339aa30fb54acf018a2318e26041
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162412482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c153f6fec2349df07565406ea5f5563a153be3673c7622b87f48b5eebfd648`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:50 GMT
ADD file:32fc7b9b5853c93c45b1a96054c30104fd200ac7d40d0388aff736c478f917cb in / 
# Tue, 02 Aug 2022 01:30:52 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 03:44:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 03 Aug 2022 03:44:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 19:16:47 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 19:19:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 19:19:19 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1a9ff13e38cae7994b55e6db5c3d190d2b7a03043ae238a6f71a285376de46bb`  
		Last Modified: Tue, 02 Aug 2022 01:33:07 GMT  
		Size: 30.4 MB (30441470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99970d1735353adabddaef52faa1237908c9cdf39198088cf543cb21ecb3fa69`  
		Last Modified: Wed, 03 Aug 2022 03:52:54 GMT  
		Size: 3.1 MB (3075943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9501b5b22fed4db7ff494e125e8d08db9f15c579219c407c9707f7051a82644`  
		Last Modified: Fri, 26 Aug 2022 19:25:25 GMT  
		Size: 128.9 MB (128895069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:00cd2eaa02ca5ad01bf0373fd720cca3cc59c7518e1e95dad2857cddc3a5d839
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154502164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73d216c3a69dba42223d14fdb977e1cbc0656370a8474e89450c14ecd90d196`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:01:57 GMT
ADD file:3d2e9b401524527b395347bc3847be7c9cb465b9a214a1a1d31e74330e293c45 in / 
# Tue, 02 Aug 2022 01:01:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:19:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 13:19:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 18:41:51 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 18:42:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 18:42:46 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:be3ed498266c519f84268ff1f02085fa249c0e32fb60a59466e24c862b5f094b`  
		Last Modified: Tue, 02 Aug 2022 01:03:25 GMT  
		Size: 25.4 MB (25369584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2ed0adcefe11b30e3dff027bcb1cb9fe759f39f50b008bafb3644d3d2fcba8`  
		Last Modified: Tue, 02 Aug 2022 13:22:41 GMT  
		Size: 2.7 MB (2671706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811ae78985ec89d3fada71c34fdf570518d7e32fa5472f26184d5756ae76fdd3`  
		Last Modified: Fri, 26 Aug 2022 18:45:21 GMT  
		Size: 126.5 MB (126460874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:263b0490cba0d6984ff7147d57dbd781c20c0239a2b40b9d20b65c795aa834ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:9971eb51472410f69d29bea1ca972b1448d20c741fa9b0a8e518145a862477ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196154912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ef5fde90c59b389280d3c6f756995c48ed0ba2b1839045fa6c496537dc7976`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:09:52 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 20:10:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 19:19:41 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 19:22:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 19:22:48 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6715a1bb89fcf5e91403be2bc6130f23e6b3cfd0da73e6b09e937d028409d3`  
		Last Modified: Tue, 02 Aug 2022 20:13:24 GMT  
		Size: 3.0 MB (2957815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6cdce2ccb323bebec9b805ea2dc497e05c29bb130b9e677f16b8d640f67e2e`  
		Last Modified: Fri, 26 Aug 2022 19:24:03 GMT  
		Size: 166.5 MB (166486827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:5706e481beb2961655b941f9145da971f64abd725a1fb3d6dbd34d05345b731d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184645856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9026932eb4af386e6d12486d92b92ac520d3126054a6c8199a01a2be81460270`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:50:55 GMT
ADD file:6d22c6318075d01068d0a9213f33655abf6c251f8a71d98c17b857b9021b43bd in / 
# Tue, 02 Aug 2022 00:50:55 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:23:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 16:23:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 18:38:36 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 18:41:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 18:41:21 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:5496b4c91dece81ce997c62cf2e1ef6f1764e612c6e8f0b385722c6645e4ad30`  
		Last Modified: Tue, 02 Aug 2022 00:51:39 GMT  
		Size: 27.2 MB (27164268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0dd584134d885dc07df56cb1531c30c56e50d96a7cc1cb92c61c41813d18e0`  
		Last Modified: Tue, 02 Aug 2022 16:27:10 GMT  
		Size: 3.0 MB (2983285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b418c6060077b571834f79c19cdd79d37e05c48bffc73222ce29ab3751bf6d33`  
		Last Modified: Fri, 26 Aug 2022 18:43:20 GMT  
		Size: 154.5 MB (154498303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1a35791d89e28d527d8038c85395a204d3f1df9f054f06857653424c774c6bdf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199681572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b1894d66f2aafdedb5ab94fa1cabfc83f327c351a3da4f8fa377f4c484d84d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:50 GMT
ADD file:32fc7b9b5853c93c45b1a96054c30104fd200ac7d40d0388aff736c478f917cb in / 
# Tue, 02 Aug 2022 01:30:52 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 03:44:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 03 Aug 2022 03:44:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 19:16:47 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 19:24:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 19:24:34 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1a9ff13e38cae7994b55e6db5c3d190d2b7a03043ae238a6f71a285376de46bb`  
		Last Modified: Tue, 02 Aug 2022 01:33:07 GMT  
		Size: 30.4 MB (30441470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99970d1735353adabddaef52faa1237908c9cdf39198088cf543cb21ecb3fa69`  
		Last Modified: Wed, 03 Aug 2022 03:52:54 GMT  
		Size: 3.1 MB (3075943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3cdcfd9d87a8f2ec1af50b373d04ca288c74903f98a94be3703b54c7005a42`  
		Last Modified: Fri, 26 Aug 2022 19:26:26 GMT  
		Size: 166.2 MB (166164159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:0db5690c7d2328d01412a8d9fbb5cff39a6bbe8d7eb18c99685b02e41ef6f31f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184801432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a6cc4673186cdc592f2ec0a2a6ec2924980dd0745d3d7ccf572cffa1ed718f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:01:57 GMT
ADD file:3d2e9b401524527b395347bc3847be7c9cb465b9a214a1a1d31e74330e293c45 in / 
# Tue, 02 Aug 2022 01:01:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:19:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 13:19:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 18:41:51 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 18:44:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 18:44:40 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:be3ed498266c519f84268ff1f02085fa249c0e32fb60a59466e24c862b5f094b`  
		Last Modified: Tue, 02 Aug 2022 01:03:25 GMT  
		Size: 25.4 MB (25369584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2ed0adcefe11b30e3dff027bcb1cb9fe759f39f50b008bafb3644d3d2fcba8`  
		Last Modified: Tue, 02 Aug 2022 13:22:41 GMT  
		Size: 2.7 MB (2671706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a6f64148edbea443a0ce18ea8770812e8fc9c7e48afc9808e782af72b93618`  
		Last Modified: Fri, 26 Aug 2022 18:45:54 GMT  
		Size: 156.8 MB (156760142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:8b4a522c4009b0c0f88fc12e86688f264b3cdc4d719dcb1f8feafcb899359a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:3e6db5052f954d718c4a0a629182a229238e9800e76228b321fed29f8b62cb7c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94688367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226b92eb5103f6c963f4f890e6f67aab5aed6b1564e93720318475dac7d2f3a5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:09:52 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 20:10:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 19:19:41 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 19:21:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b3760f9f5ec720bcfee6e2a21cfe3e7d3539513ebd9e51e1a1b9998bb768c7a';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='c7e3ddae49d67eae37a70e48593214e8387aa07599479a22b2cfd1e3eb73aae0';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='820a906fbd7dd8b6d91ef8573376080e7596e9c70eb87d052b08a48bfa1eda79';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='052f7c06e16187b123b5e3007ed39c2b14176fcd7ae9b9da029469fe57da69d8';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='f9cb898fce2b3c2a384db5e998a73007265a5f45c11a0cee13e742fc84311c52';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 19:21:30 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6715a1bb89fcf5e91403be2bc6130f23e6b3cfd0da73e6b09e937d028409d3`  
		Last Modified: Tue, 02 Aug 2022 20:13:24 GMT  
		Size: 3.0 MB (2957815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96bdbca13caefef9196c4bb6b40ae6f65058bb787abb1fcb8a6c33551fbab8e5`  
		Last Modified: Fri, 26 Aug 2022 19:23:42 GMT  
		Size: 65.0 MB (65020282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:1b4100e525ff30fb0ff76a75d0ed5dac389fba34145996c3ce0f136bbad5820c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94531869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0fb32d98db7203f77d3833f326dd4a004e5fe963b0efcaa595a7c0458ea2f23`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:50:55 GMT
ADD file:6d22c6318075d01068d0a9213f33655abf6c251f8a71d98c17b857b9021b43bd in / 
# Tue, 02 Aug 2022 00:50:55 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:23:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 16:23:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 18:38:36 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 18:40:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b3760f9f5ec720bcfee6e2a21cfe3e7d3539513ebd9e51e1a1b9998bb768c7a';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='c7e3ddae49d67eae37a70e48593214e8387aa07599479a22b2cfd1e3eb73aae0';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='820a906fbd7dd8b6d91ef8573376080e7596e9c70eb87d052b08a48bfa1eda79';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='052f7c06e16187b123b5e3007ed39c2b14176fcd7ae9b9da029469fe57da69d8';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='f9cb898fce2b3c2a384db5e998a73007265a5f45c11a0cee13e742fc84311c52';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 18:40:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:5496b4c91dece81ce997c62cf2e1ef6f1764e612c6e8f0b385722c6645e4ad30`  
		Last Modified: Tue, 02 Aug 2022 00:51:39 GMT  
		Size: 27.2 MB (27164268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0dd584134d885dc07df56cb1531c30c56e50d96a7cc1cb92c61c41813d18e0`  
		Last Modified: Tue, 02 Aug 2022 16:27:10 GMT  
		Size: 3.0 MB (2983285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6528bca0536b1763afc195ef53119aac04fd8e3fbd8a8c6d98d2867bf7ae9f`  
		Last Modified: Fri, 26 Aug 2022 18:42:38 GMT  
		Size: 64.4 MB (64384316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:dd72846d3c1d6ee68f3c2f1ae72be0af92ac90cf8507f1eed0543b5a93d908a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98752540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d6a38a82258e2c18e442f7c87e78f902faa01d07c4fdada5b6e3c3f5a75396`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:50 GMT
ADD file:32fc7b9b5853c93c45b1a96054c30104fd200ac7d40d0388aff736c478f917cb in / 
# Tue, 02 Aug 2022 01:30:52 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 03:44:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 03 Aug 2022 03:44:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 19:16:47 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 19:21:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b3760f9f5ec720bcfee6e2a21cfe3e7d3539513ebd9e51e1a1b9998bb768c7a';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='c7e3ddae49d67eae37a70e48593214e8387aa07599479a22b2cfd1e3eb73aae0';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='820a906fbd7dd8b6d91ef8573376080e7596e9c70eb87d052b08a48bfa1eda79';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='052f7c06e16187b123b5e3007ed39c2b14176fcd7ae9b9da029469fe57da69d8';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='f9cb898fce2b3c2a384db5e998a73007265a5f45c11a0cee13e742fc84311c52';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 19:21:23 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1a9ff13e38cae7994b55e6db5c3d190d2b7a03043ae238a6f71a285376de46bb`  
		Last Modified: Tue, 02 Aug 2022 01:33:07 GMT  
		Size: 30.4 MB (30441470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99970d1735353adabddaef52faa1237908c9cdf39198088cf543cb21ecb3fa69`  
		Last Modified: Wed, 03 Aug 2022 03:52:54 GMT  
		Size: 3.1 MB (3075943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12c134638b4339cc91ca3ed409c3a37e27a76d32874d1c4915870acc4925981`  
		Last Modified: Fri, 26 Aug 2022 19:25:55 GMT  
		Size: 65.2 MB (65235127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:781a1a89161dfdd76e78dab30d7c19c55b4a323adb300c1d2c0833519045fa37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94160799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b62fd986848465a8492832f586c3578686be3afcbaffc50ef780b94b287fa8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:01:57 GMT
ADD file:3d2e9b401524527b395347bc3847be7c9cb465b9a214a1a1d31e74330e293c45 in / 
# Tue, 02 Aug 2022 01:01:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:19:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 13:19:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 18:41:51 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 18:43:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b3760f9f5ec720bcfee6e2a21cfe3e7d3539513ebd9e51e1a1b9998bb768c7a';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='c7e3ddae49d67eae37a70e48593214e8387aa07599479a22b2cfd1e3eb73aae0';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='820a906fbd7dd8b6d91ef8573376080e7596e9c70eb87d052b08a48bfa1eda79';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='052f7c06e16187b123b5e3007ed39c2b14176fcd7ae9b9da029469fe57da69d8';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='f9cb898fce2b3c2a384db5e998a73007265a5f45c11a0cee13e742fc84311c52';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 18:43:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:be3ed498266c519f84268ff1f02085fa249c0e32fb60a59466e24c862b5f094b`  
		Last Modified: Tue, 02 Aug 2022 01:03:25 GMT  
		Size: 25.4 MB (25369584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2ed0adcefe11b30e3dff027bcb1cb9fe759f39f50b008bafb3644d3d2fcba8`  
		Last Modified: Tue, 02 Aug 2022 13:22:41 GMT  
		Size: 2.7 MB (2671706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cbf9cef742556563bb7cbecb7cd313dab5159f649063b7a6c44d16a4364e08`  
		Last Modified: Fri, 26 Aug 2022 18:45:37 GMT  
		Size: 66.1 MB (66119509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:75221bf9a1c2ccc846ce05205b26db6da6fe1ab33b4e2ae1aea7e6fbe51e2c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:2f84ac129faa2e8d64207bae1ef5d99149a9553b4de834f6b372a4a1d7cdc4ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159010292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f05c3b9b99fee213cdf386a94fce39816fab1c25ee708b151f53621ff3ad85c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:09:52 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 20:10:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 19:19:41 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 19:20:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 19:20:40 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6715a1bb89fcf5e91403be2bc6130f23e6b3cfd0da73e6b09e937d028409d3`  
		Last Modified: Tue, 02 Aug 2022 20:13:24 GMT  
		Size: 3.0 MB (2957815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a98fa70bcc08366a44c285d736a35471c6af0c09f278e8a51e1687daec0d70`  
		Last Modified: Fri, 26 Aug 2022 19:23:23 GMT  
		Size: 129.3 MB (129342207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; 386

```console
$ docker pull ibmjava@sha256:85e74c913750585e66de9c1d97c2c1f146eedd22746528ae81ce1df3d7558010
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147610305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137d978d6d28922ed0f50e0e710066b7bd1f0fd2cac9f5c2e49094945bd29978`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:50:55 GMT
ADD file:6d22c6318075d01068d0a9213f33655abf6c251f8a71d98c17b857b9021b43bd in / 
# Tue, 02 Aug 2022 00:50:55 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:23:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 16:23:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 18:38:36 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 18:39:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 18:39:27 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:5496b4c91dece81ce997c62cf2e1ef6f1764e612c6e8f0b385722c6645e4ad30`  
		Last Modified: Tue, 02 Aug 2022 00:51:39 GMT  
		Size: 27.2 MB (27164268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0dd584134d885dc07df56cb1531c30c56e50d96a7cc1cb92c61c41813d18e0`  
		Last Modified: Tue, 02 Aug 2022 16:27:10 GMT  
		Size: 3.0 MB (2983285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4754877954ce670bc1c090044af2c4dde2de36f4ad1ea1d2cdaa9e1ecce40df9`  
		Last Modified: Fri, 26 Aug 2022 18:42:09 GMT  
		Size: 117.5 MB (117462752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:5adc59a78a71a51002e2422e59defb3084a9339aa30fb54acf018a2318e26041
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162412482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c153f6fec2349df07565406ea5f5563a153be3673c7622b87f48b5eebfd648`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:50 GMT
ADD file:32fc7b9b5853c93c45b1a96054c30104fd200ac7d40d0388aff736c478f917cb in / 
# Tue, 02 Aug 2022 01:30:52 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 03:44:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 03 Aug 2022 03:44:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 19:16:47 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 19:19:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 19:19:19 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1a9ff13e38cae7994b55e6db5c3d190d2b7a03043ae238a6f71a285376de46bb`  
		Last Modified: Tue, 02 Aug 2022 01:33:07 GMT  
		Size: 30.4 MB (30441470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99970d1735353adabddaef52faa1237908c9cdf39198088cf543cb21ecb3fa69`  
		Last Modified: Wed, 03 Aug 2022 03:52:54 GMT  
		Size: 3.1 MB (3075943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9501b5b22fed4db7ff494e125e8d08db9f15c579219c407c9707f7051a82644`  
		Last Modified: Fri, 26 Aug 2022 19:25:25 GMT  
		Size: 128.9 MB (128895069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:00cd2eaa02ca5ad01bf0373fd720cca3cc59c7518e1e95dad2857cddc3a5d839
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154502164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73d216c3a69dba42223d14fdb977e1cbc0656370a8474e89450c14ecd90d196`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:01:57 GMT
ADD file:3d2e9b401524527b395347bc3847be7c9cb465b9a214a1a1d31e74330e293c45 in / 
# Tue, 02 Aug 2022 01:01:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:19:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 13:19:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 18:41:51 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 18:42:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 18:42:46 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:be3ed498266c519f84268ff1f02085fa249c0e32fb60a59466e24c862b5f094b`  
		Last Modified: Tue, 02 Aug 2022 01:03:25 GMT  
		Size: 25.4 MB (25369584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2ed0adcefe11b30e3dff027bcb1cb9fe759f39f50b008bafb3644d3d2fcba8`  
		Last Modified: Tue, 02 Aug 2022 13:22:41 GMT  
		Size: 2.7 MB (2671706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811ae78985ec89d3fada71c34fdf570518d7e32fa5472f26184d5756ae76fdd3`  
		Last Modified: Fri, 26 Aug 2022 18:45:21 GMT  
		Size: 126.5 MB (126460874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:75221bf9a1c2ccc846ce05205b26db6da6fe1ab33b4e2ae1aea7e6fbe51e2c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:latest` - linux; amd64

```console
$ docker pull ibmjava@sha256:2f84ac129faa2e8d64207bae1ef5d99149a9553b4de834f6b372a4a1d7cdc4ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159010292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f05c3b9b99fee213cdf386a94fce39816fab1c25ee708b151f53621ff3ad85c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:09:52 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 20:10:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 19:19:41 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 19:20:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 19:20:40 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6715a1bb89fcf5e91403be2bc6130f23e6b3cfd0da73e6b09e937d028409d3`  
		Last Modified: Tue, 02 Aug 2022 20:13:24 GMT  
		Size: 3.0 MB (2957815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a98fa70bcc08366a44c285d736a35471c6af0c09f278e8a51e1687daec0d70`  
		Last Modified: Fri, 26 Aug 2022 19:23:23 GMT  
		Size: 129.3 MB (129342207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; 386

```console
$ docker pull ibmjava@sha256:85e74c913750585e66de9c1d97c2c1f146eedd22746528ae81ce1df3d7558010
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147610305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137d978d6d28922ed0f50e0e710066b7bd1f0fd2cac9f5c2e49094945bd29978`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:50:55 GMT
ADD file:6d22c6318075d01068d0a9213f33655abf6c251f8a71d98c17b857b9021b43bd in / 
# Tue, 02 Aug 2022 00:50:55 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:23:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 16:23:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 18:38:36 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 18:39:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 18:39:27 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:5496b4c91dece81ce997c62cf2e1ef6f1764e612c6e8f0b385722c6645e4ad30`  
		Last Modified: Tue, 02 Aug 2022 00:51:39 GMT  
		Size: 27.2 MB (27164268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0dd584134d885dc07df56cb1531c30c56e50d96a7cc1cb92c61c41813d18e0`  
		Last Modified: Tue, 02 Aug 2022 16:27:10 GMT  
		Size: 3.0 MB (2983285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4754877954ce670bc1c090044af2c4dde2de36f4ad1ea1d2cdaa9e1ecce40df9`  
		Last Modified: Fri, 26 Aug 2022 18:42:09 GMT  
		Size: 117.5 MB (117462752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:5adc59a78a71a51002e2422e59defb3084a9339aa30fb54acf018a2318e26041
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162412482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c153f6fec2349df07565406ea5f5563a153be3673c7622b87f48b5eebfd648`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:50 GMT
ADD file:32fc7b9b5853c93c45b1a96054c30104fd200ac7d40d0388aff736c478f917cb in / 
# Tue, 02 Aug 2022 01:30:52 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 03:44:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 03 Aug 2022 03:44:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 19:16:47 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 19:19:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 19:19:19 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1a9ff13e38cae7994b55e6db5c3d190d2b7a03043ae238a6f71a285376de46bb`  
		Last Modified: Tue, 02 Aug 2022 01:33:07 GMT  
		Size: 30.4 MB (30441470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99970d1735353adabddaef52faa1237908c9cdf39198088cf543cb21ecb3fa69`  
		Last Modified: Wed, 03 Aug 2022 03:52:54 GMT  
		Size: 3.1 MB (3075943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9501b5b22fed4db7ff494e125e8d08db9f15c579219c407c9707f7051a82644`  
		Last Modified: Fri, 26 Aug 2022 19:25:25 GMT  
		Size: 128.9 MB (128895069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:00cd2eaa02ca5ad01bf0373fd720cca3cc59c7518e1e95dad2857cddc3a5d839
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154502164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73d216c3a69dba42223d14fdb977e1cbc0656370a8474e89450c14ecd90d196`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:01:57 GMT
ADD file:3d2e9b401524527b395347bc3847be7c9cb465b9a214a1a1d31e74330e293c45 in / 
# Tue, 02 Aug 2022 01:01:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:19:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 13:19:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 18:41:51 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 18:42:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 18:42:46 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:be3ed498266c519f84268ff1f02085fa249c0e32fb60a59466e24c862b5f094b`  
		Last Modified: Tue, 02 Aug 2022 01:03:25 GMT  
		Size: 25.4 MB (25369584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2ed0adcefe11b30e3dff027bcb1cb9fe759f39f50b008bafb3644d3d2fcba8`  
		Last Modified: Tue, 02 Aug 2022 13:22:41 GMT  
		Size: 2.7 MB (2671706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811ae78985ec89d3fada71c34fdf570518d7e32fa5472f26184d5756ae76fdd3`  
		Last Modified: Fri, 26 Aug 2022 18:45:21 GMT  
		Size: 126.5 MB (126460874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:263b0490cba0d6984ff7147d57dbd781c20c0239a2b40b9d20b65c795aa834ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:9971eb51472410f69d29bea1ca972b1448d20c741fa9b0a8e518145a862477ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196154912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ef5fde90c59b389280d3c6f756995c48ed0ba2b1839045fa6c496537dc7976`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:09:52 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 20:10:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 19:19:41 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 19:22:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 19:22:48 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6715a1bb89fcf5e91403be2bc6130f23e6b3cfd0da73e6b09e937d028409d3`  
		Last Modified: Tue, 02 Aug 2022 20:13:24 GMT  
		Size: 3.0 MB (2957815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6cdce2ccb323bebec9b805ea2dc497e05c29bb130b9e677f16b8d640f67e2e`  
		Last Modified: Fri, 26 Aug 2022 19:24:03 GMT  
		Size: 166.5 MB (166486827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:5706e481beb2961655b941f9145da971f64abd725a1fb3d6dbd34d05345b731d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184645856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9026932eb4af386e6d12486d92b92ac520d3126054a6c8199a01a2be81460270`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:50:55 GMT
ADD file:6d22c6318075d01068d0a9213f33655abf6c251f8a71d98c17b857b9021b43bd in / 
# Tue, 02 Aug 2022 00:50:55 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:23:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 16:23:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 18:38:36 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 18:41:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 18:41:21 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:5496b4c91dece81ce997c62cf2e1ef6f1764e612c6e8f0b385722c6645e4ad30`  
		Last Modified: Tue, 02 Aug 2022 00:51:39 GMT  
		Size: 27.2 MB (27164268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0dd584134d885dc07df56cb1531c30c56e50d96a7cc1cb92c61c41813d18e0`  
		Last Modified: Tue, 02 Aug 2022 16:27:10 GMT  
		Size: 3.0 MB (2983285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b418c6060077b571834f79c19cdd79d37e05c48bffc73222ce29ab3751bf6d33`  
		Last Modified: Fri, 26 Aug 2022 18:43:20 GMT  
		Size: 154.5 MB (154498303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1a35791d89e28d527d8038c85395a204d3f1df9f054f06857653424c774c6bdf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199681572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b1894d66f2aafdedb5ab94fa1cabfc83f327c351a3da4f8fa377f4c484d84d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:50 GMT
ADD file:32fc7b9b5853c93c45b1a96054c30104fd200ac7d40d0388aff736c478f917cb in / 
# Tue, 02 Aug 2022 01:30:52 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 03:44:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 03 Aug 2022 03:44:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 19:16:47 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 19:24:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 19:24:34 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1a9ff13e38cae7994b55e6db5c3d190d2b7a03043ae238a6f71a285376de46bb`  
		Last Modified: Tue, 02 Aug 2022 01:33:07 GMT  
		Size: 30.4 MB (30441470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99970d1735353adabddaef52faa1237908c9cdf39198088cf543cb21ecb3fa69`  
		Last Modified: Wed, 03 Aug 2022 03:52:54 GMT  
		Size: 3.1 MB (3075943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3cdcfd9d87a8f2ec1af50b373d04ca288c74903f98a94be3703b54c7005a42`  
		Last Modified: Fri, 26 Aug 2022 19:26:26 GMT  
		Size: 166.2 MB (166164159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:0db5690c7d2328d01412a8d9fbb5cff39a6bbe8d7eb18c99685b02e41ef6f31f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184801432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a6cc4673186cdc592f2ec0a2a6ec2924980dd0745d3d7ccf572cffa1ed718f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:01:57 GMT
ADD file:3d2e9b401524527b395347bc3847be7c9cb465b9a214a1a1d31e74330e293c45 in / 
# Tue, 02 Aug 2022 01:01:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:19:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 13:19:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 18:41:51 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 18:44:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 18:44:40 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:be3ed498266c519f84268ff1f02085fa249c0e32fb60a59466e24c862b5f094b`  
		Last Modified: Tue, 02 Aug 2022 01:03:25 GMT  
		Size: 25.4 MB (25369584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2ed0adcefe11b30e3dff027bcb1cb9fe759f39f50b008bafb3644d3d2fcba8`  
		Last Modified: Tue, 02 Aug 2022 13:22:41 GMT  
		Size: 2.7 MB (2671706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a6f64148edbea443a0ce18ea8770812e8fc9c7e48afc9808e782af72b93618`  
		Last Modified: Fri, 26 Aug 2022 18:45:54 GMT  
		Size: 156.8 MB (156760142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:8b4a522c4009b0c0f88fc12e86688f264b3cdc4d719dcb1f8feafcb899359a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:3e6db5052f954d718c4a0a629182a229238e9800e76228b321fed29f8b62cb7c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94688367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226b92eb5103f6c963f4f890e6f67aab5aed6b1564e93720318475dac7d2f3a5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:42 GMT
ADD file:0eb7f0555d03ff4f0755bba2c3d133e68737888f41390c17710f64b70c8e662a in / 
# Tue, 02 Aug 2022 01:30:42 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 20:09:52 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 20:10:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 19:19:41 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 19:21:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b3760f9f5ec720bcfee6e2a21cfe3e7d3539513ebd9e51e1a1b9998bb768c7a';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='c7e3ddae49d67eae37a70e48593214e8387aa07599479a22b2cfd1e3eb73aae0';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='820a906fbd7dd8b6d91ef8573376080e7596e9c70eb87d052b08a48bfa1eda79';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='052f7c06e16187b123b5e3007ed39c2b14176fcd7ae9b9da029469fe57da69d8';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='f9cb898fce2b3c2a384db5e998a73007265a5f45c11a0cee13e742fc84311c52';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 19:21:30 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:22c5ef60a68e3fa0bd8df52f48470e836e823434a3bead43e35e87098a0b01fa`  
		Last Modified: Mon, 01 Aug 2022 16:03:08 GMT  
		Size: 26.7 MB (26710270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6715a1bb89fcf5e91403be2bc6130f23e6b3cfd0da73e6b09e937d028409d3`  
		Last Modified: Tue, 02 Aug 2022 20:13:24 GMT  
		Size: 3.0 MB (2957815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96bdbca13caefef9196c4bb6b40ae6f65058bb787abb1fcb8a6c33551fbab8e5`  
		Last Modified: Fri, 26 Aug 2022 19:23:42 GMT  
		Size: 65.0 MB (65020282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:1b4100e525ff30fb0ff76a75d0ed5dac389fba34145996c3ce0f136bbad5820c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94531869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0fb32d98db7203f77d3833f326dd4a004e5fe963b0efcaa595a7c0458ea2f23`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 00:50:55 GMT
ADD file:6d22c6318075d01068d0a9213f33655abf6c251f8a71d98c17b857b9021b43bd in / 
# Tue, 02 Aug 2022 00:50:55 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 16:23:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 16:23:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 18:38:36 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 18:40:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b3760f9f5ec720bcfee6e2a21cfe3e7d3539513ebd9e51e1a1b9998bb768c7a';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='c7e3ddae49d67eae37a70e48593214e8387aa07599479a22b2cfd1e3eb73aae0';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='820a906fbd7dd8b6d91ef8573376080e7596e9c70eb87d052b08a48bfa1eda79';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='052f7c06e16187b123b5e3007ed39c2b14176fcd7ae9b9da029469fe57da69d8';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='f9cb898fce2b3c2a384db5e998a73007265a5f45c11a0cee13e742fc84311c52';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 18:40:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:5496b4c91dece81ce997c62cf2e1ef6f1764e612c6e8f0b385722c6645e4ad30`  
		Last Modified: Tue, 02 Aug 2022 00:51:39 GMT  
		Size: 27.2 MB (27164268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0dd584134d885dc07df56cb1531c30c56e50d96a7cc1cb92c61c41813d18e0`  
		Last Modified: Tue, 02 Aug 2022 16:27:10 GMT  
		Size: 3.0 MB (2983285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6528bca0536b1763afc195ef53119aac04fd8e3fbd8a8c6d98d2867bf7ae9f`  
		Last Modified: Fri, 26 Aug 2022 18:42:38 GMT  
		Size: 64.4 MB (64384316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:dd72846d3c1d6ee68f3c2f1ae72be0af92ac90cf8507f1eed0543b5a93d908a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98752540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d6a38a82258e2c18e442f7c87e78f902faa01d07c4fdada5b6e3c3f5a75396`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:50 GMT
ADD file:32fc7b9b5853c93c45b1a96054c30104fd200ac7d40d0388aff736c478f917cb in / 
# Tue, 02 Aug 2022 01:30:52 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 03:44:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 03 Aug 2022 03:44:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 19:16:47 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 19:21:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b3760f9f5ec720bcfee6e2a21cfe3e7d3539513ebd9e51e1a1b9998bb768c7a';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='c7e3ddae49d67eae37a70e48593214e8387aa07599479a22b2cfd1e3eb73aae0';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='820a906fbd7dd8b6d91ef8573376080e7596e9c70eb87d052b08a48bfa1eda79';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='052f7c06e16187b123b5e3007ed39c2b14176fcd7ae9b9da029469fe57da69d8';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='f9cb898fce2b3c2a384db5e998a73007265a5f45c11a0cee13e742fc84311c52';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 19:21:23 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1a9ff13e38cae7994b55e6db5c3d190d2b7a03043ae238a6f71a285376de46bb`  
		Last Modified: Tue, 02 Aug 2022 01:33:07 GMT  
		Size: 30.4 MB (30441470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99970d1735353adabddaef52faa1237908c9cdf39198088cf543cb21ecb3fa69`  
		Last Modified: Wed, 03 Aug 2022 03:52:54 GMT  
		Size: 3.1 MB (3075943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12c134638b4339cc91ca3ed409c3a37e27a76d32874d1c4915870acc4925981`  
		Last Modified: Fri, 26 Aug 2022 19:25:55 GMT  
		Size: 65.2 MB (65235127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:781a1a89161dfdd76e78dab30d7c19c55b4a323adb300c1d2c0833519045fa37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94160799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b62fd986848465a8492832f586c3578686be3afcbaffc50ef780b94b287fa8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:01:57 GMT
ADD file:3d2e9b401524527b395347bc3847be7c9cb465b9a214a1a1d31e74330e293c45 in / 
# Tue, 02 Aug 2022 01:01:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 13:19:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 02 Aug 2022 13:19:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Aug 2022 18:41:51 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 26 Aug 2022 18:43:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b3760f9f5ec720bcfee6e2a21cfe3e7d3539513ebd9e51e1a1b9998bb768c7a';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='c7e3ddae49d67eae37a70e48593214e8387aa07599479a22b2cfd1e3eb73aae0';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='820a906fbd7dd8b6d91ef8573376080e7596e9c70eb87d052b08a48bfa1eda79';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='052f7c06e16187b123b5e3007ed39c2b14176fcd7ae9b9da029469fe57da69d8';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='f9cb898fce2b3c2a384db5e998a73007265a5f45c11a0cee13e742fc84311c52';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Aug 2022 18:43:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:be3ed498266c519f84268ff1f02085fa249c0e32fb60a59466e24c862b5f094b`  
		Last Modified: Tue, 02 Aug 2022 01:03:25 GMT  
		Size: 25.4 MB (25369584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2ed0adcefe11b30e3dff027bcb1cb9fe759f39f50b008bafb3644d3d2fcba8`  
		Last Modified: Tue, 02 Aug 2022 13:22:41 GMT  
		Size: 2.7 MB (2671706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cbf9cef742556563bb7cbecb7cd313dab5159f649063b7a6c44d16a4364e08`  
		Last Modified: Fri, 26 Aug 2022 18:45:37 GMT  
		Size: 66.1 MB (66119509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
