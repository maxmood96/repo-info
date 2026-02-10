## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:577ff13494dfdcfdf30a603359f7f294abbe42d63f2b171a9c442760289d154f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:b160eef98f562f2f40279a707d1a3807fed55e243273eb01efd4304b7f7f7752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.6 MB (503589195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498c9bf60f1bee5c5b886943171515600c57ee074561c16faea064a7388f3409`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:49 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:04 GMT
ARG version=1.8.0_482.b08-1
# Tue, 10 Feb 2026 18:31:04 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:31:04 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 10 Feb 2026 19:11:13 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 10 Feb 2026 19:11:14 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 10 Feb 2026 19:11:14 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 10 Feb 2026 19:11:14 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 10 Feb 2026 19:11:14 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 10 Feb 2026 19:11:14 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 10 Feb 2026 19:11:14 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 10 Feb 2026 19:11:14 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 10 Feb 2026 19:11:14 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 10 Feb 2026 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 10 Feb 2026 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 10 Feb 2026 19:11:15 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 10 Feb 2026 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Tue, 10 Feb 2026 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 10 Feb 2026 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 10 Feb 2026 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3ffbc2e8833044834ccfc60c99f6275f3632718226c6ef0c9706b41890795123`  
		Last Modified: Mon, 09 Feb 2026 18:58:55 GMT  
		Size: 54.0 MB (54038228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffde5948ea75b47d8b1d783268ee006167908155c0b852232a68d3addb78f4e`  
		Last Modified: Tue, 10 Feb 2026 18:31:57 GMT  
		Size: 330.9 MB (330926190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0374fd42174f7170ec2847f960e597c22882ca634b275e64b33b0827f4a32671`  
		Last Modified: Tue, 10 Feb 2026 19:11:41 GMT  
		Size: 103.9 MB (103896502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d3a2973f1f95c2c55b2bd73cfdd767016887844ff733620aecb97f2aa6e890`  
		Last Modified: Tue, 10 Feb 2026 19:11:38 GMT  
		Size: 5.4 MB (5414990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f33bb0c1a9f161753034523679966f775f42b903be4d2c620565273a318a3e`  
		Last Modified: Tue, 10 Feb 2026 19:11:39 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82802a2c9a18d2a76a4101fcde7cfd88f3a27d397fcbeacdd6863847cd13fe8`  
		Last Modified: Tue, 10 Feb 2026 19:11:38 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0277c72fd872c85ae47a2b0bc805d6d0b2ac026a737c2fc9dbb13264ae0ac41e`  
		Last Modified: Tue, 10 Feb 2026 19:11:40 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:f867d199551ced999e514c24e51ca1feb8ea2b8d7e50aedb401f8c65c4a213c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f86d4c1af932b9ee90190cdf23db210524ae9e213afc6d4132607df7e2bf62c`

```dockerfile
```

-	Layers:
	-	`sha256:3db39fd0df7082aa72f832eb273a8a47875c0d5adf4f87f2554a9e03088acd49`  
		Last Modified: Tue, 10 Feb 2026 19:11:39 GMT  
		Size: 13.8 MB (13828220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24ea4cc2874d101cd0250e83525c9f47f16999d9affc3097844f065d233d0cb7`  
		Last Modified: Tue, 10 Feb 2026 19:11:38 GMT  
		Size: 18.3 KB (18282 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1ab315c9813d867ded9aada0620d6973a6a8811c997610fa02bb3cf8854bb736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 MB (293306579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3638395ae99beec5efbb5d5545fec0eb1a88f56cb403a8678c49a80b029b7e01`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:36 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:36 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:30:39 GMT
ARG version=1.8.0_482.b08-1
# Tue, 10 Feb 2026 18:30:39 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:30:39 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:30:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 10 Feb 2026 19:13:44 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 10 Feb 2026 19:13:47 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 10 Feb 2026 19:13:47 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 10 Feb 2026 19:13:47 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 10 Feb 2026 19:13:47 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 10 Feb 2026 19:13:47 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 10 Feb 2026 19:13:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 10 Feb 2026 19:13:47 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 10 Feb 2026 19:13:47 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 10 Feb 2026 19:13:47 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 10 Feb 2026 19:13:47 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 10 Feb 2026 19:13:47 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 10 Feb 2026 19:13:47 GMT
ARG USER_HOME_DIR=/root
# Tue, 10 Feb 2026 19:13:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 10 Feb 2026 19:13:47 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 10 Feb 2026 19:13:47 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:72831a4cffd207c00f002b53208af67cc59cf3af51b98b118c11c230a7926a2d`  
		Last Modified: Mon, 09 Feb 2026 20:01:25 GMT  
		Size: 52.9 MB (52918211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0baf47396438aac29add42cb10c2c15d95e93ce32ecd998e951f3511d5ac22`  
		Last Modified: Tue, 10 Feb 2026 18:30:59 GMT  
		Size: 118.0 MB (117959813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ead90157f2397b69fae4cdf4db9474a7a6385b9b1a0dc925b64425af95b60c`  
		Last Modified: Tue, 10 Feb 2026 19:14:05 GMT  
		Size: 100.4 MB (100371915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af1d5d6569b52d87c76ec79680e3e2d4cfcf12726d90cc1144b2a7d7d635287`  
		Last Modified: Tue, 10 Feb 2026 19:14:03 GMT  
		Size: 12.7 MB (12743354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff526f9d3df2b22e431cffd240c5c8bcdb96cce259c453b9e7cdba812f3cd1c0`  
		Last Modified: Tue, 10 Feb 2026 19:14:03 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fba97e21194df17a060b5a08ee373c6b4af892421e520fe8e3f2661dbd2c08f`  
		Last Modified: Tue, 10 Feb 2026 19:14:02 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1303334602b12c06bf6f2c5cd85bd710145974ea490f2b4c71677beb3f470ebf`  
		Last Modified: Tue, 10 Feb 2026 19:14:04 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:11fe83e90a3957990e81ef750fc256768d5152fa31fe4fce27cb3270ebb09acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45b52d94d9bbcb53f87e77e8fcf9e36447a71a8ac0379267eb54b314dc16cd2`

```dockerfile
```

-	Layers:
	-	`sha256:8ba2b23d47ce07dfae8f5e11e35362c2c5cfa1b350d1e8fbb119bdcdd167b11b`  
		Last Modified: Tue, 10 Feb 2026 19:14:03 GMT  
		Size: 6.6 MB (6609541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee5a4e8738d19426efd6de734c8bf787f60bc5fdf4a1d612a3bd5ba4674cbcc`  
		Last Modified: Tue, 10 Feb 2026 19:14:02 GMT  
		Size: 18.4 KB (18435 bytes)  
		MIME: application/vnd.in-toto+json
