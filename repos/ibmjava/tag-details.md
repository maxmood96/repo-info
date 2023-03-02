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
$ docker pull ibmjava@sha256:7fc7bd657d410c79ad36371a138baff3371bf49bcf980a5ab5cefa6f361d62aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8` - linux; amd64

```console
$ docker pull ibmjava@sha256:f8344d55f5aec48ae36de1d2bcc916f336e3588f4828acf58b82d46da8d79836
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158983841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa43273b3fdb28466b0ea2fcd0ea5403600ac78b0bf4ed6a7b837c0fd9301ac0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:52:57 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 18:53:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:53:08 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 18:54:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 18:54:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50d379550397205b8ddddb58a89653deca5ebaf37b5564da526dff208f1655e`  
		Last Modified: Tue, 31 Jan 2023 18:56:44 GMT  
		Size: 2.9 MB (2949581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7556f23e7ad4703b5bb5a5d97170999166c94d46ad5b493cecab2368f292ee`  
		Last Modified: Tue, 31 Jan 2023 18:56:53 GMT  
		Size: 129.3 MB (129322666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; 386

```console
$ docker pull ibmjava@sha256:8f8aef15e68b1cd9faf076f1f1685b61ef1bdd046d12cd89c353ad0496b2dc5c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147606447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acd7545ae7d84b1d7309a97d47dd319d1ff6a0b5b0b0d49081228dbcefd71cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:01 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:03 GMT
ADD file:b9b814a7d1e7611a2c531fac3419a48c733c622470d3f275ce29f9ba8764eaeb in / 
# Thu, 26 Jan 2023 10:03:04 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:43:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 17:43:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:43:20 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 17:44:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 17:44:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a1177ecacc42e51782037ed649a91241b82866cc72c6eb0f205cbcc350f44d43`  
		Last Modified: Tue, 31 Jan 2023 17:42:04 GMT  
		Size: 27.2 MB (27165349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bd4ed927791f68d34f96a84af2a713efcb2234c018146289b0a0fafb33eef2`  
		Last Modified: Tue, 31 Jan 2023 17:47:42 GMT  
		Size: 3.0 MB (2981539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a696e32069dd164ed13db4e11cb34f76ed3a52c02b60893b413cfdd53c0110`  
		Last Modified: Tue, 31 Jan 2023 17:47:49 GMT  
		Size: 117.5 MB (117459559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:accb3f91bf07505b05addb38cb91288811728973036119c3e0bf0f37854c0adf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162514738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32408a15087e13c59eaca5c5bb18b84fd2f97ee8c383a624af8c2dde3ef9e5bc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:43:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 18:44:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:44:01 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 18:46:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 18:46:20 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:15579125cdf95166fecb7637769c3c9eb2551401759fb21f44848947ead59cbd`  
		Last Modified: Tue, 31 Jan 2023 18:13:22 GMT  
		Size: 30.4 MB (30442586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3845debd31d52c26de72c4219e4ec0bd27d14c2986651d541a2135cadc9b48`  
		Last Modified: Tue, 31 Jan 2023 18:51:43 GMT  
		Size: 3.1 MB (3075781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e886f1423f03ec32342fc5b0ad9cff55a07614765fba8be473be7f1b30c0207b`  
		Last Modified: Tue, 31 Jan 2023 18:52:00 GMT  
		Size: 129.0 MB (128996371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:ceab38e1c632c83c0664d16ed5288764d28457f46df1b24de1824147409dec0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154513094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb1b58a416fc4340f49e5028cc0dab0d8bcc85981a32978aef3f8d3cbdc502d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:18:09 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:11 GMT
ADD file:49b5368b8703fe0aa128fe923b83da7ab2a30a7a1c0395682c905b9271e7f503 in / 
# Wed, 01 Mar 2023 03:18:11 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:01:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 02 Mar 2023 03:01:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 03:02:00 GMT
ENV JAVA_VERSION=8.0.7.20
# Thu, 02 Mar 2023 03:02:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 02 Mar 2023 03:02:51 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:306d1b363f89f239f5dc6314e0033094c067617b584ce004fd8db99402dab321`  
		Last Modified: Thu, 02 Mar 2023 02:21:31 GMT  
		Size: 25.4 MB (25371412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fe795fb99ed72a95436de37d2cdb8fbd2edb3445e421c880c502757fb41be9`  
		Last Modified: Thu, 02 Mar 2023 03:05:21 GMT  
		Size: 2.7 MB (2669070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71635f0577860033cfd705acd9dc1da98523ce13547ace36963fa5a22b5c36e`  
		Last Modified: Thu, 02 Mar 2023 03:05:30 GMT  
		Size: 126.5 MB (126472612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:7fc7bd657d410c79ad36371a138baff3371bf49bcf980a5ab5cefa6f361d62aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:f8344d55f5aec48ae36de1d2bcc916f336e3588f4828acf58b82d46da8d79836
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158983841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa43273b3fdb28466b0ea2fcd0ea5403600ac78b0bf4ed6a7b837c0fd9301ac0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:52:57 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 18:53:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:53:08 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 18:54:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 18:54:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50d379550397205b8ddddb58a89653deca5ebaf37b5564da526dff208f1655e`  
		Last Modified: Tue, 31 Jan 2023 18:56:44 GMT  
		Size: 2.9 MB (2949581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7556f23e7ad4703b5bb5a5d97170999166c94d46ad5b493cecab2368f292ee`  
		Last Modified: Tue, 31 Jan 2023 18:56:53 GMT  
		Size: 129.3 MB (129322666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; 386

```console
$ docker pull ibmjava@sha256:8f8aef15e68b1cd9faf076f1f1685b61ef1bdd046d12cd89c353ad0496b2dc5c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147606447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acd7545ae7d84b1d7309a97d47dd319d1ff6a0b5b0b0d49081228dbcefd71cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:01 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:03 GMT
ADD file:b9b814a7d1e7611a2c531fac3419a48c733c622470d3f275ce29f9ba8764eaeb in / 
# Thu, 26 Jan 2023 10:03:04 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:43:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 17:43:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:43:20 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 17:44:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 17:44:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a1177ecacc42e51782037ed649a91241b82866cc72c6eb0f205cbcc350f44d43`  
		Last Modified: Tue, 31 Jan 2023 17:42:04 GMT  
		Size: 27.2 MB (27165349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bd4ed927791f68d34f96a84af2a713efcb2234c018146289b0a0fafb33eef2`  
		Last Modified: Tue, 31 Jan 2023 17:47:42 GMT  
		Size: 3.0 MB (2981539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a696e32069dd164ed13db4e11cb34f76ed3a52c02b60893b413cfdd53c0110`  
		Last Modified: Tue, 31 Jan 2023 17:47:49 GMT  
		Size: 117.5 MB (117459559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:accb3f91bf07505b05addb38cb91288811728973036119c3e0bf0f37854c0adf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162514738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32408a15087e13c59eaca5c5bb18b84fd2f97ee8c383a624af8c2dde3ef9e5bc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:43:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 18:44:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:44:01 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 18:46:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 18:46:20 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:15579125cdf95166fecb7637769c3c9eb2551401759fb21f44848947ead59cbd`  
		Last Modified: Tue, 31 Jan 2023 18:13:22 GMT  
		Size: 30.4 MB (30442586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3845debd31d52c26de72c4219e4ec0bd27d14c2986651d541a2135cadc9b48`  
		Last Modified: Tue, 31 Jan 2023 18:51:43 GMT  
		Size: 3.1 MB (3075781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e886f1423f03ec32342fc5b0ad9cff55a07614765fba8be473be7f1b30c0207b`  
		Last Modified: Tue, 31 Jan 2023 18:52:00 GMT  
		Size: 129.0 MB (128996371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:ceab38e1c632c83c0664d16ed5288764d28457f46df1b24de1824147409dec0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154513094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb1b58a416fc4340f49e5028cc0dab0d8bcc85981a32978aef3f8d3cbdc502d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:18:09 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:11 GMT
ADD file:49b5368b8703fe0aa128fe923b83da7ab2a30a7a1c0395682c905b9271e7f503 in / 
# Wed, 01 Mar 2023 03:18:11 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:01:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 02 Mar 2023 03:01:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 03:02:00 GMT
ENV JAVA_VERSION=8.0.7.20
# Thu, 02 Mar 2023 03:02:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 02 Mar 2023 03:02:51 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:306d1b363f89f239f5dc6314e0033094c067617b584ce004fd8db99402dab321`  
		Last Modified: Thu, 02 Mar 2023 02:21:31 GMT  
		Size: 25.4 MB (25371412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fe795fb99ed72a95436de37d2cdb8fbd2edb3445e421c880c502757fb41be9`  
		Last Modified: Thu, 02 Mar 2023 03:05:21 GMT  
		Size: 2.7 MB (2669070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71635f0577860033cfd705acd9dc1da98523ce13547ace36963fa5a22b5c36e`  
		Last Modified: Thu, 02 Mar 2023 03:05:30 GMT  
		Size: 126.5 MB (126472612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:82ec4866b6dc3c50be0ebef2ad1c6453e5f35811bce55238a788175205480ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:44af894e772f04cb85805965e7be1600043074f63e2b3468a3b20f8627b55c07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196135763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c670bca5116f34b0ac4e80aa08a40d3d5bc99e62efdeca6ca9fc0d7bd8f5bfbc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:52:57 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 18:53:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:53:08 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 18:56:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f6aef4c3550a8f85288da8bc6fada405b0ce2226d6b1b57d0aae98cd5eef5e4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fa7661c2eb2982c4fb85c6894e7a975970b27b6ee82d5facb352f075cc1dfca3';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a56803671fe7d1c85f18d566dbcb7fbaf1d60c6f1d6de34e35a257e0c8095f9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='71c913a1eed7daae952657e18eb9a2e71723106b6e7b56373f18564db77f551e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c8641bc22443ebccaedf1822a12ec1303d89577d45c875702e1f628066c7f383';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 18:56:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50d379550397205b8ddddb58a89653deca5ebaf37b5564da526dff208f1655e`  
		Last Modified: Tue, 31 Jan 2023 18:56:44 GMT  
		Size: 2.9 MB (2949581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afae7776152d7a72cfee5aa067a79adad7581e1b24351fecf5c7ad000dc58420`  
		Last Modified: Tue, 31 Jan 2023 18:57:30 GMT  
		Size: 166.5 MB (166474588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:e7937c6f989c3344a9d1e0c5f9fedc905d9f5c0f55ae1f5859e94bc1c0939f64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184641524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601eaa609e2faa044927d641ac898d86799eddd82379e89728369ef6b8f6c14a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:01 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:03 GMT
ADD file:b9b814a7d1e7611a2c531fac3419a48c733c622470d3f275ce29f9ba8764eaeb in / 
# Thu, 26 Jan 2023 10:03:04 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:43:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 17:43:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:43:20 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 17:47:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f6aef4c3550a8f85288da8bc6fada405b0ce2226d6b1b57d0aae98cd5eef5e4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fa7661c2eb2982c4fb85c6894e7a975970b27b6ee82d5facb352f075cc1dfca3';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a56803671fe7d1c85f18d566dbcb7fbaf1d60c6f1d6de34e35a257e0c8095f9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='71c913a1eed7daae952657e18eb9a2e71723106b6e7b56373f18564db77f551e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c8641bc22443ebccaedf1822a12ec1303d89577d45c875702e1f628066c7f383';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 17:47:05 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a1177ecacc42e51782037ed649a91241b82866cc72c6eb0f205cbcc350f44d43`  
		Last Modified: Tue, 31 Jan 2023 17:42:04 GMT  
		Size: 27.2 MB (27165349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bd4ed927791f68d34f96a84af2a713efcb2234c018146289b0a0fafb33eef2`  
		Last Modified: Tue, 31 Jan 2023 17:47:42 GMT  
		Size: 3.0 MB (2981539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c37f7c0b2f224cfbbe89118e9dd236eecff6987c8848732440d0dc1fdbb4f7`  
		Last Modified: Tue, 31 Jan 2023 17:48:41 GMT  
		Size: 154.5 MB (154494636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:e460da507ff6de67707ec64a8b9483e921647f96e4d4935937e8f048a31a2a5e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.8 MB (199790621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6fc7d184e515abaaf3086c0ee8c7060dd09fd9f6694f950cb9424e010ac155`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:43:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 18:44:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:44:01 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 18:51:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f6aef4c3550a8f85288da8bc6fada405b0ce2226d6b1b57d0aae98cd5eef5e4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fa7661c2eb2982c4fb85c6894e7a975970b27b6ee82d5facb352f075cc1dfca3';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a56803671fe7d1c85f18d566dbcb7fbaf1d60c6f1d6de34e35a257e0c8095f9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='71c913a1eed7daae952657e18eb9a2e71723106b6e7b56373f18564db77f551e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c8641bc22443ebccaedf1822a12ec1303d89577d45c875702e1f628066c7f383';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 18:51:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:15579125cdf95166fecb7637769c3c9eb2551401759fb21f44848947ead59cbd`  
		Last Modified: Tue, 31 Jan 2023 18:13:22 GMT  
		Size: 30.4 MB (30442586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3845debd31d52c26de72c4219e4ec0bd27d14c2986651d541a2135cadc9b48`  
		Last Modified: Tue, 31 Jan 2023 18:51:43 GMT  
		Size: 3.1 MB (3075781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92791528b56fea6c9ba84bbd42299552177b57a1cbb9ab73c0e995fdb505ec0d`  
		Last Modified: Tue, 31 Jan 2023 18:53:01 GMT  
		Size: 166.3 MB (166272254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:90e85adeb1522f5cbcc2f9319494532d95f8f9c5935942b20e8d88314338d0de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184804744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b79d2fe5ac5614d0be3f633b9a34b90bf148e5e323fd32401f7d771639622fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:18:09 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:11 GMT
ADD file:49b5368b8703fe0aa128fe923b83da7ab2a30a7a1c0395682c905b9271e7f503 in / 
# Wed, 01 Mar 2023 03:18:11 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:01:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 02 Mar 2023 03:01:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 03:02:00 GMT
ENV JAVA_VERSION=8.0.7.20
# Thu, 02 Mar 2023 03:04:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f6aef4c3550a8f85288da8bc6fada405b0ce2226d6b1b57d0aae98cd5eef5e4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fa7661c2eb2982c4fb85c6894e7a975970b27b6ee82d5facb352f075cc1dfca3';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a56803671fe7d1c85f18d566dbcb7fbaf1d60c6f1d6de34e35a257e0c8095f9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='71c913a1eed7daae952657e18eb9a2e71723106b6e7b56373f18564db77f551e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c8641bc22443ebccaedf1822a12ec1303d89577d45c875702e1f628066c7f383';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 02 Mar 2023 03:04:44 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:306d1b363f89f239f5dc6314e0033094c067617b584ce004fd8db99402dab321`  
		Last Modified: Thu, 02 Mar 2023 02:21:31 GMT  
		Size: 25.4 MB (25371412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fe795fb99ed72a95436de37d2cdb8fbd2edb3445e421c880c502757fb41be9`  
		Last Modified: Thu, 02 Mar 2023 03:05:21 GMT  
		Size: 2.7 MB (2669070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1faca277882f5361876339ebbf10a447709eb207e81aea404f21a9db495ec02`  
		Last Modified: Thu, 02 Mar 2023 03:06:04 GMT  
		Size: 156.8 MB (156764262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:74f4b8df67ffdd6c32f02ef43f24a7da9195045c54c70cec99d9e475b9f4ed09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:fbe7060a4d03eafb2c32eb72ca41732b2dc8ef3fb03b5d261044e0896ddf3082
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94670044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ddef974fd13f93141315158feed5667da41a1da4041c59786b10b365bb93ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:52:57 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 18:53:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:53:08 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 18:55:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb548976980c436b15e59e0db7b4e99a7ed273df39e17db60047f950c2863c1b';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='768e6f8df5c9735d703f2dd5352b7c063949d59c6e15bc7d5c31d7ac667a241a';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='1ce92e9c420b2d081c8cd63c8441b324e49348360490d61e08a0908b830748cb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e790dc7707417153227e1f3164db1c699e3b6b9f697d9e1c9c9142bc0e3d3409';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='bfac3d6409a7996301d948faedfd4c19920dbb667ba699b7fd4719188366be8b';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 18:55:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50d379550397205b8ddddb58a89653deca5ebaf37b5564da526dff208f1655e`  
		Last Modified: Tue, 31 Jan 2023 18:56:44 GMT  
		Size: 2.9 MB (2949581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1af266f77a5a0ab6e80eb971f0a758b4350891d1fc5ad09a78496cb74f02d49`  
		Last Modified: Tue, 31 Jan 2023 18:57:10 GMT  
		Size: 65.0 MB (65008869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:3dab6da2741ea09deba4e68c25d9a9a41024a4ebe1e333cc1e08b66de56016c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94531997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804c381aceb007e4288f567f1dd8bdec54e90b546538bdb6156d504a7b58fb97`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:01 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:03 GMT
ADD file:b9b814a7d1e7611a2c531fac3419a48c733c622470d3f275ce29f9ba8764eaeb in / 
# Thu, 26 Jan 2023 10:03:04 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:43:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 17:43:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:43:20 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 17:45:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb548976980c436b15e59e0db7b4e99a7ed273df39e17db60047f950c2863c1b';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='768e6f8df5c9735d703f2dd5352b7c063949d59c6e15bc7d5c31d7ac667a241a';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='1ce92e9c420b2d081c8cd63c8441b324e49348360490d61e08a0908b830748cb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e790dc7707417153227e1f3164db1c699e3b6b9f697d9e1c9c9142bc0e3d3409';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='bfac3d6409a7996301d948faedfd4c19920dbb667ba699b7fd4719188366be8b';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 17:45:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a1177ecacc42e51782037ed649a91241b82866cc72c6eb0f205cbcc350f44d43`  
		Last Modified: Tue, 31 Jan 2023 17:42:04 GMT  
		Size: 27.2 MB (27165349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bd4ed927791f68d34f96a84af2a713efcb2234c018146289b0a0fafb33eef2`  
		Last Modified: Tue, 31 Jan 2023 17:47:42 GMT  
		Size: 3.0 MB (2981539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100b15b020f7dc00e89148d01048def6f7296b195f6bb40a22e26f903b8c8d95`  
		Last Modified: Tue, 31 Jan 2023 17:48:11 GMT  
		Size: 64.4 MB (64385109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:57ac8c15cacf297d8deadb240db2fe8bcd6cfd1098d3928fe9b2d84826e7662a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98808081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b2dc1040f0002f52eb000d20384b9cd286e52610c01f8c708557f0cfb3c3a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:43:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 18:44:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:44:01 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 18:48:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb548976980c436b15e59e0db7b4e99a7ed273df39e17db60047f950c2863c1b';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='768e6f8df5c9735d703f2dd5352b7c063949d59c6e15bc7d5c31d7ac667a241a';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='1ce92e9c420b2d081c8cd63c8441b324e49348360490d61e08a0908b830748cb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e790dc7707417153227e1f3164db1c699e3b6b9f697d9e1c9c9142bc0e3d3409';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='bfac3d6409a7996301d948faedfd4c19920dbb667ba699b7fd4719188366be8b';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 18:48:05 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:15579125cdf95166fecb7637769c3c9eb2551401759fb21f44848947ead59cbd`  
		Last Modified: Tue, 31 Jan 2023 18:13:22 GMT  
		Size: 30.4 MB (30442586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3845debd31d52c26de72c4219e4ec0bd27d14c2986651d541a2135cadc9b48`  
		Last Modified: Tue, 31 Jan 2023 18:51:43 GMT  
		Size: 3.1 MB (3075781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0df1bcfd49130e5ce956143668e834f79a4b5251d6299aaa1bad8433729a4b`  
		Last Modified: Tue, 31 Jan 2023 18:52:30 GMT  
		Size: 65.3 MB (65289714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:f7d0e2c77007bc0673c6b98ebcc2416773bf4949b5db48d2adb15d4de16da86b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94163617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b466f1fe7c37894f07123127150ceee65a03d6f2d2a658976d2bd48b8f0c690`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:18:09 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:11 GMT
ADD file:49b5368b8703fe0aa128fe923b83da7ab2a30a7a1c0395682c905b9271e7f503 in / 
# Wed, 01 Mar 2023 03:18:11 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:01:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 02 Mar 2023 03:01:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 03:02:00 GMT
ENV JAVA_VERSION=8.0.7.20
# Thu, 02 Mar 2023 03:03:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb548976980c436b15e59e0db7b4e99a7ed273df39e17db60047f950c2863c1b';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='768e6f8df5c9735d703f2dd5352b7c063949d59c6e15bc7d5c31d7ac667a241a';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='1ce92e9c420b2d081c8cd63c8441b324e49348360490d61e08a0908b830748cb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e790dc7707417153227e1f3164db1c699e3b6b9f697d9e1c9c9142bc0e3d3409';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='bfac3d6409a7996301d948faedfd4c19920dbb667ba699b7fd4719188366be8b';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 02 Mar 2023 03:03:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:306d1b363f89f239f5dc6314e0033094c067617b584ce004fd8db99402dab321`  
		Last Modified: Thu, 02 Mar 2023 02:21:31 GMT  
		Size: 25.4 MB (25371412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fe795fb99ed72a95436de37d2cdb8fbd2edb3445e421c880c502757fb41be9`  
		Last Modified: Thu, 02 Mar 2023 03:05:21 GMT  
		Size: 2.7 MB (2669070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff637b5ce43a2ff1c562d9e5cf98e491a6facbc722aaf3f68d7821b234976e2e`  
		Last Modified: Thu, 02 Mar 2023 03:05:46 GMT  
		Size: 66.1 MB (66123135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:7fc7bd657d410c79ad36371a138baff3371bf49bcf980a5ab5cefa6f361d62aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:f8344d55f5aec48ae36de1d2bcc916f336e3588f4828acf58b82d46da8d79836
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158983841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa43273b3fdb28466b0ea2fcd0ea5403600ac78b0bf4ed6a7b837c0fd9301ac0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:52:57 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 18:53:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:53:08 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 18:54:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 18:54:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50d379550397205b8ddddb58a89653deca5ebaf37b5564da526dff208f1655e`  
		Last Modified: Tue, 31 Jan 2023 18:56:44 GMT  
		Size: 2.9 MB (2949581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7556f23e7ad4703b5bb5a5d97170999166c94d46ad5b493cecab2368f292ee`  
		Last Modified: Tue, 31 Jan 2023 18:56:53 GMT  
		Size: 129.3 MB (129322666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; 386

```console
$ docker pull ibmjava@sha256:8f8aef15e68b1cd9faf076f1f1685b61ef1bdd046d12cd89c353ad0496b2dc5c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147606447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acd7545ae7d84b1d7309a97d47dd319d1ff6a0b5b0b0d49081228dbcefd71cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:01 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:03 GMT
ADD file:b9b814a7d1e7611a2c531fac3419a48c733c622470d3f275ce29f9ba8764eaeb in / 
# Thu, 26 Jan 2023 10:03:04 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:43:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 17:43:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:43:20 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 17:44:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 17:44:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a1177ecacc42e51782037ed649a91241b82866cc72c6eb0f205cbcc350f44d43`  
		Last Modified: Tue, 31 Jan 2023 17:42:04 GMT  
		Size: 27.2 MB (27165349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bd4ed927791f68d34f96a84af2a713efcb2234c018146289b0a0fafb33eef2`  
		Last Modified: Tue, 31 Jan 2023 17:47:42 GMT  
		Size: 3.0 MB (2981539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a696e32069dd164ed13db4e11cb34f76ed3a52c02b60893b413cfdd53c0110`  
		Last Modified: Tue, 31 Jan 2023 17:47:49 GMT  
		Size: 117.5 MB (117459559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:accb3f91bf07505b05addb38cb91288811728973036119c3e0bf0f37854c0adf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162514738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32408a15087e13c59eaca5c5bb18b84fd2f97ee8c383a624af8c2dde3ef9e5bc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:43:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 18:44:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:44:01 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 18:46:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 18:46:20 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:15579125cdf95166fecb7637769c3c9eb2551401759fb21f44848947ead59cbd`  
		Last Modified: Tue, 31 Jan 2023 18:13:22 GMT  
		Size: 30.4 MB (30442586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3845debd31d52c26de72c4219e4ec0bd27d14c2986651d541a2135cadc9b48`  
		Last Modified: Tue, 31 Jan 2023 18:51:43 GMT  
		Size: 3.1 MB (3075781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e886f1423f03ec32342fc5b0ad9cff55a07614765fba8be473be7f1b30c0207b`  
		Last Modified: Tue, 31 Jan 2023 18:52:00 GMT  
		Size: 129.0 MB (128996371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:ceab38e1c632c83c0664d16ed5288764d28457f46df1b24de1824147409dec0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154513094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb1b58a416fc4340f49e5028cc0dab0d8bcc85981a32978aef3f8d3cbdc502d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:18:09 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:11 GMT
ADD file:49b5368b8703fe0aa128fe923b83da7ab2a30a7a1c0395682c905b9271e7f503 in / 
# Wed, 01 Mar 2023 03:18:11 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:01:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 02 Mar 2023 03:01:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 03:02:00 GMT
ENV JAVA_VERSION=8.0.7.20
# Thu, 02 Mar 2023 03:02:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 02 Mar 2023 03:02:51 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:306d1b363f89f239f5dc6314e0033094c067617b584ce004fd8db99402dab321`  
		Last Modified: Thu, 02 Mar 2023 02:21:31 GMT  
		Size: 25.4 MB (25371412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fe795fb99ed72a95436de37d2cdb8fbd2edb3445e421c880c502757fb41be9`  
		Last Modified: Thu, 02 Mar 2023 03:05:21 GMT  
		Size: 2.7 MB (2669070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71635f0577860033cfd705acd9dc1da98523ce13547ace36963fa5a22b5c36e`  
		Last Modified: Thu, 02 Mar 2023 03:05:30 GMT  
		Size: 126.5 MB (126472612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:7fc7bd657d410c79ad36371a138baff3371bf49bcf980a5ab5cefa6f361d62aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:latest` - linux; amd64

```console
$ docker pull ibmjava@sha256:f8344d55f5aec48ae36de1d2bcc916f336e3588f4828acf58b82d46da8d79836
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158983841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa43273b3fdb28466b0ea2fcd0ea5403600ac78b0bf4ed6a7b837c0fd9301ac0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:52:57 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 18:53:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:53:08 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 18:54:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 18:54:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50d379550397205b8ddddb58a89653deca5ebaf37b5564da526dff208f1655e`  
		Last Modified: Tue, 31 Jan 2023 18:56:44 GMT  
		Size: 2.9 MB (2949581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7556f23e7ad4703b5bb5a5d97170999166c94d46ad5b493cecab2368f292ee`  
		Last Modified: Tue, 31 Jan 2023 18:56:53 GMT  
		Size: 129.3 MB (129322666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; 386

```console
$ docker pull ibmjava@sha256:8f8aef15e68b1cd9faf076f1f1685b61ef1bdd046d12cd89c353ad0496b2dc5c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147606447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acd7545ae7d84b1d7309a97d47dd319d1ff6a0b5b0b0d49081228dbcefd71cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:01 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:03 GMT
ADD file:b9b814a7d1e7611a2c531fac3419a48c733c622470d3f275ce29f9ba8764eaeb in / 
# Thu, 26 Jan 2023 10:03:04 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:43:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 17:43:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:43:20 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 17:44:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 17:44:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a1177ecacc42e51782037ed649a91241b82866cc72c6eb0f205cbcc350f44d43`  
		Last Modified: Tue, 31 Jan 2023 17:42:04 GMT  
		Size: 27.2 MB (27165349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bd4ed927791f68d34f96a84af2a713efcb2234c018146289b0a0fafb33eef2`  
		Last Modified: Tue, 31 Jan 2023 17:47:42 GMT  
		Size: 3.0 MB (2981539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a696e32069dd164ed13db4e11cb34f76ed3a52c02b60893b413cfdd53c0110`  
		Last Modified: Tue, 31 Jan 2023 17:47:49 GMT  
		Size: 117.5 MB (117459559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:accb3f91bf07505b05addb38cb91288811728973036119c3e0bf0f37854c0adf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162514738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32408a15087e13c59eaca5c5bb18b84fd2f97ee8c383a624af8c2dde3ef9e5bc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:43:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 18:44:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:44:01 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 18:46:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 18:46:20 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:15579125cdf95166fecb7637769c3c9eb2551401759fb21f44848947ead59cbd`  
		Last Modified: Tue, 31 Jan 2023 18:13:22 GMT  
		Size: 30.4 MB (30442586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3845debd31d52c26de72c4219e4ec0bd27d14c2986651d541a2135cadc9b48`  
		Last Modified: Tue, 31 Jan 2023 18:51:43 GMT  
		Size: 3.1 MB (3075781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e886f1423f03ec32342fc5b0ad9cff55a07614765fba8be473be7f1b30c0207b`  
		Last Modified: Tue, 31 Jan 2023 18:52:00 GMT  
		Size: 129.0 MB (128996371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:ceab38e1c632c83c0664d16ed5288764d28457f46df1b24de1824147409dec0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154513094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb1b58a416fc4340f49e5028cc0dab0d8bcc85981a32978aef3f8d3cbdc502d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:18:09 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:11 GMT
ADD file:49b5368b8703fe0aa128fe923b83da7ab2a30a7a1c0395682c905b9271e7f503 in / 
# Wed, 01 Mar 2023 03:18:11 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:01:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 02 Mar 2023 03:01:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 03:02:00 GMT
ENV JAVA_VERSION=8.0.7.20
# Thu, 02 Mar 2023 03:02:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 02 Mar 2023 03:02:51 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:306d1b363f89f239f5dc6314e0033094c067617b584ce004fd8db99402dab321`  
		Last Modified: Thu, 02 Mar 2023 02:21:31 GMT  
		Size: 25.4 MB (25371412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fe795fb99ed72a95436de37d2cdb8fbd2edb3445e421c880c502757fb41be9`  
		Last Modified: Thu, 02 Mar 2023 03:05:21 GMT  
		Size: 2.7 MB (2669070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71635f0577860033cfd705acd9dc1da98523ce13547ace36963fa5a22b5c36e`  
		Last Modified: Thu, 02 Mar 2023 03:05:30 GMT  
		Size: 126.5 MB (126472612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:82ec4866b6dc3c50be0ebef2ad1c6453e5f35811bce55238a788175205480ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:44af894e772f04cb85805965e7be1600043074f63e2b3468a3b20f8627b55c07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196135763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c670bca5116f34b0ac4e80aa08a40d3d5bc99e62efdeca6ca9fc0d7bd8f5bfbc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:52:57 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 18:53:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:53:08 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 18:56:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f6aef4c3550a8f85288da8bc6fada405b0ce2226d6b1b57d0aae98cd5eef5e4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fa7661c2eb2982c4fb85c6894e7a975970b27b6ee82d5facb352f075cc1dfca3';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a56803671fe7d1c85f18d566dbcb7fbaf1d60c6f1d6de34e35a257e0c8095f9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='71c913a1eed7daae952657e18eb9a2e71723106b6e7b56373f18564db77f551e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c8641bc22443ebccaedf1822a12ec1303d89577d45c875702e1f628066c7f383';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 18:56:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50d379550397205b8ddddb58a89653deca5ebaf37b5564da526dff208f1655e`  
		Last Modified: Tue, 31 Jan 2023 18:56:44 GMT  
		Size: 2.9 MB (2949581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afae7776152d7a72cfee5aa067a79adad7581e1b24351fecf5c7ad000dc58420`  
		Last Modified: Tue, 31 Jan 2023 18:57:30 GMT  
		Size: 166.5 MB (166474588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:e7937c6f989c3344a9d1e0c5f9fedc905d9f5c0f55ae1f5859e94bc1c0939f64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184641524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601eaa609e2faa044927d641ac898d86799eddd82379e89728369ef6b8f6c14a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:01 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:03 GMT
ADD file:b9b814a7d1e7611a2c531fac3419a48c733c622470d3f275ce29f9ba8764eaeb in / 
# Thu, 26 Jan 2023 10:03:04 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:43:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 17:43:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:43:20 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 17:47:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f6aef4c3550a8f85288da8bc6fada405b0ce2226d6b1b57d0aae98cd5eef5e4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fa7661c2eb2982c4fb85c6894e7a975970b27b6ee82d5facb352f075cc1dfca3';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a56803671fe7d1c85f18d566dbcb7fbaf1d60c6f1d6de34e35a257e0c8095f9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='71c913a1eed7daae952657e18eb9a2e71723106b6e7b56373f18564db77f551e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c8641bc22443ebccaedf1822a12ec1303d89577d45c875702e1f628066c7f383';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 17:47:05 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a1177ecacc42e51782037ed649a91241b82866cc72c6eb0f205cbcc350f44d43`  
		Last Modified: Tue, 31 Jan 2023 17:42:04 GMT  
		Size: 27.2 MB (27165349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bd4ed927791f68d34f96a84af2a713efcb2234c018146289b0a0fafb33eef2`  
		Last Modified: Tue, 31 Jan 2023 17:47:42 GMT  
		Size: 3.0 MB (2981539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c37f7c0b2f224cfbbe89118e9dd236eecff6987c8848732440d0dc1fdbb4f7`  
		Last Modified: Tue, 31 Jan 2023 17:48:41 GMT  
		Size: 154.5 MB (154494636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:e460da507ff6de67707ec64a8b9483e921647f96e4d4935937e8f048a31a2a5e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.8 MB (199790621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6fc7d184e515abaaf3086c0ee8c7060dd09fd9f6694f950cb9424e010ac155`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:43:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 18:44:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:44:01 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 18:51:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f6aef4c3550a8f85288da8bc6fada405b0ce2226d6b1b57d0aae98cd5eef5e4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fa7661c2eb2982c4fb85c6894e7a975970b27b6ee82d5facb352f075cc1dfca3';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a56803671fe7d1c85f18d566dbcb7fbaf1d60c6f1d6de34e35a257e0c8095f9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='71c913a1eed7daae952657e18eb9a2e71723106b6e7b56373f18564db77f551e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c8641bc22443ebccaedf1822a12ec1303d89577d45c875702e1f628066c7f383';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 18:51:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:15579125cdf95166fecb7637769c3c9eb2551401759fb21f44848947ead59cbd`  
		Last Modified: Tue, 31 Jan 2023 18:13:22 GMT  
		Size: 30.4 MB (30442586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3845debd31d52c26de72c4219e4ec0bd27d14c2986651d541a2135cadc9b48`  
		Last Modified: Tue, 31 Jan 2023 18:51:43 GMT  
		Size: 3.1 MB (3075781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92791528b56fea6c9ba84bbd42299552177b57a1cbb9ab73c0e995fdb505ec0d`  
		Last Modified: Tue, 31 Jan 2023 18:53:01 GMT  
		Size: 166.3 MB (166272254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:90e85adeb1522f5cbcc2f9319494532d95f8f9c5935942b20e8d88314338d0de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184804744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b79d2fe5ac5614d0be3f633b9a34b90bf148e5e323fd32401f7d771639622fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:18:09 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:11 GMT
ADD file:49b5368b8703fe0aa128fe923b83da7ab2a30a7a1c0395682c905b9271e7f503 in / 
# Wed, 01 Mar 2023 03:18:11 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:01:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 02 Mar 2023 03:01:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 03:02:00 GMT
ENV JAVA_VERSION=8.0.7.20
# Thu, 02 Mar 2023 03:04:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f6aef4c3550a8f85288da8bc6fada405b0ce2226d6b1b57d0aae98cd5eef5e4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fa7661c2eb2982c4fb85c6894e7a975970b27b6ee82d5facb352f075cc1dfca3';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a56803671fe7d1c85f18d566dbcb7fbaf1d60c6f1d6de34e35a257e0c8095f9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='71c913a1eed7daae952657e18eb9a2e71723106b6e7b56373f18564db77f551e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c8641bc22443ebccaedf1822a12ec1303d89577d45c875702e1f628066c7f383';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 02 Mar 2023 03:04:44 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:306d1b363f89f239f5dc6314e0033094c067617b584ce004fd8db99402dab321`  
		Last Modified: Thu, 02 Mar 2023 02:21:31 GMT  
		Size: 25.4 MB (25371412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fe795fb99ed72a95436de37d2cdb8fbd2edb3445e421c880c502757fb41be9`  
		Last Modified: Thu, 02 Mar 2023 03:05:21 GMT  
		Size: 2.7 MB (2669070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1faca277882f5361876339ebbf10a447709eb207e81aea404f21a9db495ec02`  
		Last Modified: Thu, 02 Mar 2023 03:06:04 GMT  
		Size: 156.8 MB (156764262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:74f4b8df67ffdd6c32f02ef43f24a7da9195045c54c70cec99d9e475b9f4ed09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:fbe7060a4d03eafb2c32eb72ca41732b2dc8ef3fb03b5d261044e0896ddf3082
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94670044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ddef974fd13f93141315158feed5667da41a1da4041c59786b10b365bb93ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:52:57 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 18:53:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:53:08 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 18:55:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb548976980c436b15e59e0db7b4e99a7ed273df39e17db60047f950c2863c1b';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='768e6f8df5c9735d703f2dd5352b7c063949d59c6e15bc7d5c31d7ac667a241a';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='1ce92e9c420b2d081c8cd63c8441b324e49348360490d61e08a0908b830748cb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e790dc7707417153227e1f3164db1c699e3b6b9f697d9e1c9c9142bc0e3d3409';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='bfac3d6409a7996301d948faedfd4c19920dbb667ba699b7fd4719188366be8b';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 18:55:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50d379550397205b8ddddb58a89653deca5ebaf37b5564da526dff208f1655e`  
		Last Modified: Tue, 31 Jan 2023 18:56:44 GMT  
		Size: 2.9 MB (2949581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1af266f77a5a0ab6e80eb971f0a758b4350891d1fc5ad09a78496cb74f02d49`  
		Last Modified: Tue, 31 Jan 2023 18:57:10 GMT  
		Size: 65.0 MB (65008869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:3dab6da2741ea09deba4e68c25d9a9a41024a4ebe1e333cc1e08b66de56016c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94531997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804c381aceb007e4288f567f1dd8bdec54e90b546538bdb6156d504a7b58fb97`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:01 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:03 GMT
ADD file:b9b814a7d1e7611a2c531fac3419a48c733c622470d3f275ce29f9ba8764eaeb in / 
# Thu, 26 Jan 2023 10:03:04 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:43:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 17:43:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:43:20 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 17:45:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb548976980c436b15e59e0db7b4e99a7ed273df39e17db60047f950c2863c1b';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='768e6f8df5c9735d703f2dd5352b7c063949d59c6e15bc7d5c31d7ac667a241a';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='1ce92e9c420b2d081c8cd63c8441b324e49348360490d61e08a0908b830748cb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e790dc7707417153227e1f3164db1c699e3b6b9f697d9e1c9c9142bc0e3d3409';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='bfac3d6409a7996301d948faedfd4c19920dbb667ba699b7fd4719188366be8b';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 17:45:04 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a1177ecacc42e51782037ed649a91241b82866cc72c6eb0f205cbcc350f44d43`  
		Last Modified: Tue, 31 Jan 2023 17:42:04 GMT  
		Size: 27.2 MB (27165349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bd4ed927791f68d34f96a84af2a713efcb2234c018146289b0a0fafb33eef2`  
		Last Modified: Tue, 31 Jan 2023 17:47:42 GMT  
		Size: 3.0 MB (2981539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100b15b020f7dc00e89148d01048def6f7296b195f6bb40a22e26f903b8c8d95`  
		Last Modified: Tue, 31 Jan 2023 17:48:11 GMT  
		Size: 64.4 MB (64385109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:57ac8c15cacf297d8deadb240db2fe8bcd6cfd1098d3928fe9b2d84826e7662a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98808081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b2dc1040f0002f52eb000d20384b9cd286e52610c01f8c708557f0cfb3c3a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:43:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 31 Jan 2023 18:44:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:44:01 GMT
ENV JAVA_VERSION=8.0.7.20
# Tue, 31 Jan 2023 18:48:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb548976980c436b15e59e0db7b4e99a7ed273df39e17db60047f950c2863c1b';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='768e6f8df5c9735d703f2dd5352b7c063949d59c6e15bc7d5c31d7ac667a241a';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='1ce92e9c420b2d081c8cd63c8441b324e49348360490d61e08a0908b830748cb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e790dc7707417153227e1f3164db1c699e3b6b9f697d9e1c9c9142bc0e3d3409';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='bfac3d6409a7996301d948faedfd4c19920dbb667ba699b7fd4719188366be8b';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 31 Jan 2023 18:48:05 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:15579125cdf95166fecb7637769c3c9eb2551401759fb21f44848947ead59cbd`  
		Last Modified: Tue, 31 Jan 2023 18:13:22 GMT  
		Size: 30.4 MB (30442586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3845debd31d52c26de72c4219e4ec0bd27d14c2986651d541a2135cadc9b48`  
		Last Modified: Tue, 31 Jan 2023 18:51:43 GMT  
		Size: 3.1 MB (3075781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0df1bcfd49130e5ce956143668e834f79a4b5251d6299aaa1bad8433729a4b`  
		Last Modified: Tue, 31 Jan 2023 18:52:30 GMT  
		Size: 65.3 MB (65289714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:f7d0e2c77007bc0673c6b98ebcc2416773bf4949b5db48d2adb15d4de16da86b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94163617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b466f1fe7c37894f07123127150ceee65a03d6f2d2a658976d2bd48b8f0c690`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Mar 2023 03:18:09 GMT
ARG RELEASE
# Wed, 01 Mar 2023 03:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 03:18:09 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 01 Mar 2023 03:18:11 GMT
ADD file:49b5368b8703fe0aa128fe923b83da7ab2a30a7a1c0395682c905b9271e7f503 in / 
# Wed, 01 Mar 2023 03:18:11 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:01:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 02 Mar 2023 03:01:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 03:02:00 GMT
ENV JAVA_VERSION=8.0.7.20
# Thu, 02 Mar 2023 03:03:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb548976980c436b15e59e0db7b4e99a7ed273df39e17db60047f950c2863c1b';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='768e6f8df5c9735d703f2dd5352b7c063949d59c6e15bc7d5c31d7ac667a241a';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='1ce92e9c420b2d081c8cd63c8441b324e49348360490d61e08a0908b830748cb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e790dc7707417153227e1f3164db1c699e3b6b9f697d9e1c9c9142bc0e3d3409';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='bfac3d6409a7996301d948faedfd4c19920dbb667ba699b7fd4719188366be8b';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 02 Mar 2023 03:03:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:306d1b363f89f239f5dc6314e0033094c067617b584ce004fd8db99402dab321`  
		Last Modified: Thu, 02 Mar 2023 02:21:31 GMT  
		Size: 25.4 MB (25371412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fe795fb99ed72a95436de37d2cdb8fbd2edb3445e421c880c502757fb41be9`  
		Last Modified: Thu, 02 Mar 2023 03:05:21 GMT  
		Size: 2.7 MB (2669070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff637b5ce43a2ff1c562d9e5cf98e491a6facbc722aaf3f68d7821b234976e2e`  
		Last Modified: Thu, 02 Mar 2023 03:05:46 GMT  
		Size: 66.1 MB (66123135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
