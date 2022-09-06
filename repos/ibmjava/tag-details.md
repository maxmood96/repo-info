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
$ docker pull ibmjava@sha256:daa7f364f22609dbbf4704bd6d0d91ffad3328dba77b9631c3947f6d03db0f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8` - linux; amd64

```console
$ docker pull ibmjava@sha256:feb1d7e0acbf1b7845dc432572e23064a74ca065119c58f1ba729a080c0c487e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159010074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee2a2c8d157e6c3838f6090f24ea51974f8bf31753eae8d9b666f25394be77d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:33:09 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Sep 2022 03:33:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:33:18 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 02 Sep 2022 03:34:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Sep 2022 03:34:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157830093eea5fa46b30d4135fd942c7664880357dd7417359d97eb1a68cf09a`  
		Last Modified: Fri, 02 Sep 2022 03:36:34 GMT  
		Size: 3.0 MB (2957843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e878949a754d958979ecdf2fa9b28074473049ad58d7bd32a63d0da4818362b9`  
		Last Modified: Fri, 02 Sep 2022 03:36:44 GMT  
		Size: 129.3 MB (129342146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; 386

```console
$ docker pull ibmjava@sha256:eed101b36ceffeee8d92f87890921197b482af7f56e86cc39dbf0b32a5372e82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147610769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42765ae1e5ce14ba8913744ccd9d715198cad2acf9ab675bfd51162d4b5b0165`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:40:06 GMT
ADD file:31701667cc90b9f4ce7d6ede94bf7dae4d63c49e62d3725094d547f9601e1165 in / 
# Tue, 06 Sep 2022 18:40:07 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 18:56:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 18:56:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 18:56:31 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 18:57:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 18:57:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:10d3032d1995d3163c20a7f2f197299fae258c2ad020a8fd586fd6b7dd1b0e1d`  
		Last Modified: Tue, 06 Sep 2022 18:40:53 GMT  
		Size: 27.2 MB (27164710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246b95ff97894a60bd98bbfe32df134abb0711c29aae72dd2607024590e794e8`  
		Last Modified: Tue, 06 Sep 2022 18:59:51 GMT  
		Size: 3.0 MB (2983211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b655dd18d139a9193f5dea9c38e377d47f98ef681c92d7862ffa94465fb07663`  
		Last Modified: Tue, 06 Sep 2022 18:59:58 GMT  
		Size: 117.5 MB (117462848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:227d7d09bf3f48ba9c00fa2627fbbfc2ee3999ee6fb32393d6b7d31da050cd81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162412143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac07db4be9add9b1d2891e4d1c39c81a85bd6fa3600d5e047f2164394a03b1e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:38 GMT
ADD file:57b462f3139cb98a97a7020f0d1be33f5beb6500115500a9bfd7aaec39854e35 in / 
# Thu, 01 Sep 2022 23:49:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:21:23 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Sep 2022 04:21:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:21:37 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 02 Sep 2022 04:24:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Sep 2022 04:24:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:c48fbbfad89e07e20864186f593c37c87089700f93ddb1b88e1912f891bf3ae2`  
		Last Modified: Thu, 01 Sep 2022 23:51:47 GMT  
		Size: 30.4 MB (30441333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fffad9d09df8eacfb827ff53912f2db90c9b5d206f352fe60189296aa85884`  
		Last Modified: Fri, 02 Sep 2022 04:29:31 GMT  
		Size: 3.1 MB (3075853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03285ad6d5cde21a4e0b8954de2f1e548e19f4050e1135988b6b2540e81c44e7`  
		Last Modified: Fri, 02 Sep 2022 04:29:47 GMT  
		Size: 128.9 MB (128894957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:65384fec9cfdc45a49b7313ba16ecefc0d3e2fe7dd30e5fbe32a4aeebc596acc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154502673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75774e32f7cb3f45430565fa996cdf95392683eb8b9b0ded699afd80eff00ca9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:43:36 GMT
ADD file:dbe2a8e3943129e654ee29c636cab2bb10dd7eb0ac27d51e6954af2ccbe22807 in / 
# Tue, 06 Sep 2022 18:43:37 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 19:00:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 19:00:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:00:55 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 19:01:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 19:01:47 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:be6761156800c616810cb8aeb5b3ae71b9a2082f1c1221210befe119f082e879`  
		Last Modified: Tue, 06 Sep 2022 18:45:00 GMT  
		Size: 25.4 MB (25370130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85df87bfee2629b9bcbd6e19094a6bef3a7109cc473de2f41ee8e4f7d454d2b3`  
		Last Modified: Tue, 06 Sep 2022 19:04:07 GMT  
		Size: 2.7 MB (2671671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d483a11afa5fa57f7836535de21cd2c129e994527a0aabd4ee8a1a3a468581d4`  
		Last Modified: Tue, 06 Sep 2022 19:04:16 GMT  
		Size: 126.5 MB (126460872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:daa7f364f22609dbbf4704bd6d0d91ffad3328dba77b9631c3947f6d03db0f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:feb1d7e0acbf1b7845dc432572e23064a74ca065119c58f1ba729a080c0c487e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159010074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee2a2c8d157e6c3838f6090f24ea51974f8bf31753eae8d9b666f25394be77d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:33:09 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Sep 2022 03:33:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:33:18 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 02 Sep 2022 03:34:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Sep 2022 03:34:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157830093eea5fa46b30d4135fd942c7664880357dd7417359d97eb1a68cf09a`  
		Last Modified: Fri, 02 Sep 2022 03:36:34 GMT  
		Size: 3.0 MB (2957843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e878949a754d958979ecdf2fa9b28074473049ad58d7bd32a63d0da4818362b9`  
		Last Modified: Fri, 02 Sep 2022 03:36:44 GMT  
		Size: 129.3 MB (129342146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; 386

```console
$ docker pull ibmjava@sha256:eed101b36ceffeee8d92f87890921197b482af7f56e86cc39dbf0b32a5372e82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147610769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42765ae1e5ce14ba8913744ccd9d715198cad2acf9ab675bfd51162d4b5b0165`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:40:06 GMT
ADD file:31701667cc90b9f4ce7d6ede94bf7dae4d63c49e62d3725094d547f9601e1165 in / 
# Tue, 06 Sep 2022 18:40:07 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 18:56:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 18:56:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 18:56:31 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 18:57:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 18:57:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:10d3032d1995d3163c20a7f2f197299fae258c2ad020a8fd586fd6b7dd1b0e1d`  
		Last Modified: Tue, 06 Sep 2022 18:40:53 GMT  
		Size: 27.2 MB (27164710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246b95ff97894a60bd98bbfe32df134abb0711c29aae72dd2607024590e794e8`  
		Last Modified: Tue, 06 Sep 2022 18:59:51 GMT  
		Size: 3.0 MB (2983211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b655dd18d139a9193f5dea9c38e377d47f98ef681c92d7862ffa94465fb07663`  
		Last Modified: Tue, 06 Sep 2022 18:59:58 GMT  
		Size: 117.5 MB (117462848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:227d7d09bf3f48ba9c00fa2627fbbfc2ee3999ee6fb32393d6b7d31da050cd81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162412143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac07db4be9add9b1d2891e4d1c39c81a85bd6fa3600d5e047f2164394a03b1e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:38 GMT
ADD file:57b462f3139cb98a97a7020f0d1be33f5beb6500115500a9bfd7aaec39854e35 in / 
# Thu, 01 Sep 2022 23:49:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:21:23 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Sep 2022 04:21:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:21:37 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 02 Sep 2022 04:24:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Sep 2022 04:24:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:c48fbbfad89e07e20864186f593c37c87089700f93ddb1b88e1912f891bf3ae2`  
		Last Modified: Thu, 01 Sep 2022 23:51:47 GMT  
		Size: 30.4 MB (30441333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fffad9d09df8eacfb827ff53912f2db90c9b5d206f352fe60189296aa85884`  
		Last Modified: Fri, 02 Sep 2022 04:29:31 GMT  
		Size: 3.1 MB (3075853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03285ad6d5cde21a4e0b8954de2f1e548e19f4050e1135988b6b2540e81c44e7`  
		Last Modified: Fri, 02 Sep 2022 04:29:47 GMT  
		Size: 128.9 MB (128894957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:65384fec9cfdc45a49b7313ba16ecefc0d3e2fe7dd30e5fbe32a4aeebc596acc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154502673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75774e32f7cb3f45430565fa996cdf95392683eb8b9b0ded699afd80eff00ca9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:43:36 GMT
ADD file:dbe2a8e3943129e654ee29c636cab2bb10dd7eb0ac27d51e6954af2ccbe22807 in / 
# Tue, 06 Sep 2022 18:43:37 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 19:00:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 19:00:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:00:55 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 19:01:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 19:01:47 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:be6761156800c616810cb8aeb5b3ae71b9a2082f1c1221210befe119f082e879`  
		Last Modified: Tue, 06 Sep 2022 18:45:00 GMT  
		Size: 25.4 MB (25370130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85df87bfee2629b9bcbd6e19094a6bef3a7109cc473de2f41ee8e4f7d454d2b3`  
		Last Modified: Tue, 06 Sep 2022 19:04:07 GMT  
		Size: 2.7 MB (2671671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d483a11afa5fa57f7836535de21cd2c129e994527a0aabd4ee8a1a3a468581d4`  
		Last Modified: Tue, 06 Sep 2022 19:04:16 GMT  
		Size: 126.5 MB (126460872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:ffb8bbfebab4daacb0991eb69f8d263fbe38738da27a6b4e7308352f5ff39300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:26067464526923c481c494718454de875a37e6513e4e699f26ad5371e9e0cc41
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196155297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa2e570259f28fcfa357176b4ba637f7ee1dcf03ce56f2450f57d3c47186938`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:33:09 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Sep 2022 03:33:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:33:18 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 02 Sep 2022 03:36:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Sep 2022 03:36:09 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157830093eea5fa46b30d4135fd942c7664880357dd7417359d97eb1a68cf09a`  
		Last Modified: Fri, 02 Sep 2022 03:36:34 GMT  
		Size: 3.0 MB (2957843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7630f172482f6f0ad189c3a43dcddff43ae6b72aede2fe1a6c6521650cc918`  
		Last Modified: Fri, 02 Sep 2022 03:37:24 GMT  
		Size: 166.5 MB (166487369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:4f8ac7b6babd7f5134688f50cc98181c1b0c69f24786ce926625884d105675b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184646115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d05d454ec0bb7122b232e171a5a54071afcff8d9b51a790d2a4af112890ef13`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:40:06 GMT
ADD file:31701667cc90b9f4ce7d6ede94bf7dae4d63c49e62d3725094d547f9601e1165 in / 
# Tue, 06 Sep 2022 18:40:07 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 18:56:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 18:56:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 18:56:31 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 18:59:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 18:59:16 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:10d3032d1995d3163c20a7f2f197299fae258c2ad020a8fd586fd6b7dd1b0e1d`  
		Last Modified: Tue, 06 Sep 2022 18:40:53 GMT  
		Size: 27.2 MB (27164710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246b95ff97894a60bd98bbfe32df134abb0711c29aae72dd2607024590e794e8`  
		Last Modified: Tue, 06 Sep 2022 18:59:51 GMT  
		Size: 3.0 MB (2983211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512724726918b6067a91dd1d2bb0a01890a704aa6e8ea39ce0a96938837acdc6`  
		Last Modified: Tue, 06 Sep 2022 19:00:48 GMT  
		Size: 154.5 MB (154498194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:14cbea2b5201fbca19cfa3392f9aba072e3c33345e13b8708f12857cd4f841ec
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199681097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcaf485a890a2b547293081247528749a683fb98ef4b32dea87829517396b6e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:38 GMT
ADD file:57b462f3139cb98a97a7020f0d1be33f5beb6500115500a9bfd7aaec39854e35 in / 
# Thu, 01 Sep 2022 23:49:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:21:23 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Sep 2022 04:21:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:21:37 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 02 Sep 2022 04:28:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Sep 2022 04:29:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:c48fbbfad89e07e20864186f593c37c87089700f93ddb1b88e1912f891bf3ae2`  
		Last Modified: Thu, 01 Sep 2022 23:51:47 GMT  
		Size: 30.4 MB (30441333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fffad9d09df8eacfb827ff53912f2db90c9b5d206f352fe60189296aa85884`  
		Last Modified: Fri, 02 Sep 2022 04:29:31 GMT  
		Size: 3.1 MB (3075853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0197ecfec3122b9a28749937ef4a45bce412fe3f13345b81bd90173cc63346e`  
		Last Modified: Fri, 02 Sep 2022 04:30:45 GMT  
		Size: 166.2 MB (166163911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:892c43499038e11eb0a0b02560ed5bf5cce778f84416f6ab9c846aaca012fc35
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184801958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f29b95df453ed3830153ad669587d1385904c9c9a2447a44a6917fa97a4f5a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:43:36 GMT
ADD file:dbe2a8e3943129e654ee29c636cab2bb10dd7eb0ac27d51e6954af2ccbe22807 in / 
# Tue, 06 Sep 2022 18:43:37 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 19:00:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 19:00:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:00:55 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 19:03:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 19:03:37 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:be6761156800c616810cb8aeb5b3ae71b9a2082f1c1221210befe119f082e879`  
		Last Modified: Tue, 06 Sep 2022 18:45:00 GMT  
		Size: 25.4 MB (25370130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85df87bfee2629b9bcbd6e19094a6bef3a7109cc473de2f41ee8e4f7d454d2b3`  
		Last Modified: Tue, 06 Sep 2022 19:04:07 GMT  
		Size: 2.7 MB (2671671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f7c8c37bccd761caca18ceb0d6cce477753e96bf38f326628e381a5566b9aa`  
		Last Modified: Tue, 06 Sep 2022 19:04:50 GMT  
		Size: 156.8 MB (156760157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:025b3805f6afb6a7ce8e1c5b36fe5a64341937e6e1206ca9bd13c5018c1f93d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:41df0dd965c8a61c21a7bb2dae361d8a0b7fea88fa9db1f8406aec3bd2b019f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94688195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9472ee3cbc38be63ac9f02c403ac9c2c95b0d59a2db85d6f593abf22677713f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:33:09 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Sep 2022 03:33:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:33:18 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 02 Sep 2022 03:34:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b3760f9f5ec720bcfee6e2a21cfe3e7d3539513ebd9e51e1a1b9998bb768c7a';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='c7e3ddae49d67eae37a70e48593214e8387aa07599479a22b2cfd1e3eb73aae0';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='820a906fbd7dd8b6d91ef8573376080e7596e9c70eb87d052b08a48bfa1eda79';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='052f7c06e16187b123b5e3007ed39c2b14176fcd7ae9b9da029469fe57da69d8';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='f9cb898fce2b3c2a384db5e998a73007265a5f45c11a0cee13e742fc84311c52';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Sep 2022 03:34:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157830093eea5fa46b30d4135fd942c7664880357dd7417359d97eb1a68cf09a`  
		Last Modified: Fri, 02 Sep 2022 03:36:34 GMT  
		Size: 3.0 MB (2957843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86141b0359b392107dde7767d0ecf56e543f6aa88d5378fa4056c2f14f317570`  
		Last Modified: Fri, 02 Sep 2022 03:37:03 GMT  
		Size: 65.0 MB (65020267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:3e683db2c98016e1d2a6e9b810ce6164fcf638ffbc4e9fca04df0f52626edc3e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94532229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889e62733c1f9df9c6e29315b46e1e79d0c2c4b7bfac8e0c21f093cae2c53965`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:40:06 GMT
ADD file:31701667cc90b9f4ce7d6ede94bf7dae4d63c49e62d3725094d547f9601e1165 in / 
# Tue, 06 Sep 2022 18:40:07 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 18:56:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 18:56:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 18:56:31 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 18:58:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b3760f9f5ec720bcfee6e2a21cfe3e7d3539513ebd9e51e1a1b9998bb768c7a';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='c7e3ddae49d67eae37a70e48593214e8387aa07599479a22b2cfd1e3eb73aae0';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='820a906fbd7dd8b6d91ef8573376080e7596e9c70eb87d052b08a48bfa1eda79';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='052f7c06e16187b123b5e3007ed39c2b14176fcd7ae9b9da029469fe57da69d8';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='f9cb898fce2b3c2a384db5e998a73007265a5f45c11a0cee13e742fc84311c52';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 18:58:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:10d3032d1995d3163c20a7f2f197299fae258c2ad020a8fd586fd6b7dd1b0e1d`  
		Last Modified: Tue, 06 Sep 2022 18:40:53 GMT  
		Size: 27.2 MB (27164710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246b95ff97894a60bd98bbfe32df134abb0711c29aae72dd2607024590e794e8`  
		Last Modified: Tue, 06 Sep 2022 18:59:51 GMT  
		Size: 3.0 MB (2983211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fada85ea22469f60b63e8a005c8e3428755efe46d38c8ea194fd6bea30923fe0`  
		Last Modified: Tue, 06 Sep 2022 19:00:24 GMT  
		Size: 64.4 MB (64384308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:fa68abb114d00a9946236a2ad1733c2fb757dc89697f2f8c64ee47ebccda8d22
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98752332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e124f31245df794569797110a31a4c91110df7f2db76903f0ee9bf4bb83b2455`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:38 GMT
ADD file:57b462f3139cb98a97a7020f0d1be33f5beb6500115500a9bfd7aaec39854e35 in / 
# Thu, 01 Sep 2022 23:49:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:21:23 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Sep 2022 04:21:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:21:37 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 02 Sep 2022 04:25:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b3760f9f5ec720bcfee6e2a21cfe3e7d3539513ebd9e51e1a1b9998bb768c7a';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='c7e3ddae49d67eae37a70e48593214e8387aa07599479a22b2cfd1e3eb73aae0';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='820a906fbd7dd8b6d91ef8573376080e7596e9c70eb87d052b08a48bfa1eda79';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='052f7c06e16187b123b5e3007ed39c2b14176fcd7ae9b9da029469fe57da69d8';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='f9cb898fce2b3c2a384db5e998a73007265a5f45c11a0cee13e742fc84311c52';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Sep 2022 04:25:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:c48fbbfad89e07e20864186f593c37c87089700f93ddb1b88e1912f891bf3ae2`  
		Last Modified: Thu, 01 Sep 2022 23:51:47 GMT  
		Size: 30.4 MB (30441333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fffad9d09df8eacfb827ff53912f2db90c9b5d206f352fe60189296aa85884`  
		Last Modified: Fri, 02 Sep 2022 04:29:31 GMT  
		Size: 3.1 MB (3075853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348c637a8d3a8ee4bee569282b4a681893b6ace473be88449d9729ad93c85035`  
		Last Modified: Fri, 02 Sep 2022 04:30:14 GMT  
		Size: 65.2 MB (65235146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:b5b3645bee74d6044153bd570190fe6605e8f0dcc7857c87579e82d8d42498e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94161244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1faf50a2713c3dfb8e6791c620e06fce5bdf1f77392b437e0fb48349532ac073`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:43:36 GMT
ADD file:dbe2a8e3943129e654ee29c636cab2bb10dd7eb0ac27d51e6954af2ccbe22807 in / 
# Tue, 06 Sep 2022 18:43:37 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 19:00:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 19:00:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:00:55 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 19:02:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b3760f9f5ec720bcfee6e2a21cfe3e7d3539513ebd9e51e1a1b9998bb768c7a';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='c7e3ddae49d67eae37a70e48593214e8387aa07599479a22b2cfd1e3eb73aae0';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='820a906fbd7dd8b6d91ef8573376080e7596e9c70eb87d052b08a48bfa1eda79';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='052f7c06e16187b123b5e3007ed39c2b14176fcd7ae9b9da029469fe57da69d8';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='f9cb898fce2b3c2a384db5e998a73007265a5f45c11a0cee13e742fc84311c52';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 19:02:32 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:be6761156800c616810cb8aeb5b3ae71b9a2082f1c1221210befe119f082e879`  
		Last Modified: Tue, 06 Sep 2022 18:45:00 GMT  
		Size: 25.4 MB (25370130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85df87bfee2629b9bcbd6e19094a6bef3a7109cc473de2f41ee8e4f7d454d2b3`  
		Last Modified: Tue, 06 Sep 2022 19:04:07 GMT  
		Size: 2.7 MB (2671671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe04609738db02992b786c33f3658e78c696ec888097010dd150adf08e51b56`  
		Last Modified: Tue, 06 Sep 2022 19:04:32 GMT  
		Size: 66.1 MB (66119443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:daa7f364f22609dbbf4704bd6d0d91ffad3328dba77b9631c3947f6d03db0f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:feb1d7e0acbf1b7845dc432572e23064a74ca065119c58f1ba729a080c0c487e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159010074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee2a2c8d157e6c3838f6090f24ea51974f8bf31753eae8d9b666f25394be77d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:33:09 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Sep 2022 03:33:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:33:18 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 02 Sep 2022 03:34:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Sep 2022 03:34:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157830093eea5fa46b30d4135fd942c7664880357dd7417359d97eb1a68cf09a`  
		Last Modified: Fri, 02 Sep 2022 03:36:34 GMT  
		Size: 3.0 MB (2957843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e878949a754d958979ecdf2fa9b28074473049ad58d7bd32a63d0da4818362b9`  
		Last Modified: Fri, 02 Sep 2022 03:36:44 GMT  
		Size: 129.3 MB (129342146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; 386

```console
$ docker pull ibmjava@sha256:eed101b36ceffeee8d92f87890921197b482af7f56e86cc39dbf0b32a5372e82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147610769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42765ae1e5ce14ba8913744ccd9d715198cad2acf9ab675bfd51162d4b5b0165`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:40:06 GMT
ADD file:31701667cc90b9f4ce7d6ede94bf7dae4d63c49e62d3725094d547f9601e1165 in / 
# Tue, 06 Sep 2022 18:40:07 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 18:56:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 18:56:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 18:56:31 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 18:57:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 18:57:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:10d3032d1995d3163c20a7f2f197299fae258c2ad020a8fd586fd6b7dd1b0e1d`  
		Last Modified: Tue, 06 Sep 2022 18:40:53 GMT  
		Size: 27.2 MB (27164710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246b95ff97894a60bd98bbfe32df134abb0711c29aae72dd2607024590e794e8`  
		Last Modified: Tue, 06 Sep 2022 18:59:51 GMT  
		Size: 3.0 MB (2983211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b655dd18d139a9193f5dea9c38e377d47f98ef681c92d7862ffa94465fb07663`  
		Last Modified: Tue, 06 Sep 2022 18:59:58 GMT  
		Size: 117.5 MB (117462848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:227d7d09bf3f48ba9c00fa2627fbbfc2ee3999ee6fb32393d6b7d31da050cd81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162412143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac07db4be9add9b1d2891e4d1c39c81a85bd6fa3600d5e047f2164394a03b1e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:38 GMT
ADD file:57b462f3139cb98a97a7020f0d1be33f5beb6500115500a9bfd7aaec39854e35 in / 
# Thu, 01 Sep 2022 23:49:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:21:23 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Sep 2022 04:21:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:21:37 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 02 Sep 2022 04:24:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Sep 2022 04:24:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:c48fbbfad89e07e20864186f593c37c87089700f93ddb1b88e1912f891bf3ae2`  
		Last Modified: Thu, 01 Sep 2022 23:51:47 GMT  
		Size: 30.4 MB (30441333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fffad9d09df8eacfb827ff53912f2db90c9b5d206f352fe60189296aa85884`  
		Last Modified: Fri, 02 Sep 2022 04:29:31 GMT  
		Size: 3.1 MB (3075853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03285ad6d5cde21a4e0b8954de2f1e548e19f4050e1135988b6b2540e81c44e7`  
		Last Modified: Fri, 02 Sep 2022 04:29:47 GMT  
		Size: 128.9 MB (128894957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:65384fec9cfdc45a49b7313ba16ecefc0d3e2fe7dd30e5fbe32a4aeebc596acc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154502673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75774e32f7cb3f45430565fa996cdf95392683eb8b9b0ded699afd80eff00ca9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:43:36 GMT
ADD file:dbe2a8e3943129e654ee29c636cab2bb10dd7eb0ac27d51e6954af2ccbe22807 in / 
# Tue, 06 Sep 2022 18:43:37 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 19:00:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 19:00:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:00:55 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 19:01:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 19:01:47 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:be6761156800c616810cb8aeb5b3ae71b9a2082f1c1221210befe119f082e879`  
		Last Modified: Tue, 06 Sep 2022 18:45:00 GMT  
		Size: 25.4 MB (25370130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85df87bfee2629b9bcbd6e19094a6bef3a7109cc473de2f41ee8e4f7d454d2b3`  
		Last Modified: Tue, 06 Sep 2022 19:04:07 GMT  
		Size: 2.7 MB (2671671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d483a11afa5fa57f7836535de21cd2c129e994527a0aabd4ee8a1a3a468581d4`  
		Last Modified: Tue, 06 Sep 2022 19:04:16 GMT  
		Size: 126.5 MB (126460872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:daa7f364f22609dbbf4704bd6d0d91ffad3328dba77b9631c3947f6d03db0f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:latest` - linux; amd64

```console
$ docker pull ibmjava@sha256:feb1d7e0acbf1b7845dc432572e23064a74ca065119c58f1ba729a080c0c487e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159010074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee2a2c8d157e6c3838f6090f24ea51974f8bf31753eae8d9b666f25394be77d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:33:09 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Sep 2022 03:33:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:33:18 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 02 Sep 2022 03:34:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Sep 2022 03:34:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157830093eea5fa46b30d4135fd942c7664880357dd7417359d97eb1a68cf09a`  
		Last Modified: Fri, 02 Sep 2022 03:36:34 GMT  
		Size: 3.0 MB (2957843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e878949a754d958979ecdf2fa9b28074473049ad58d7bd32a63d0da4818362b9`  
		Last Modified: Fri, 02 Sep 2022 03:36:44 GMT  
		Size: 129.3 MB (129342146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; 386

```console
$ docker pull ibmjava@sha256:eed101b36ceffeee8d92f87890921197b482af7f56e86cc39dbf0b32a5372e82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147610769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42765ae1e5ce14ba8913744ccd9d715198cad2acf9ab675bfd51162d4b5b0165`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:40:06 GMT
ADD file:31701667cc90b9f4ce7d6ede94bf7dae4d63c49e62d3725094d547f9601e1165 in / 
# Tue, 06 Sep 2022 18:40:07 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 18:56:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 18:56:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 18:56:31 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 18:57:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 18:57:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:10d3032d1995d3163c20a7f2f197299fae258c2ad020a8fd586fd6b7dd1b0e1d`  
		Last Modified: Tue, 06 Sep 2022 18:40:53 GMT  
		Size: 27.2 MB (27164710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246b95ff97894a60bd98bbfe32df134abb0711c29aae72dd2607024590e794e8`  
		Last Modified: Tue, 06 Sep 2022 18:59:51 GMT  
		Size: 3.0 MB (2983211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b655dd18d139a9193f5dea9c38e377d47f98ef681c92d7862ffa94465fb07663`  
		Last Modified: Tue, 06 Sep 2022 18:59:58 GMT  
		Size: 117.5 MB (117462848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:227d7d09bf3f48ba9c00fa2627fbbfc2ee3999ee6fb32393d6b7d31da050cd81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162412143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac07db4be9add9b1d2891e4d1c39c81a85bd6fa3600d5e047f2164394a03b1e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:38 GMT
ADD file:57b462f3139cb98a97a7020f0d1be33f5beb6500115500a9bfd7aaec39854e35 in / 
# Thu, 01 Sep 2022 23:49:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:21:23 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Sep 2022 04:21:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:21:37 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 02 Sep 2022 04:24:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Sep 2022 04:24:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:c48fbbfad89e07e20864186f593c37c87089700f93ddb1b88e1912f891bf3ae2`  
		Last Modified: Thu, 01 Sep 2022 23:51:47 GMT  
		Size: 30.4 MB (30441333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fffad9d09df8eacfb827ff53912f2db90c9b5d206f352fe60189296aa85884`  
		Last Modified: Fri, 02 Sep 2022 04:29:31 GMT  
		Size: 3.1 MB (3075853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03285ad6d5cde21a4e0b8954de2f1e548e19f4050e1135988b6b2540e81c44e7`  
		Last Modified: Fri, 02 Sep 2022 04:29:47 GMT  
		Size: 128.9 MB (128894957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:65384fec9cfdc45a49b7313ba16ecefc0d3e2fe7dd30e5fbe32a4aeebc596acc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154502673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75774e32f7cb3f45430565fa996cdf95392683eb8b9b0ded699afd80eff00ca9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:43:36 GMT
ADD file:dbe2a8e3943129e654ee29c636cab2bb10dd7eb0ac27d51e6954af2ccbe22807 in / 
# Tue, 06 Sep 2022 18:43:37 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 19:00:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 19:00:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:00:55 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 19:01:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b789e740367f1c01581135052b66f35dff8c2cc780cdaeaa5075b5578d3e8e42';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='96c3433896f36f7c3f088c42629350778e13b878162d498d2f8df4e5b806d2cd';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='379517c106ff3e93f09f8b05821c8f98ddd7446a29d28f35a447f51e7fc4ce47';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='09c7c778c8163085a027e37f0f73a7142e7da77b921bc662c06f7fce223fa989';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='658d719236698b775def5f3b6643641db333d59b1729af51aa5f35da7144868e';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 19:01:47 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:be6761156800c616810cb8aeb5b3ae71b9a2082f1c1221210befe119f082e879`  
		Last Modified: Tue, 06 Sep 2022 18:45:00 GMT  
		Size: 25.4 MB (25370130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85df87bfee2629b9bcbd6e19094a6bef3a7109cc473de2f41ee8e4f7d454d2b3`  
		Last Modified: Tue, 06 Sep 2022 19:04:07 GMT  
		Size: 2.7 MB (2671671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d483a11afa5fa57f7836535de21cd2c129e994527a0aabd4ee8a1a3a468581d4`  
		Last Modified: Tue, 06 Sep 2022 19:04:16 GMT  
		Size: 126.5 MB (126460872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:ffb8bbfebab4daacb0991eb69f8d263fbe38738da27a6b4e7308352f5ff39300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:26067464526923c481c494718454de875a37e6513e4e699f26ad5371e9e0cc41
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196155297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa2e570259f28fcfa357176b4ba637f7ee1dcf03ce56f2450f57d3c47186938`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:33:09 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Sep 2022 03:33:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:33:18 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 02 Sep 2022 03:36:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Sep 2022 03:36:09 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157830093eea5fa46b30d4135fd942c7664880357dd7417359d97eb1a68cf09a`  
		Last Modified: Fri, 02 Sep 2022 03:36:34 GMT  
		Size: 3.0 MB (2957843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7630f172482f6f0ad189c3a43dcddff43ae6b72aede2fe1a6c6521650cc918`  
		Last Modified: Fri, 02 Sep 2022 03:37:24 GMT  
		Size: 166.5 MB (166487369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:4f8ac7b6babd7f5134688f50cc98181c1b0c69f24786ce926625884d105675b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184646115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d05d454ec0bb7122b232e171a5a54071afcff8d9b51a790d2a4af112890ef13`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:40:06 GMT
ADD file:31701667cc90b9f4ce7d6ede94bf7dae4d63c49e62d3725094d547f9601e1165 in / 
# Tue, 06 Sep 2022 18:40:07 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 18:56:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 18:56:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 18:56:31 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 18:59:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 18:59:16 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:10d3032d1995d3163c20a7f2f197299fae258c2ad020a8fd586fd6b7dd1b0e1d`  
		Last Modified: Tue, 06 Sep 2022 18:40:53 GMT  
		Size: 27.2 MB (27164710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246b95ff97894a60bd98bbfe32df134abb0711c29aae72dd2607024590e794e8`  
		Last Modified: Tue, 06 Sep 2022 18:59:51 GMT  
		Size: 3.0 MB (2983211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512724726918b6067a91dd1d2bb0a01890a704aa6e8ea39ce0a96938837acdc6`  
		Last Modified: Tue, 06 Sep 2022 19:00:48 GMT  
		Size: 154.5 MB (154498194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:14cbea2b5201fbca19cfa3392f9aba072e3c33345e13b8708f12857cd4f841ec
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.7 MB (199681097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcaf485a890a2b547293081247528749a683fb98ef4b32dea87829517396b6e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:38 GMT
ADD file:57b462f3139cb98a97a7020f0d1be33f5beb6500115500a9bfd7aaec39854e35 in / 
# Thu, 01 Sep 2022 23:49:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:21:23 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Sep 2022 04:21:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:21:37 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 02 Sep 2022 04:28:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Sep 2022 04:29:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:c48fbbfad89e07e20864186f593c37c87089700f93ddb1b88e1912f891bf3ae2`  
		Last Modified: Thu, 01 Sep 2022 23:51:47 GMT  
		Size: 30.4 MB (30441333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fffad9d09df8eacfb827ff53912f2db90c9b5d206f352fe60189296aa85884`  
		Last Modified: Fri, 02 Sep 2022 04:29:31 GMT  
		Size: 3.1 MB (3075853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0197ecfec3122b9a28749937ef4a45bce412fe3f13345b81bd90173cc63346e`  
		Last Modified: Fri, 02 Sep 2022 04:30:45 GMT  
		Size: 166.2 MB (166163911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:892c43499038e11eb0a0b02560ed5bf5cce778f84416f6ab9c846aaca012fc35
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184801958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f29b95df453ed3830153ad669587d1385904c9c9a2447a44a6917fa97a4f5a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:43:36 GMT
ADD file:dbe2a8e3943129e654ee29c636cab2bb10dd7eb0ac27d51e6954af2ccbe22807 in / 
# Tue, 06 Sep 2022 18:43:37 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 19:00:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 19:00:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:00:55 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 19:03:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 19:03:37 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:be6761156800c616810cb8aeb5b3ae71b9a2082f1c1221210befe119f082e879`  
		Last Modified: Tue, 06 Sep 2022 18:45:00 GMT  
		Size: 25.4 MB (25370130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85df87bfee2629b9bcbd6e19094a6bef3a7109cc473de2f41ee8e4f7d454d2b3`  
		Last Modified: Tue, 06 Sep 2022 19:04:07 GMT  
		Size: 2.7 MB (2671671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f7c8c37bccd761caca18ceb0d6cce477753e96bf38f326628e381a5566b9aa`  
		Last Modified: Tue, 06 Sep 2022 19:04:50 GMT  
		Size: 156.8 MB (156760157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:025b3805f6afb6a7ce8e1c5b36fe5a64341937e6e1206ca9bd13c5018c1f93d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:41df0dd965c8a61c21a7bb2dae361d8a0b7fea88fa9db1f8406aec3bd2b019f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94688195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9472ee3cbc38be63ac9f02c403ac9c2c95b0d59a2db85d6f593abf22677713f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:33:09 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Sep 2022 03:33:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:33:18 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 02 Sep 2022 03:34:54 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b3760f9f5ec720bcfee6e2a21cfe3e7d3539513ebd9e51e1a1b9998bb768c7a';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='c7e3ddae49d67eae37a70e48593214e8387aa07599479a22b2cfd1e3eb73aae0';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='820a906fbd7dd8b6d91ef8573376080e7596e9c70eb87d052b08a48bfa1eda79';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='052f7c06e16187b123b5e3007ed39c2b14176fcd7ae9b9da029469fe57da69d8';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='f9cb898fce2b3c2a384db5e998a73007265a5f45c11a0cee13e742fc84311c52';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Sep 2022 03:34:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157830093eea5fa46b30d4135fd942c7664880357dd7417359d97eb1a68cf09a`  
		Last Modified: Fri, 02 Sep 2022 03:36:34 GMT  
		Size: 3.0 MB (2957843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86141b0359b392107dde7767d0ecf56e543f6aa88d5378fa4056c2f14f317570`  
		Last Modified: Fri, 02 Sep 2022 03:37:03 GMT  
		Size: 65.0 MB (65020267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:3e683db2c98016e1d2a6e9b810ce6164fcf638ffbc4e9fca04df0f52626edc3e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94532229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889e62733c1f9df9c6e29315b46e1e79d0c2c4b7bfac8e0c21f093cae2c53965`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:40:06 GMT
ADD file:31701667cc90b9f4ce7d6ede94bf7dae4d63c49e62d3725094d547f9601e1165 in / 
# Tue, 06 Sep 2022 18:40:07 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 18:56:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 18:56:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 18:56:31 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 18:58:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b3760f9f5ec720bcfee6e2a21cfe3e7d3539513ebd9e51e1a1b9998bb768c7a';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='c7e3ddae49d67eae37a70e48593214e8387aa07599479a22b2cfd1e3eb73aae0';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='820a906fbd7dd8b6d91ef8573376080e7596e9c70eb87d052b08a48bfa1eda79';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='052f7c06e16187b123b5e3007ed39c2b14176fcd7ae9b9da029469fe57da69d8';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='f9cb898fce2b3c2a384db5e998a73007265a5f45c11a0cee13e742fc84311c52';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 18:58:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:10d3032d1995d3163c20a7f2f197299fae258c2ad020a8fd586fd6b7dd1b0e1d`  
		Last Modified: Tue, 06 Sep 2022 18:40:53 GMT  
		Size: 27.2 MB (27164710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246b95ff97894a60bd98bbfe32df134abb0711c29aae72dd2607024590e794e8`  
		Last Modified: Tue, 06 Sep 2022 18:59:51 GMT  
		Size: 3.0 MB (2983211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fada85ea22469f60b63e8a005c8e3428755efe46d38c8ea194fd6bea30923fe0`  
		Last Modified: Tue, 06 Sep 2022 19:00:24 GMT  
		Size: 64.4 MB (64384308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:fa68abb114d00a9946236a2ad1733c2fb757dc89697f2f8c64ee47ebccda8d22
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98752332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e124f31245df794569797110a31a4c91110df7f2db76903f0ee9bf4bb83b2455`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:38 GMT
ADD file:57b462f3139cb98a97a7020f0d1be33f5beb6500115500a9bfd7aaec39854e35 in / 
# Thu, 01 Sep 2022 23:49:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:21:23 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Sep 2022 04:21:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:21:37 GMT
ENV JAVA_VERSION=8.0.7.15
# Fri, 02 Sep 2022 04:25:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b3760f9f5ec720bcfee6e2a21cfe3e7d3539513ebd9e51e1a1b9998bb768c7a';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='c7e3ddae49d67eae37a70e48593214e8387aa07599479a22b2cfd1e3eb73aae0';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='820a906fbd7dd8b6d91ef8573376080e7596e9c70eb87d052b08a48bfa1eda79';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='052f7c06e16187b123b5e3007ed39c2b14176fcd7ae9b9da029469fe57da69d8';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='f9cb898fce2b3c2a384db5e998a73007265a5f45c11a0cee13e742fc84311c52';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 02 Sep 2022 04:25:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:c48fbbfad89e07e20864186f593c37c87089700f93ddb1b88e1912f891bf3ae2`  
		Last Modified: Thu, 01 Sep 2022 23:51:47 GMT  
		Size: 30.4 MB (30441333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fffad9d09df8eacfb827ff53912f2db90c9b5d206f352fe60189296aa85884`  
		Last Modified: Fri, 02 Sep 2022 04:29:31 GMT  
		Size: 3.1 MB (3075853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348c637a8d3a8ee4bee569282b4a681893b6ace473be88449d9729ad93c85035`  
		Last Modified: Fri, 02 Sep 2022 04:30:14 GMT  
		Size: 65.2 MB (65235146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:b5b3645bee74d6044153bd570190fe6605e8f0dcc7857c87579e82d8d42498e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94161244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1faf50a2713c3dfb8e6791c620e06fce5bdf1f77392b437e0fb48349532ac073`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Sep 2022 18:43:36 GMT
ADD file:dbe2a8e3943129e654ee29c636cab2bb10dd7eb0ac27d51e6954af2ccbe22807 in / 
# Tue, 06 Sep 2022 18:43:37 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 19:00:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 19:00:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:00:55 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 19:02:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b3760f9f5ec720bcfee6e2a21cfe3e7d3539513ebd9e51e1a1b9998bb768c7a';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='c7e3ddae49d67eae37a70e48593214e8387aa07599479a22b2cfd1e3eb73aae0';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='820a906fbd7dd8b6d91ef8573376080e7596e9c70eb87d052b08a48bfa1eda79';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='052f7c06e16187b123b5e3007ed39c2b14176fcd7ae9b9da029469fe57da69d8';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='f9cb898fce2b3c2a384db5e998a73007265a5f45c11a0cee13e742fc84311c52';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 19:02:32 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:be6761156800c616810cb8aeb5b3ae71b9a2082f1c1221210befe119f082e879`  
		Last Modified: Tue, 06 Sep 2022 18:45:00 GMT  
		Size: 25.4 MB (25370130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85df87bfee2629b9bcbd6e19094a6bef3a7109cc473de2f41ee8e4f7d454d2b3`  
		Last Modified: Tue, 06 Sep 2022 19:04:07 GMT  
		Size: 2.7 MB (2671671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe04609738db02992b786c33f3658e78c696ec888097010dd150adf08e51b56`  
		Last Modified: Tue, 06 Sep 2022 19:04:32 GMT  
		Size: 66.1 MB (66119443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
