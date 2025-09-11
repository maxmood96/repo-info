## `maven:3-ibmjava-8`

```console
$ docker pull maven@sha256:04edad293fa61c9314cd0aae56fb86d5f333cdef31930994391296c5cbfbefe9
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
$ docker pull maven@sha256:b771b93b89e75e784a3b4305c8ce2fd4f2242b6718019349b922d0119cd3af6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.0 MB (216008349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad316e0ba31aaeae7d83a0969505a9d2dcaa4726752688019f681f72b093866`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_VERSION=8.0.8.51
# Wed, 16 Jul 2025 06:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a0a43a17fd78011daa47787c44ea72f73e11f7ae3e30cca39436a8f5a808eb5b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2a74815308d189cda1c66c960683ea600d7583625a2b1bf36aa6247406303bdc';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c9fec655a4840a48b14b89c335418a8f653e532f50c33d5458f5baba48ad9863';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6501625c0bd93c3a9e7bdafec2b1df8d65ee819572e7bb6e337314ab31718ce`  
		Last Modified: Thu, 11 Sep 2025 16:55:12 GMT  
		Size: 1.5 MB (1450049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cd794a5e418d61cd9f0391f9aa128310c0ef64a7a804c3fddc9453c8e60e54`  
		Last Modified: Thu, 11 Sep 2025 16:55:28 GMT  
		Size: 172.7 MB (172664633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253abca9820ef8997b45f94802c25d5455a319385c7821b2f0b0b3a7cb2c8f05`  
		Last Modified: Thu, 11 Sep 2025 17:00:13 GMT  
		Size: 3.1 MB (3113124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dae00a287bdca4571a17c13fb5a49fdef827510bcb6d2d9486c4c9c8314b990`  
		Last Modified: Thu, 11 Sep 2025 17:00:13 GMT  
		Size: 9.2 MB (9242570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d9d652492bf85f0694f02d1062cc0d9336bc6bd1e4467256b0a77fa57c72c8`  
		Last Modified: Thu, 11 Sep 2025 16:59:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e0074bc3d86ec8aac15e9a745b1a95b93935ad871ba92d14c956ab46cd3021`  
		Last Modified: Thu, 11 Sep 2025 17:00:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibmjava-8` - unknown; unknown

```console
$ docker pull maven@sha256:f7c9c81fe158bfd7c8cbd207a6969da2f676e99f696d81081ca13f6a6874e97c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3295111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9a751a6297ede9dd92abda3308ef90039f21deb32395bbb3f119bc7cfde0cb`

```dockerfile
```

-	Layers:
	-	`sha256:c45e76bcee066dcf215755332705a93e13039e4f5a991ec1aa23eaed4366ee16`  
		Last Modified: Thu, 11 Sep 2025 17:27:51 GMT  
		Size: 3.3 MB (3276292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0055c2f9ef0003cb4a15cab648a1f9a145c702ae32f2b002ccfb366817bc8bf0`  
		Last Modified: Thu, 11 Sep 2025 17:27:52 GMT  
		Size: 18.8 KB (18819 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibmjava-8` - linux; ppc64le

```console
$ docker pull maven@sha256:89c24a24b3721f4e34f27f50376862eadc04b407a13e13e5c7a25544212b38a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222961948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af36166f8fc63287dc2286c992f9a7d84cd1f53328d9f68f036336f56bcbf6ec`
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
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_VERSION=8.0.8.51
# Wed, 16 Jul 2025 06:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a0a43a17fd78011daa47787c44ea72f73e11f7ae3e30cca39436a8f5a808eb5b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2a74815308d189cda1c66c960683ea600d7583625a2b1bf36aa6247406303bdc';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c9fec655a4840a48b14b89c335418a8f653e532f50c33d5458f5baba48ad9863';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c192fa06531347041f063475dcc6b4d9821e21d789e42dbdb74912b07cb28d9`  
		Last Modified: Tue, 02 Sep 2025 01:05:09 GMT  
		Size: 1.5 MB (1536215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161a9f118ca1f1cbf4058ca82bc7edc4791643f5aab1e787697cb7e9c745ab8b`  
		Last Modified: Thu, 11 Sep 2025 19:08:09 GMT  
		Size: 173.8 MB (173813396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58da7465292dbef4103cb9498a28b7abbc5300ab85e4a1243f55184af4d7b9b1`  
		Last Modified: Thu, 11 Sep 2025 18:24:48 GMT  
		Size: 3.9 MB (3925490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44517cf4c55b16a18a86ed41e5d23589ea7bf55b27feab713eec17af60118abd`  
		Last Modified: Thu, 11 Sep 2025 18:24:49 GMT  
		Size: 9.2 MB (9242584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac10908af1dfd90d278538a1197bc4c79c895a5016d424cacc76c75bc44d01f`  
		Last Modified: Thu, 11 Sep 2025 18:24:48 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e73e0a7f846991ddb504eb956b8a95ca211f9d770774ef5255ccd52a08906f`  
		Last Modified: Thu, 11 Sep 2025 18:24:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibmjava-8` - unknown; unknown

```console
$ docker pull maven@sha256:8716c471f308fc1970ed16f3d0c62852461fc03c958a6281bed28c76ad7d1d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3281298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666e3fcbbf4188db7f92a5c5a42c49cb40114f60dcb33f43acddcfedfd85c95d`

```dockerfile
```

-	Layers:
	-	`sha256:bfa0c9a9539ef7fda1508e13b205d9b669a35412b6c27db26b093ee645e3fa10`  
		Last Modified: Thu, 11 Sep 2025 20:27:58 GMT  
		Size: 3.3 MB (3262403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2f9ef6641ec0222edd6b521143eee91c1691f7c7f24f6027ca6f2b2457c14e5`  
		Last Modified: Thu, 11 Sep 2025 20:27:59 GMT  
		Size: 18.9 KB (18895 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibmjava-8` - linux; s390x

```console
$ docker pull maven@sha256:8dec15ab9f274bd10988f3e3a1ace309cc3d651bfaa7d8142d286cf59580ad39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.4 MB (204390074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38526543d3097311735bc40d84c81922de0ea95056cf5183f1e33c7745c2bf8`
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
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_VERSION=8.0.8.51
# Wed, 16 Jul 2025 06:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a0a43a17fd78011daa47787c44ea72f73e11f7ae3e30cca39436a8f5a808eb5b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2a74815308d189cda1c66c960683ea600d7583625a2b1bf36aa6247406303bdc';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='c9fec655a4840a48b14b89c335418a8f653e532f50c33d5458f5baba48ad9863';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
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
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20c245bb91f7038c8e7666e50e3b477d3bb0faf772b531b6ddcd81ed6b348c`  
		Last Modified: Thu, 11 Sep 2025 16:54:02 GMT  
		Size: 1.5 MB (1455758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b95b4dad0cf791eac4470394de71d0a10e6de0edfef58b1a82a54a4246b113`  
		Last Modified: Thu, 11 Sep 2025 18:09:36 GMT  
		Size: 162.6 MB (162632978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d5ef017c96c0a045a8e48519ea962eb5ec93f5cdcbb0228e79ea31ac69513c`  
		Last Modified: Thu, 11 Sep 2025 17:53:35 GMT  
		Size: 3.1 MB (3054047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f612d24c22b717652897713bf5f52ec5768f858ef3713daac3d51db662d13232`  
		Last Modified: Thu, 11 Sep 2025 17:53:36 GMT  
		Size: 9.2 MB (9242586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a923e4b36f7b82a82641f3db66c7aab62a1e1d773bb7c1da708eaafa584ae3`  
		Last Modified: Thu, 11 Sep 2025 17:53:35 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a876d2a181f8e3c4f58efdcbc3c86eef5861d5277b86b01a70a2598950fd1f37`  
		Last Modified: Thu, 11 Sep 2025 17:53:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibmjava-8` - unknown; unknown

```console
$ docker pull maven@sha256:1850f1e4ce78361a7801afdb9c8dad7ff52f5b414d905cdbd339f01b0f089837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2968412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906079a26edabd97dd5ed48ad355456e7b255986daba88638d2ad5418678093e`

```dockerfile
```

-	Layers:
	-	`sha256:e555a9ad59afcec6307877f2c371f3730a4f2a5fb94ae2f15806fd760eaa5383`  
		Last Modified: Thu, 11 Sep 2025 20:28:03 GMT  
		Size: 2.9 MB (2949592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53b52173448578bbba75a6c03eb9e475ccaf2d8be3dea367c13f70f4968ad4e8`  
		Last Modified: Thu, 11 Sep 2025 20:28:04 GMT  
		Size: 18.8 KB (18820 bytes)  
		MIME: application/vnd.in-toto+json
