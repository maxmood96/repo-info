## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:36b456050a8e96358e543885a1108a0851508c334f0900180c5be70e8273f23f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:2bef42c44f628985faad6385854826e29c23f303d28dd76ed863d5cbfaff1ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328331027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9da51bce938394aac1eef56d3c43d0a17c1199e2468de1bb42dd512686a132`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:57 GMT
ARG version=11.0.30.7-1
# Wed, 21 Jan 2026 18:59:57 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 18:59:57 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 21 Jan 2026 19:21:24 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 21 Jan 2026 19:21:27 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 21 Jan 2026 19:21:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 21 Jan 2026 19:21:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:21:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:21:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 21 Jan 2026 19:21:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jan 2026 19:21:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 21 Jan 2026 19:21:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 21 Jan 2026 19:21:27 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 21 Jan 2026 19:21:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 21 Jan 2026 19:21:27 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 21 Jan 2026 19:21:27 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jan 2026 19:21:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jan 2026 19:21:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jan 2026 19:21:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:09:37 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a07ea5032c792d7ba679b74d72cf278e3e104563477a78ec86bb42a7f99648e`  
		Last Modified: Wed, 21 Jan 2026 19:17:31 GMT  
		Size: 153.4 MB (153367384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134c3be4cc01a575ba638f48c7919b896f7a231d0515a27ebb41ef485580b728`  
		Last Modified: Wed, 21 Jan 2026 21:59:08 GMT  
		Size: 99.1 MB (99128907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af14be5a9a854f9d477b62d1658c980f883026bcc881509e4ee0d790842de1c`  
		Last Modified: Wed, 21 Jan 2026 19:21:41 GMT  
		Size: 12.5 MB (12500249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc67195f4fac27bbb8f1a8521f0b8bea1780d13f7739ca1bd0c4981f068a795`  
		Last Modified: Wed, 21 Jan 2026 19:21:41 GMT  
		Size: 9.3 MB (9312239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9941581f7adb58989356187922278777765750c80035a3d22e5d3e86be27e44`  
		Last Modified: Wed, 21 Jan 2026 20:05:00 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65d75bf4155e47c9fb256983bbe6e0da67d640016ba31d6ceb1913e0c9b39ff`  
		Last Modified: Wed, 21 Jan 2026 21:23:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:84cd881fa9020b2a6a082b81e9759bce77a2dc4bd33c4e98f68b865c36daa01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db70d950b34a102f2afd791147122153e0f0f0e121768d38cd11df0304b2c2fb`

```dockerfile
```

-	Layers:
	-	`sha256:9a46ffcb81f6da353e476316d89df5977414eae580e2324ab1925190f86f34f1`  
		Last Modified: Wed, 21 Jan 2026 19:21:41 GMT  
		Size: 6.3 MB (6257535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ba10826f9e8876de91d251a6bda174de302bc67df56ff496f1239caf91ba9d2`  
		Last Modified: Wed, 21 Jan 2026 19:21:40 GMT  
		Size: 18.3 KB (18285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:65a33337eac32ea5d6d802ebe827ba141622cec149526abecc961078e993a9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324796851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4279124e13f6e5c7e25779b136d9fee1fd8c552897064de7dc3be3e1d5d5cabb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:00:16 GMT
ARG version=11.0.30.7-1
# Wed, 21 Jan 2026 19:00:16 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 19:00:16 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 21 Jan 2026 19:21:31 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 21 Jan 2026 19:21:34 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 21 Jan 2026 19:21:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 21 Jan 2026 19:21:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:21:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:21:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 21 Jan 2026 19:21:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jan 2026 19:21:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 21 Jan 2026 19:21:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 21 Jan 2026 19:21:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 21 Jan 2026 19:21:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 21 Jan 2026 19:21:34 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 21 Jan 2026 19:21:34 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jan 2026 19:21:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jan 2026 19:21:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jan 2026 19:21:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:36 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436dca49d48a119ba29e5c58e3826eb3069953cb00876a3cfc8081de1fdd358b`  
		Last Modified: Wed, 21 Jan 2026 19:16:45 GMT  
		Size: 151.9 MB (151921187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c443ce8f6a8c94fbb001a9ce09d57f1d50001ee2f5736ae8ce1064c55ac6bf`  
		Last Modified: Wed, 21 Jan 2026 19:21:52 GMT  
		Size: 97.9 MB (97885162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caae37a5ae218a14fab894474d6d1a046266add9843bb1eb00c283611c8f772d`  
		Last Modified: Wed, 21 Jan 2026 19:22:12 GMT  
		Size: 12.8 MB (12762859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eea141201e2b4ffb853f490c1acb6536515f7e846233a5b6e2694118931494`  
		Last Modified: Wed, 21 Jan 2026 19:21:50 GMT  
		Size: 9.3 MB (9312242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c1407a106e555a05bc740ac2ddc77c9f552f2bd1ee9a637c92dcc2260198d8`  
		Last Modified: Wed, 21 Jan 2026 19:21:50 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd3f95e550d2e78432067a2973569b0d47196e650fe26a933ad93d723fe86aa`  
		Last Modified: Wed, 21 Jan 2026 19:22:07 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:d0d982f9712154f76e7321dbecc233e354a9b7b41c3b8875629360d27639e693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8ca38a22944a3db02776781ce95be4c35e7f90ec1f72d3e7cd6d8d2f98a17b`

```dockerfile
```

-	Layers:
	-	`sha256:d55244497070a60295f77cc90be863ecadb67c96194e6a33774ae4921fa2781a`  
		Last Modified: Wed, 21 Jan 2026 19:21:50 GMT  
		Size: 6.3 MB (6257309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b506b2ae46c902ea37f17007434ee5751a3fa0ddfd7c9b8884d49a3d8d0698d`  
		Last Modified: Wed, 21 Jan 2026 19:21:50 GMT  
		Size: 18.4 KB (18433 bytes)  
		MIME: application/vnd.in-toto+json
