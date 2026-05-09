## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:532785ebbb9cdf68e7e4fb5490d12b283e0803a821f0268b791d08509e627970
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:c14c2cce22ba06cff50d286dfa6052677bb574aca99a2852a8b88d33fda68a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345188528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff5a18e950120f625d8134f77af16c8caa45a8415188b6cf47a11332d9cc7be`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:18:06 GMT
ARG version=11.0.31.11-1
# Sat, 09 May 2026 00:18:06 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:18:06 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:18:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 09 May 2026 01:24:23 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Sat, 09 May 2026 01:24:25 GMT
RUN yum install -y openssh-clients # buildkit
# Sat, 09 May 2026 01:24:25 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 09 May 2026 01:24:25 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 01:24:25 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 01:24:25 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 09 May 2026 01:24:25 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 09 May 2026 01:24:25 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 09 May 2026 01:24:25 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 09 May 2026 01:24:25 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 09 May 2026 01:24:25 GMT
ARG USER_HOME_DIR=/root
# Sat, 09 May 2026 01:24:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 09 May 2026 01:24:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 09 May 2026 01:24:25 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e8ef4b5fb927c0c86de92b3247666810672cabd7e058c5262c750d5d34c79`  
		Last Modified: Sat, 09 May 2026 00:18:27 GMT  
		Size: 153.5 MB (153472393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03fd2872e3f87e7c0782d481245e7eeef837625b5ab59fbd318e617d8914bd9`  
		Last Modified: Sat, 09 May 2026 01:24:44 GMT  
		Size: 115.3 MB (115296064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6f2a6bb8d556a71df502ba9daa9795d54808cdec949d6c8f9928454db549d9`  
		Last Modified: Sat, 09 May 2026 01:24:41 GMT  
		Size: 12.5 MB (12530001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895c94910b84a827c0d67cb32896d9790a8cbcea120f0c9fb6fac586637daee8`  
		Last Modified: Sat, 09 May 2026 01:24:41 GMT  
		Size: 9.3 MB (9312256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e592c46cfa05a4cd50108c6244e67b5a0a1f9aba001b11582cc5c1638f7c864`  
		Last Modified: Sat, 09 May 2026 01:24:40 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691719058feefa523b632b19ae3b8f4085ce5d86c719e29af94bf7d73da5215f`  
		Last Modified: Sat, 09 May 2026 01:24:41 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:3cd88381f5e5d7c7d5ac080cfa47097a67d39607a5e90cb0e8428ba9f96d41a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6280419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efcb019e5be736a0a43adaba6dd211a24ada5de0f224063a06e54071ec3fbfe`

```dockerfile
```

-	Layers:
	-	`sha256:9c238c26b781e2d2052c669b32b2d8f8a3fe4a86a1df14bc6587050d38e1b3b4`  
		Last Modified: Sat, 09 May 2026 01:24:40 GMT  
		Size: 6.3 MB (6263977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a928afc4f81f774fca28de0de3445fcea4b50096f3e9abd5259d22d6496ead0`  
		Last Modified: Sat, 09 May 2026 01:24:39 GMT  
		Size: 16.4 KB (16442 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:59198b54fd1bde69f2c6e5d0804b978e32cbc79f08306f09dcbb48e6a779d3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341663054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3ce8224410def63021175c09773bb78b925f34def633323a57aa8ef8a94599`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:15:25 GMT
ARG version=11.0.31.11-1
# Sat, 09 May 2026 00:15:25 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:15:25 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:15:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 09 May 2026 01:48:50 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Sat, 09 May 2026 01:48:52 GMT
RUN yum install -y openssh-clients # buildkit
# Sat, 09 May 2026 01:48:52 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 09 May 2026 01:48:52 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 01:48:52 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 01:48:52 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 09 May 2026 01:48:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 09 May 2026 01:48:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 09 May 2026 01:48:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 09 May 2026 01:48:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 09 May 2026 01:48:52 GMT
ARG USER_HOME_DIR=/root
# Sat, 09 May 2026 01:48:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 09 May 2026 01:48:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 09 May 2026 01:48:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8763299e6b6a5390624676a6a883b80df08afbd0fe328882a6aa37029abd1826`  
		Last Modified: Sat, 09 May 2026 00:15:47 GMT  
		Size: 152.1 MB (152051820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6942156a673b4993b17ac3025515d7bec24a091c8fc4c78d3570794e97942c93`  
		Last Modified: Sat, 09 May 2026 01:49:11 GMT  
		Size: 114.0 MB (114046949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9289d399ed8d75b3480f6813730a868b06d9c1107880d7c913c7735355dcb74a`  
		Last Modified: Sat, 09 May 2026 01:49:08 GMT  
		Size: 12.8 MB (12794050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c32a7dec9812b0fe745d2c3bdb07364307703ca43be2e8d62b5633c4ad7711`  
		Last Modified: Sat, 09 May 2026 01:49:08 GMT  
		Size: 9.3 MB (9312253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14ea139d32810b1b44cf38fcd0cbfb5cf65bf46e056e5ff29f08b3560af9387`  
		Last Modified: Sat, 09 May 2026 01:49:08 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c813c05d5eddf0461663295790880b24cf105dfb848de01d766e4b52317c0b0`  
		Last Modified: Sat, 09 May 2026 01:49:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:eb244c291e390045e35a2fac815a202dc53f5886e2a9cf44b3ff706431a4ba57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6280342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3932f94b4e565cc46462e1dbbf0cb0d583d8d306e4a460b31b7e23d9ace5df98`

```dockerfile
```

-	Layers:
	-	`sha256:3fff5a7f82690f4d6fca13461e615d4fd0efcee8b22387bb3b635ae8cffeeb1f`  
		Last Modified: Sat, 09 May 2026 01:49:08 GMT  
		Size: 6.3 MB (6263751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3755b50b020f3d2deceb1e759eb6408311d8c6ab4cd8caba55540d93937a4af8`  
		Last Modified: Sat, 09 May 2026 01:49:08 GMT  
		Size: 16.6 KB (16591 bytes)  
		MIME: application/vnd.in-toto+json
