## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:1749ad18d1dd21b3502bf844f46fb9a69bcb0b1180f07b8415b2ea41c34bf257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:e4902a53f615051e4d11974bd33491e1ade29cab282a6185fbfbd23885b87cd1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101763512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284ba6d230838f9cec2ca26c6b1f352551dabd76e56d746a0953589073eec36f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:24:44 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Feb 2024 07:24:50 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Feb 2024 01:41:42 GMT
ENV JAVA_VERSION=8.0.8.20
# Wed, 14 Feb 2024 01:42:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c8055351ef6f0e475c934a1aed1d8cb8aa5c493d58dccaa9b6e9b10b58d7865f';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a4d6bdb8dcf011f327b48012306348924e83ed4de5bc0ca4afc16ef94b48eb74';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6b6c31fcbbf22b579bb00203a2c643a444fe99f8b48b1b089249fd3ff16402ce';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='116dd00607ea28327b2b1b1fa77e341d9da693706f1ab93dfbfdb24c352063ec';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Wed, 14 Feb 2024 01:42:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722294e5505e295cdb03c53a0d2e94ce13dd4bceae93a4e917840b4435aae29d`  
		Last Modified: Fri, 02 Feb 2024 07:28:29 GMT  
		Size: 1.5 MB (1469133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bfb00f2a2a69c1518b44483e333c4394db3012ca3ed952ae34153bc68f8065`  
		Last Modified: Wed, 14 Feb 2024 01:43:02 GMT  
		Size: 69.8 MB (69846497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:da7f55c764680b8dc38939adcf3ed284687ee8adda0204465b50240a640858f2
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107582788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e55650411850b4dbce07d0ffbe36157c97705f459f9164f08d79ee7a66d8c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:59 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:02 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Thu, 25 Jan 2024 17:57:02 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:03:29 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Feb 2024 01:03:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Feb 2024 01:44:59 GMT
ENV JAVA_VERSION=8.0.8.20
# Wed, 14 Feb 2024 01:45:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c8055351ef6f0e475c934a1aed1d8cb8aa5c493d58dccaa9b6e9b10b58d7865f';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a4d6bdb8dcf011f327b48012306348924e83ed4de5bc0ca4afc16ef94b48eb74';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6b6c31fcbbf22b579bb00203a2c643a444fe99f8b48b1b089249fd3ff16402ce';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='116dd00607ea28327b2b1b1fa77e341d9da693706f1ab93dfbfdb24c352063ec';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Wed, 14 Feb 2024 01:45:28 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4cddbbaaed5c0bb0075d1b49c5185496b73a0103b0d818f916036e28a6cb5f81`  
		Last Modified: Fri, 02 Feb 2024 00:09:07 GMT  
		Size: 35.7 MB (35659183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd44d0ae6effa1825c8a8307599048102b451fb680e4a036406ce4fbb658c884`  
		Last Modified: Fri, 02 Feb 2024 01:07:57 GMT  
		Size: 1.6 MB (1574379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f9d09645e38ddc4949e06a3e61d598150767f3902706f51d7ac060d83a9e5d`  
		Last Modified: Wed, 14 Feb 2024 01:46:33 GMT  
		Size: 70.3 MB (70349226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:90d5cc6186454f91354453f1970484bf354a830c084802a8b85555263c4c78e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100708135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d98056a68bbfaecbd47c73de4ce94395de8ebd88955e60e5bf7dec4b4a57c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 18:07:14 GMT
ARG RELEASE
# Thu, 25 Jan 2024 18:07:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 18:07:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 18:07:16 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Thu, 25 Jan 2024 18:07:16 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:36:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 02 Feb 2024 00:36:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Feb 2024 02:02:37 GMT
ENV JAVA_VERSION=8.0.8.20
# Wed, 14 Feb 2024 02:04:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c8055351ef6f0e475c934a1aed1d8cb8aa5c493d58dccaa9b6e9b10b58d7865f';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a4d6bdb8dcf011f327b48012306348924e83ed4de5bc0ca4afc16ef94b48eb74';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6b6c31fcbbf22b579bb00203a2c643a444fe99f8b48b1b089249fd3ff16402ce';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='116dd00607ea28327b2b1b1fa77e341d9da693706f1ab93dfbfdb24c352063ec';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Wed, 14 Feb 2024 02:04:11 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4d63bfd51bdce6fd8dfe83946feba0ea66b3823f4955c098602769d1933dfb1a`  
		Last Modified: Fri, 02 Feb 2024 00:42:52 GMT  
		Size: 28.7 MB (28655632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9236abd83cca7b270bbe4fcd004aba112da73b433d97d63329e5980d47fb583`  
		Last Modified: Fri, 02 Feb 2024 00:42:49 GMT  
		Size: 1.5 MB (1477213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abafb710e83e7090f8cf26cb7023f533540c83c4a811e2d29ed3d961771b6fdc`  
		Last Modified: Wed, 14 Feb 2024 02:07:15 GMT  
		Size: 70.6 MB (70575290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
