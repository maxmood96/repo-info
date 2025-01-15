## `maven:3-amazoncorretto-23`

```console
$ docker pull maven@sha256:d6cf459cce5ba146d59c701f48d65cd67af0b19cbcab37ea0623df0824c3b069
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-23` - linux; amd64

```console
$ docker pull maven@sha256:3aad49b4e74c1474054d1ced18da44abfc7c677bad7303125fc5bf545e9e426a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309700697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496b3769df1c3e9135d9bd3de15c36a3fdc5a51be21a29662340cade27ddd68b`
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
	-	`sha256:2d449a9cb20bfb0f76c698e4adb686874f9bd35779c1f8f9d76c5528c87b3366`  
		Last Modified: Wed, 15 Jan 2025 00:43:54 GMT  
		Size: 53.2 MB (53156717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337a18b449a4819df278e44bd7a8c95cca47e636222db5b9b4318c0572528b82`  
		Last Modified: Wed, 15 Jan 2025 18:31:20 GMT  
		Size: 177.6 MB (177569470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279c3babe7425d011856420914974b68787d18085f3e3c4d27d7664e634c9b26`  
		Last Modified: Wed, 15 Jan 2025 19:09:59 GMT  
		Size: 69.8 MB (69803030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92838e61ab88426ace25e30238bfd437cd16c38e69c046545e1e404a7311918f`  
		Last Modified: Wed, 15 Jan 2025 19:09:58 GMT  
		Size: 9.2 MB (9170436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de175b3d4e65912888f819c81f31f54b61872df01646afa7c53bbe5b0c58dcc`  
		Last Modified: Wed, 15 Jan 2025 19:09:58 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8edadd253b494213340332c8ac3ce69b8148c97ec02556fe12455032468d9a`  
		Last Modified: Wed, 15 Jan 2025 19:09:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23` - unknown; unknown

```console
$ docker pull maven@sha256:87a0a58b3dbb1e5837665afc02468fab0ef08416248d9b58278abbe01f1327cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6206411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e722be4da78f7a5c4500d5e96d3d1347e4f9945e3003823ab7ca34fa458e9c9b`

```dockerfile
```

-	Layers:
	-	`sha256:2fd01e66ee6937fae81cbbb4952f77f499105262fde5866080ebcdd53a5b8dbf`  
		Last Modified: Wed, 15 Jan 2025 19:09:58 GMT  
		Size: 6.2 MB (6190105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d01c6b2486d2a5c48b147ac989c42f9032fb86c0fbbc2f77e3bee9a489b019a2`  
		Last Modified: Wed, 15 Jan 2025 19:09:58 GMT  
		Size: 16.3 KB (16306 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-23` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:178b3a69573e5bec8c1e1fdc9a60e646009d9a78d64120b0a862e5733d06042d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306622469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5aba63ec32f9d0db525af15eef0f1533614593829e2861ca84650a2a8d0acc`
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
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Fri, 10 Jan 2025 02:14:49 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd30df951d52363ba9c4e788796c51aafd05b6df3a3ce4b89fe59669e7eb09f8`  
		Last Modified: Sat, 11 Jan 2025 03:12:41 GMT  
		Size: 175.5 MB (175538098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d1fbd269bf4e955acadf6ce5a9e0a4164453d83971890a62a63c0315ba999b`  
		Last Modified: Sat, 11 Jan 2025 04:18:07 GMT  
		Size: 69.6 MB (69644702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840e83b7078d59a044937995673d36b9a34e24c98bddebd9a78521760b87545f`  
		Last Modified: Sat, 11 Jan 2025 04:18:05 GMT  
		Size: 9.2 MB (9170426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c4ca70c0e1403fa872526bb858081db9ec51d2beaba7b77ace3f085cad6459`  
		Last Modified: Sat, 11 Jan 2025 04:18:04 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff7d7a5f7fd741771722aa527aa091f8bff2508333025f5119418d267442453`  
		Last Modified: Sat, 11 Jan 2025 04:18:04 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23` - unknown; unknown

```console
$ docker pull maven@sha256:e46785ff6e465b88ef24beb6b752f16299b55fb2b5ca46297a233ac7c3c5bd87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6204664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d78b8630c285046e810795a0c2035f0c55ce25a721e81a290bee3d5688004d7`

```dockerfile
```

-	Layers:
	-	`sha256:e519ef9eb51512a18a599a0d2cd949be81b3ed5738e028fc89850cbdfd762f41`  
		Last Modified: Sat, 11 Jan 2025 04:18:05 GMT  
		Size: 6.2 MB (6188225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2246e39dc11e2eaa173e183de8d9fed1d43846c50c72ab90ccded771c4c2f765`  
		Last Modified: Sat, 11 Jan 2025 04:18:04 GMT  
		Size: 16.4 KB (16439 bytes)  
		MIME: application/vnd.in-toto+json
