## `maven:3-ibmjava-8`

```console
$ docker pull maven@sha256:8a6a96ef106e9b2a22f96269e47c3b8dde672e0dd62a81313774b5422a37da37
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
$ docker pull maven@sha256:02c3122f87bbec2813d518e82db93de5549e6bfaca6477e0b823e78698ed5bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.0 MB (215988507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553e9d1132efeeeb341dfcaaa8be3e53f2e2149a532762e6a9bd537137b0a385`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c93cb839cb6e8a082ecaddd43a5736bb33784ff578adf743a3970b418113655b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85fb7353a7d5ac486d9f9843bc4968c6fd1f989adcbc214bb35191842e90db7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1acec5687144529687057af8d40c37913b0bc22a09fa413aed0fd266bb4b979e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ff575513c14515bc1fc281152ff4702540e63028c4c8900abb6df98f9ce2d1ec';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c22e75fb9dfc02c2b846fdb7ea830b729536ea6e69c37adbe23e490a2a5b387`  
		Last Modified: Tue, 17 Sep 2024 00:59:30 GMT  
		Size: 1.4 MB (1438138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae95ac88ac0804bc3b7ca3e44688c77636d9eed729564f2ccecbc336cb0f2c0`  
		Last Modified: Tue, 17 Sep 2024 00:59:33 GMT  
		Size: 172.1 MB (172132677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30732df03e64665908948b466d931deea35d6759d57a0f734b0b21253e102aa7`  
		Last Modified: Fri, 27 Sep 2024 19:55:47 GMT  
		Size: 3.7 MB (3710528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72db9255b590af3d0749fedd3033f3c4bd7ca671b0621b62a73005a48e0ebf8`  
		Last Modified: Fri, 27 Sep 2024 19:55:47 GMT  
		Size: 9.2 MB (9170439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98eb0accde4a9722abdacb53eacd0ce80d3c2193d3d2b5c660b54a67bae7b72`  
		Last Modified: Fri, 27 Sep 2024 19:55:47 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcc8830516be9b782801258606bb48c537c4b12da966de59bb655b42b1f56a5`  
		Last Modified: Fri, 27 Sep 2024 19:55:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibmjava-8` - unknown; unknown

```console
$ docker pull maven@sha256:60f3cf7cf97d3886537bdad432a528e0e8fe5bddf208bc465e4b34155b65a5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3141930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbe592c812b7a04ba88f81833306017c4a7eb63dbbb01603e8d74bc1136c2e5`

```dockerfile
```

-	Layers:
	-	`sha256:a2f07ecb658c5de97948b2f067af10dd09a0e2f6dbd593e86e44dfcce1bddce0`  
		Last Modified: Fri, 27 Sep 2024 19:55:47 GMT  
		Size: 3.1 MB (3123157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f714da8f0ed5e5e9f04fac4bf3430fe7dc634d4aa72f0e04ed43af5d36df1f06`  
		Last Modified: Fri, 27 Sep 2024 19:55:47 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibmjava-8` - linux; ppc64le

```console
$ docker pull maven@sha256:2b737c3fa79d2e6a1ccc28f3b9dd74de809acc9293426309c6703e8cac4e6d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221819188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d58007e820161ddca459a1f33da58ca23f8e0945c0eb57d62c07fc26f5d0a4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c93cb839cb6e8a082ecaddd43a5736bb33784ff578adf743a3970b418113655b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85fb7353a7d5ac486d9f9843bc4968c6fd1f989adcbc214bb35191842e90db7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1acec5687144529687057af8d40c37913b0bc22a09fa413aed0fd266bb4b979e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ff575513c14515bc1fc281152ff4702540e63028c4c8900abb6df98f9ce2d1ec';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
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
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5432b06a5eb0b15c862e467e7550b35e423da42224cc982fc620a3e04b458d07`  
		Last Modified: Tue, 17 Sep 2024 01:31:54 GMT  
		Size: 1.5 MB (1523245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62636db2ac4815fe48801a3b62ed8d568ad28ca0e2330b3a84e227a61b023a72`  
		Last Modified: Tue, 17 Sep 2024 01:34:57 GMT  
		Size: 172.7 MB (172748853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9448d479801a6c2f7ff86033f4dcd5ca8a64c3a64b45d57f4c72ee23de9839`  
		Last Modified: Tue, 17 Sep 2024 09:31:33 GMT  
		Size: 3.9 MB (3927383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374e8da8e9f9a99eb1727861ad2b208faca233f1c84f76206e178f4e1f4fd9b3`  
		Last Modified: Tue, 17 Sep 2024 09:31:33 GMT  
		Size: 9.2 MB (9170426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3949647ac3ee542cdccb2b56f1466331c8e726d6663a4302997c5562fd0cb58b`  
		Last Modified: Tue, 17 Sep 2024 09:31:33 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e556e153202d327b167967a50ffdcd1862d33aed9e33f889cc48412b63c12a51`  
		Last Modified: Tue, 17 Sep 2024 09:31:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibmjava-8` - unknown; unknown

```console
$ docker pull maven@sha256:de0d9221340a1e6631c929f555e5f710fa8b480a6b57db6ffcbe5e5dff881f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed939f738c46031b0bbaab5067af73281ae7c1ee7986c55ddeaaefee2ad1695`

```dockerfile
```

-	Layers:
	-	`sha256:c3ecee6f260e8e1883cb9d8a6f6f51d43d866c646865c7a886ea77a27d29f4b2`  
		Last Modified: Sat, 28 Sep 2024 06:03:32 GMT  
		Size: 3.1 MB (3103219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a0b7fd45e440aaac6456ac894797bcc266d64a94b67d8eb29f28861c9bc80fb`  
		Last Modified: Sat, 28 Sep 2024 06:03:31 GMT  
		Size: 18.9 KB (18878 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-ibmjava-8` - linux; s390x

```console
$ docker pull maven@sha256:9de0b9d953cd206c108ed50c0fba2dfdb7d4e34870e73ceab8397d61ab9f3112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204474286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b5134150d40e0091599baf4e67f0daf70aefe0d633569aee67f0c4303c89ab`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Aug 2024 07:06:00 GMT
ARG RELEASE
# Thu, 15 Aug 2024 07:06:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Aug 2024 07:06:00 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 15 Aug 2024 07:06:00 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Thu, 15 Aug 2024 07:06:00 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c93cb839cb6e8a082ecaddd43a5736bb33784ff578adf743a3970b418113655b';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='85fb7353a7d5ac486d9f9843bc4968c6fd1f989adcbc214bb35191842e90db7f';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='1acec5687144529687057af8d40c37913b0bc22a09fa413aed0fd266bb4b979e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ff575513c14515bc1fc281152ff4702540e63028c4c8900abb6df98f9ce2d1ec';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
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
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6d015aafef1cc8c93af1c71f0f144845de0b5e0e0bbcd3c27bccf671404292`  
		Last Modified: Tue, 17 Sep 2024 02:12:21 GMT  
		Size: 1.4 MB (1441914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f675c68607c669df079bb79b19cf6109bef13663f5009617064a4ba0e4f20d89`  
		Last Modified: Tue, 17 Sep 2024 02:15:19 GMT  
		Size: 162.2 MB (162211289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1fac6c708d19c66096da041dda7d740fbceb6b1756c96c7d8af67ca8aa32d8`  
		Last Modified: Wed, 02 Oct 2024 03:10:35 GMT  
		Size: 3.6 MB (3648160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5185b01a77ef5d4e81ee06bd24e2a266b92db496d8a7010311b06f6f2afd95`  
		Last Modified: Wed, 02 Oct 2024 03:10:35 GMT  
		Size: 9.2 MB (9170413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cbb26c29ef3309e81070901bc32a4096a6e6232f7e6a8b4c3bfab7ba8e7edf`  
		Last Modified: Wed, 02 Oct 2024 03:10:35 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea6d1b860957d634a52f4451ec3ce5919da0e81ee6d0e3817e1cbdda49fd1c4`  
		Last Modified: Wed, 02 Oct 2024 03:10:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-ibmjava-8` - unknown; unknown

```console
$ docker pull maven@sha256:85e65d259712b7fc45016b6feb6961302c9977f5993531c907dee9c045ba10b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2817296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6188e8ec04b173f5f787fd8638540d98ffeab8a0bca7c88adc224e2e792712`

```dockerfile
```

-	Layers:
	-	`sha256:3044e94787fe166592179255c1e698c09b6da40e143f6cf9b95e5c7fc28354f5`  
		Last Modified: Wed, 02 Oct 2024 03:10:35 GMT  
		Size: 2.8 MB (2798487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e1ccf46f9918c6c8164ef8ccffb8e28cd7bd1f8bf64c5dd8202a9bea2b817b2`  
		Last Modified: Wed, 02 Oct 2024 03:10:35 GMT  
		Size: 18.8 KB (18809 bytes)  
		MIME: application/vnd.in-toto+json
