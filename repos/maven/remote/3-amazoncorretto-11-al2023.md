## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:28813e8f38028cdc78185cc00dd36bac4c4f52132e1ef30ce7674ae4e7000e29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:c45cc5d7454dd77d3bd0c9444a82f13a2e8d88169f414aca7a9eec6ce2820b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330760144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0699550b9b69ab632d1ad39ac188f469469b44b6a12708879b1e3dd41b22e77b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:49 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:30:59 GMT
ARG version=11.0.30.7-1
# Tue, 10 Feb 2026 18:30:59 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:30:59 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:30:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 17 Feb 2026 22:29:19 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 17 Feb 2026 22:29:21 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 17 Feb 2026 22:29:21 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:29:21 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:29:21 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:29:21 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:29:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:29:21 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:29:21 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:29:21 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:29:21 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:29:21 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:29:21 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:29:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:29:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:29:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3ffbc2e8833044834ccfc60c99f6275f3632718226c6ef0c9706b41890795123`  
		Last Modified: Mon, 09 Feb 2026 18:58:55 GMT  
		Size: 54.0 MB (54038228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4813123a6ec9537c4a8ad81d395a04d6cda2fb38203e651b03c910f6504f12a6`  
		Last Modified: Tue, 10 Feb 2026 18:31:19 GMT  
		Size: 153.4 MB (153363419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72ba1e886773b430f9b68cd6ad58ef1be61c3d914d88e45dfe850eae585e48c`  
		Last Modified: Tue, 17 Feb 2026 22:29:39 GMT  
		Size: 101.5 MB (101546599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb26367ae3d3cae5bb607ac24c129b52e5aa88ea024301a56134dc927e34e62`  
		Last Modified: Tue, 17 Feb 2026 22:29:36 GMT  
		Size: 12.5 MB (12498619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8557e823657d34f25eb7322ace25b06a2e166cc56c11e455aa5067ad94fe24a1`  
		Last Modified: Tue, 17 Feb 2026 22:29:36 GMT  
		Size: 9.3 MB (9312240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23a0839f8c33a90771f579ce5f7ea358b24125c28d15140850d2ae40ff712da`  
		Last Modified: Tue, 17 Feb 2026 22:29:35 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef732c429245045313cbc0d5f81519d0d53c69e6e0f664b69c8e47bfa66b4fe`  
		Last Modified: Tue, 17 Feb 2026 22:29:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:539368cdb76e46e79a346e27792534f042aca91af977c43ee295845f6ca0ea16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111fb84af20825f7d199e8b25b5c6b92877df3c3c596e8208cdf65e9aacfe639`

```dockerfile
```

-	Layers:
	-	`sha256:677375a7de2194f2820bfa07e4f242ed5ac7ae34481eb659778e25700accd244`  
		Last Modified: Tue, 17 Feb 2026 22:29:36 GMT  
		Size: 6.3 MB (6257535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83fe2c4cec007d1e045d1047a698ceb913cb02c2f5adf70d310f892e1b6a7218`  
		Last Modified: Tue, 17 Feb 2026 22:29:36 GMT  
		Size: 18.3 KB (18291 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:efe798be6458816bf23284e31b176cf9beee028c5737b37bb61e5f383b4adbe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.3 MB (327289122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e150e2fd546cda32acef9c4d3a0b2eb499b69cda5aefd328e648589d71e194`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:36 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:36 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:30:51 GMT
ARG version=11.0.30.7-1
# Tue, 10 Feb 2026 18:30:51 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:30:51 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:30:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 17 Feb 2026 22:17:29 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 17 Feb 2026 22:17:32 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 17 Feb 2026 22:17:32 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:17:32 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:17:32 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:17:32 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:17:32 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:17:32 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:17:32 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:17:32 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:17:32 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:17:32 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:17:32 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:17:32 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:17:32 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:17:32 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:72831a4cffd207c00f002b53208af67cc59cf3af51b98b118c11c230a7926a2d`  
		Last Modified: Mon, 09 Feb 2026 20:01:25 GMT  
		Size: 52.9 MB (52918211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe09cbb5e7a2b065a6b8b1308384deff3a73a806922a2cad78f5af69f4a16aff`  
		Last Modified: Tue, 10 Feb 2026 18:31:13 GMT  
		Size: 151.9 MB (151920991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fca1f93dff4083ac940ee1e66e8ce18343e846058b1259eda6b940af4f0f613`  
		Last Modified: Tue, 17 Feb 2026 22:17:50 GMT  
		Size: 100.4 MB (100379405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6558c7a5d8a450363fba33382938a1d3a5dca57f539de784453df4d684e54980`  
		Last Modified: Tue, 17 Feb 2026 22:17:48 GMT  
		Size: 12.8 MB (12757218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f181c646e1fd2b4d6efd6dfa78cfd88f86071c10bf497c2c8a4a15b5c9801cb1`  
		Last Modified: Tue, 17 Feb 2026 22:17:48 GMT  
		Size: 9.3 MB (9312256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490384d0697ac6595723c90c5f88f084edc3850607e06fcf047b821112699749`  
		Last Modified: Tue, 17 Feb 2026 22:17:48 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b95dfcaabb9ee700469421c4a5953c18d6de9a04bfe9fc577059299796b8768`  
		Last Modified: Tue, 17 Feb 2026 22:17:49 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:7e8fe05d2d7e90bff48b1d756fa7257b96da018e905cb449e9c8ba5073803112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef13ce06be158d4d8b7734dbf1c582f5e9322d0cbace5ff56f90b3379cca4683`

```dockerfile
```

-	Layers:
	-	`sha256:c6fc84df2a6b688d0e925bb34adb829863d307cd1dbfd4a9cbbe6d6baf2875ae`  
		Last Modified: Tue, 17 Feb 2026 22:17:48 GMT  
		Size: 6.3 MB (6257309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1670491aee26433dc7152e0caccc85035b377f7ed80ff3559a3b0477e76a8fd5`  
		Last Modified: Tue, 17 Feb 2026 22:17:48 GMT  
		Size: 18.4 KB (18439 bytes)  
		MIME: application/vnd.in-toto+json
