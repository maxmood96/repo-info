## `maven:3-amazoncorretto-23`

```console
$ docker pull maven@sha256:a7706d31e64b36c7c35ae2fd3f4aebcc9950d455feb8f0b6b35811d53adcf569
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-23` - linux; amd64

```console
$ docker pull maven@sha256:3cc302ce373c76567f9011aff43ff2ab8947ee557778c426286dc0a1b4764776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (305047132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0364c9669f93ddf2788e5fea48e9fcedbd22c75ad447e1d5f2e9c38cde43e20e`
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
	-	`sha256:42ce99aa0f68a7f3dc752dad87f21431a084b94a3818ff00f932236a9010d564`  
		Last Modified: Tue, 15 Oct 2024 02:06:15 GMT  
		Size: 52.3 MB (52343832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63432d46f0bf9dcc129c24c901e228dcb4238fd6c3d3049c5cdb5418c717d991`  
		Last Modified: Mon, 21 Oct 2024 18:57:31 GMT  
		Size: 177.5 MB (177514361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a4426ed0ea44fba025cea2f8c41c9bf19df5c323e3b21fd4ece9a485047a12`  
		Last Modified: Mon, 21 Oct 2024 19:49:25 GMT  
		Size: 66.0 MB (66017464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f1d643895702ed05861336621eda8bcd7ff4e5760b084ef127b903aaf0a711`  
		Last Modified: Mon, 21 Oct 2024 19:49:24 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abc3c4e67fe002bd3b37a394d5b9d64ef93648fb1b982e3197ede6e2bef9c89`  
		Last Modified: Mon, 21 Oct 2024 19:49:24 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cedb970649c26e2a077d0349c0745fe77a47beedfe691a45816657c2cc4e82`  
		Last Modified: Mon, 21 Oct 2024 19:49:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23` - unknown; unknown

```console
$ docker pull maven@sha256:d790029dc68aa20329f92b062f181122b6cb3ad9783e46f37ebc2f4c193c8054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6214866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd6b144e4d0eacffa23733397c5a9f764e49a604cdbfc43b1914132d99143ed`

```dockerfile
```

-	Layers:
	-	`sha256:4bf113becb5a1fee9930d4acc4354479cd618fc495a9852b265059847c51c55d`  
		Last Modified: Mon, 21 Oct 2024 19:49:24 GMT  
		Size: 6.2 MB (6198561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1420af88981183ef26c3853e1c807a1e37e6c5e9185c98ac21918e1ecfc82db`  
		Last Modified: Mon, 21 Oct 2024 19:49:24 GMT  
		Size: 16.3 KB (16305 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-23` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:468f3ad8c88ae40ad13da3f482629255f5f650e029acdccb4f089335b71910dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.7 MB (300652622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c081075b2b2aa8a7bd245891987c736a9a8dc1dda508a0a5477612c58ff9c16`
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
	-	`sha256:9e91bc818827f819b6de2c247e4fed5f971ec9990bc2b6330e067ca2f956815d`  
		Last Modified: Thu, 03 Oct 2024 17:46:58 GMT  
		Size: 51.4 MB (51426364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b39012886f509ba8d8b15f9a9fae7324e1b87b7f6f5344cc22388dca51a546f`  
		Last Modified: Wed, 16 Oct 2024 18:39:50 GMT  
		Size: 175.4 MB (175419552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699e7110ba896e2ef8daf41e3f7774eeb8146ef55ef48e4ab0e2edcaefcdf852`  
		Last Modified: Wed, 16 Oct 2024 20:20:13 GMT  
		Size: 64.6 MB (64635222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3406dbd1c6229e23a3811b08b74772ee3b2b307c884a6892a8b0302d0ef8091b`  
		Last Modified: Wed, 16 Oct 2024 20:20:12 GMT  
		Size: 9.2 MB (9170437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d658650a4c298dd940e69281a668c087ab6d7cb6e0fd0360511ab02ed1518423`  
		Last Modified: Wed, 16 Oct 2024 20:20:11 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef7319c064ca2635b7df5d37ed07b2fa2496c7342018e07f9893507fb57e227`  
		Last Modified: Wed, 16 Oct 2024 20:20:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23` - unknown; unknown

```console
$ docker pull maven@sha256:3d2125cee4ee209f44130243f84a96537b361c8992ad72595f9fbc977daf2f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6212934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98fe0f0b47ae6e712d6e2754c6a53c0e3284d7244900b846631187cbe46246f`

```dockerfile
```

-	Layers:
	-	`sha256:22024940908f1398f25c51726e878b1a46a2ee64ee1de2731d48efecf22e5e21`  
		Last Modified: Sat, 19 Oct 2024 22:44:09 GMT  
		Size: 6.2 MB (6196495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99b8b3d5576e41e1223289e8680e2b5dc327b3cd3c4216aea76dd7bb8edfd17`  
		Last Modified: Sat, 19 Oct 2024 22:44:09 GMT  
		Size: 16.4 KB (16439 bytes)  
		MIME: application/vnd.in-toto+json
