## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:d07e29323836507efd1c05eaae5114101386abd48c768d5b3ea34389f4555eb8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:b1ea953ad6f20ef58e992402feeedfaa459bc97b9fa359dc370f1bed9912ed3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384460794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70f7e994049e48acd2f7897d55b1ec54af6074567883c43a833a2c6d843e61d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 30 May 2026 00:26:56 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:26:56 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:51 GMT
ARG version=25.0.3.9-1
# Sat, 30 May 2026 01:12:51 GMT
ARG package_version=1
# Sat, 30 May 2026 01:12:51 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:12:51 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 02 Jun 2026 10:26:49 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 02 Jun 2026 10:26:49 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:26:49 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:26:49 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:26:49 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:26:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:26:49 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:26:49 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:26:49 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:26:49 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:26:49 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:26:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:26:49 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ba643eb28fc9c4131e00c61b5afb90ae7a75af1859c82faa13932360f5c05d`  
		Last Modified: Sat, 30 May 2026 01:13:15 GMT  
		Size: 189.4 MB (189412862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b968c9c99cd68edbf8534e935fbbafe40034428910ee94bd4c51a3462dbc94aa`  
		Last Modified: Tue, 02 Jun 2026 10:27:09 GMT  
		Size: 131.1 MB (131115811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9ba491522a90be1872842abbcc302f74556e93bab855c92d349fc186d57d07`  
		Last Modified: Tue, 02 Jun 2026 10:27:06 GMT  
		Size: 9.4 MB (9359958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d180856281e2fe189d35e0d84272746a72ca18bcfeb005f0942148f7f69b8c`  
		Last Modified: Tue, 02 Jun 2026 10:27:06 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e9160bf0cf40718fc29eb858e0b61b055d5e67eceb32ce68a200fadd0cb2b8`  
		Last Modified: Tue, 02 Jun 2026 10:27:06 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:df9e770b0b986a244166e02cc95fc3c7a59bdd6436679c57fb633b39167d40ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6231981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb6eb18088d6b2d451e6caefc235ee9e20b5fea6a47d2e0088760d32450f785`

```dockerfile
```

-	Layers:
	-	`sha256:6a5eab25ddc44b1ce8244f84bfe84f49807c140c3f2019bcbb1d62b8e8413364`  
		Last Modified: Tue, 02 Jun 2026 10:27:06 GMT  
		Size: 6.2 MB (6216271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:891b32ea130746d3c39d66cd5adaed24b149dba01b4496e1a8f01060912134fb`  
		Last Modified: Tue, 02 Jun 2026 10:27:06 GMT  
		Size: 15.7 KB (15710 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:50e05098e7bf448b26e1052c4296beb183d694d2986af93d3876d03b0ab16358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 MB (380178723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090b390d49453df335a6b5853cbb3537b71ae5932221d5948e24502bf9f336c0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:37 GMT
ARG version=25.0.3.9-1
# Sat, 30 May 2026 01:12:37 GMT
ARG package_version=1
# Sat, 30 May 2026 01:12:37 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:12:37 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 02 Jun 2026 10:24:01 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 02 Jun 2026 10:24:01 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:24:01 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:24:01 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:24:01 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:24:01 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:24:01 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:24:01 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:24:01 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:24:01 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:24:01 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:24:01 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:24:01 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e414a9bc884c1212e04d64b8c9b4918d7362ecf315931f7c7483992d4894a4`  
		Last Modified: Sat, 30 May 2026 01:13:03 GMT  
		Size: 187.3 MB (187327339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17aa9483a3ea88a6a34331c0d823c6cda04eba971d67e4e8a24cc835434e137a`  
		Last Modified: Tue, 02 Jun 2026 10:24:21 GMT  
		Size: 130.0 MB (130032588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c3393ccb38e21cd3dcb76d96edf51924de9cf4667e836eb520157190d59d98`  
		Last Modified: Tue, 02 Jun 2026 10:24:19 GMT  
		Size: 9.4 MB (9359960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181f5cfb4ea7483f78544a9e3a639e397df026b2e05b366ef43ff51c25197309`  
		Last Modified: Tue, 02 Jun 2026 10:24:18 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baea07b4dab37de434f789d9acc76a2eeefc667bf6c492284f6c6dcc428bbf7b`  
		Last Modified: Tue, 02 Jun 2026 10:24:18 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:d25e3b5ca0df7e78b04eed6b479b760700f190f07bbd86830de5d454f4cb3c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6231155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af9f5d0e87d0b914c83a7c0d2452545e420b3dc12fb19f223a84ec862f82c4e`

```dockerfile
```

-	Layers:
	-	`sha256:25dbaad999b429e8cad1c997c3ef49b1ebc0231aad2ea6839e8b69370ffc2f1a`  
		Last Modified: Tue, 02 Jun 2026 10:24:19 GMT  
		Size: 6.2 MB (6215264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cc69b13a9eaa6cf6b0d2f7e2c36f59d763aa774bd8ca2f119e3f0bb35955944`  
		Last Modified: Tue, 02 Jun 2026 10:24:18 GMT  
		Size: 15.9 KB (15891 bytes)  
		MIME: application/vnd.in-toto+json
