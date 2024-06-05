## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:37449f7ee5c3db490d7f03a128e18505870ed1e676b16ac49f04d4a9708cd639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:6caf28cae12b66060fbb6080f135c0ca483dbcf47ad9740bf9f3db1b5376fdb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.4 MB (388380128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64eca86ac2acde5c3dac0d34c0aec8fcf5c5b25643a5013b45e9347de2774ac`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Apr 2024 22:25:10 GMT
COPY dir:c7d5463abe17dfd3879bd12c94f31ebdaedb939167b5199c40650e35e379f334 in / 
# Fri, 19 Apr 2024 22:25:10 GMT
CMD ["/bin/bash"]
# Fri, 19 Apr 2024 22:49:51 GMT
ARG version=1.8.0_412.b08-1
# Fri, 19 Apr 2024 22:50:25 GMT
# ARGS: version=1.8.0_412.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 19 Apr 2024 22:50:27 GMT
ENV LANG=C.UTF-8
# Fri, 19 Apr 2024 22:50:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 27 May 2024 15:57:48 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6f59c9417334b7a9eb6449cc09a14d6738ae8afbfb25d681f2c27740e7d4856c`  
		Last Modified: Fri, 19 Apr 2024 22:25:53 GMT  
		Size: 52.3 MB (52323609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ab07dd353945d07adcee3e5f73d96c66c34ecc9197df9c4b3c10c8c03f4233`  
		Last Modified: Fri, 19 Apr 2024 23:05:32 GMT  
		Size: 278.3 MB (278316802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88192725d61004d1e490f2f2be4c7239e5399e61e6992dc22cfc311855cd38c4`  
		Last Modified: Tue, 28 May 2024 19:58:31 GMT  
		Size: 48.1 MB (48090771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410805149d1d67674688255a2bbd85988a7045cf52f30b90416f3e8987d60823`  
		Last Modified: Tue, 28 May 2024 19:58:29 GMT  
		Size: 9.6 MB (9647569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099215b85970ab64539e1c07cec268af49e8c818ccca8a76b61c54d53aeac6b3`  
		Last Modified: Tue, 28 May 2024 19:58:28 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c2eb3f4a64cf2110a603f94fb6ef4f410963e9ddc7d1f51f4dc9561ee73893`  
		Last Modified: Tue, 28 May 2024 19:58:28 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b767e22a38b041b7ee1916a24bd561d0bf05fc4cf7f0ba0ae9f2d0a2661d51af`  
		Last Modified: Tue, 28 May 2024 19:58:28 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6f1d3882b250aa20fd1410beb49f4337fd7c3c51051b0000a1f956fb17b002d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227872477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1954fec2e42b5bbe13a459f7556191229059ba7c095eac0907c337e9ecb938b1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 05 Jun 2024 00:47:28 GMT
COPY dir:ba9790f78add1c4638ee46d842ce6b7ee4d659e1ce4ca5bfa2485adaf6cac8ec in / 
# Wed, 05 Jun 2024 00:47:29 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:29:07 GMT
ARG version=1.8.0_412.b08-1
# Wed, 05 Jun 2024 02:29:23 GMT
# ARGS: version=1.8.0_412.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 05 Jun 2024 02:29:24 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:29:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 27 May 2024 15:57:48 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:decbb28a26fad91fa4c617ae5541ffaa8f680fc91855c8bb640254519df67bf1`  
		Last Modified: Wed, 29 May 2024 02:10:34 GMT  
		Size: 51.4 MB (51403878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0b4b1ab2e85f5f87982a15269e6d0182710f93c34667718346bda4b24d21c9`  
		Last Modified: Wed, 05 Jun 2024 02:40:51 GMT  
		Size: 118.5 MB (118544599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674f9ba556e380f10e76b384a1c0c659c2f8f2d9889bbfc43cbfb2b1ef87bb84`  
		Last Modified: Wed, 05 Jun 2024 03:20:36 GMT  
		Size: 48.3 MB (48275107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1d5ed5ac4854378c3b689c1c02cf97762ab56a477e27b5def2375be91793a8`  
		Last Modified: Wed, 05 Jun 2024 03:20:35 GMT  
		Size: 9.6 MB (9647515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907f1e5ad1924973699ab0b3ce1f7a412e01e3de36b1ced408360df046d03966`  
		Last Modified: Wed, 05 Jun 2024 03:20:34 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4041c968c971f8457306c53fbba51a495909b90087da8c0e4db8d2100a441731`  
		Last Modified: Wed, 05 Jun 2024 03:20:34 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcf8c3ed652c5b2b25384283906ad471a8981ff86bfe0387146dded6d9bc3f9`  
		Last Modified: Wed, 05 Jun 2024 03:20:34 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
