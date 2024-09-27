## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:9bab265c34cfe492d4fd81c7e6d531f15a88eabb3909de5a7d20a75f33dd70b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:66b039bab89417ccbb062e5e3a853dafb76ceae4be338285fa0a5becb7acfb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.8 MB (402843772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef2bc0393e0ad1f7f5e33b9f1e26625b8140c3032050d6c1f33be049480a587`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=1.8.0_422.b05-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9a0f8ca95549caa504c79acef976bd6b204271a0f61eacfa1a045c2ce6bb0d43`  
		Last Modified: Tue, 17 Sep 2024 02:04:40 GMT  
		Size: 52.3 MB (52324958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762b8628b852c41cabec7d5c0cf55a81e5eb385c6564ab5434eba061c5c6d3e3`  
		Last Modified: Tue, 24 Sep 2024 01:57:00 GMT  
		Size: 280.2 MB (280181381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1143c7a6c538a8bd407cb896c4bd8f3296c3219a90f4643732b77009c9b48eb`  
		Last Modified: Fri, 27 Sep 2024 19:57:22 GMT  
		Size: 56.4 MB (56408133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3407f1366437394cdd8ffb4d36d5daac38c4d6ee2413428cee77d14fb8e36a47`  
		Last Modified: Fri, 27 Sep 2024 19:57:20 GMT  
		Size: 4.8 MB (4757825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdd12e80cc8fcafda3bfaf9e1d97e8cc6f5e385407e4c5fe91f5da79a6ecb7f`  
		Last Modified: Fri, 27 Sep 2024 19:57:20 GMT  
		Size: 9.2 MB (9170437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ef2018d7b3d900a35e3785857e419c202db060920fb68fcd55080e14f70db3`  
		Last Modified: Fri, 27 Sep 2024 19:57:20 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8791934233583ff14b09a2e28103176b14d473a40e634b73eb810fc9142e11`  
		Last Modified: Fri, 27 Sep 2024 19:57:21 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:56093eeaf41eb7fad7ecc03dc20b2b6f9b1bcca7f7e4f05b93bf3d439878073d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12729714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db727a031f905f8ddd942c7cfba07e5a18df987716942e48050e787b75f8d766`

```dockerfile
```

-	Layers:
	-	`sha256:eff45bba2f23bc1ad8b7182b754c32514ed72cfcc32d27f5f12cbc02922d5d9e`  
		Last Modified: Fri, 27 Sep 2024 19:57:20 GMT  
		Size: 12.7 MB (12711436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3651a1d7c5bea1ce8d254a75e9b2c992d5ab5e6491a4b448ca7ff38f9f690592`  
		Last Modified: Fri, 27 Sep 2024 19:57:20 GMT  
		Size: 18.3 KB (18278 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:2097e5f578ed0078fb0ff80aa93e9389b971a940777d9b6633c79308ebf13a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246378723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b2aeaa3ffa02a748c97bd86cb2c772612cd2f49bf92dc2b35b1506ad9dbb0a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /rootfs/ / # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["/bin/bash"]
# Mon, 19 Aug 2024 08:57:28 GMT
ARG version=1.8.0_422.b05-1
# Mon, 19 Aug 2024 08:57:28 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENV LANG=C.UTF-8
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8e0a984b7f222102e6d0bbaa2dac67ec2c00d5735727c1b5e918160055b8f617`  
		Last Modified: Tue, 17 Sep 2024 02:35:27 GMT  
		Size: 51.4 MB (51425992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d9448814ef9d728ec3534293be49f60d5bbbc3a263fa9bd0038d8900cde973`  
		Last Modified: Tue, 24 Sep 2024 02:27:16 GMT  
		Size: 118.5 MB (118538360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636a04f2d59825a0e5261d9e31a4fd5eccc7909024962cf3c2de42e4228d0fbb`  
		Last Modified: Tue, 24 Sep 2024 03:13:16 GMT  
		Size: 54.5 MB (54469227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eced0b0d6d2f7c9054c4c4a6eba576b3cc32cade7a8659e22cd043af44f08686`  
		Last Modified: Tue, 24 Sep 2024 03:13:14 GMT  
		Size: 12.8 MB (12773662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c92a22b92259803dd7ae1e36b03ae1eafc2449758fec3d27b30c7861a0d8d33`  
		Last Modified: Tue, 24 Sep 2024 03:13:14 GMT  
		Size: 9.2 MB (9170441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc703a1841d1acbb8fcac3bf3ede3e9ea60785c5438e8c2b4e3133150779604`  
		Last Modified: Tue, 24 Sep 2024 03:13:14 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e2a9f017d33ea8134cf42d2cdc9117cdacac567c2824d3896bc82698b8b9aa`  
		Last Modified: Tue, 24 Sep 2024 03:13:15 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:9a6ba54796ed5837bd3089cdded4139fdf4f6ebe1d23b0bcc2343124cc9ed307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6623490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b1ee039e982628eb89e8632cb6c473eb77fb2043d146ed2eabcb8ed37a40ee`

```dockerfile
```

-	Layers:
	-	`sha256:fac81059b559720451633062fa4bf0c98dc9c637bbd4f8a63dc5a15660ded9dc`  
		Last Modified: Tue, 24 Sep 2024 03:13:14 GMT  
		Size: 6.6 MB (6604482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ce9b46e2e0c888d4b32f1e5a8fc549ff1079ed16339eee305aee051fe8abc6b`  
		Last Modified: Tue, 24 Sep 2024 03:13:13 GMT  
		Size: 19.0 KB (19008 bytes)  
		MIME: application/vnd.in-toto+json
