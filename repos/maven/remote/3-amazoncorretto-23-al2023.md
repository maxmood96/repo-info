## `maven:3-amazoncorretto-23-al2023`

```console
$ docker pull maven@sha256:3e702ca3a4d85f638620796ec66e9b15b66eba36a89104e0a739c7740bd4c23f
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
		Last Modified: Fri, 20 Dec 2024 23:16:23 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9c76488c87a65f1131843f3ec23ab6f92856a47ee33217f309656321ec5d3e`  
		Last Modified: Fri, 20 Dec 2024 23:16:23 GMT  
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
$ docker pull maven@sha256:871d62590f5ef1bc3b5dd3bb00b0a2e5facaf5eb28a8f8a370d443d92091568d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303987921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc5b28585421e3f5a2554c37975bc6d8f2cbc3a1fe70253fb61d06f83da76ee`
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
	-	`sha256:c4986d7f39b7bf5efc7dcb24fad3d45645e69ad032505693865ef726c1550fb5`  
		Last Modified: Sat, 23 Nov 2024 01:38:05 GMT  
		Size: 51.5 MB (51455844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a1a30d671c2eefa174e9ed9df10f3183c4fc537c6c954702f75aa306d4113b`  
		Last Modified: Mon, 02 Dec 2024 23:31:16 GMT  
		Size: 175.5 MB (175499891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97229f4b6af38b9005e5cdf430c7259b437e781af2901b58759783a7989cc38c`  
		Last Modified: Tue, 10 Dec 2024 02:27:09 GMT  
		Size: 67.9 MB (67860717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd83b1f280a4c347d63fb6d3aef2094633cae9ffbe452615a760836189d2bb32`  
		Last Modified: Tue, 10 Dec 2024 02:27:08 GMT  
		Size: 9.2 MB (9170429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88957ff253e4fd4b1e471255fd1600921ca79214e6db82a87b64bf6040a133ea`  
		Last Modified: Tue, 10 Dec 2024 02:27:07 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329c99d56b23b62c3a0f8e2fd8c12406b3e0f26cc84560d807dc5d462672d2ca`  
		Last Modified: Tue, 10 Dec 2024 02:27:07 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:9fa84dcff6e51c17b628cf3c5d5ee642f2753a08b735cc37c0e054310f23a14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6213207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c66d28fb23642cf4004c760f300b781d2394feb91d8eeff48d298390203f2b`

```dockerfile
```

-	Layers:
	-	`sha256:fcb374b4ff0bfabccf0b23ef70ffea70491b6ceb38df2857db43328371023859`  
		Last Modified: Tue, 10 Dec 2024 02:27:21 GMT  
		Size: 6.2 MB (6196697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9301a973e980221f1b41056816618ed4e7a57c277e7e84cf75e3d9b9500f477e`  
		Last Modified: Tue, 10 Dec 2024 02:27:21 GMT  
		Size: 16.5 KB (16510 bytes)  
		MIME: application/vnd.in-toto+json
