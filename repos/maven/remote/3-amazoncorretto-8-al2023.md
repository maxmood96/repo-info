## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:7e3436fde566dc9b2b89b256ee4de07f8c1a0511a5b2e322d684a6f9683154ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:ac8e702eb98d3ae1ec53fa7a7ef0c03ee26030a29cb431a57376e28b11da08d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.5 MB (494496216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc1d958abb825cd386a542a0de54b092b4b66b718a7cf5b9fb2153123c9de44`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:25 GMT
ARG version=1.8.0_472.b08-1
# Fri, 31 Oct 2025 00:11:25 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:11:25 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 31 Oct 2025 01:16:27 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 31 Oct 2025 01:16:27 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 31 Oct 2025 01:16:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 31 Oct 2025 01:16:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:16:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:16:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 31 Oct 2025 01:16:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 31 Oct 2025 01:16:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 31 Oct 2025 01:16:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 31 Oct 2025 01:16:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 31 Oct 2025 01:16:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 31 Oct 2025 01:16:28 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 31 Oct 2025 01:16:28 GMT
ARG USER_HOME_DIR=/root
# Fri, 31 Oct 2025 01:16:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 31 Oct 2025 01:16:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 31 Oct 2025 01:16:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d90a02718a2ec471735b22a7012a63f3b6fd6aa7b11464ff1edf280a2e204b8`  
		Last Modified: Fri, 31 Oct 2025 01:12:00 GMT  
		Size: 330.9 MB (330868176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57f33a34b084b3485065b668ebe61e2488353b877704eb32e694387f60757bd`  
		Last Modified: Fri, 31 Oct 2025 01:17:14 GMT  
		Size: 94.9 MB (94932699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d013a72c6943acd35b3b09114e32166da6bb3faca937d18ddbd2a0f16d8554cc`  
		Last Modified: Fri, 31 Oct 2025 01:17:03 GMT  
		Size: 5.5 MB (5450469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24018d832f265703f38633514569bd5c60bfb9ac7da5098b79023790bfab39d4`  
		Last Modified: Fri, 31 Oct 2025 01:17:04 GMT  
		Size: 9.2 MB (9242594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccea35093260761c96acf871878f36fbe4d86da7dba01b62b31ff28c15001f4`  
		Last Modified: Fri, 31 Oct 2025 01:17:02 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d9ca1587be84efddf00b30977d86ee4ee37de8dbc0e6c1114fc8b8013ecf87`  
		Last Modified: Fri, 31 Oct 2025 01:17:03 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:4490cae34385984dbb1303535a60bb1c2a70779bfd1b12c5275d1631f1447fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b935dfbaa9c199914c24c5227d4ad7808bb30357286a34642e0ff9171f0976`

```dockerfile
```

-	Layers:
	-	`sha256:68248852e45fe0122494b94651e1e68941734567d612157d0cd78bbfa90ffae4`  
		Last Modified: Fri, 31 Oct 2025 02:28:50 GMT  
		Size: 13.8 MB (13828199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f453df5fa1284abfee94d315ca35044f1552e5f8ee37223167b3bade1c0a73`  
		Last Modified: Fri, 31 Oct 2025 02:28:51 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c9f9befb6e8bb5241cace19b3e89bb0a6b516a3bca50290764f0e5a714c40b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284571557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45593d8036df835be60b07572269aa82707e852df1d0ecceab6136fa0f15fcb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:11:25 GMT
ARG version=1.8.0_472.b08-1
# Thu, 06 Nov 2025 22:11:25 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:11:25 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:11:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 06 Nov 2025 23:15:50 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 06 Nov 2025 23:15:54 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 06 Nov 2025 23:15:54 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 06 Nov 2025 23:15:54 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 06 Nov 2025 23:15:54 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 06 Nov 2025 23:15:54 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 06 Nov 2025 23:15:54 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 06 Nov 2025 23:15:54 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 06 Nov 2025 23:15:54 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 06 Nov 2025 23:15:54 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 06 Nov 2025 23:15:54 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 06 Nov 2025 23:15:54 GMT
ARG MAVEN_VERSION=3.9.11
# Thu, 06 Nov 2025 23:15:54 GMT
ARG USER_HOME_DIR=/root
# Thu, 06 Nov 2025 23:15:54 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 06 Nov 2025 23:15:54 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 06 Nov 2025 23:15:54 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d1f499ea2be350aeea557e5a54efc605e09542e2e0eb46c78b5696360c7ce2`  
		Last Modified: Thu, 06 Nov 2025 22:12:07 GMT  
		Size: 118.0 MB (117956781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f52803b412a5845df495a4dd28f2c70a05e39fb7d14804b62a821948ff455d3`  
		Last Modified: Thu, 06 Nov 2025 23:16:35 GMT  
		Size: 91.7 MB (91712072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d47976d9997ce7e51943482c46effab51d2d1d37d783a690bcdecd3c6d2499b`  
		Last Modified: Thu, 06 Nov 2025 23:16:21 GMT  
		Size: 12.8 MB (12757391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6939dd336e0778235382e6dfa545db180904bc8107f96fc28bd13db5f1fc99`  
		Last Modified: Thu, 06 Nov 2025 23:16:20 GMT  
		Size: 9.2 MB (9242585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8305dd5baea3b4c0da6d60dcd98445366970f76668cfabc01d5f58d0c23389`  
		Last Modified: Thu, 06 Nov 2025 23:16:19 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d1c39dcfc69b0155acb656eea5e760c02266af291f50018e79b4cfc316b709`  
		Last Modified: Thu, 06 Nov 2025 23:16:19 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:928aa4b62c0437e669a1f7af8ca1423b75671f7613440753a10617e14d78f6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdd9f8fc854333d6076ad83eca3ee08f73a55f559ae9ca9c82a4389cfd9c939b`

```dockerfile
```

-	Layers:
	-	`sha256:b3eb33fb696059b61587228bf3a921cee202f3c407b6e08167e35e4eb546fda2`  
		Last Modified: Fri, 07 Nov 2025 00:28:41 GMT  
		Size: 6.6 MB (6609530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e17e8e10b85ba4cb12e7abdbb5644f2ae7bf4f58992c370dacb611b9e6e3811`  
		Last Modified: Fri, 07 Nov 2025 00:28:42 GMT  
		Size: 18.4 KB (18429 bytes)  
		MIME: application/vnd.in-toto+json
