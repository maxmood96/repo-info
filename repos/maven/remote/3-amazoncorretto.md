## `maven:3-amazoncorretto`

```console
$ docker pull maven@sha256:1b8fea5cb50d91f030d766c1606bf132e4c70fe823d633b8fcc9ad799eb29050
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:c58e86179e531a1fefd522a86e9bf04ff81f45ce9e0728c499ed90bd6b9c5b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.9 MB (354854406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f652c76d6d3fe3e588172dae4908747bf0b4253dbe18b8d66493baf319019360`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 06 Nov 2025 22:15:48 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:15:48 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 23:12:37 GMT
ARG version=25.0.1.9-1
# Thu, 06 Nov 2025 23:12:37 GMT
ARG package_version=1
# Thu, 06 Nov 2025 23:12:37 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 23:12:37 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 23:12:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 07 Nov 2025 00:14:12 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 07 Nov 2025 00:14:12 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 07 Nov 2025 00:14:12 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 07 Nov 2025 00:14:12 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 07 Nov 2025 00:14:12 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 07 Nov 2025 00:14:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 07 Nov 2025 00:14:12 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 07 Nov 2025 00:14:12 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 07 Nov 2025 00:14:12 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 07 Nov 2025 00:14:12 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 07 Nov 2025 00:14:12 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 07 Nov 2025 00:14:12 GMT
ARG USER_HOME_DIR=/root
# Fri, 07 Nov 2025 00:14:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 07 Nov 2025 00:14:12 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 07 Nov 2025 00:14:12 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7857af70cc37714ae4781f1d58242c7667f933ef8be05b0636d2c50e756263b2`  
		Last Modified: Wed, 05 Nov 2025 21:09:20 GMT  
		Size: 54.0 MB (54000503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ff4d7205da8b8271c826b4d33c535dc537a1d647dc5aaac7acbed9389cdd36`  
		Last Modified: Fri, 07 Nov 2025 00:11:33 GMT  
		Size: 189.2 MB (189168050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3e7293023522d5bf3d29affdcedafdbaf1f392771648b60312efc8f1465ab3`  
		Last Modified: Fri, 07 Nov 2025 00:14:49 GMT  
		Size: 102.4 MB (102442221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477b4206d42ae02dfa9dbd65d5e78952de79384d18b19f1f21a0683d65f1a624`  
		Last Modified: Fri, 07 Nov 2025 00:14:37 GMT  
		Size: 9.2 MB (9242589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d442fd99bd52e05b0bef4bac1c221c0fa6bd0ee4d70bad79ebc5df0ec2f66bff`  
		Last Modified: Fri, 07 Nov 2025 00:14:36 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89ad480f2b064b1661aeb2cb1b7ca437b20f39b5c44e15c53dbb2cfadc98e2b`  
		Last Modified: Fri, 07 Nov 2025 00:14:36 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:6322d4f41a548729b3601b8c57baadbab17e315ce36790a2c8be8958fed88ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6226555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18fc0f3fb0974921f89dd879c60fac223dfde380c8446fcf6d6f524aa81bec36`

```dockerfile
```

-	Layers:
	-	`sha256:bd2e2d910034920414eed99b501a77292975bfa4a3661a86e6155bacf2374dbd`  
		Last Modified: Fri, 07 Nov 2025 03:27:20 GMT  
		Size: 6.2 MB (6209006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03f0d057a23d756b75fb85cdcf728831d3e6e8ba0d159dd884dbe2f0762cddcb`  
		Last Modified: Fri, 07 Nov 2025 03:27:21 GMT  
		Size: 17.5 KB (17549 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5001b2b4d9e61b7bd2cbff5a5def5c7912ac30725ae8d22162fa221153437379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350988816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0929af583f4c85d7cb316fcb3a2f8a19d9520448d36f0fd3ffee45f6288552`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:14:39 GMT
ARG version=25.0.1.9-1
# Thu, 06 Nov 2025 22:14:39 GMT
ARG package_version=1
# Thu, 06 Nov 2025 22:14:39 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:14:39 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:14:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 06 Nov 2025 23:15:29 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Thu, 06 Nov 2025 23:15:29 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 06 Nov 2025 23:15:29 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 06 Nov 2025 23:15:29 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 06 Nov 2025 23:15:29 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 06 Nov 2025 23:15:29 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 06 Nov 2025 23:15:29 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 06 Nov 2025 23:15:29 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 06 Nov 2025 23:15:29 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 06 Nov 2025 23:15:29 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 06 Nov 2025 23:15:29 GMT
ARG MAVEN_VERSION=3.9.11
# Thu, 06 Nov 2025 23:15:29 GMT
ARG USER_HOME_DIR=/root
# Thu, 06 Nov 2025 23:15:29 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 06 Nov 2025 23:15:29 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 06 Nov 2025 23:15:29 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123460810639ecd99796c2d04c9c602287fe1bbb2613c2622aabd5176f1a2c40`  
		Last Modified: Thu, 06 Nov 2025 23:10:36 GMT  
		Size: 187.1 MB (187092407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd03707b837866547058488774267d04e3616e820fa3545cfe0a2f5dbd865a01`  
		Last Modified: Thu, 06 Nov 2025 23:16:10 GMT  
		Size: 101.8 MB (101751086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0dc3fa50b0f53a46cd5d808fbc4e5e5000ea00a17c5da53eda7104819db75d`  
		Last Modified: Thu, 06 Nov 2025 23:15:57 GMT  
		Size: 9.2 MB (9242596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a8c47f734e5d66a2d18a3e86f3cfe6d3670bc3e631a33c0bb4d9dc4e4126db`  
		Last Modified: Thu, 06 Nov 2025 23:15:54 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88271572d616be093454e47e165b93a5a83d7f31ea93e61d172dcdf4532d2c60`  
		Last Modified: Thu, 06 Nov 2025 23:15:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:c4d70daa1b639a8df7c010a1e99e1ae98aac308befa625f775ab2097a07f806b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6225728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3615b4bfb838f7354223d6b42fadcf1a68394819fada40187ae8028ffbc817a9`

```dockerfile
```

-	Layers:
	-	`sha256:a6251b4bdbb32c3f5375e9553e2240c252c1a29fcc1205218f626333f58f8c51`  
		Last Modified: Fri, 07 Nov 2025 00:27:27 GMT  
		Size: 6.2 MB (6207998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3225ee5e876a03d6ee553a185401f28a952ff047cf759057513c22173b9ae7e8`  
		Last Modified: Fri, 07 Nov 2025 00:27:28 GMT  
		Size: 17.7 KB (17730 bytes)  
		MIME: application/vnd.in-toto+json
