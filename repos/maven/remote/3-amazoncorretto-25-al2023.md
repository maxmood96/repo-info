## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:9e2c9179e8cfdd7d6d857fd69a1d738796991fa72ea3fb719ccd1c981bf26ea7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:41f8113e1b7e358db83fc4ddb2c81053a4af1b100f80492af0000a546af54be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362088506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f558056d389acfa187601da19bd42300cbe6b8f4419b3cf3fe5bce062af4286`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:10:02 GMT
ARG version=25.0.2.10-1
# Wed, 28 Jan 2026 04:10:02 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:10:02 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:10:02 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:10:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 05 Feb 2026 23:30:42 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Thu, 05 Feb 2026 23:30:42 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:30:42 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:30:42 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:30:42 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:30:42 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:30:42 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:30:42 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:30:42 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:30:43 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:30:43 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:30:43 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:30:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:30:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:30:43 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cb6fcb38396d39f54d43d1b722399b74f95aea87f5b449eac9d4eac383e396`  
		Last Modified: Wed, 28 Jan 2026 04:10:25 GMT  
		Size: 189.2 MB (189191028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a17faac10f2f4c3d7a0e6971d2bbff057804b43cebbe87ac58ab52f791c246`  
		Last Modified: Thu, 05 Feb 2026 23:31:02 GMT  
		Size: 109.6 MB (109560349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1d70707f10bd6d75fe1620d466158422d3c41d93920d56bbae8ffcf80c35f2`  
		Last Modified: Thu, 05 Feb 2026 23:31:00 GMT  
		Size: 9.3 MB (9312250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4baba86ed4132062cb19edc85ad8ca164524c804cbbd8d077b337fef8e749c2f`  
		Last Modified: Thu, 05 Feb 2026 23:30:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17679abb5ceb0ffc29c16fdb911537261bb8f2a47f31b88c063fb6696774671c`  
		Last Modified: Thu, 05 Feb 2026 23:31:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:be3ddd61cc58b354c2d5f02d0a637a8226d0b3f79402bb5a5e0763fde1e1e4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11eee5d9f844f13262569bc29f50f55cce20e545fb5b9fce51e7c34bc512f72d`

```dockerfile
```

-	Layers:
	-	`sha256:166a4f71049f92a54cd9b550d24aec00275b25da93b153f1fd5e405f6ab11fce`  
		Last Modified: Thu, 05 Feb 2026 23:31:00 GMT  
		Size: 6.2 MB (6207795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f39862d6a5c4611c9156afed4a7fc312bb98e4c9346c5e773018e38e3914b6b9`  
		Last Modified: Thu, 05 Feb 2026 23:30:59 GMT  
		Size: 16.4 KB (16350 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ae7bb2a9d388b1f8f1fd9fafb68b2c1c024f9ba53004287d55eadebffb29ae69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.2 MB (358163102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70d8510afdb4d449f244216c76912472dc1acdbe0d3a422ed9352c1c44bd4f1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:31:03 GMT
ARG version=25.0.2.10-1
# Wed, 28 Jan 2026 04:31:03 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:31:03 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:31:03 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:31:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 05 Feb 2026 23:41:42 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Thu, 05 Feb 2026 23:41:42 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:41:42 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:41:42 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:41:42 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:41:42 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:41:42 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:41:42 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:41:42 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:41:42 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:41:42 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:41:42 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:41:42 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:41:42 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:41:42 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a396e73c665f4fa119c9cd20fbfa42ece312688cd9297587073bc7d229c333b4`  
		Last Modified: Wed, 28 Jan 2026 04:31:30 GMT  
		Size: 187.1 MB (187090861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c235d15d1aadc4d4b52efabf432b791663316493c04db4db71ca3c4982e56ac`  
		Last Modified: Thu, 05 Feb 2026 23:42:03 GMT  
		Size: 108.8 MB (108842314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03170a8d3151b683c1ce5e1ee870a8f98c2590128960bc46efb8cbe4073ceb05`  
		Last Modified: Thu, 05 Feb 2026 23:42:01 GMT  
		Size: 9.3 MB (9312246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd33805b08d1c9dd8cc876678a65e30c0b1ee79d9ca8c19785a00345b8e9054a`  
		Last Modified: Thu, 05 Feb 2026 23:42:00 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb18a027cf4c6eaa662431b96296c77b7841c2ea1bda40ad6940d9f76b46c50`  
		Last Modified: Thu, 05 Feb 2026 23:42:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:46ac02062d7e81added21bc31c25d65f863c74d7eeaa5e46e304de6ebb544176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ee3b9c5f435ffc182d584f41af2e6a5d7db8b8cf701d189b3a0e822904e530`

```dockerfile
```

-	Layers:
	-	`sha256:72ad52557e74f55fb3b1e4a0d321cda6e325bb089888c85b2ebfe4f9f23e5628`  
		Last Modified: Thu, 05 Feb 2026 23:42:00 GMT  
		Size: 6.2 MB (6206739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0154f114ec4768ed93bd8d6a0daf6f5531bcbf9d84f113abc6291ede3cdcb5c7`  
		Last Modified: Thu, 05 Feb 2026 23:42:00 GMT  
		Size: 16.5 KB (16483 bytes)  
		MIME: application/vnd.in-toto+json
