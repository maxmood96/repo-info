## `maven:ibmjava`

```console
$ docker pull maven@sha256:734011d87f4594a60d1ab99433137a21d4b5e677a32b5a3c91d5ed98ac6e835a
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
$ docker pull maven@sha256:d73e971181038dd527ecff48c5ab4a68cb79ff601e901216aa98d869c4d7537d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216176642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64554a7a11b3b23226826315d4efca7849d43fb5baffcd586ca5b3631701a9b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=8.0.8.40
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='edd0607f53f2b2517e9c4ef3299fabc80eedde2ff59baa15e1590ee48af49e93';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a10e7af283f45f9cfa8cdc93148d3dc0e54db768269974eb9f5249e8ee73ddfb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f0e88d365c3a9627b87abec45fa53d019b41a91a30ab8e8ac4b2ff0ce2574243';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab03ec578bf7e98879eeb6e91b76bdfb8b14c3b85568bcb98d925f36a6a3863e';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404b9155c2c09a6ae0a653ab18c1a2facb2b71624b3847e19f2a327d7424afc2`  
		Last Modified: Tue, 18 Feb 2025 21:29:50 GMT  
		Size: 1.5 MB (1450070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8ea5bcc2decfd928da95bd6911cee15e2b0878c28ef33d3f5ec2b23a745689`  
		Last Modified: Tue, 18 Feb 2025 21:29:53 GMT  
		Size: 172.9 MB (172907503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb37abda2fa96b5c91cc9588361bd3d2c344da3b5a34d695fee2f9df29a7712`  
		Last Modified: Tue, 18 Feb 2025 22:27:34 GMT  
		Size: 3.1 MB (3111662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c3f986d818751d236e7a78f94835d8c705f1509be8b5a09755039edc724efb`  
		Last Modified: Tue, 18 Feb 2025 22:27:34 GMT  
		Size: 9.2 MB (9170425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793f57e42e404045e55b5787596c7479aea542684cf0f764c9f08d53dae37a82`  
		Last Modified: Tue, 18 Feb 2025 22:27:34 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4a30e294e591d1327075fba5a0e812ce9fdbcf764491ce28882ddced16f57a`  
		Last Modified: Tue, 18 Feb 2025 22:27:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:47873815e1cf3d3ecb932c5ad4b78559c077008ecc895a6f605b9ea54f4b7a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3157765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fb79c13d98821d9a7b3c3ccdc368771218fa853576dfd350885e56c1560709`

```dockerfile
```

-	Layers:
	-	`sha256:49f459c066fed3227203c7a8847649d5977c5e966965b67c6899a4c7b60c1507`  
		Last Modified: Tue, 18 Feb 2025 22:27:33 GMT  
		Size: 3.1 MB (3138957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ce0e2af2750e21ea97fddf943eac19b4217ea91be0c618ae61db5d1445d684`  
		Last Modified: Tue, 18 Feb 2025 22:27:33 GMT  
		Size: 18.8 KB (18808 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:ibmjava` - linux; ppc64le

```console
$ docker pull maven@sha256:c979c492a4633c5499d49d7614fa6bc4a15afaca333710f29d9bc8cf177f6a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223021357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4408ec9b4e392c9c796d0eb84d748738aef9116d8b97eda1eab20a75e07a010b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=8.0.8.40
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='edd0607f53f2b2517e9c4ef3299fabc80eedde2ff59baa15e1590ee48af49e93';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a10e7af283f45f9cfa8cdc93148d3dc0e54db768269974eb9f5249e8ee73ddfb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f0e88d365c3a9627b87abec45fa53d019b41a91a30ab8e8ac4b2ff0ce2574243';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab03ec578bf7e98879eeb6e91b76bdfb8b14c3b85568bcb98d925f36a6a3863e';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549562dbb9f45949b79117ad60c4bbdb1ae9a0fd0a32b6119b57bf804e7f1c77`  
		Last Modified: Tue, 04 Feb 2025 08:22:06 GMT  
		Size: 1.5 MB (1536037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be22b512b5a96a4fe3331474ad127315a608e672c8ea3e79391be0db725d01a`  
		Last Modified: Tue, 18 Feb 2025 21:33:04 GMT  
		Size: 173.9 MB (173941697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e75267792d071a2f286835deee7412130ccf7be184c209a35124d5aecdd664`  
		Last Modified: Tue, 18 Feb 2025 22:47:33 GMT  
		Size: 3.9 MB (3924214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441f6d874420d418409ca470216578945ac41de3cdda690a4273c95c2de2a89d`  
		Last Modified: Tue, 18 Feb 2025 22:47:34 GMT  
		Size: 9.2 MB (9170436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07f322bf7773ebcaeb125334ad0dd93ee64297aedeb53681dedb361c718b8e3`  
		Last Modified: Tue, 18 Feb 2025 22:47:33 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765e50e8d5f680acc191a6fcecf41e70cb77d7df0afbddb29b8c038a7e2809ac`  
		Last Modified: Tue, 18 Feb 2025 22:47:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:09ab07001779ffb3acfdb9cedadd0c0ef0d8e95cb8fed286878352b0a3caba73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3143810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969485a07dfa5921905e8a80ec7811a5886ebab0d8c37e21a47b9d0ab09463a0`

```dockerfile
```

-	Layers:
	-	`sha256:4c377083feb51a83c0caa5b8956069186f70ed556ec873f56c5f8bdbf47c0029`  
		Last Modified: Tue, 18 Feb 2025 22:47:33 GMT  
		Size: 3.1 MB (3124928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b8c48eb3dc51e0df49a118adb6deb713a94b38dfcc32e844cd5f86fb7b96787`  
		Last Modified: Tue, 18 Feb 2025 22:47:33 GMT  
		Size: 18.9 KB (18882 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:ibmjava` - linux; s390x

```console
$ docker pull maven@sha256:9f244512946a2bdd730e5e9d63a4db0f924e9472507df86718bde687041dea53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204730288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c17ea9ecf99e5fae282266f7bfbc7bc120158037d079956c686a5aac52a48f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ARG RELEASE
# Tue, 20 Aug 2024 18:12:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=8.0.8.40
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='edd0607f53f2b2517e9c4ef3299fabc80eedde2ff59baa15e1590ee48af49e93';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a10e7af283f45f9cfa8cdc93148d3dc0e54db768269974eb9f5249e8ee73ddfb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f0e88d365c3a9627b87abec45fa53d019b41a91a30ab8e8ac4b2ff0ce2574243';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab03ec578bf7e98879eeb6e91b76bdfb8b14c3b85568bcb98d925f36a6a3863e';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f4ed4c83fd203a93b2e2d3afc549f52d4e75a4e9c4ecade96808e6a2fe3ebb`  
		Last Modified: Tue, 18 Feb 2025 21:29:44 GMT  
		Size: 1.5 MB (1455567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae97d923a9d8a7f083dca06b2b1940a95758b3f7b691117f2db3c03beddc5b0e`  
		Last Modified: Tue, 18 Feb 2025 21:32:46 GMT  
		Size: 163.0 MB (163049714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5250fd9ea8881ba0ddb0f37ac225818edc4c483ae8f6568b58fee84b374fa1`  
		Last Modified: Tue, 18 Feb 2025 22:33:00 GMT  
		Size: 3.1 MB (3052603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eba96933776949aaaaffe2c86adab34977277b0bc14ddf2079d64d57abadbb`  
		Last Modified: Tue, 18 Feb 2025 22:33:00 GMT  
		Size: 9.2 MB (9170433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100dfd129121d091c8adf138182fb2ef6ecde62660958c663c888d42bac9f186`  
		Last Modified: Tue, 18 Feb 2025 22:32:59 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe473f6db85584ca9686caae706a8e9a9e076d031e90d2f2a4527fa405d286c`  
		Last Modified: Tue, 18 Feb 2025 22:32:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:d7a3ce76ab17ed81e49f0749e272c512601493aec2ef756cb5e716fbf8dfa5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2833456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250ed840209d7856bcf3c66d863a09f407ec8c9bce9b7369c53e8d78b798a4cd`

```dockerfile
```

-	Layers:
	-	`sha256:140737e05535e55917d17e7a45fc356690f91c2e7aeb5c3cff352e596576e48e`  
		Last Modified: Tue, 18 Feb 2025 22:32:59 GMT  
		Size: 2.8 MB (2814649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2772bd156f3fdf948b86546178c17d8e02303d6cf87444fe9c7b840b02c22742`  
		Last Modified: Tue, 18 Feb 2025 22:32:59 GMT  
		Size: 18.8 KB (18807 bytes)  
		MIME: application/vnd.in-toto+json
