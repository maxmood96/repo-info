## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:2cf010189b05202d3f3f9dccf7646d9165a31ad5d7a734fdc2dd66366db5bc1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:7bb10f7a5fd69a870f2007923911536e586bad04c115e09a82091ddae9709dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.9 MB (347871732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91906c84d7955d0a9d171fc754f1790ee56c8af8caea8e48e49590790e6cd7c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:21 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:12:21 GMT
ARG package_version=1
# Mon, 04 May 2026 20:12:21 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:12:21 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 08 May 2026 00:30:24 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 08 May 2026 00:30:25 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 08 May 2026 00:30:25 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 00:30:25 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:30:25 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:30:25 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 00:30:25 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 00:30:25 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 00:30:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 00:30:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 00:30:26 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 00:30:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 00:30:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 00:30:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be73c3ad3366393074a6eed7a125da1ff3733ec46325d456499b501d1e3f64ea`  
		Last Modified: Mon, 04 May 2026 20:12:44 GMT  
		Size: 157.2 MB (157155466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1369a3c06bc2cf0b307970c9426b0fe4324cea1ce8eb1d0eaca749e5aba9e364`  
		Last Modified: Fri, 08 May 2026 00:30:46 GMT  
		Size: 114.3 MB (114300688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cc55a997bbe1b450844aeb7b6513c57c6b85d45fad420d2f5c490039671996`  
		Last Modified: Fri, 08 May 2026 00:30:44 GMT  
		Size: 12.5 MB (12525565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6e116281d6c7f52d09101ca275bc0e0bf28efecfdcc85cc46d0bc0396496de`  
		Last Modified: Fri, 08 May 2026 00:30:44 GMT  
		Size: 9.3 MB (9312252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffc2e010df2366e5decbc5e11d1fa35c7449b0140ad3fd1e102d9f14f06c465`  
		Last Modified: Fri, 08 May 2026 00:30:43 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb6aa70532df068bc46845f70819eb6594e11a8fc71b17107ae9f3a23b22752`  
		Last Modified: Fri, 08 May 2026 00:30:44 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:d674f0838246fee0b1112afaf2c366d97ef622cdf89bfe8e20fc4b4e62f48d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041b56e211c63c737d3d061642c9e04b51671238715d39341261d69b64de1d46`

```dockerfile
```

-	Layers:
	-	`sha256:c45f9ac1e14cc647f5f420b9fcf4472756ae9dd53522b2c8e6791df1bd8a82df`  
		Last Modified: Fri, 08 May 2026 00:30:43 GMT  
		Size: 6.2 MB (6239286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b73327a9b5d3ac783bf54c641f950ee7e8c93ee46c3a51d16f1a753bc21ca4e`  
		Last Modified: Fri, 08 May 2026 00:30:43 GMT  
		Size: 16.4 KB (16442 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e5f5c3fe26acad78b4952872f3fb622b918b61d5ecfcf6e42999bf9c6a8f6cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344605370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ab1099f25da6b6de0180af570b251d3387cc23fab5428e396397217bb4eb0a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:40 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:11:40 GMT
ARG package_version=1
# Mon, 04 May 2026 20:11:40 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:40 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 08 May 2026 00:29:25 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 08 May 2026 00:29:27 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 08 May 2026 00:29:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 00:29:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:29:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:29:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 00:29:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 00:29:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 00:29:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 00:29:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 00:29:27 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 00:29:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 00:29:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 00:29:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322640e3642311a443627a18ff0c4fa0690feddc7c348c64a06d1c5fdac713ba`  
		Last Modified: Mon, 04 May 2026 20:12:03 GMT  
		Size: 156.0 MB (155989760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99172cf8a9c61396f50b52c95c34a6b5fe39c3c0a7db1d0400c5c39e45cd1ee0`  
		Last Modified: Fri, 08 May 2026 00:29:47 GMT  
		Size: 113.1 MB (113055409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e59005c69bcb185afff9f3012a356f6c023201acf0275900c09d59ee80e1a0f`  
		Last Modified: Fri, 08 May 2026 00:29:45 GMT  
		Size: 12.8 MB (12790174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2696850090a140e5fc594e7755ad46061a8e4fd13788e70913776d24ff289a`  
		Last Modified: Fri, 08 May 2026 00:29:45 GMT  
		Size: 9.3 MB (9312249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e12f8d8443da4e50a523d20238a1cd8e13a70c004858216e2d14014f5e2fc1`  
		Last Modified: Fri, 08 May 2026 00:29:44 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d603b7633b2667fe07bc0d91a0c6e7b0ed87af4acbedfab9c44f402e4fa93a5f`  
		Last Modified: Fri, 08 May 2026 00:29:45 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:86d852a8e52d1be8bc6afa7b43308ed94b1cbec1d7e1d2c3adff147d885f2a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca308ed024b038b20ec22c8f653f7db54bb371812323afb1c0b6cc3ac74f157`

```dockerfile
```

-	Layers:
	-	`sha256:76bb87c8e15d0fe3bc89055dde6e6dfa6d3b41a8015f67ce667a1579d3f1dab6`  
		Last Modified: Fri, 08 May 2026 00:29:44 GMT  
		Size: 6.2 MB (6238217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4160caca62af06fadc75422a54aa2f0ff921ef37a904b7074d5d528bf52f3360`  
		Last Modified: Fri, 08 May 2026 00:29:44 GMT  
		Size: 16.6 KB (16591 bytes)  
		MIME: application/vnd.in-toto+json
