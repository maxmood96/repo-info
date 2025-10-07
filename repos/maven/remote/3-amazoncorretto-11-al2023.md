## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:57c61dc2ffb90a6f2cc99c5de4107fbb1e9542c17f7d7ccbfac39e6f211fa7e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:7952ec325d5c709631c10b980ca883b22cf29242447cc8eb6f0c03f707ff5476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.2 MB (319197526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf523f5758d913b0f8d770cef7b2701f03e39ff16fa4b22873bddb025806c59`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=11.0.28.6-1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y openssh-clients # buildkit
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
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bea491ccf4f1cb4479c0d0dd695e9eaea15d1c73558a4e304bd3314fb876293`  
		Last Modified: Mon, 06 Oct 2025 22:11:15 GMT  
		Size: 154.1 MB (154072396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351641ddc0e016d58040e7b0cd36c33f0095b90e7f00064f3dea6485f4120648`  
		Last Modified: Tue, 07 Oct 2025 01:05:45 GMT  
		Size: 89.3 MB (89347082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e791044a2cab37bdd16fc68633b091af9ddef29aa91d4d34127a34c11230639b`  
		Last Modified: Mon, 06 Oct 2025 22:14:37 GMT  
		Size: 12.5 MB (12529277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7f6dda584269651880b9faf1dd89ac5efef3afd25601cf720b662729206a05`  
		Last Modified: Mon, 06 Oct 2025 22:14:35 GMT  
		Size: 9.2 MB (9242596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9742f5610cee4f3b62eb3908e2695b191f1eea439f7bc8e3cda83a8d7a36aa`  
		Last Modified: Mon, 06 Oct 2025 22:14:25 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f429a07adba62207572d7e53761d25ec6ff2eeb6d9c8016969872dce3b71cd24`  
		Last Modified: Mon, 06 Oct 2025 22:14:25 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:05157ed569784d5ed45adc6bafbbefadd379290a55e9da0f0cd06361df59f699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0196cf6cb2f3e26c3efeada2883346e3970ca2b232912ee4ea330c1fa12f6e`

```dockerfile
```

-	Layers:
	-	`sha256:0df00730cc86fe8afc31d8848900d1c5f58519c857ae151c2dbe1bb1a30a7e87`  
		Last Modified: Mon, 06 Oct 2025 23:27:42 GMT  
		Size: 6.3 MB (6257448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70a4b4a63fe5606413c7efcbae651096a394a3994421faa3bd86dd052d0ea5de`  
		Last Modified: Mon, 06 Oct 2025 23:27:43 GMT  
		Size: 18.3 KB (18328 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:731dcd8c90c8366cc7e0a3e6b5f4d2de9cfb8444cad3bda43a3735bf14b6f76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (315955512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89cd7307538526b8f6b7b81650bef70dd27d5548ffdc4f5a43b026a9457adbf`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=11.0.28.6-1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y openssh-clients # buildkit
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
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60693563db8a15ef6cbbb254b5f7cdd25c3f0b7dea83ba28e605d00261462016`  
		Last Modified: Mon, 06 Oct 2025 22:11:35 GMT  
		Size: 152.6 MB (152580439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f241ac0a3a0e970e824efb2296edcc94294abcc1a372d05003883916e4869d`  
		Last Modified: Tue, 07 Oct 2025 01:06:23 GMT  
		Size: 88.5 MB (88458465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46137ba2e10bd7423d4f920c12cbbb5c14e6a7220acb73d9043ea6e5b93fde31`  
		Last Modified: Tue, 07 Oct 2025 01:06:26 GMT  
		Size: 12.8 MB (12781783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8858825d152d8ce751ecf26176e5dc58c374119984af85e7cfa8881c91d02f96`  
		Last Modified: Mon, 06 Oct 2025 23:41:11 GMT  
		Size: 9.2 MB (9242576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9d11ebc4aee848a43c25531c6d05b9139e7585570d9a7f14a007dce0593cdc`  
		Last Modified: Mon, 06 Oct 2025 23:41:10 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4435e499553cd1a99d2b9ef746bad75dafa55e431c203caec2fe0d65429574ed`  
		Last Modified: Mon, 06 Oct 2025 23:41:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:1abc5e7a5074fd164d7695c1b10e242786b5389e3c0b77903b243c1c1955937e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a056c6cf3c54136fb53c61af4ec02b5267999c684b6202359003111e6611010`

```dockerfile
```

-	Layers:
	-	`sha256:aeb8b69f2f3b94ee516d450aa30ed65beae59ccb0c904592283a5e3d21101684`  
		Last Modified: Mon, 06 Oct 2025 23:27:48 GMT  
		Size: 6.3 MB (6257222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:608ac86e79ab5e8504fcf82709ea4d22862393e6e0f53be5f4ba906ea0bcc5f9`  
		Last Modified: Mon, 06 Oct 2025 23:27:49 GMT  
		Size: 18.5 KB (18476 bytes)  
		MIME: application/vnd.in-toto+json
