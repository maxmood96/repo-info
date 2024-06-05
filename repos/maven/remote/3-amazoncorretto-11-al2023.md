## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:9a2f76e15b9993f96076ca72a366d71a876bcc1555e23bd44081a57d80c0f171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:575187e58f86e6afc9d0a9b9ea59e883b53376f2d27ae7905de02d798f8f58a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb099149fef7c5867ed02c7ba201b2614eb8760aac8d4c78d22d4beb4cb92e83`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Apr 2024 22:25:10 GMT
COPY dir:c7d5463abe17dfd3879bd12c94f31ebdaedb939167b5199c40650e35e379f334 in / 
# Fri, 19 Apr 2024 22:25:10 GMT
CMD ["/bin/bash"]
# Fri, 19 Apr 2024 22:52:55 GMT
ARG version=11.0.23.9-1
# Fri, 19 Apr 2024 22:53:16 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 19 Apr 2024 22:53:17 GMT
ENV LANG=C.UTF-8
# Fri, 19 Apr 2024 22:53:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:6ebb46d7684d1ef9b78d5e67f709ba2bee2ad798178388c835ceb50cf536721e`  
		Last Modified: Fri, 19 Apr 2024 23:07:19 GMT  
		Size: 153.8 MB (153769655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a67bccbf93427c212820d01537805b22d8f70aef98d8499a7423def3b376233`  
		Last Modified: Tue, 28 May 2024 19:55:01 GMT  
		Size: 46.6 MB (46613900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65a0fd5fdcdd504d0c5074c2b6b66e120751f90a4b4eca679488f5a83b21c7b`  
		Last Modified: Tue, 28 May 2024 19:54:58 GMT  
		Size: 9.6 MB (9647569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae19b345c35c67bdad309951244e324aa89aabd361361984b3555de05d22b9f`  
		Last Modified: Tue, 28 May 2024 19:54:58 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5e7a0a3b5b75e023cdaff4686a491ce20d5e27e813ac00257acf24d5ee1b85`  
		Last Modified: Tue, 28 May 2024 19:54:58 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b547a8236ec1b299b479e4c79f2b90e5c133bfb62583d7e5a0d36dcb8c75dbd6`  
		Last Modified: Tue, 28 May 2024 19:54:58 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:72260894ac3f05fcb9026977c62a6afb6c4c1bad156a8cf3a9bc5b5ac457bcc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261550956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99719ea53bc52446515822d93c5210ab1e585eccf039c8c093da3182dfa09362`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 05 Jun 2024 00:47:28 GMT
COPY dir:ba9790f78add1c4638ee46d842ce6b7ee4d659e1ce4ca5bfa2485adaf6cac8ec in / 
# Wed, 05 Jun 2024 00:47:29 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:30:52 GMT
ARG version=11.0.23.9-1
# Wed, 05 Jun 2024 02:31:12 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 05 Jun 2024 02:31:13 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:31:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:5811509d8e8b83d6c7a3a361523e9056d5283f3775589d95d34e3d8f4a75fd30`  
		Last Modified: Wed, 05 Jun 2024 02:42:15 GMT  
		Size: 152.2 MB (152209930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c153b68e1d462cc68bff99190301c5a2e4b19d081f4f6161dbf3ef84257ab4`  
		Last Modified: Wed, 05 Jun 2024 03:18:54 GMT  
		Size: 48.3 MB (48288249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bc67de01be1392e1d4944b33916849e9d02117c715aac8a38f0632fb3340ce`  
		Last Modified: Wed, 05 Jun 2024 03:18:52 GMT  
		Size: 9.6 MB (9647519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9fccc3c1040be6bc0ceb88d5087331f996c7c0e4a8c03691b73732dc326c1e`  
		Last Modified: Wed, 05 Jun 2024 03:18:51 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcbd18641a32521b778ed8f54dfe871dfd76609b36574f3a0ba6f5e59c0241d`  
		Last Modified: Wed, 05 Jun 2024 03:18:51 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a4da27b2aaef47ce58cd7ee2c321dc206d063af94d3c338ad832fb7a5d24d1`  
		Last Modified: Wed, 05 Jun 2024 03:18:51 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
