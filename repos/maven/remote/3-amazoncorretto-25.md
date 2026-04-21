## `maven:3-amazoncorretto-25`

```console
$ docker pull maven@sha256:372ba8608e119bf241223032ee1f197bbd3f0085fadd108ac9fea484bb1a630d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25` - linux; amd64

```console
$ docker pull maven@sha256:5d697874b99aa0877c5da57c37664957a003d6cd7b5ecf4ab786a7fbf576a422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.9 MB (371928745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74a129717ab8f86f04e748ba78c82deb1df6a861ad3ac1c9284e9a315f432d3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:26:44 GMT
ARG version=25.0.2.10-1
# Wed, 15 Apr 2026 21:26:44 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:26:44 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:26:44 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:26:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 21 Apr 2026 18:12:20 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 21 Apr 2026 18:12:20 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:12:20 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:20 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:20 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:12:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:12:20 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:12:20 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:12:20 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:12:20 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:12:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:12:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:12:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1ea217645c100a6a722630601c1c84cdadb45351d90b7a9d6e48270865321b`  
		Last Modified: Wed, 15 Apr 2026 21:27:09 GMT  
		Size: 189.2 MB (189188253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62724fe263f74137182c220e29b8fbb15264d7db2fd92486ea006950abbb0dfd`  
		Last Modified: Tue, 21 Apr 2026 18:12:41 GMT  
		Size: 118.9 MB (118856028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a40b9c5cceb716af50d2b599e8ebc877335bf1f643f27f1726e4b202493b25`  
		Last Modified: Tue, 21 Apr 2026 18:12:38 GMT  
		Size: 9.3 MB (9312201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32d3bd21ac0d25fcc6d5bb66e3bfb2d71d87bd93afd68e9f02bae825494848`  
		Last Modified: Tue, 21 Apr 2026 18:12:38 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc86fc00d37333357c1b896530cd60d47418b7e6c1b13f75c902bf43267e8b6`  
		Last Modified: Tue, 21 Apr 2026 18:12:38 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25` - unknown; unknown

```console
$ docker pull maven@sha256:23890fac51a72ac13f7c250ad7674a9bb73c3fdcb516784e6fe5d3b83445ae16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6231168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2490083a7b0089b77f0176d828facb0db1d71d881a01fceb6b9d0b8a79231f`

```dockerfile
```

-	Layers:
	-	`sha256:ee66879cc484e4fc15f43ecbd9e47de9155f51fcc62dfcd750eda0d1cc5f864c`  
		Last Modified: Tue, 21 Apr 2026 18:12:38 GMT  
		Size: 6.2 MB (6215459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f76a677a9c03410a792ffd5f0e5b77fc34a615e4000482b7168431c5f718b134`  
		Last Modified: Tue, 21 Apr 2026 18:12:38 GMT  
		Size: 15.7 KB (15709 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e2dec863dbe884142087506e831683278cf2bcf17709d7660c9cbab9444515ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367837735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cee15f61ed27a83fd4881e3ff017c5e9b8d467fd9ff5d06f5b7375f8510901e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:39:50 GMT
ARG version=25.0.2.10-1
# Wed, 15 Apr 2026 21:39:50 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:39:50 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:39:50 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:39:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 21 Apr 2026 18:12:14 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 21 Apr 2026 18:12:14 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:12:14 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:14 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:14 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:12:14 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:12:14 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:12:14 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:12:14 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:12:14 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:12:14 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:12:14 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:12:14 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e5eaff5c173c2d572c7ece0a4ad5d4ba6d11aa38fa3b123836e74ff874e0f`  
		Last Modified: Wed, 15 Apr 2026 21:40:18 GMT  
		Size: 187.1 MB (187089832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399ddfd317937ebc8c7accf6bb2a09813aa59d18f560ca05653baa171735b794`  
		Last Modified: Tue, 21 Apr 2026 18:12:36 GMT  
		Size: 118.0 MB (117991903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbf477dc051045f67294767e270b0ad5c8b82f52c5ca29dcc4a5fbf45d0589c`  
		Last Modified: Tue, 21 Apr 2026 18:12:32 GMT  
		Size: 9.3 MB (9312254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b41f6f726333d87c339577ae4fbfe530574dd304da1c24ba5e1d3d3242c419`  
		Last Modified: Tue, 21 Apr 2026 18:12:32 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764537f17bf2edd3a3eab22ccefe9b7083cb723fc1fc01c7b97d2bc0f552905c`  
		Last Modified: Tue, 21 Apr 2026 18:12:31 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25` - unknown; unknown

```console
$ docker pull maven@sha256:24ecad55d25bf2ea39ec93a5b2cdd9981f20492f98fb954ceef443c98ae8a2b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6230341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124f7cfc391af95e893a6cc24dfecdd12256df59fa2eb8e536157ee01ad27491`

```dockerfile
```

-	Layers:
	-	`sha256:a7eba7967ca3f3e7e413aa48306cab333ab95bd9935af3fd1de605cf056a70ab`  
		Last Modified: Tue, 21 Apr 2026 18:12:32 GMT  
		Size: 6.2 MB (6214451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfcf1c0a2f3f4b280b7e2c1cee81c5163d15c36cedf47eacbfdc1041fe341d63`  
		Last Modified: Tue, 21 Apr 2026 18:12:32 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json
