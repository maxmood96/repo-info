## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:87fe4076026894dad88c8a00769b6d7445630a282e258b057941c86cb3c97513
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:6416795084fb0763cdf355998d66e5c227139b2dd99a489ec347ec8b257b9f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322674067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941461b0fd9469e5fdbdc6562fcd42d273d18fc412d70b98aaeac7447334a62d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:30 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:30 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:16:02 GMT
ARG version=11.0.29.7-1
# Fri, 14 Nov 2025 02:16:02 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:16:02 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:16:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 14 Nov 2025 03:18:18 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 14 Nov 2025 03:18:20 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 14 Nov 2025 03:18:20 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 03:18:20 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:18:20 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:18:20 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 03:18:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 03:18:20 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 03:18:21 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 03:18:21 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 03:18:21 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 03:18:21 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 03:18:21 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 03:18:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 03:18:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 03:18:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b64ab808fd6d460065684b4dcddcfaed550a0161a81a4f24db38100a7cef4ade`  
		Last Modified: Tue, 11 Nov 2025 02:45:03 GMT  
		Size: 54.0 MB (53976715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3baf3ad00d266a6cd950c1ef05e3ea6552d3c96ef132cd066150f8a1a4a790e`  
		Last Modified: Fri, 14 Nov 2025 03:13:57 GMT  
		Size: 153.3 MB (153320811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab4df602775517e42d2df89ad6837386d2e4e30929d9b5cf1a9168056b9b926`  
		Last Modified: Fri, 14 Nov 2025 03:18:58 GMT  
		Size: 93.6 MB (93633245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070dd973c552d5ea6b083b58c97101e1304f681fbc3de59f898392f0329bb108`  
		Last Modified: Fri, 14 Nov 2025 03:18:45 GMT  
		Size: 12.5 MB (12499671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e46e35b6116a99458dcb43ef3e2755e041cb46120f9421a840c64bd7cfa51c`  
		Last Modified: Fri, 14 Nov 2025 03:18:44 GMT  
		Size: 9.2 MB (9242585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fc3b66891963e6a47f4582647db08a3803f630b0cdd7ba9233cd9a8cbec108`  
		Last Modified: Fri, 14 Nov 2025 03:18:43 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5f860d1de3231a7c890f23d74c12fffec9a36e65d64be54c9844d9464bf0c9`  
		Last Modified: Fri, 14 Nov 2025 03:18:43 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:b5dd9a2548e32daee68ca8ddf68f08e4baed967fcb88db1f89a30a15f3a9a74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b100da631ec60d766710422f7b5dec3585ac4925ff2a9a44d431b0fd4fceaa`

```dockerfile
```

-	Layers:
	-	`sha256:907d1eb2debeb566dfe8a78c55cee5a65b7fe152a6fcd7a6881e4f6579fce796`  
		Last Modified: Fri, 14 Nov 2025 06:27:44 GMT  
		Size: 6.3 MB (6257524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef5bcb32d96825ca39f277f7f9c31081655d5f643c89f397dc53fa9fb0eebac`  
		Last Modified: Fri, 14 Nov 2025 06:27:45 GMT  
		Size: 18.3 KB (18285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0912809e2859d3f76981d4ec092028c48ce711d467f9b8d5aa4f459b1a541c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.4 MB (319412057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8fd8657fdea1b741ef7d6edc7eddef1fd2b49a45eed9d1c3e61e10cd89989fa`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:24 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:15:38 GMT
ARG version=11.0.29.7-1
# Fri, 14 Nov 2025 02:15:38 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:15:38 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:15:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 14 Nov 2025 03:18:13 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 14 Nov 2025 03:18:15 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 14 Nov 2025 03:18:15 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 03:18:15 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:18:15 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:18:15 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 03:18:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 03:18:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 03:18:16 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 03:18:16 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 03:18:16 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 03:18:16 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 03:18:16 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 03:18:16 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 03:18:16 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 03:18:16 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7bff4bcb213fec2224ece2638c720fadc39b0d185d5cfe08391265c58685a0ae`  
		Last Modified: Tue, 11 Nov 2025 02:45:05 GMT  
		Size: 52.9 MB (52876656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5c02697f1999b18cff2e99538ca5f01dd4d56fac28560d7e4909f1c288a600`  
		Last Modified: Fri, 14 Nov 2025 03:14:32 GMT  
		Size: 151.9 MB (151868279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba41587b30203ae3ab414e1ef9d230818f2d9c9c83456328993e5374fc516ea7`  
		Last Modified: Fri, 14 Nov 2025 03:18:58 GMT  
		Size: 92.7 MB (92663096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56aac0eb8f7feea90033f9e404d649ab6b4b85e3ce827453598f40e538277fc2`  
		Last Modified: Fri, 14 Nov 2025 03:18:42 GMT  
		Size: 12.8 MB (12760411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dafe67a442630fcfeb7359f6ea29184e2cb927c14da770305347731a13a75c`  
		Last Modified: Fri, 14 Nov 2025 03:18:42 GMT  
		Size: 9.2 MB (9242576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcf2cbf44dfb29433500de9dd6f0672bfe7c91f40ea2c9f2630c51ec16d4c85`  
		Last Modified: Fri, 14 Nov 2025 03:18:40 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc979fb68093e8c6a082879a219cca476f433c6c9ecce4b790d310ab8912683`  
		Last Modified: Fri, 14 Nov 2025 03:18:41 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:fb5b9c3d5d61bb5d7f45b69af33618bdf72d51c2fdaddf31513582aa8b38c81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b089491b40ba7ff129b769cb4efd98ee20018f7170cd318607c54884c6f37e`

```dockerfile
```

-	Layers:
	-	`sha256:2b9ca44aab149e2695eec4f0d883f7ccd9b30b8257ea33e65cad241cbbd1af0f`  
		Last Modified: Fri, 14 Nov 2025 06:27:50 GMT  
		Size: 6.3 MB (6257298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f248c2d10ff89c72faf2527facb3539f205dc4221c069a8d4f122d74f15d2739`  
		Last Modified: Fri, 14 Nov 2025 06:27:50 GMT  
		Size: 18.4 KB (18433 bytes)  
		MIME: application/vnd.in-toto+json
