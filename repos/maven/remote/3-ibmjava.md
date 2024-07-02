## `maven:3-ibmjava`

```console
$ docker pull maven@sha256:6dbe7f44218e30510e8eabb60a7b1070b7d6ddb4219286064cc9e37a0d2b99ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `maven:3-ibmjava` - linux; amd64

```console
$ docker pull maven@sha256:0e89fa187273ec6a32d7ebc1fa71e66e7364bed3cbdbe54f8d78e84ff11a92ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213913527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bcc3e5c44541119a8ee3e8d8050fc65a019031ee571a6eacaadcbb4f4c127b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
ARG RELEASE
# Thu, 27 Jun 2024 09:17:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_VERSION=8.0.8.26
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='72902f658ff14a4fade3aa5dea3f74c5ed92bd58e01a0ded5701bea56c3894f0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3a5a3d2f6dbbebceab07aef6ee0cb9111703bc8fd4e63ec78030440e2faf97a';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='377f4824ebd4df1e62ffa78b1ab7141338e89f3f4a742222d2a1636cc8d9b6d9';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a8638ff059e7420d70b0e7b2368aea4b387cc28a242c56bd8005ee99d4e3fc51';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b7314d6b7e39503736d64744c95bb7467e6ebc8d9db88102350cc0a3d3203b`  
		Last Modified: Tue, 02 Jul 2024 03:03:46 GMT  
		Size: 1.4 MB (1438198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc12a4a066686684a17d23642ac15591656eb5dcf84e0b48ec2c8e313f4a6f4`  
		Last Modified: Tue, 02 Jul 2024 03:03:51 GMT  
		Size: 172.2 MB (172234494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62ab618ab38b2eaa7b0faf8d7faa0bbfcf8b816e782601aa0bbd2f3ee96bdae`  
		Last Modified: Tue, 02 Jul 2024 09:09:26 GMT  
		Size: 1.5 MB (1543926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c025d7b587e999544db545a418f53608131f1b4d18890426c8673d864bd3df`  
		Last Modified: Tue, 02 Jul 2024 09:09:26 GMT  
		Size: 9.2 MB (9161816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e73023529315a5d950c5bc6cb8d17ff1472053f9966bfb68b773ce99c107402`  
		Last Modified: Tue, 02 Jul 2024 09:09:26 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ad5b3779d9fcd74d3b422b74f3e8a43e990ccc3a0665bbb023decf3f7eb443`  
		Last Modified: Tue, 02 Jul 2024 09:09:26 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:d058a58cd96d432ff6b0ce0098e5aa1bcd5f52cbe14f3f1e8e06fb238c9d9e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2183546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525a75ccd9f3fc4eaaa57ea990c665848d4223c45b51a79e836da697f23ab482`

```dockerfile
```

-	Layers:
	-	`sha256:487dadf97229a1f4c3ce07659c743bf0dcd91281d51c65de5e4ecef42e535c81`  
		Last Modified: Tue, 02 Jul 2024 09:09:25 GMT  
		Size: 2.2 MB (2164808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b63e9f80d5368a2208ad9088ebd7b7fb688c7ee1af300db2ea5728d269c974`  
		Last Modified: Tue, 02 Jul 2024 09:09:25 GMT  
		Size: 18.7 KB (18738 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibmjava` - linux; ppc64le

```console
$ docker pull maven@sha256:42bd1573842ffb86836652d0a67094030666bb9af523e2220d823cb5115ed389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219899053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5ebdcb88823852acafb38339027e1d8e42b8cce5b85b87ccd57f0d28d84727`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 09 May 2024 05:12:02 GMT
ARG RELEASE
# Thu, 09 May 2024 05:12:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 09 May 2024 05:12:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 09 May 2024 05:12:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 09 May 2024 05:12:02 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Thu, 09 May 2024 05:12:02 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 05:12:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 09 May 2024 05:12:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_VERSION=8.0.8.25
# Thu, 09 May 2024 05:12:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='12d4145412244d3d10c1e59eb89122fe71ab73ff42333761231316cfe3156312';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5db8c679a3d9c8b26c8b1b013cfc76935fcc84d663c665adafe24680931d05ed';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='9d6afc539410670ae7715e87e6cd737bdb068731bfa389d9837495e0df6f3dd4';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a84557a63264fb26c288df55f9431169416800c4fe7078c5506a88b35d9c1f72';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6361c43922dd1b73a50a72a014784973eb6b06d1b73af66328a1fedcc021e480`  
		Last Modified: Tue, 25 Jun 2024 23:50:31 GMT  
		Size: 1.6 MB (1574413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2f2b2bb92517562cc54a7709a1649468050868172a075982c9539f0882cc5e`  
		Last Modified: Tue, 25 Jun 2024 23:52:29 GMT  
		Size: 172.8 MB (172805995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc8d40c84f241498b17667719196a5ecc4d02ac280ecc13ed52b92f0db877cf`  
		Last Modified: Thu, 27 Jun 2024 19:04:43 GMT  
		Size: 1.9 MB (1895126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d94fc0d5570c7c87fe80e6e072579fc7a029cc5b865f72eec4544d403c1a972`  
		Last Modified: Thu, 27 Jun 2024 19:04:44 GMT  
		Size: 9.2 MB (9161782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2114368adf889335c1972bdeb7f96cec2c7474178c616a7b8ba5dd6b7355992b`  
		Last Modified: Thu, 27 Jun 2024 19:04:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb375b4ca7b22f7ad80cafdc6800857923bd303fefa207d49242fdcc6943bea`  
		Last Modified: Thu, 27 Jun 2024 19:04:43 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:ae2ae948ed8049baad4e4987faa7fd5d8f9d1a08460abad62488e4aa44b76cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9302be7442d0a01ec5428649a61042c0bf6b53b0be957c07ab7bbf1f7e65ee60`

```dockerfile
```

-	Layers:
	-	`sha256:f484bdcfafe3a7335d6c3d9924bda5dfca61dddeb2b2e90b7fa2e25fd3d5a027`  
		Last Modified: Thu, 27 Jun 2024 19:04:43 GMT  
		Size: 2.2 MB (2167328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52467e6291bac259d525e2a8e1a8d7ae1e5c29e631245228f90bed91df214f1e`  
		Last Modified: Thu, 27 Jun 2024 19:04:43 GMT  
		Size: 18.8 KB (18842 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibmjava` - linux; s390x

```console
$ docker pull maven@sha256:71f14c70686ea74c89737422b00d4d54ef0ff0b766a896e4cda9002449d3a6e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202221537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ccbbbf3591189ef0c338d9f2d22f1169fa2b83d513c5ff3522a83b2a361178e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 09 May 2024 05:12:02 GMT
ARG RELEASE
# Thu, 09 May 2024 05:12:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 09 May 2024 05:12:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 09 May 2024 05:12:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 09 May 2024 05:12:02 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Thu, 09 May 2024 05:12:02 GMT
CMD ["/bin/bash"]
# Thu, 09 May 2024 05:12:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 09 May 2024 05:12:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_VERSION=8.0.8.25
# Thu, 09 May 2024 05:12:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='12d4145412244d3d10c1e59eb89122fe71ab73ff42333761231316cfe3156312';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='5db8c679a3d9c8b26c8b1b013cfc76935fcc84d663c665adafe24680931d05ed';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='9d6afc539410670ae7715e87e6cd737bdb068731bfa389d9837495e0df6f3dd4';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='a84557a63264fb26c288df55f9431169416800c4fe7078c5506a88b35d9c1f72';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 09 May 2024 05:12:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51938117bdde1396c0e2d8ef3c52c92b614260596f918f02273bccf82a7f3ff4`  
		Last Modified: Tue, 25 Jun 2024 23:29:58 GMT  
		Size: 1.5 MB (1477329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4682166c6f2936c53cc51970d9c062706c3618580e5db67faa6dee70be84f899`  
		Last Modified: Tue, 25 Jun 2024 23:31:34 GMT  
		Size: 162.0 MB (162041279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713ac2992535fc20e2f841209ac75264547b6c098e82cb836c908670035569ee`  
		Last Modified: Thu, 27 Jun 2024 19:01:59 GMT  
		Size: 1.5 MB (1539570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9249c65d9e2fdde5b7374ce0717c065acea8b39771020c37f66224218ba1e47a`  
		Last Modified: Thu, 27 Jun 2024 19:02:00 GMT  
		Size: 9.2 MB (9161803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002a5fd0212a3fafc3730cc6f74d0ab544b9baf4819b2bffe818c45e466eeb7c`  
		Last Modified: Thu, 27 Jun 2024 19:01:59 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe0427c5f351b04f1bbda8f10ff5abf0372626d469659ec82feaf3947408e9f`  
		Last Modified: Thu, 27 Jun 2024 19:01:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:bdd972add33499c2314470135510febc691fc61b35495f20f5ff6a73160a3d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b538a30fff9b8b9d83255f6d10a9d73a0730da9637cd04b97eff0667b911de9`

```dockerfile
```

-	Layers:
	-	`sha256:c89db6ea8514bed2ee846413e5c386cb7071a134c306c0aa0cf9be8c5ba8f7dd`  
		Last Modified: Thu, 27 Jun 2024 19:01:59 GMT  
		Size: 2.1 MB (2138519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e186670a06db58b7e2953826e264464dae909e047f7b933451bb444fcfe5e2df`  
		Last Modified: Thu, 27 Jun 2024 19:01:59 GMT  
		Size: 18.8 KB (18768 bytes)  
		MIME: application/vnd.in-toto+json
