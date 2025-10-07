## `maven:3-amazoncorretto-21-al2023`

```console
$ docker pull maven@sha256:74ea4e4f7396962bd2eb3411da0927f1d447b824edd7ac02581af6f3f0d63d40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-al2023` - linux; amd64

```console
$ docker pull maven@sha256:5b0b4878f7026ca2fb4660fe67921e010c26041f94bdc9dbc87cbfcdf134be6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.2 MB (335230460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ecd9f383b301b200d921e02672a1979c5460b5209aeec6afd0e7ce0887ffd8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=21.0.8.9-1
# Wed, 16 Jul 2025 06:51:38 GMT
ARG package_version=1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:35ab0f5daa9757c219d957de4bc99df722590984a8d297992d157eb4f728e8d5`  
		Last Modified: Mon, 06 Oct 2025 22:10:33 GMT  
		Size: 170.1 MB (170110963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b1e226d8f3b4556eeafd1da94f680593cdf4d10f275ac68d784d0b61f4b01`  
		Last Modified: Mon, 06 Oct 2025 22:15:13 GMT  
		Size: 89.3 MB (89344348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dc6045393bf7852d5219a2e327ad2d59329cffdb59ec1e05407e15625fc5d5`  
		Last Modified: Mon, 06 Oct 2025 22:15:03 GMT  
		Size: 12.5 MB (12526391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ff684156a975d42b5227c30d3795e56c8da0e92ecc8bacc2fb97aa8d4baeca`  
		Last Modified: Mon, 06 Oct 2025 22:15:03 GMT  
		Size: 9.2 MB (9242585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3ac4e7e162e21d375e23b00c8298d2fae175e0d7f5a61f008e18a75f021c7c`  
		Last Modified: Mon, 06 Oct 2025 22:15:02 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639abb97af154da0abc55c0c93862df72efaec50b50df1d59cdecbcb3183fd6`  
		Last Modified: Mon, 06 Oct 2025 22:15:02 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:a547efee0d11cfc360548d7778eb79c9aad5a8905c1296ef9fe7e38c3dc1f70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6252680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c0fbef060d5d4b7414fcd94c924ef47b4b44b3ca8cbc765c5064a0d93764af`

```dockerfile
```

-	Layers:
	-	`sha256:05922f39a97d09d58a521d69c57f2718a20289c3b1c4793dac146e305f94fd37`  
		Last Modified: Mon, 06 Oct 2025 23:28:23 GMT  
		Size: 6.2 MB (6234352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47af99c9f00b461f322767f0084ff36e7ed37f2d573b3ea9d821e03b25ffa0e5`  
		Last Modified: Mon, 06 Oct 2025 23:28:23 GMT  
		Size: 18.3 KB (18328 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:aeafaf31a2821f6fbc16fd0ef8c6aec9ebc03829f1addaf9b7ecf6299fd6098a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331776833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b247dfe25ab032e975e5a74ae033e08fd4c333412cce1f525264ccc9e9a901`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=21.0.8.9-1
# Wed, 16 Jul 2025 06:51:38 GMT
ARG package_version=1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:834a85f06ef857b766214cfb56d85c0c3442badc2e54384823cb952324d49130`  
		Last Modified: Mon, 06 Oct 2025 22:11:08 GMT  
		Size: 168.4 MB (168403112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4078685cb44deeede5fdca3e09f4335007632957a2bbb6a33c52de8b4522881f`  
		Last Modified: Mon, 06 Oct 2025 22:15:40 GMT  
		Size: 88.5 MB (88457774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c29c6ef3a076ac604c43a981085d97ab77b83916c5d5986b8226bb6e41d9ce`  
		Last Modified: Mon, 06 Oct 2025 22:15:20 GMT  
		Size: 12.8 MB (12781124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336b7d6a8d3d3d85912228b020a5221a7d46d2697ba468a853fe1d95fcf42cc6`  
		Last Modified: Mon, 06 Oct 2025 22:15:19 GMT  
		Size: 9.2 MB (9242576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d889799c6a1955e688c7a2cdca34746131a7c29b559a0ea513be551c732b417`  
		Last Modified: Mon, 06 Oct 2025 22:15:17 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e60f2e70db582bcc53e3dda14d28d3312baee2e1ab1c18f58815f2a010aaa83`  
		Last Modified: Mon, 06 Oct 2025 22:15:17 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:596ee6a40a6a9519233a122de1937e737a447af8a1f3ab3bd79cb957d4f6613b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20041846695368f57bb5d6363ccb461859789a2fdc090f62e0f200d7d35de9d8`

```dockerfile
```

-	Layers:
	-	`sha256:defe4658ef5a68ad9afa0a4bbc863ab8fa94d96af5298491c5f6a5996c8c0c2b`  
		Last Modified: Mon, 06 Oct 2025 23:28:28 GMT  
		Size: 6.2 MB (6233285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f4e6d891c4c00fd38fa285fc03cb49245ae1adab6d5fc7611d221014149abbb`  
		Last Modified: Mon, 06 Oct 2025 23:28:29 GMT  
		Size: 18.5 KB (18475 bytes)  
		MIME: application/vnd.in-toto+json
