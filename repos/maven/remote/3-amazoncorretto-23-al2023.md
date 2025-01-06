## `maven:3-amazoncorretto-23-al2023`

```console
$ docker pull maven@sha256:cd3f54a508f9ddb03e72705fdceaf2b982712e641711668b67114acab94a0b40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-23-al2023` - linux; amd64

```console
$ docker pull maven@sha256:7468990f442537696d8337a761b309d57c717a96a1a1480068db5101479739df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.1 MB (309114452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc87003927d01f87d9638f9e9bc03d8ea98a88fb2efed5f237a42abb0e0b335`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 19:11:46 GMT
ARG version=23.0.1.8-1
# Mon, 23 Sep 2024 19:11:46 GMT
ARG package_version=1
# Mon, 23 Sep 2024 19:11:46 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
ENV LANG=C.UTF-8
# Mon, 23 Sep 2024 19:11:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Mon, 23 Sep 2024 19:11:46 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 19:11:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 19:11:46 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 19:11:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 19:11:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 19:11:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:351cdd1ae1934b18a2b9071735ba92b02b0a1b8775e2a03f31fdaf06f2fba243`  
		Last Modified: Mon, 16 Dec 2024 23:59:50 GMT  
		Size: 53.2 MB (53156313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e3ad49c8506e0d302aebee4fb134ecf63af597150b3973092be755c3ef985d`  
		Last Modified: Fri, 20 Dec 2024 22:33:35 GMT  
		Size: 177.6 MB (177569435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a4aff6c13e28512f61435b4fcb3797e11ab2728b17f309710b706bd1ac2b5c`  
		Last Modified: Fri, 20 Dec 2024 23:16:24 GMT  
		Size: 69.2 MB (69217223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6262f8707fd946614e1658ff1567d6dfddb27b94b07738ef336d3c00ae6a5c8b`  
		Last Modified: Fri, 20 Dec 2024 23:16:23 GMT  
		Size: 9.2 MB (9170436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d477c5597263eb11b92cbee669731424dd636ac9f79f49a97c23e0e7df1b0361`  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9c76488c87a65f1131843f3ec23ab6f92856a47ee33217f309656321ec5d3e`  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:ba3de00177275b2a6126eff812bed8aac02a8382c790148e303cf8acaf1bfa7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6206524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059df1724a3808646d751db540eb320d9c58b9fb1f83e80e1afa2ee6045619f6`

```dockerfile
```

-	Layers:
	-	`sha256:e26b44db77423956917508e2e07e8f7ec02515f2ff899c14753ee317cf59bdd1`  
		Last Modified: Fri, 20 Dec 2024 23:16:23 GMT  
		Size: 6.2 MB (6190147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:080156b6fafb6448aa750b7c0f1721b88b8274497ac576948419598470b845ae`  
		Last Modified: Fri, 20 Dec 2024 23:16:23 GMT  
		Size: 16.4 KB (16377 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-23-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f801ce74acfc91be2f99bbef7c52aa141dc966f60e31f4fe68052168c05c252c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305862845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2408c243bbce7c0f36c61a374c5990dc648334c9588d13ecc75492ff18575258`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 19:11:46 GMT
ARG version=23.0.1.8-1
# Mon, 23 Sep 2024 19:11:46 GMT
ARG package_version=1
# Mon, 23 Sep 2024 19:11:46 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
ENV LANG=C.UTF-8
# Mon, 23 Sep 2024 19:11:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Mon, 23 Sep 2024 19:11:46 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 19:11:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 19:11:46 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 19:11:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 19:11:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 19:11:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:98ab3ce9b55607064b358289eeb810db43f69e016067c07e7136a807475f6f27`  
		Last Modified: Tue, 17 Dec 2024 02:01:08 GMT  
		Size: 52.3 MB (52276382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0114ad8310150fa45d13980dac0fd19302899e1c1faeb8bc711ed49da79822fe`  
		Last Modified: Sat, 21 Dec 2024 01:52:55 GMT  
		Size: 175.5 MB (175542653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34612bc713e77ec9fcd0ea0b1808cc4cd67fdd5a11e46bfee177d4a25d5c43d4`  
		Size: 68.9 MB (68872322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd034cf00f16a88e7c7168a4f57ffdb1005574a280f5a6c3aef1d42217908a1`  
		Last Modified: Sat, 21 Dec 2024 04:58:56 GMT  
		Size: 9.2 MB (9170444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679a1e1e60c69a1507eeaeb14926e12d7680da4c674ec228bb54a0c8a48856e6`  
		Last Modified: Sat, 21 Dec 2024 04:58:55 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8208e0dad8bcd96ac0f9fa8567b0a6a52d1215c02bc7cfc041749f3ff2c59641`  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:90e8a391310d99c86ff35e11312083404058bb1024a2e0180b7351c6723622cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6204777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b0dcb2d171eba795349f7a891952dbfb84b3e5be2006a561913f296211dd4e`

```dockerfile
```

-	Layers:
	-	`sha256:52d88e54b3269e36f9b45b7607d731034baea77890ed4b81776c240ab3481d1e`  
		Last Modified: Sat, 21 Dec 2024 04:59:09 GMT  
		Size: 6.2 MB (6188267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db65fe1683edbf060ab6e254acebcdff742c19f581b2fe16b1be4174a14bfb65`  
		Last Modified: Sat, 21 Dec 2024 04:59:09 GMT  
		Size: 16.5 KB (16510 bytes)  
		MIME: application/vnd.in-toto+json
