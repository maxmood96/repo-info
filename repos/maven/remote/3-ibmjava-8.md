## `maven:3-ibmjava-8`

```console
$ docker pull maven@sha256:c2739a7ea8d6d045a8974bcfc6860dbbaba739ead643c2459a795f79bc4e1432
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
$ docker pull maven@sha256:ff1879c7287d163c3c5c42beca4c9545eb1f067dbc477efa3bb72137b378e262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217137794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01603252a0b0e2689b1d1962d9f6d0e1b5bb6fdf3990b493ec3053cddc0129b5`
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
# Fri, 15 May 2026 21:51:25 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:51:25 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 15 May 2026 21:51:25 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 15 May 2026 21:51:25 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 15 May 2026 21:51:25 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 15 May 2026 21:51:25 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 15 May 2026 21:51:25 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 15 May 2026 21:51:25 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:51:25 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 15 May 2026 21:51:25 GMT
ARG USER_HOME_DIR=/root
# Fri, 15 May 2026 21:51:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 15 May 2026 21:51:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 15 May 2026 21:51:25 GMT
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
	-	`sha256:d77afe6b56ea80e57bb3b9504af3dccb8819c787e250779f1e510b50b8ae40d3`  
		Last Modified: Fri, 15 May 2026 21:51:34 GMT  
		Size: 3.1 MB (3116329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2816edcaa5a7ed98786bfdb111e4e017785b835a91212ff0c7b44ea376a4e6be`  
		Last Modified: Fri, 15 May 2026 21:51:35 GMT  
		Size: 9.3 MB (9312259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf7f828ff9ca221da7cba86899359d53f8a586b8a1f534b2a07869a4a8494bc`  
		Last Modified: Fri, 15 May 2026 21:51:34 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ef434d2467458a955e16466feab8d141ccf7ff76e193fe994de3da190b684f`  
		Last Modified: Fri, 15 May 2026 21:51:34 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibmjava-8` - unknown; unknown

```console
$ docker pull maven@sha256:d85fc7bf916c445a395cc61af7cfabd957d86c5428edb2039661557558b711cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3294417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2724cc2d0d3fbd41d32a367621606427f5b3dd7e52da5efc0e2e0836d0f62d6`

```dockerfile
```

-	Layers:
	-	`sha256:84864a20493d1e3bfe1c5d264f4f1aec85d65688f8175c50a573f50c1ed66f97`  
		Last Modified: Fri, 15 May 2026 21:51:34 GMT  
		Size: 3.3 MB (3277484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40702d2dd24496b77abbe87e97ea55ee26e0e724967169842078ab607cf8ee73`  
		Last Modified: Fri, 15 May 2026 21:51:34 GMT  
		Size: 16.9 KB (16933 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibmjava-8` - linux; ppc64le

```console
$ docker pull maven@sha256:fb7f3033c22961a7164fa1c24abd5df5073700e42e593b953507435b43857833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224072126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc36e928ad0b2c741098308513f00ba0d94a133bb4ce438c94cdd404ea361188`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:55:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 15 Apr 2026 21:55:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:55:16 GMT
ENV JAVA_VERSION=8.0.8.65
# Fri, 24 Apr 2026 17:27:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0978a87ce0b78bf6530fe5b9bd9fb737ff04ecc8dae1c849cb1c42908b1095a8';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='731c2693424a66054fcc45624c411461ea8a62efd898a90f508bdbd20c0b6125';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='8a1cfafb51e8cf4753df40fb9906d3571ae086ed33b1bbcf807c416beac37521';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Fri, 24 Apr 2026 17:27:25 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 08 May 2026 01:53:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 01:53:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 01:53:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 01:53:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 01:53:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 01:53:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 01:53:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 01:53:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 01:53:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 01:53:08 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 01:53:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 01:53:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 01:53:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627beed1bb6b7851a42d83bf152b722e90303fa76712b52f97569f072936cf73`  
		Last Modified: Wed, 15 Apr 2026 21:56:26 GMT  
		Size: 1.5 MB (1536184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2132eaca12df4dc2a7b0af262a8068d86a7122d98ccc02571ca194fca2fb9e83`  
		Last Modified: Fri, 24 Apr 2026 17:28:02 GMT  
		Size: 174.6 MB (174644995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b2aa04832206212667eeb36439ebe4a513854a80416e20840e0e6e7fe479d0`  
		Last Modified: Fri, 08 May 2026 01:53:27 GMT  
		Size: 3.9 MB (3929298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0f6d1d9025a9fb63a9d2c5e3a82f46df447d92798f0b9ca085a8b7d4b0faca`  
		Last Modified: Fri, 08 May 2026 01:53:27 GMT  
		Size: 9.3 MB (9312247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83e647db2618d1423b75305c30948aa9366fcf0e4bae5cbbb35c98ae182dc08`  
		Last Modified: Fri, 08 May 2026 01:53:26 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6130c4a25a0d74bbaa1dc171e5743b5521ef90f35613c825c5e6458277073802`  
		Last Modified: Fri, 08 May 2026 01:53:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibmjava-8` - unknown; unknown

```console
$ docker pull maven@sha256:8f10553981844e318befc9c1c8a6b732f9b0ab8e98b398661d798ce35003b9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3280596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb53473aa34aa60e0131102199efcc8f92891d764d4fd6e5ccc6924348aded6`

```dockerfile
```

-	Layers:
	-	`sha256:947396f17073f062eae088a335819ccbf43992b75267e85b3ae1ac79aa2edbf8`  
		Last Modified: Fri, 08 May 2026 01:53:26 GMT  
		Size: 3.3 MB (3263591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89006aa4e38cb3c604a7cdc156b2e6572c80966ebef0e0a73bf4414aba616d17`  
		Last Modified: Fri, 08 May 2026 01:53:26 GMT  
		Size: 17.0 KB (17005 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibmjava-8` - linux; s390x

```console
$ docker pull maven@sha256:8f2c6cbc07450f841558ec1f6a30a20e6390cdba5edaa74789cd6edd9b87a528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207199350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bedb9124e16faefb9d8dcebffecbda782263e07aeda6cca4cd76d4f5fdde2d08`
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
# Fri, 15 May 2026 21:57:37 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 15 May 2026 21:57:37 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 15 May 2026 21:57:37 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 15 May 2026 21:57:37 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 15 May 2026 21:57:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 15 May 2026 21:57:37 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 15 May 2026 21:57:37 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:57:37 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 15 May 2026 21:57:37 GMT
ARG USER_HOME_DIR=/root
# Fri, 15 May 2026 21:57:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 15 May 2026 21:57:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 15 May 2026 21:57:37 GMT
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
	-	`sha256:89005c6afcb9dc4ad1e7a0d7c4396fc3fa6f63d2c4d304259d5e0c7ff10156c3`  
		Last Modified: Fri, 15 May 2026 21:57:51 GMT  
		Size: 9.3 MB (9312247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9182e6ba194c00ffc09120683da00935f4cd708175ba4bc65f7a670ace21ddd9`  
		Last Modified: Fri, 15 May 2026 21:57:51 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652e2d1f5d684394a6842f668f37681098bbd19c7790848acffe86f4f7ab8045`  
		Last Modified: Fri, 15 May 2026 21:57:51 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibmjava-8` - unknown; unknown

```console
$ docker pull maven@sha256:31622a8df1ac3f19403ab29e39c48480db062217da97cfc5834ccc7602e02dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a47875e667986d1aebf5564a60d2222185f5b6a1040c07570f02a1554a46bf`

```dockerfile
```

-	Layers:
	-	`sha256:8453322a0e62f1adffae36e4f8acac129ccb9fd8c639392febe10216a3d54b5b`  
		Last Modified: Fri, 15 May 2026 21:57:51 GMT  
		Size: 3.0 MB (2950770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b4ef26d1d52c6da4b7b49271aad7683a410167672a8dc378a3ad35b7cbf1a56`  
		Last Modified: Fri, 15 May 2026 21:57:51 GMT  
		Size: 16.9 KB (16933 bytes)  
		MIME: application/vnd.in-toto+json
