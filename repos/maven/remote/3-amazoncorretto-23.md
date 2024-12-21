## `maven:3-amazoncorretto-23`

```console
$ docker pull maven@sha256:7e9282d5cc2373ce7c88497afa61108a480023d9e5a18eec05cf77d0c364d6b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-23` - linux; amd64

```console
$ docker pull maven@sha256:82aa77a83824e4b92cc5ba14f691a00f6db5cda012a3c327baa89f7ca8d62fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.1 MB (309114166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7fd45ad41688ecd8ea38b4b242c8ca3d3cfe3fe153626214fc75b5fe8ed94e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 17:02:08 GMT
ARG version=23.0.1.8-1
# Mon, 23 Sep 2024 17:02:08 GMT
ARG package_version=1
# Mon, 23 Sep 2024 17:02:08 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENV LANG=C.UTF-8
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Mon, 23 Sep 2024 17:02:08 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
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
	-	`sha256:e8845fe6f56e8f6a52991073be25334dbc98c26eeb8a6463da76b5947acae6ad`  
		Last Modified: Fri, 20 Dec 2024 23:16:21 GMT  
		Size: 69.2 MB (69216937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee180755ae595e24d43116e39de679a226faa5eadd8ef96c8c887a2a1d90aafd`  
		Last Modified: Fri, 20 Dec 2024 23:16:20 GMT  
		Size: 9.2 MB (9170436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75d28266ae1bdb30e64847af6579173b602ea9cff29bf83d098284cf6d95989`  
		Last Modified: Fri, 20 Dec 2024 23:16:20 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249c8b070c6bf369c82c853b3106413015c2bff75534bcd8e60edbb14b0f0132`  
		Last Modified: Fri, 20 Dec 2024 23:16:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23` - unknown; unknown

```console
$ docker pull maven@sha256:a2762b767fefd688cf24ad00f1d42750c6b99e03d4c7fe60b0c88cf55e4bd0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6206411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b45e918cf88747a784bd035d79c440964eb25d60d57f460b92d0e15a7037dc3`

```dockerfile
```

-	Layers:
	-	`sha256:afa59b809527daed6195285cfb50cd48a4af7dcbd648f09631f954f754f2737e`  
		Last Modified: Fri, 20 Dec 2024 23:16:20 GMT  
		Size: 6.2 MB (6190105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:846af38ad7874a216ed7908bbc310d73b2eec7ebbf1a5b1c29c1c367fd0094e2`  
		Last Modified: Fri, 20 Dec 2024 23:16:20 GMT  
		Size: 16.3 KB (16306 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-23` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:52d4c823c761206d9e830ae12268a07f71b2b6b7b247002ab7a12dcda2b00479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303987921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75a7588ab52f392710398865840b4acf72a1b23bca19a8ce24d1bf46cd57aa4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 17:02:08 GMT
ARG version=23.0.1.8-1
# Mon, 23 Sep 2024 17:02:08 GMT
ARG package_version=1
# Mon, 23 Sep 2024 17:02:08 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ENV LANG=C.UTF-8
# Mon, 23 Sep 2024 17:02:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Mon, 23 Sep 2024 17:02:08 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 17:02:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 17:02:08 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 17:02:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 17:02:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 17:02:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 17:02:08 GMT
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

### `maven:3-amazoncorretto-23` - unknown; unknown

```console
$ docker pull maven@sha256:a6e088531c3e1088b7e727ce7743b8f06de4344f2e475f1bd665d1054959d0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6213094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b5ed47f837ce1eb083e8ddd26c551ef0bc85abdf00204b238c2c7cfff831c8`

```dockerfile
```

-	Layers:
	-	`sha256:7cda06d2093cf595ffdb6d5bb9171cb097994e17fed2229beb22b2a36f703e8e`  
		Last Modified: Tue, 10 Dec 2024 02:27:08 GMT  
		Size: 6.2 MB (6196655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae24dda69d36f4893e08d8aefe5b3ca7267780ae076a4ed8bc8490b7914b9d69`  
		Last Modified: Tue, 10 Dec 2024 02:27:07 GMT  
		Size: 16.4 KB (16439 bytes)  
		MIME: application/vnd.in-toto+json
