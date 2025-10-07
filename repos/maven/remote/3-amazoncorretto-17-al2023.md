## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:cf214c13b05e2a529aa781103d25e3e50766b790a561c1373f3409896af9caf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:b7ba1186501e08fb209042b867f53f8e60de056d16475cb9b3b2d68c8b57790b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.9 MB (321921482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dc9cd0f10a374c4a979d2883193d6a544c07dea9a12ed83e08ca1dc55624b3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=17.0.16.8-1
# Wed, 16 Jul 2025 06:51:38 GMT
ARG package_version=1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:066436e61e3d33b0cc28ae048efed629a64fe7d3e632846048aefbb83ad50fa0`  
		Last Modified: Mon, 06 Oct 2025 22:10:53 GMT  
		Size: 156.8 MB (156803165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca04db50aef049de53275f0c38c0e296d6afd4ddb7ecf670d25ffec8187e9647`  
		Last Modified: Mon, 06 Oct 2025 22:14:34 GMT  
		Size: 89.3 MB (89344212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1883b06a52d7b1da0c1859bb853ce26abe832118cd42cc1428ad4267b2066ad`  
		Last Modified: Mon, 06 Oct 2025 22:14:25 GMT  
		Size: 12.5 MB (12525338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57dfa88e66f6de21a97bf5e91f9441c1200bb8a5de843ae59a83b569054fd40`  
		Last Modified: Mon, 06 Oct 2025 22:14:25 GMT  
		Size: 9.2 MB (9242593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba94f05271e4a39e85f964ba6e8a279fd1e085210387c29f4a218b613ee4c3e9`  
		Last Modified: Mon, 06 Oct 2025 22:14:24 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72350618bb1884b5395295c2ef36fbaa8b4de2879c1956f25dbac43482aff04a`  
		Last Modified: Mon, 06 Oct 2025 22:14:24 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:851f4b51f03e2dd8262cba7ed88858b5ae591c9925b2d0e5576c3d41d077b280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd06149c7284eece90b9c7bb9e5886f1ffd35e06417d3a9c933270454483650a`

```dockerfile
```

-	Layers:
	-	`sha256:3ede374bd0737d8a2b999eb082ef85ac251fcd3bd5b68a0d21611b3692002f84`  
		Last Modified: Mon, 06 Oct 2025 23:28:00 GMT  
		Size: 6.2 MB (6231938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65f0efa612e9185a45bb2b924f6e4e118a0c2de22f4b0c2e17c0de39b70a00d1`  
		Last Modified: Mon, 06 Oct 2025 23:28:01 GMT  
		Size: 18.3 KB (18328 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:83f8b0b996c636da08f02715b657bf63cefe3d580b4ed619842dd8caa1e20a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (318968126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed553bc37ff6363cf49374b6bdb4897546af3d4c19e56b0fcfb3ed3f6849958`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=17.0.16.8-1
# Wed, 16 Jul 2025 06:51:38 GMT
ARG package_version=1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:ccd616be23263ff6adc68def052eb1d74774c33ddd8df1898b4198f35efac337`  
		Last Modified: Mon, 06 Oct 2025 22:10:49 GMT  
		Size: 155.6 MB (155594469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f38d8287a2a1db2a4d797dd1f31b8cfcaa300606b10e1a1c4c9c48edb515b4`  
		Last Modified: Mon, 06 Oct 2025 22:15:23 GMT  
		Size: 88.5 MB (88457446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da75cd49b8b190ef7c86a0d1c36431ca3ad45ad80e99751491a5930b5d0a902`  
		Last Modified: Mon, 06 Oct 2025 22:15:05 GMT  
		Size: 12.8 MB (12781380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f39195b0e767f1d50bbd7dd6ce3effd599ed4c25fd15644fca9acdd67ef4059`  
		Last Modified: Mon, 06 Oct 2025 22:15:05 GMT  
		Size: 9.2 MB (9242583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a8a5fc5b31451318c6a2b32e156c4dfeccfead6a8f7553e026313bc1d69857`  
		Last Modified: Mon, 06 Oct 2025 22:15:02 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ecfbffd626885097d1333489807638726306facb3397fef47903369ab08f8e`  
		Last Modified: Mon, 06 Oct 2025 22:15:02 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:4f097b44f459d1d9a9149ff36d44937e99b99d3f86ac2b256d6f02f4db24bf13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6249344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6660ec2ec581961507ed6bbc2bff1239ca1ef3a377407351b4f799ecff2ac521`

```dockerfile
```

-	Layers:
	-	`sha256:81597486490b0933ab256819adb8f6b6dfc29b940dc8f4f6e14d87b7f999689c`  
		Last Modified: Mon, 06 Oct 2025 23:28:06 GMT  
		Size: 6.2 MB (6230868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f6805f48eab392b541692d3f048efbda2ea37b17f2a231bff66ffe5e2fba800`  
		Last Modified: Mon, 06 Oct 2025 23:28:07 GMT  
		Size: 18.5 KB (18476 bytes)  
		MIME: application/vnd.in-toto+json
