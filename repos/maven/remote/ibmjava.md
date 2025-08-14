## `maven:ibmjava`

```console
$ docker pull maven@sha256:05775f9772615b62e5a0ceba69b124ab97543058b5ffc6d919112758a365d568
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `maven:ibmjava` - linux; amd64

```console
$ docker pull maven@sha256:796200059a1d845728b1fe0e1249a090ebc21226e2fe702b7ed8db7c3f510682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.0 MB (216016330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9183e08388bb27eec5ff294a7614610622ae8c449edeed8d2fb87e4bc06f03f5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
ARG RELEASE
# Wed, 16 Jul 2025 06:51:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Jul 2025 06:51:38 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_VERSION=8.0.8.50
# Wed, 16 Jul 2025 06:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5bd4cc4749040ff2af6126adac1259dddc09d4c43dfc14779b1c6e83fb77c47a';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='58d2b8c23e815fa02019874109f78ad8ae01dee8f44e44ea0c69e29ececfd844';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='0c17796c0c75f71717b95843b93a93e27f1d91f23bc6e2d1d1005feb20fd7530';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0551be367fd50b97f502140b9d811f1c3923476f5c9d50f976225fcff67022`  
		Last Modified: Tue, 12 Aug 2025 18:09:15 GMT  
		Size: 1.5 MB (1450024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34774f59a374f39e2b8157f86129828379ae33cd60f4288943a4f58483a0129`  
		Last Modified: Tue, 12 Aug 2025 18:09:36 GMT  
		Size: 172.7 MB (172672539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5155575938590f21dd626f2438c263ee434059133488020a7d9eef5bd2ce2b7a`  
		Last Modified: Tue, 12 Aug 2025 19:44:02 GMT  
		Size: 3.1 MB (3113155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fb0299b828d59367d33d1e8ec678938e153a89dc475ec75a07bea73d7a76c8`  
		Last Modified: Tue, 12 Aug 2025 19:44:22 GMT  
		Size: 9.2 MB (9242583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94389a41f72a614f00a9e8b5402d9f900fb2dd90720bea8a9307ffb306dad13`  
		Last Modified: Tue, 12 Aug 2025 19:44:02 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a4a5f5036957ad70ca1bf86a11cdfa5927bbc591fdd3c19cf4411ffeab29d7`  
		Last Modified: Tue, 12 Aug 2025 19:44:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:9c7b0bb0f44980fe3867bc73793becd47a1f06026319483fbd0684f6465989bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3295096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1548fb74faea4767f2995f539e619e6958313233b8d637d3e95604e80fab92f`

```dockerfile
```

-	Layers:
	-	`sha256:a46cf9bdcc46ad4847bc45e2f53df71d5c12e2968bade79c641496c03fc1eaf5`  
		Last Modified: Tue, 12 Aug 2025 20:30:38 GMT  
		Size: 3.3 MB (3276276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bb058882aeae465e86775289576f261eaeaa984908f34cc696f7825feab85e`  
		Last Modified: Tue, 12 Aug 2025 20:30:38 GMT  
		Size: 18.8 KB (18820 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:ibmjava` - linux; ppc64le

```console
$ docker pull maven@sha256:c2673bf5820330ac5c3a4f0cef4abf3a8c88d7e92cd3357ef44b3dbfe3840a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222964537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14fae778ed9e9039003211bb14c1524e141de7eca671c737d8e16b3d2125647`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
ARG RELEASE
# Wed, 16 Jul 2025 06:51:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Jul 2025 06:51:38 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_VERSION=8.0.8.50
# Wed, 16 Jul 2025 06:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5bd4cc4749040ff2af6126adac1259dddc09d4c43dfc14779b1c6e83fb77c47a';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='58d2b8c23e815fa02019874109f78ad8ae01dee8f44e44ea0c69e29ececfd844';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='0c17796c0c75f71717b95843b93a93e27f1d91f23bc6e2d1d1005feb20fd7530';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2927a1e71e8665a0426e9c87b474fb1e405fba2f397cd65dfa47740d2204a7b`  
		Last Modified: Tue, 12 Aug 2025 18:23:37 GMT  
		Size: 1.5 MB (1536169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a1e9cd76df11cf884d2a1f9ade58772e0f6f878920b9ef002ff05b94bbbe60`  
		Last Modified: Tue, 12 Aug 2025 20:15:54 GMT  
		Size: 173.8 MB (173816259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dd5aa84e49d348a96c97916b4e5b2ae255f88358b86799068c29bad0f4106d`  
		Last Modified: Thu, 14 Aug 2025 02:08:05 GMT  
		Size: 3.9 MB (3925343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b414271b8ce12bb7a0fffc9f68c70888be382e431a20995aede72ea0a3a9b35`  
		Last Modified: Thu, 14 Aug 2025 02:08:05 GMT  
		Size: 9.2 MB (9242584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3373dda76eadee933bac38ba4994b42a9037ee2c60136039ee93a5bbb6ab160b`  
		Last Modified: Thu, 14 Aug 2025 02:08:05 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1549cf7ce64a59a721b6b7a56f4a5347bbba73e4fa1d41b31771cedadaf3b8d`  
		Last Modified: Thu, 14 Aug 2025 02:08:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:757ab82c1980d974897170e8c1a4bae5fa307ba4d0e57330e92887e92ba49bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3281282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1c11ee01782a14bbae650db5fe2ff3ce2eeaa0dff170be8b4b7b474797df61`

```dockerfile
```

-	Layers:
	-	`sha256:bbce4a3f94a1f0e642594ac49c7f9d3d251043a9b8fd017e04136bf680f910ce`  
		Last Modified: Thu, 14 Aug 2025 02:28:51 GMT  
		Size: 3.3 MB (3262387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f4f997f4418cf5e0aa45d194982521bbe6b3013671a3927101522e47f38f0c6`  
		Last Modified: Thu, 14 Aug 2025 02:28:51 GMT  
		Size: 18.9 KB (18895 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:ibmjava` - linux; s390x

```console
$ docker pull maven@sha256:bc00003a4616152e5553d7985eb94e4f013b57aa1ba7911a348bbeefd13f4b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.4 MB (204386820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2ac0569eb510efcf157192ffac0a5684b16e0d029853889b537ed0b08b246a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
ARG RELEASE
# Wed, 16 Jul 2025 06:51:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Jul 2025 06:51:38 GMT
ADD file:e0994d65dd44d220b4a55ce1033f7309688125fc54c99056866a92caff4bce78 in / 
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_VERSION=8.0.8.50
# Wed, 16 Jul 2025 06:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5bd4cc4749040ff2af6126adac1259dddc09d4c43dfc14779b1c6e83fb77c47a';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='58d2b8c23e815fa02019874109f78ad8ae01dee8f44e44ea0c69e29ececfd844';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='0c17796c0c75f71717b95843b93a93e27f1d91f23bc6e2d1d1005feb20fd7530';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9c54d9d5bd2c16422a2ac0653717d2ef3d3e03f04fb894713d9682ff2fb1a339`  
		Last Modified: Tue, 12 Aug 2025 17:29:30 GMT  
		Size: 28.0 MB (28003219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1f8a63a7a987fdc761e7e8968ba27654e47f55b299e1e97fe6e51a2c4940f6`  
		Last Modified: Tue, 12 Aug 2025 18:03:01 GMT  
		Size: 1.5 MB (1455837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397ca2c90bb4662b9b3e972a6aac6702d5fa9aa6d3bab89fbf5f367416c6f7d2`  
		Last Modified: Tue, 12 Aug 2025 19:02:25 GMT  
		Size: 162.6 MB (162630022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd01b10eec02617f214176a4cf57b2cf10c230c36b79d69a0286dc8ad0e7654`  
		Last Modified: Wed, 13 Aug 2025 07:34:30 GMT  
		Size: 3.1 MB (3054143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c63d3f2f703a02e090a65be18e61f881daad8b1269849fd831c4444b16a2cf8`  
		Last Modified: Wed, 13 Aug 2025 07:34:31 GMT  
		Size: 9.2 MB (9242563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84722081aee0f33cdc8bf0093f08841012a0971f984dc3c2a4982c1651a8bdfc`  
		Last Modified: Wed, 13 Aug 2025 07:34:30 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5bb1910ccfa9a43940c6d6f45800dce8a49aa9d206cff22531e131d43af01b`  
		Last Modified: Wed, 13 Aug 2025 07:34:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:c00df096ce0eb560f45a5cddc8970799359b3dbce30993d670a8641e98328c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2968397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12679929190b41d7114768a2e9dc9024b2e5423b171f155f69653cba0334f386`

```dockerfile
```

-	Layers:
	-	`sha256:3140b54537515d01b6c48ffd21364efae62df8a56cc15bff2489fa3d62eec97e`  
		Last Modified: Wed, 13 Aug 2025 08:28:27 GMT  
		Size: 2.9 MB (2949576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a10c0be7c6d24c59329492c940e51f5b970f9543d08ab45aa0501cf2761877`  
		Last Modified: Wed, 13 Aug 2025 08:28:27 GMT  
		Size: 18.8 KB (18821 bytes)  
		MIME: application/vnd.in-toto+json
