## `maven:3-ibmjava-8`

```console
$ docker pull maven@sha256:b913f539c9d79cf41e7b11ac5afcbe2a0263fe87bedb10ab8a3fa2af4774f648
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `maven:3-ibmjava-8` - linux; amd64

```console
$ docker pull maven@sha256:f7a1592f1b9ac24d5225cbdec72c7364447f02fd275fa6b6718575c50edb0c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217185494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893b1eb69df603b13a753f22e8633172009b895e1665754eb83ad2beb77869bc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:19:11 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 15 May 2026 21:19:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:19:11 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 15 May 2026 21:20:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0978a87ce0b78bf6530fe5b9bd9fb737ff04ecc8dae1c849cb1c42908b1095a8';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='731c2693424a66054fcc45624c411461ea8a62efd898a90f508bdbd20c0b6125';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8a1cfafb51e8cf4753df40fb9906d3571ae086ed33b1bbcf807c416beac37521';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 15 May 2026 21:20:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Mon, 18 May 2026 22:40:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 May 2026 22:40:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 18 May 2026 22:40:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:40:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:40:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 18 May 2026 22:40:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 May 2026 22:40:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 May 2026 22:40:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 May 2026 22:40:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 May 2026 22:40:07 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 May 2026 22:40:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 May 2026 22:40:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 May 2026 22:40:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2787f09070467d2285d3d30f0b5a2210ae872eaa7b477483f9a32fcb02ad0a`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 1.5 MB (1450153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ffb12faa39cf44064f44ce05797a1052a8c7c67e226d28f0a04a81f2d3e048`  
		Last Modified: Fri, 15 May 2026 21:20:21 GMT  
		Size: 173.5 MB (173521360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8586ed11e1c5ea9fb5bc9b17b6d281aae912a4cf4d225f324d2fb6a31b8b1795`  
		Last Modified: Mon, 18 May 2026 22:40:17 GMT  
		Size: 3.1 MB (3116322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af31360b8ec62f66accb8ba1c72ffaa5853e7aa0045cbd838a5dcc1793fb1bb`  
		Last Modified: Mon, 18 May 2026 22:40:18 GMT  
		Size: 9.4 MB (9359968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccdb3f8ee420c940cf98d9316ce87037bdfdddc0fa65c2f997eeb8ead36c28c`  
		Last Modified: Mon, 18 May 2026 22:40:17 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83bc6b311f47e97db7857720d68d489af93bc9ff7615cbc71a39e6a868ef24c`  
		Last Modified: Mon, 18 May 2026 22:40:17 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibmjava-8` - unknown; unknown

```console
$ docker pull maven@sha256:7a0c7f043b0e6fe8fbf789a03537d523d8765675d82621ca6ecf7c7f738814ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3294266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbad98cc5e923b9906a8a3f4c77a9b835aba3de21bd20a372524e77f76013a3`

```dockerfile
```

-	Layers:
	-	`sha256:3b21fefb957ca56f56dc6caccc8c4b453f41b348b2d4b032537b2858d760fd63`  
		Last Modified: Mon, 18 May 2026 22:40:17 GMT  
		Size: 3.3 MB (3277487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0193e7dc62b3f84055ee2aa7e203947c61042f4d174d0fbf8ff0c0439731a4b9`  
		Last Modified: Mon, 18 May 2026 22:40:17 GMT  
		Size: 16.8 KB (16779 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibmjava-8` - linux; ppc64le

```console
$ docker pull maven@sha256:173b91912876bfb8c2aa52e02e33dcfa9f31934a363c8c30e30ba114ed3f5495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224118475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788b80267304b1b1037052d1f9d5a7a4a95c7bf1914ca17098bc04aa1db7c5e3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:28:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 15 May 2026 21:28:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:28:40 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 15 May 2026 21:30:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0978a87ce0b78bf6530fe5b9bd9fb737ff04ecc8dae1c849cb1c42908b1095a8';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='731c2693424a66054fcc45624c411461ea8a62efd898a90f508bdbd20c0b6125';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8a1cfafb51e8cf4753df40fb9906d3571ae086ed33b1bbcf807c416beac37521';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 15 May 2026 21:30:53 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 15 May 2026 22:33:10 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 May 2026 22:38:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 18 May 2026 22:38:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:38:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:38:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 18 May 2026 22:38:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 May 2026 22:38:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 May 2026 22:38:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 May 2026 22:39:00 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 May 2026 22:39:00 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 May 2026 22:39:00 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 May 2026 22:39:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 May 2026 22:39:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1d9502a29e5927b7c6acfcd4d85b9058b023b826aa21b29033ebc1aa0f839a`  
		Last Modified: Fri, 15 May 2026 21:29:48 GMT  
		Size: 1.5 MB (1536350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7f2efad79d94e93f841931f8cfc5c67cbdabdbfaf887a278b736b62f7369b6`  
		Last Modified: Fri, 15 May 2026 21:31:30 GMT  
		Size: 174.6 MB (174644954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11efd580b47d1958ef2996fd023e36e0d149dc2714a4b1e3902ac5c7eb73ab8`  
		Last Modified: Fri, 15 May 2026 22:33:40 GMT  
		Size: 3.9 MB (3929474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce6047bad39c898fae5c9995142730a6700e773846465da2ac57e24dac95344`  
		Last Modified: Mon, 18 May 2026 22:39:23 GMT  
		Size: 9.4 MB (9359969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bac8f609de881298bdb0e73a07816060681d5806d4fee9892e93e825596126e`  
		Last Modified: Mon, 18 May 2026 22:39:22 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1786f94fd8356c11ded5dfa5275c7d4af70819e93e361aa06fb50af6b8489a`  
		Last Modified: Mon, 18 May 2026 22:39:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibmjava-8` - unknown; unknown

```console
$ docker pull maven@sha256:79ecf68fb465588ec249781ad492f93d14e1112e9953dc0a597455387da5da16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3280450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba19aff07506f2fdf0dce376c9e34498a08c3bfb5085af945a2de5bc5b1ecc6`

```dockerfile
```

-	Layers:
	-	`sha256:60067bb0f5fca3f515f5a728b266de8034b7042684372792a3c8d63ca5adfd8c`  
		Last Modified: Mon, 18 May 2026 22:39:22 GMT  
		Size: 3.3 MB (3263598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb6654aa42d1ef7909e9661bdd3e2ad241c4a9a8bea6a505b2f20500b15a39da`  
		Last Modified: Mon, 18 May 2026 22:39:22 GMT  
		Size: 16.9 KB (16852 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibmjava-8` - linux; s390x

```console
$ docker pull maven@sha256:43d1b27865f1a5a385fb64f8d8ef21e4c9dbc7b171b29a8dfe313b0f3e595e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207247076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9847bad8a7832eba4dcd116e02977e77b84d048731c752179cc0b39c5eb26d4b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 09 May 2026 04:50:49 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:51 GMT
ADD file:17ca3274b34edf79b2d4401a24984fb8dc339a8298f0e3703af025f51b67336b in / 
# Sat, 09 May 2026 04:50:51 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:25:56 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 15 May 2026 21:25:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:25:56 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 15 May 2026 21:27:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0978a87ce0b78bf6530fe5b9bd9fb737ff04ecc8dae1c849cb1c42908b1095a8';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='731c2693424a66054fcc45624c411461ea8a62efd898a90f508bdbd20c0b6125';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8a1cfafb51e8cf4753df40fb9906d3571ae086ed33b1bbcf807c416beac37521';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 15 May 2026 21:27:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 15 May 2026 21:57:36 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 May 2026 22:37:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 18 May 2026 22:37:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:37:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:37:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 18 May 2026 22:37:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 May 2026 22:37:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 May 2026 22:37:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 May 2026 22:37:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 May 2026 22:37:34 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 May 2026 22:37:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 May 2026 22:37:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 May 2026 22:37:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c8acb84faa73cc102915433858f425bdd6749804de64fd2e27d5f491f005a91b`  
		Last Modified: Sat, 09 May 2026 05:25:25 GMT  
		Size: 28.2 MB (28202305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db157cb22854d83df151b1cab375b07af965e81376821890ae19bc26409b7219`  
		Last Modified: Fri, 15 May 2026 21:26:47 GMT  
		Size: 1.5 MB (1455969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce20b46a2ab7510b71e6cea882a2232747c83d160dfe8d2829ce2304b82f0cc`  
		Last Modified: Fri, 15 May 2026 21:28:36 GMT  
		Size: 165.2 MB (165169467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d72c33bb8afdbbca891cac44786c2977f9392fd208cc971d6b066a4d991817`  
		Last Modified: Fri, 15 May 2026 21:57:51 GMT  
		Size: 3.1 MB (3058354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3540c00e5a5b59deb74091aac8abe50f1247b4dcbc00471c56a3fd91f1f84339`  
		Last Modified: Mon, 18 May 2026 22:37:50 GMT  
		Size: 9.4 MB (9359972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e9b99c87afd84739b35619c984e6263ed9aa4d967097258089de983dd4bcf6`  
		Last Modified: Mon, 18 May 2026 22:37:50 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a8d39902b3fe690af278e0e692d797ab7b0fa4f686189bd136fc089eeb500a`  
		Last Modified: Mon, 18 May 2026 22:37:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibmjava-8` - unknown; unknown

```console
$ docker pull maven@sha256:10586b39f8c4195ebb6e3f7a34ff3a6b66f3419132e97e95c0351f95b294f3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d611c25664c5d53dce1f909e0ddb758656fd1e2ee40bf8db1382152b7183f02e`

```dockerfile
```

-	Layers:
	-	`sha256:730d538c3a33090a208d8ab5623059cf4db72f31e0709aae012d1fa7c96325d1`  
		Last Modified: Mon, 18 May 2026 22:37:50 GMT  
		Size: 3.0 MB (2950773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417ee595912a2ad99dd32fbf75e9b7c7f388240f58487204b6c6112d507445ff`  
		Last Modified: Mon, 18 May 2026 22:37:50 GMT  
		Size: 16.8 KB (16779 bytes)  
		MIME: application/vnd.in-toto+json
