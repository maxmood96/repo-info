## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:d033fea40b137742446688008a0bb168acb881077928dd4a7fab228366c60ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:a9d8734f5e13e73797d92fa0f3cc8f1030000065c5cf3ea372a4751a17a7a122
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166915282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c6fcc2a818e6af7de5e78e2e1de60b59e92bed05a2286b04b8ca500e7d67ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:25:37 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 02 May 2024 02:25:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 09 May 2024 16:25:46 GMT
ENV JAVA_VERSION=8.0.8.25
# Thu, 09 May 2024 16:25:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Thu, 09 May 2024 16:25:58 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f8db45b3d5d0ac0b6b07122767bc090d41c210ecb9b4b374ecae77c6a71bbd`  
		Last Modified: Thu, 02 May 2024 02:26:48 GMT  
		Size: 1.5 MB (1469725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a78ea0a20549516f864538c4071c42e658ee010dfa95606233855d8e7f5cba`  
		Last Modified: Thu, 09 May 2024 16:26:48 GMT  
		Size: 135.0 MB (135005908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:d7b4a0b278297a45eebf1a8db3494369c9513e06a9957df81f383a419b4275c4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172638795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d54a3023ed1d3e99fa5700922eaaf15931d7728472b7887faa24c87188f13a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:38:39 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 02 May 2024 01:38:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 09 May 2024 16:17:38 GMT
ENV JAVA_VERSION=8.0.8.25
# Thu, 09 May 2024 16:17:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Thu, 09 May 2024 16:17:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:ef1313ed517c6def5644ab70e25cc66f1c4cd52b1e81c07fb33bfb8850b39c25`  
		Last Modified: Thu, 02 May 2024 01:40:15 GMT  
		Size: 35.6 MB (35588524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d160f4318a88a056643db72fa03a8b4f47253fd4510ad83ce855372df5d000c4`  
		Last Modified: Thu, 02 May 2024 01:40:10 GMT  
		Size: 1.6 MB (1574876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d55a2b6671c4d9d73cd45efdd613e63a36b662a6db877d81758e62aafb86186`  
		Last Modified: Thu, 09 May 2024 16:18:59 GMT  
		Size: 135.5 MB (135475395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:2ca43d824a791ce0327a9030075b5fe15847fcc6e4f0a47e8356509aed740eff
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161873164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852144538b3c548f0137a11ce5d3ee2232ff0775664900ee87e5a490b2d4c6e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 03:16:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 05 Jun 2024 03:16:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 03:16:17 GMT
ENV JAVA_VERSION=8.0.8.25
# Wed, 05 Jun 2024 03:16:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='82be3936ccd4acbba83fdea2302770fa9a89266829fa2ff22c06b11e616281c0';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='7892771ebe4ee2988988031bf504b054c41fdc905fefc87c53d7bc499d7b44fa';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='55647d87f192db41e52e8cc5ea517266a0bded42e3c326cf2e8f03a64a473a96';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='dc1ffb2b769a6a08f161b801f7dfd413400d9cfcebed3c6e7229d48dd1a52bad';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz;
# Wed, 05 Jun 2024 03:16:27 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:0424de0056677a3a1d049300220cb3d875fb304aae1fa90f7b0292500716e5ed`  
		Last Modified: Wed, 05 Jun 2024 03:12:35 GMT  
		Size: 28.6 MB (28637399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea35c7b73745512a6fefe998e1f5b91f1ad4217979740be244176436058b2e4`  
		Last Modified: Wed, 05 Jun 2024 03:17:12 GMT  
		Size: 1.5 MB (1477651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7414515d2b33d95d026385dd8aaaa774f5819193a348f66d67440c2ec3ca151f`  
		Last Modified: Wed, 05 Jun 2024 03:17:20 GMT  
		Size: 131.8 MB (131758114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
