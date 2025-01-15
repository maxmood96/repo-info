## `maven:3-amazoncorretto-23-al2023`

```console
$ docker pull maven@sha256:ed40b7038b05128f0c5ba149febe59d9df51bd943dd32861d493aca8dd3534f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-23-al2023` - linux; amd64

```console
$ docker pull maven@sha256:64b145b5af1228292dfefa6d3c1353cdf0e7c478a683c174169e59cedcb4d024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309700783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4d8e95e7edf52f6253b94e25b9a3a04653b4b93f22106e9c64e4aa2deba8f7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 19:11:46 GMT
ARG version=23.0.1.8-1
# Mon, 23 Sep 2024 19:11:46 GMT
ARG package_version=1
# Mon, 23 Sep 2024 19:11:46 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
ENV LANG=C.UTF-8
# Mon, 23 Sep 2024 19:11:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Mon, 23 Sep 2024 19:11:46 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 19:11:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 19:11:46 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 19:11:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 19:11:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 19:11:46 GMT
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
	-	`sha256:bbf2b6b5da9c821ddf911f240e557830aae51859da6911989b4cc6e3d7a43ff1`  
		Last Modified: Wed, 15 Jan 2025 19:10:01 GMT  
		Size: 69.8 MB (69803115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac3d4f2334e66fc20f0ee1499ae468c836b4d55c9f88b0599246c2987787ea3`  
		Last Modified: Wed, 15 Jan 2025 19:10:00 GMT  
		Size: 9.2 MB (9170439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbecc54062bba8d8264cf16045da7f918b443ab7bc1e587b15732bb9cd72347`  
		Last Modified: Wed, 15 Jan 2025 19:10:00 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06f22a9b52787e1a9781a986ef8f51fdad23ffffc44db7c36567d2aee7d6a0d`  
		Last Modified: Wed, 15 Jan 2025 19:10:00 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:a9b7ea47cd30454dbd93e33c643caa01e0d57a6c068351d3349a090200f1bae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6206524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ebf4aeb0ad79b51209553aff89194519bc19f90b9fe83365800e9ca9f215e7`

```dockerfile
```

-	Layers:
	-	`sha256:a42e991463d18e01688bf9b4f80d6c48a457cf931b31eb79789fd8fea5f990a5`  
		Last Modified: Wed, 15 Jan 2025 19:10:00 GMT  
		Size: 6.2 MB (6190147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fe0e949981ac91ebdae7de66fe7bce4a85950204401b7f1bedc857d682016bd`  
		Last Modified: Wed, 15 Jan 2025 19:10:00 GMT  
		Size: 16.4 KB (16377 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-23-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9178f9acedaaa44e0e5368e1e701da768f114311e11384e19b3a3f94b842ce5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306622469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f351dec32b1f4c60d9b23dafd00e85406e919c2b2e2c976537016d87c1c11af`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 19:11:46 GMT
ARG version=23.0.1.8-1
# Mon, 23 Sep 2024 19:11:46 GMT
ARG package_version=1
# Mon, 23 Sep 2024 19:11:46 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
ENV LANG=C.UTF-8
# Mon, 23 Sep 2024 19:11:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Mon, 23 Sep 2024 19:11:46 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 19:11:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 19:11:46 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 19:11:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 19:11:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 19:11:46 GMT
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

### `maven:3-amazoncorretto-23-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:5ae77c4176849dee2a1111c2ce92d5b8b1de4d32e4d35a324858f3a15adcc34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6203197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee18caa297e1be9134bc9c4c2a51aa5acb6b7f1346a70e0bbdd55b5fc74b9fc`

```dockerfile
```

-	Layers:
	-	`sha256:ae284ede865a8a98f1b1576459260fc82755e1ec06c98b35772cd2f3fc4bb2e8`  
		Last Modified: Sat, 11 Jan 2025 04:19:27 GMT  
		Size: 6.2 MB (6188267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a876f8f8ca38ee6d2f206a01c7a553c6ec9cec7bba7a273408dd17ca610e221`  
		Last Modified: Sat, 11 Jan 2025 04:19:26 GMT  
		Size: 14.9 KB (14930 bytes)  
		MIME: application/vnd.in-toto+json
