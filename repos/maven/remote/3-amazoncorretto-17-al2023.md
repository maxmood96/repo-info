## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:ffa94316de85c52b4796c2c828ef8e6e32d15c4a53178ca0601b94986b8a4a11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:7ae91017d1e8f8e415eaedd37066d00398a894724c3dd38ca15bbc10669fbeae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.9 MB (331873476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343b9739d7c34d48486dd1a304d7c63ee810551f735ed6144974657f848ba725`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:24 GMT
ARG version=17.0.18.8-1
# Wed, 21 Jan 2026 18:59:24 GMT
ARG package_version=1
# Wed, 21 Jan 2026 18:59:24 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 18:59:24 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 21 Jan 2026 19:21:43 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 21 Jan 2026 19:21:45 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 21 Jan 2026 19:21:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 21 Jan 2026 19:21:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:21:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:21:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 21 Jan 2026 19:21:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jan 2026 19:21:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 21 Jan 2026 19:21:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 21 Jan 2026 19:21:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 21 Jan 2026 19:21:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 21 Jan 2026 19:21:46 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 21 Jan 2026 19:21:46 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jan 2026 19:21:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jan 2026 19:21:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jan 2026 19:21:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:08:12 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9611f4d384734b62e775c9d6504436549d04bb86a1c85fb4d696880e755c9a`  
		Last Modified: Wed, 21 Jan 2026 18:59:47 GMT  
		Size: 156.9 MB (156916086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01201f1c4a10cb33eef8652293b14cdc26bf626eea922a816f2a0b91deb3c08d`  
		Last Modified: Wed, 21 Jan 2026 21:32:05 GMT  
		Size: 99.1 MB (99126228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a64d4f1ff3053a0989f3cab2cb710ec65523774cdb8d811a9f89bd6f283cd5`  
		Last Modified: Wed, 21 Jan 2026 19:22:38 GMT  
		Size: 12.5 MB (12496672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2eea61dac9f21a5528462ea6c0a31ebb19313eb3a5507764b0d8dd4660ee63`  
		Last Modified: Wed, 21 Jan 2026 20:19:05 GMT  
		Size: 9.3 MB (9312243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c57e0013a0b31222d43c9d24850e644808076e70397c2770daed72827477d39`  
		Last Modified: Wed, 21 Jan 2026 19:22:01 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3fb3beda4e9dd7f75f5ef0dafb9ec116c7b242f2172232c52abc3e2e8c9ad7`  
		Last Modified: Wed, 21 Jan 2026 19:22:02 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:37672a58bb56f4e4b7dcd81334a1474cfa0bd25e1728638b8806e414a3d174fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d304af07898a5789f41d4799c7f34295787d4e8f912ffd551be7a70818796a53`

```dockerfile
```

-	Layers:
	-	`sha256:d2c215ecc3df9529e299dd3e796106d25aedad4ef63d42403fb10fecca8dbc32`  
		Last Modified: Wed, 21 Jan 2026 19:22:01 GMT  
		Size: 6.2 MB (6232025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:801e313667dded9d3c41f88af839acce68843ac48351d0c8ed970998e4da3a74`  
		Last Modified: Wed, 21 Jan 2026 19:22:01 GMT  
		Size: 18.3 KB (18285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:94000649594ca6c1aafb89cf60611338801cec8d2863e929429f638b976a9f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.6 MB (328589408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a8395b523c6760772692377231780a06ff46308093abc8d0fb39e85d39ce92`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:00:37 GMT
ARG version=17.0.18.8-1
# Wed, 21 Jan 2026 19:00:37 GMT
ARG package_version=1
# Wed, 21 Jan 2026 19:00:37 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 19:00:37 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 21 Jan 2026 19:21:41 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 21 Jan 2026 19:21:43 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 21 Jan 2026 19:21:43 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 21 Jan 2026 19:21:43 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:21:43 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:21:43 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 21 Jan 2026 19:21:43 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jan 2026 19:21:43 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 21 Jan 2026 19:21:43 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 21 Jan 2026 19:21:43 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 21 Jan 2026 19:21:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 21 Jan 2026 19:21:44 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 21 Jan 2026 19:21:44 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jan 2026 19:21:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jan 2026 19:21:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jan 2026 19:21:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:25 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e98527feec5a6e3b7d9dd4edae394a807158bda7cdb1fdad45eafe42104a93`  
		Last Modified: Wed, 21 Jan 2026 19:14:36 GMT  
		Size: 155.7 MB (155718940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5627fa3b97d8aacaf0a458d3094f22ab1adb7287ab8e50c66d33ec5d507a7bb1`  
		Last Modified: Wed, 21 Jan 2026 19:22:01 GMT  
		Size: 97.9 MB (97883985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c6f591a905e72528dfdb133a7d60a929678d7723264285272223bef05d4334`  
		Last Modified: Wed, 21 Jan 2026 19:22:00 GMT  
		Size: 12.8 MB (12758842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808ba504920d15e1186c679ab4ed065f387e2d63d6ee85f9c41b878803b68347`  
		Last Modified: Wed, 21 Jan 2026 23:16:10 GMT  
		Size: 9.3 MB (9312242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a45c2ae7b019778294c63590cf129e42f81852c131d2575a58bfabeca00206`  
		Last Modified: Wed, 21 Jan 2026 19:21:59 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e429418f88b4144ed7640445b77d60b47822089d27e4cff0c4b7ce975dbb2fda`  
		Last Modified: Wed, 21 Jan 2026 19:22:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:00d6f2b022b042aded6472e9de3238fb3f28a6f124192c36d89ba3f938e64108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6249385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9cce6e8fb6dc1a8c566a2ac6e52b91b2914f6191477e379f604fe6ac01867c`

```dockerfile
```

-	Layers:
	-	`sha256:4da7f67aeae27ce075151453819c3299bd95f3041af003bb2228abf5b59a315c`  
		Last Modified: Wed, 21 Jan 2026 19:21:59 GMT  
		Size: 6.2 MB (6230955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:956e9602ec7db60b59562c38f0e8abd139ed2c4e7de23f0d60fb826d37c6d817`  
		Last Modified: Wed, 21 Jan 2026 21:28:15 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json
