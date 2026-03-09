## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:494dc4d8d2d3393df0a7f499b4441b4307e423f407d6097b953aa02494aaf262
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:e0b3211f05785bb74544856cc30ed27192387125ed54c2e0bac7e528f41a4306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.3 MB (336309920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86cdd83513bfe78239abe783ac42d310b5baba1ddf3e5df12e6d4ef49c95e07d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:01 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:13:35 GMT
ARG version=17.0.18.9-1
# Mon, 02 Mar 2026 23:13:35 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:13:35 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:13:35 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:13:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 09 Mar 2026 19:13:57 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 09 Mar 2026 19:14:00 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 09 Mar 2026 19:14:00 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:14:00 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:00 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:00 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:14:00 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:14:00 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:14:00 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:14:00 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:14:00 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:14:00 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:14:00 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:14:00 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:14:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:14:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2584a8e504dfaf493eadaafafbabd8b97f7cb5bbe3cb6a319fb37cf3c4335d86`  
		Last Modified: Thu, 19 Feb 2026 02:57:43 GMT  
		Size: 54.0 MB (54032840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291656abe10718a5b7ecb3affcd502d6d49aac432bab42c4affe10d8907b4b47`  
		Last Modified: Mon, 02 Mar 2026 23:13:54 GMT  
		Size: 156.9 MB (156911090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0c336b1932f12daf336711729b8f6235d01c527980f9cf49a13bf69c80666c`  
		Last Modified: Mon, 09 Mar 2026 19:14:19 GMT  
		Size: 103.1 MB (103138611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2bdb33562cba4733f528d29f0eeebe112af64b3212193ab455840134b914a3`  
		Last Modified: Mon, 09 Mar 2026 19:14:17 GMT  
		Size: 12.5 MB (12528815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18941a240a47cf6cd52cb4af32122687938ae4a719795b29b236384975c5d5c`  
		Last Modified: Mon, 09 Mar 2026 19:14:16 GMT  
		Size: 9.7 MB (9697523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1c3927cfba79d6688fb9b42e61bd32579d9488dec7f1993d9695dfc0aa71a`  
		Last Modified: Mon, 09 Mar 2026 19:14:16 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f083de9940134933f1b7906723ccf3c31cdc0bc405de296157387858ed1f9a05`  
		Last Modified: Mon, 09 Mar 2026 19:14:17 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:5df3b545184c9651b4ab0f10c99f66242aca120b1cfa55dbec84b437b74dac37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6256863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6a0f852290e298ad1328dc52c6b7a0952df5c531519fc6a756837bb578c695`

```dockerfile
```

-	Layers:
	-	`sha256:ae1181e44793c97868c55e934c1aa772e1d222376c7bbd602cdfd49f8e7395c3`  
		Last Modified: Mon, 09 Mar 2026 19:14:17 GMT  
		Size: 6.2 MB (6238572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d530d6e6eaf525ba56934343d318f2ed48195ffa39f080552bc44e88fe41a17`  
		Last Modified: Mon, 09 Mar 2026 19:14:16 GMT  
		Size: 18.3 KB (18291 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:21f9c51c1d629e286b1b5307f6ea8a06c9418cb98d904c9a44896e0f0adcac4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.0 MB (333014914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1863273b0d21a9627df950a0dc4eb17b4c53be018159660b4085956e44f86ba7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:04 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:14:40 GMT
ARG version=17.0.18.9-1
# Mon, 02 Mar 2026 23:14:40 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:14:40 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:14:40 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:14:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 09 Mar 2026 19:13:40 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 09 Mar 2026 19:13:43 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 09 Mar 2026 19:13:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:13:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:13:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:13:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:13:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:13:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:13:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:13:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:13:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:13:44 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:13:44 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:13:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:13:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:13:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9330fae67a20d9aa2569828674140d8b67d50cfd127cb99ba0f9be275d35f976`  
		Last Modified: Thu, 19 Feb 2026 02:57:42 GMT  
		Size: 52.9 MB (52941319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458a2c883ef0e813dd59cc98f7ab9fa2c67d320d0117be74523be410b68ca3ed`  
		Last Modified: Mon, 02 Mar 2026 23:15:03 GMT  
		Size: 155.7 MB (155727670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9902b9eb67498c1ea2dc0b63588271410a2f6f82a9a6713f9712f22085ad197b`  
		Last Modified: Mon, 09 Mar 2026 19:14:03 GMT  
		Size: 101.9 MB (101857997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789d2dba229d05bb53ea1e3ae1b6f94183208e008f9c1ef2cb19c256660777b4`  
		Last Modified: Mon, 09 Mar 2026 19:14:01 GMT  
		Size: 12.8 MB (12789333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dc26faf74e78c0d4043f88d2299e2143517911c69f8784e9ea21453e20b62b`  
		Last Modified: Mon, 09 Mar 2026 19:14:01 GMT  
		Size: 9.7 MB (9697557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1387b899d102a3f79bc2a61b2dcd27a0f1477aad32544f311fcef34eb64fc6`  
		Last Modified: Mon, 09 Mar 2026 19:14:00 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81676ed236286285a1e96702a582d36436e29b67e0d728a595de04e93f409e0a`  
		Last Modified: Mon, 09 Mar 2026 19:14:01 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:5d10c4dc32e70310d55037656e493f6e09cd9937f19a8b7ce90fc06758279c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931f676115197b7423325ecc01a3e7224b069977d1d7420da80678bca1331a1d`

```dockerfile
```

-	Layers:
	-	`sha256:792887a84670197ad55697c425b1e80b1bf51853faacfafd6ab2646318e90e29`  
		Last Modified: Mon, 09 Mar 2026 19:14:00 GMT  
		Size: 6.2 MB (6237502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee41fb816fe498fd3c49017562599181c1752ba1b1cdefb4d41391d58fedaa0`  
		Last Modified: Mon, 09 Mar 2026 19:14:00 GMT  
		Size: 18.4 KB (18439 bytes)  
		MIME: application/vnd.in-toto+json
