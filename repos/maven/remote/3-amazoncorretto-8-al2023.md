## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:ca039a3607a7b6a1574b35b699d3e0089a6b0cf7fb86b03ce4ef97bcf2f92802
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:e8560d4a2183c17c1b61a310178ef224620723ed38d5adadf33164ab94647290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.5 MB (495471938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb3d2458f7c2b037202f2d6e226a67bf585cf6fc04db935415ef96df9129a29`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:30 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:30 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:15:27 GMT
ARG version=1.8.0_472.b08-1
# Fri, 14 Nov 2025 02:15:27 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:15:27 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:15:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 14 Nov 2025 03:21:07 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 14 Nov 2025 03:21:08 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 14 Nov 2025 03:21:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 03:21:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:21:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:21:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 03:21:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 03:21:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 03:21:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 03:21:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 03:21:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 03:21:08 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 03:21:08 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 03:21:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 03:21:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 03:21:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b64ab808fd6d460065684b4dcddcfaed550a0161a81a4f24db38100a7cef4ade`  
		Last Modified: Tue, 11 Nov 2025 02:45:03 GMT  
		Size: 54.0 MB (53976715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809baed2d1217d8172c8deeb035a0df5a2b40b71b3dab00a99d667761351faed`  
		Last Modified: Fri, 14 Nov 2025 03:14:19 GMT  
		Size: 330.9 MB (330851031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73759adf5e3b0392cda65a6c547b068aaec1734ec7766a00fef236d929eb6699`  
		Last Modified: Fri, 14 Nov 2025 03:22:06 GMT  
		Size: 96.0 MB (95976876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3b644fb33cf304d0850996436bee9e99ccacd49fd740ec50f659cef2bbb3f8`  
		Last Modified: Fri, 14 Nov 2025 03:21:44 GMT  
		Size: 5.4 MB (5423675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d01fab677909ae0d211c2aa0da044dc75e082f8e5f8975b61504b0a2bd8ccc1`  
		Last Modified: Fri, 14 Nov 2025 03:21:45 GMT  
		Size: 9.2 MB (9242599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5353aa3b5377e50f491099dacb1ab5a5a837055f26de5981d58946c31cddf8`  
		Last Modified: Fri, 14 Nov 2025 03:21:44 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d42d5b00087a3953a8f98ddf9692b36762cf0d9ddbf0030154e84cb875e1b6`  
		Last Modified: Fri, 14 Nov 2025 03:21:44 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:6455bcc8eebadb1b0cf0f4a35edf72bc903127e42ff215b1ce3b4a5fd11d74fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cf3023a655ce5c7397a615b0f0ec47822c2aa02a598272694a035d0c9262e6`

```dockerfile
```

-	Layers:
	-	`sha256:157a25dfce7d691476c942c450bb8f15eab786ee8095cb7dc231755d13b90f67`  
		Last Modified: Fri, 14 Nov 2025 06:28:49 GMT  
		Size: 13.8 MB (13828199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b897caec4742ccc6aa5e67d6dd8b51fa5edd414078231b187f27d92a76d8ddc6`  
		Last Modified: Fri, 14 Nov 2025 06:28:50 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:54dba5a0f1beb584999c88e2e6a4064ad4595e80652c5e6c51753400af5949bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285450375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f812bf7adf80d0b81adad5f537c01ce2a9b0e6085b3ea270a324006ee1f1736b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:24 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:14:27 GMT
ARG version=1.8.0_472.b08-1
# Fri, 14 Nov 2025 02:14:27 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:14:27 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:14:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 14 Nov 2025 03:22:10 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 14 Nov 2025 03:22:13 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 14 Nov 2025 03:22:13 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 03:22:13 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:22:13 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:22:13 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 03:22:13 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 03:22:13 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 03:22:13 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 03:22:13 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 03:22:13 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 03:22:13 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 03:22:13 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 03:22:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 03:22:13 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 03:22:13 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7bff4bcb213fec2224ece2638c720fadc39b0d185d5cfe08391265c58685a0ae`  
		Last Modified: Tue, 11 Nov 2025 02:45:05 GMT  
		Size: 52.9 MB (52876656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417b09cc61bce7063ee22fdbfec9440fa59193c657107416fc150a8b9c769d68`  
		Last Modified: Fri, 14 Nov 2025 02:15:22 GMT  
		Size: 117.9 MB (117933801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167426cf140a95a405321f4e1eb4f7b1bd650c359474b0d688fafd4e565d4b90`  
		Last Modified: Fri, 14 Nov 2025 03:22:54 GMT  
		Size: 92.7 MB (92654250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71377a3535d7ad760794c7b8c0542e79d0eea9681f36ec4a545819fbc7728e0`  
		Last Modified: Fri, 14 Nov 2025 03:22:39 GMT  
		Size: 12.7 MB (12742052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f643eb16e964baeaa00ef67a5805e78cd34edc7ce8de2c3290fd4c2d6152339`  
		Last Modified: Fri, 14 Nov 2025 03:22:41 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bfb2735e4fe66c054357c443f00928586565a15727d59fbb1d991c2cd19459`  
		Last Modified: Fri, 14 Nov 2025 03:22:37 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b413cc524eb6c942af3f12c8be8f96f71a15dc2ee1bea1f285882d33d93d1a6`  
		Last Modified: Fri, 14 Nov 2025 03:22:37 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:697db5ae6d5aedead4c14a1ec4a3c72f9319e7e58fc211d27f150cfba87c21de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888efa802caabe60e039e0f2bdbc654f0b36f4c5d415a168573e351d5be5fb77`

```dockerfile
```

-	Layers:
	-	`sha256:a604ac128569bcbc824db134923c9a693755a61d37311ff815a43beb4616af43`  
		Last Modified: Fri, 14 Nov 2025 06:29:00 GMT  
		Size: 6.6 MB (6609530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43a355503e61584af67e0d8d76e6a60138c83b9cd1318061d1d420945d13dcde`  
		Last Modified: Fri, 14 Nov 2025 06:29:01 GMT  
		Size: 18.4 KB (18429 bytes)  
		MIME: application/vnd.in-toto+json
