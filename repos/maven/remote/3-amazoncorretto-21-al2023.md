## `maven:3-amazoncorretto-21-al2023`

```console
$ docker pull maven@sha256:ac92284fb0792489e100f544279d44a5e9e63ddab67e61b9a61b4051b8131e46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-al2023` - linux; amd64

```console
$ docker pull maven@sha256:3e07010ccf66f12e3cae880569b569862f88ae2777fec26e970e5534cec6217f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 MB (282153163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d86f4c7752a63b334a1527729414c6925613302e6e345a517dd9caba54e44d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY dir:1c9e0f4db95e1ae683b8f16b1ecfc5d8693ad4e5e379a2386e2870f38383c7d8 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=21.0.3.9-1
# Thu, 27 Jun 2024 09:17:07 GMT
ARG package_version=1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: package_version=1 version=21.0.3.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 27 Jun 2024 09:17:07 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:860904071dc658e37de73aa1556e7badfb13bef4747965ea3bd1049e8ff87dcd`  
		Last Modified: Thu, 04 Jul 2024 00:20:13 GMT  
		Size: 52.3 MB (52319623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6418bb5f0190e1a1054e3d9dcb9b21f182099d39e233a713048c39993e51b824`  
		Last Modified: Thu, 04 Jul 2024 00:47:20 GMT  
		Size: 170.7 MB (170662358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853c2aa06eda81947e5582131d48214009031f888f69f65a0329a346f08b64a7`  
		Last Modified: Thu, 04 Jul 2024 01:49:50 GMT  
		Size: 50.0 MB (50008323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5654b97830b0cd4406d5d4296e4deaf7428a0afd29dcc86c02584d3677092f6f`  
		Last Modified: Thu, 04 Jul 2024 01:49:50 GMT  
		Size: 9.2 MB (9161815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e37880b42f0d136070f87de42a5111f72e7a11af6fd75f59e98783f96e3fd3`  
		Last Modified: Thu, 04 Jul 2024 01:49:50 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cd7aff64b3c88ef5e822ba0fd67d0ad960fb71d65cfc727a3a05b094ab643c`  
		Last Modified: Thu, 04 Jul 2024 01:49:51 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:a25a5ef1fce2db20d6c8c317b2f74f0815c0734430e324e9722a6948a28c6c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5452025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:398f38de2a0248e158d8a2112a5fab9b4a918d0e7598f96cfd5eb2ebe8112dfc`

```dockerfile
```

-	Layers:
	-	`sha256:0f945b9bf93a5010cb3ebb6cd7f53a91fc0fdbf6670596721529a2bbcc81b5dc`  
		Last Modified: Thu, 04 Jul 2024 01:49:50 GMT  
		Size: 5.4 MB (5435762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2350d7c2b6e6c69d5d8db35fc32216dcfe49b6d70245cf0316be49e37dfc8ca8`  
		Last Modified: Thu, 04 Jul 2024 01:49:50 GMT  
		Size: 16.3 KB (16263 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:574cfad4526b420129f360945d33118e58922efd3172466639ac223f5f52dc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.0 MB (278993541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d0d35841b6ecb5c53f7711f0ac42f2ca49f2b42fdac0574f873e5f0393d8d9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY dir:a2f5453af1f2210c7b49fadc5acdaaa335139ac35c64847d2f5879056f91a03d in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=21.0.3.9-1
# Thu, 27 Jun 2024 09:17:07 GMT
ARG package_version=1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: package_version=1 version=21.0.3.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 27 Jun 2024 09:17:07 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f95af119e05065dbdff89fbd219657362e32f7ec50d632e28754e75b5a13806e`  
		Last Modified: Thu, 04 Jul 2024 00:39:44 GMT  
		Size: 51.4 MB (51407040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28093793a392b4f3c1e720c679c78b7f244bd1cffa43347280c9abfb0246752a`  
		Last Modified: Thu, 04 Jul 2024 01:04:56 GMT  
		Size: 168.8 MB (168799209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e818a611c64c55a7004253aa1328a4b84d903c7b22685afa5db62988e3bc193`  
		Last Modified: Thu, 04 Jul 2024 01:51:42 GMT  
		Size: 49.6 MB (49624471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55249b7a91069efce03f1965c964a20d604c0e3d9c1c9d36e3701324e45350e`  
		Last Modified: Thu, 04 Jul 2024 01:51:41 GMT  
		Size: 9.2 MB (9161778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c99596bbffdb0e7590c77781658304c5ac546e1665a21ca3bbfdd808bc50d9`  
		Last Modified: Thu, 04 Jul 2024 01:51:41 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c0c1e0f5f51515da24240e0095be34009aa512968c8bcebbe8f4c7ae95c474`  
		Last Modified: Thu, 04 Jul 2024 01:51:42 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:d2963fde17d3357fc15464ca4aa217d871ccfeb197856b5635f888be2942ccb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5451608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86977ebde3784d3c99a0f368a95710e82afb5189d5048f2152d498198727a0cb`

```dockerfile
```

-	Layers:
	-	`sha256:ee2fa5361b661c3d97ed8f4486e11fda260e9a48c5832a73fa7fc42eac3c3975`  
		Last Modified: Thu, 04 Jul 2024 01:51:41 GMT  
		Size: 5.4 MB (5434692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09e089b946c4d709b408ca75f37578fd6c647166a2953c12b8ad5e8c3b8a4d7b`  
		Last Modified: Thu, 04 Jul 2024 01:51:40 GMT  
		Size: 16.9 KB (16916 bytes)  
		MIME: application/vnd.in-toto+json
